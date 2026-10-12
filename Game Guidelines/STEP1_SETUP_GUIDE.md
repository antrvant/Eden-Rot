# 🎯 PHASE 2 - STEP 1: TARGET SELECTION SYSTEM

## 📋 **OVERVIEW**

Tạo hệ thống chọn target để:
- User có thể click vào enemy để attack
- Hiển thị highlight khi có thể chọn
- Xử lý selection logic
- Connect với BattleManager để execute actions

---

## 📥 **FILES CẦN ADD:**

### **New Files:**
1. `TargetSelector.cs` - Quản lý target selection
2. `BattleAction.cs` - Data structure cho actions
3. `EnemyUI_Updated.cs` - EnemyUI với selection support

### **Update Files:**
1. `BattleManager.cs` - Thêm methods từ `BattleManager_Additions.cs`
2. `BattleUI.cs` - Connect với TargetSelector
3. `EnemyUI Prefab` - Thêm components

---

## 🔧 **SETUP STEPS:**

### **STEP 1: Copy Scripts**

```
1. TargetSelector.cs → Assets/_Game/Scripts/Battle/
2. BattleAction.cs → Assets/_Game/Scripts/Battle/
3. EnemyUI_Updated.cs → REPLACE existing EnemyUI.cs
```

---

### **STEP 2: Update BattleManager.cs**

Mở file `BattleManager.cs` và **ADD** các methods sau vào cuối class:

```csharp
// Copy toàn bộ nội dung từ BattleManager_Additions.cs
// Paste vào trước dấu } cuối của class BattleManager
```

**Methods được thêm:**
- `GetEnemies()`
- `GetPartyMembers()`
- `GetCurrentTurnUnit()`
- `ExecuteAction()`
- `ExecuteAttack()`
- `CheckBattleEnd()`
- `EndBattle()`

---

### **STEP 3: Setup TargetSelector GameObject**

```
Hierarchy > Battle Scene > Create Empty
Name: "TargetSelector"

Inspector:
Add Component > TargetSelector
```

**TargetSelector settings:**
- Không cần assign gì, script tự tìm các UI components

---

### **STEP 4: Update EnemyUI Prefab**

```
Project > Assets/_Game/Prefabs/UI > EnemyUI
Double-click để mở Prefab mode
```

#### **A. Add Button Component:**

```
Select EnemyUI root GameObject

Inspector > Add Component > Button

Button Settings:
- Target Graphic: Background Image (hoặc toàn bộ prefab)
- Transition: Color Tint
  - Normal Color: White
  - Highlighted Color: Light Yellow (1, 1, 0.8)
  - Pressed Color: Yellow (1, 1, 0.5)
```

#### **B. Create Selection Indicator:**

```
Right Click on EnemyUI > UI > Image
Name: "SelectionIndicator"

Rect Transform:
- Anchor: Stretch-Stretch
- Left: -5
- Right: -5
- Top: -5
- Bottom: -5

Image:
- Color: Yellow (1, 1, 0, 0.5)
- Raycast Target: OFF (uncheck)
```

#### **C. Create Selection Outline:**

```
Right Click on EnemyUI > UI > Image  
Name: "SelectionOutline"

Rect Transform:
- Anchor: Stretch-Stretch
- Left: 0
- Right: 0
- Top: 0
- Bottom: 0

Image:
- Source Image: None
- Color: Yellow (1, 1, 0, 0.8)
- Image Type: Simple
- Raycast Target: OFF
```

#### **D. Assign References:**

```
Select EnemyUI root

Inspector > Enemy UI (Script):
- Selection Indicator: Drag "SelectionIndicator" here
- Selection Outline: Drag "SelectionOutline" here
- Select Button: Drag EnemyUI root (the button component)
```

**Save Prefab (Ctrl+S)**

---

### **STEP 5: Update BattleUI.cs**

Mở `BattleUI.cs`, tìm method `OnAttackButtonPressed()`:

**BEFORE:**
```csharp
private void OnAttackButtonPressed()
{
    Debug.Log("[BattleUI] Attack button pressed");
    ShowTargetSelection(TargetType.SingleEnemy);
}
```

**AFTER:**
```csharp
[Header("Target Selection")]
[SerializeField] private TargetSelector targetSelector;

private void OnAttackButtonPressed()
{
    Debug.Log("[BattleUI] Attack button pressed");
    
    if (targetSelector == null)
    {
        targetSelector = FindObjectOfType<TargetSelector>();
    }
    
    // Get alive enemies
    var enemies = battleManager.GetEnemies(aliveOnly: true);
    
    if (enemies.Count == 0)
    {
        Debug.LogWarning("[BattleUI] No enemies to attack!");
        return;
    }
    
    // Start target selection
    targetSelector.StartTargetSelection(TargetType.SingleEnemy, enemies);
    
    // Subscribe to selection event (do once in Awake/Start)
    // targetSelector.OnTargetSelected.AddListener(OnTargetSelected);
}

// ADD new method
private void OnTargetSelected(BattleUnit target)
{
    Debug.Log($"[BattleUI] Target selected: {target.stats.characterName}");
    
    // Get current turn unit
    var currentUnit = battleManager.GetCurrentTurnUnit();
    
    if (currentUnit == null)
    {
        Debug.LogError("[BattleUI] No current turn unit!");
        return;
    }
    
    // Create attack action
    var action = BattleAction.CreateAttack(currentUnit, target);
    
    // Execute action
    battleManager.ExecuteAction(action);
    
    // Hide action panel
    ShowActionPanel(false);
}
```

**ADD trong Awake():**
```csharp
private void Awake()
{
    battleManager = BattleManager.Instance;
    
    // Existing button listeners...
    
    // NEW: Target selector setup
    targetSelector = FindObjectOfType<TargetSelector>();
    if (targetSelector != null)
    {
        targetSelector.OnTargetSelected.AddListener(OnTargetSelected);
        targetSelector.OnSelectionCancelled.AddListener(OnSelectionCancelled);
    }
}

// ADD new method
private void OnSelectionCancelled()
{
    Debug.Log("[BattleUI] Selection cancelled");
    ShowActionPanel(true);
}
```

---

### **STEP 6: Assign TargetSelector in BattleUI**

```
Hierarchy > Battle Scene > Canvas > BattleUI

Inspector > Battle UI (Script):
Target Selector: Drag "TargetSelector" GameObject here
```

---

## 🧪 **TESTING:**

### **Test Flow:**

1. **Click Play**
2. **Wait for battle to start** (3 heroes vs 2 enemies)
3. **Wait for a hero's turn** (console will show "🎯 [Hero Name] bắt đầu lượt!")
4. **Click "Tấn Công" button**
5. **Observe:**
   - Enemies should be highlighted yellow
   - Cursor should indicate clickable
6. **Click on an enemy**
7. **Observe:**
   - Highlight disappears
   - Console shows attack damage
   - Enemy HP bar decreases
   - Next turn starts

---

## ✅ **EXPECTED RESULTS:**

```
Console Log:
🎯 Cung Thủ bắt đầu lượt!
[BattleUI] Attack button pressed
[TargetSelector] Started selection: SingleEnemy, 2 targets
[EnemyUI] Yêu Tinh clicked!
[TargetSelector] Selected: Yêu Tinh
[BattleUI] Target selected: Yêu Tinh
[BattleManager] Executing action: Attack from Cung Thủ to Yêu Tinh
[BattleManager] Cung Thủ attacked Yêu Tinh for 15 damage!
[EnemyUI] Yêu Tinh took 15 damage!
🎯 Chiến Sĩ bắt đầu lượt!
```

---

## 🐛 **TROUBLESHOOTING:**

### **Problem: Enemies không highlight khi click Attack**

**Solution:**
- Check TargetSelector assigned in BattleUI
- Check EnemyUI prefab có SelectionIndicator + SelectionOutline
- Check Button component enabled trên EnemyUI

### **Problem: Click enemy không phản hồi**

**Solution:**
- Check Button component có Interactable = true
- Check Event System exists trong scene
- Check EnemyUI.selectButton được assign

### **Problem: NullReferenceException khi click enemy**

**Solution:**
- Check BattleManager.GetEnemies() returns valid list
- Check BattleManager.GetCurrentTurnUnit() không null
- Check trong PlayerTurn state mới được attack

---

## 📊 **ARCHITECTURE DIAGRAM:**

```
User Click "Tấn Công"
         ↓
   BattleUI.OnAttackButtonPressed()
         ↓
   TargetSelector.StartTargetSelection()
         ↓
   Highlight all EnemyUI
         ↓
User Click Enemy
         ↓
   EnemyUI.OnClicked()
         ↓
   TargetSelector.OnTargetClicked()
         ↓
   Trigger OnTargetSelected event
         ↓
   BattleUI.OnTargetSelected()
         ↓
   Create BattleAction
         ↓
   BattleManager.ExecuteAction()
         ↓
   ExecuteAttack()
         ↓
   target.TakeDamage()
         ↓
   Trigger OnDamageDealt event
         ↓
   EnemyUI.UpdateUI()
         ↓
   CheckBattleEnd()
         ↓
   StartNextTurn()
```

---

## 🎯 **SUCCESS CRITERIA:**

- [x] Click "Tấn Công" highlights enemies
- [x] Click enemy executes attack
- [x] Damage calculated và applied
- [x] HP bar updates
- [x] Console shows proper logs
- [x] Turn advances automatically
- [x] Battle ends when all enemies dead

---

## 🚀 **NEXT STEP:**

Sau khi Step 1 hoạt động:
→ **Step 2: Enemy AI** (Enemies attack back automatically)

---

**Good luck! Test kỹ và cho tôi biết kết quả!** 💪

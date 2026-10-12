# REBIRTH WARRIOR: Legends of Vietnam
## Unity 2022.3.3F1 LTS - Mobile Android (32-bit Pixel Art)

### 📁 FOLDER STRUCTURE

```
Assets/
├── _Game/
│   ├── Scripts/
│   │   ├── Core/
│   │   │   ├── GameManager.cs
│   │   │   ├── LocalizationManager.cs
│   │   │   └── AudioManager.cs
│   │   ├── Battle/
│   │   │   ├── BattleManager.cs
│   │   │   ├── TurnManager.cs
│   │   │   ├── BattleUI.cs
│   │   │   └── DamageCalculator.cs
│   │   ├── Character/
│   │   │   ├── CharacterStats.cs
│   │   │   ├── CharacterData.cs (ScriptableObject)
│   │   │   ├── SkillData.cs (ScriptableObject)
│   │   │   └── CharacterController.cs
│   │   ├── Enemy/
│   │   │   ├── EnemyData.cs (ScriptableObject)
│   │   │   └── EnemyAI.cs
│   │   ├── World/
│   │   │   ├── WorldMapManager.cs
│   │   │   ├── PlayerMovement.cs
│   │   │   └── EncounterSystem.cs
│   │   ├── UI/
│   │   │   ├── MainMenuUI.cs
│   │   │   ├── PartyUI.cs
│   │   │   ├── InventoryUI.cs
│   │   │   └── MobileInputUI.cs
│   │   ├── Quest/
│   │   │   ├── QuestManager.cs
│   │   │   └── QuestData.cs (ScriptableObject)
│   │   └── Save/
│   │       ├── SaveManager.cs
│   │       └── SaveData.cs
│   │
│   ├── Data/
│   │   ├── Characters/
│   │   ├── Skills/
│   │   ├── Enemies/
│   │   ├── Quests/
│   │   └── Localization/
│   │       ├── Vietnamese.json
│   │       ├── English.json
│   │       └── Chinese.json
│   │
│   ├── Prefabs/
│   │   ├── Characters/
│   │   ├── Enemies/
│   │   ├── UI/
│   │   └── VFX/
│   │
│   ├── Sprites/
│   │   ├── Characters/
│   │   ├── Enemies/
│   │   ├── UI/
│   │   ├── Tiles/
│   │   └── VFX/
│   │
│   ├── Scenes/
│   │   ├── _Bootstrap.unity
│   │   ├── MainMenu.unity
│   │   ├── Battle.unity
│   │   ├── WorldMap.unity
│   │   └── Towns/
│   │
│   └── Audio/
│       ├── BGM/
│       ├── SFX/
│       └── Voice/
│
└── Plugins/
    └── (Third-party assets if needed)
```

### 🎯 DEVELOPMENT PHASES

**Phase 1: Core Systems** (Current)
- Localization Manager
- Battle System Framework
- Character Stats
- Mobile UI Base

**Phase 2-10**: See main plan

### 📋 NAMING CONVENTIONS

**Scripts**: PascalCase (BattleManager.cs)
**Variables**: camelCase (currentHealth)
**Constants**: UPPER_SNAKE_CASE (MAX_PARTY_SIZE)
**Prefabs**: PascalCase with prefix (CHAR_MainHero.prefab)
**Scenes**: PascalCase (BattleScene.unity)

### 🔑 KEY CONSTANTS

```csharp
MAX_PARTY_SIZE = 4
MAX_PET_SIZE = 1
MAX_ENEMY_SIZE = 6
MAX_CHARACTERS_TOTAL = 15
TARGET_FPS = 60
```

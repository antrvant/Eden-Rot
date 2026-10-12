# Hướng Dẫn Setup Hệ Thống Encounter & Spawn Zones (Từ A-Z)

Tài liệu này hướng dẫn chi tiết cách thiết lập (setup) các tính năng mới trong **Rebirth Warrior**:
1. **World Map Random Encounter** (Node tạm thời + Random Scenes).
2. **Tactical Battle Scene** (Thiết lập điểm Spawn mặc định).
3. **Local Spawn Zone** tại các thị trấn/thành phố (City/Town Scene).

---

## 🗺️ PHẦN 1: Thiết Lập Trên World Map (WorldScene)

Hệ thống này tự động tạo một Node địa điểm tạm thời ngay tại vị trí Player đứng khi roll trúng encounter, hiển thị chữ bay báo hiệu, tự động load scene ngẫu nhiên, và xóa Node khi quay lại World Map.

### Bước 1: Thiết lập Vùng quái (WorldMapZone)
1. Trong Hierarchy của scene World Map, tạo một GameObject trống (hoặc chọn một vùng có sẵn) và đặt tên (VD: `Zone_Forest`).
2. Gắn Component **`WorldMapZone`** vào GameObject này.
3. Thêm Component **Collider** (hoặc **Collider2D** đối với map 2D) và **tích chọn `Is Trigger`**. Đây sẽ là ranh giới kích hoạt vùng quái.
4. Trên Inspector của `WorldMapZone`, thiết lập các thông số:
   - **Zone Name**: Tên của khu vực (VD: `Forest Area`).
   - **Level Range**: Ghi chú cấp độ để tham khảo (VD: `Lv 3 - 8`).
   - **Zone Enemies**: Kéo các file `CharacterData` (ScriptableObject) của quái vật có thể xuất hiện trong vùng này vào danh sách.
   - **Dungeon Scenes (Random Maps)**: Danh sách tên các Scene chiến trường chiến thuật được thiết kế sẵn cho khu vực này (VD: `Battle_Forest_01`, `Battle_Forest_02`). Khi xảy ra đụng độ, hệ thống sẽ bốc ngẫu nhiên một scene từ đây.

### Bước 2: Thiết lập Bộ quản lý World Map (WorldMapManager)
1. Chọn GameObject `WorldMapManager` trong Scene.
2. Trên Inspector, đảm bảo đã gán:
   - **World Map Player**: Tham chiếu tới Player Token (`WorldMapPlayer`).
   - **Default Fallback Enemies**: Danh sách quái phòng hờ nếu Zone hiện tại không có dữ liệu quái.
   - **Battle Arena Scenes**: Danh sách scene chiến trường phòng hờ (mặc định là `Battle`) nếu Zone không có scene riêng.
3. Đảm bảo trong Scene có GameObject chứa script **`RandomLocationGenerator`** để quản lý việc spawn và tự dọn dẹp các Node tạm thời.

---

## ⚔️ PHẦN 2: Thiết Lập Scene Chiến Trường (Battle Scene)

Để Player và đồng đội xuất hiện đúng vị trí mong muốn trong scene chiến thuật 3D ngẫu nhiên thay vì vị trí mặc định ở góc bản đồ.

1. Mở Scene chiến trường của bạn (VD: `Battle_Forest_01`).
2. Tạo một GameObject trống ở vị trí bạn muốn Player xuất hiện.
3. Đặt tên GameObject này chính xác là: **`DefaultSpawnPoint`**.
4. Đảm bảo vị trí của `DefaultSpawnPoint` nằm trên lưới **NavMesh** (Thảm màu xanh dương) để tránh việc nhân vật bị kẹt hoặc rơi tự do.

> [!TIP]
> Khi trận đấu bắt đầu, `RandomBattleEncounterLoader` sẽ tự động tìm kiếm GameObject `"DefaultSpawnPoint"` này. Player sẽ được đặt tại vị trí đó, và tối đa 4 Followers (Đồng đội/Thú cưng) đi kèm sẽ tự động xếp thành vòng tròn xung quanh tâm này.

---

## 🏙️ PHẦN 3: Thiết Lập Vùng Spawn Quái Tại City/Town (Local Scene)

Hệ thống này cho phép spawn quái ngẫu nhiên trong một phạm vi (Zone) ở các scene City/Town. Số lượng quái sẽ tự động reset và random lại mỗi khi người chơi tải lại scene đó.

### Bước 1: Chuẩn bị NavMesh
Đảm bảo khu vực City/Town của bạn đã được Bake NavMesh đầy đủ để quái vật có thể di chuyển và spawn đúng vị trí địa hình (Né tránh đá, tường, vật cản). Theo quy tắc của dự án:
1. Tạo GameObject `NavMesh_Controller`.
2. Gắn component `NavMesh Surface`.
3. Set `Use Geometry` = `Physics Colliders` và bấm **Bake**.

### Bước 2: Tạo Zone Spawn Quái Vật
1. Trong Scene City/Town, tạo một GameObject trống và đặt tên (VD: `LocalSpawnZone_Zombies`).
2. Gắn Component **`LocalEncounterZone`** vào GameObject này.
3. Gắn một **Collider 3D** (như `SphereCollider` hoặc `BoxCollider`) vào GameObject này:
   - **Tích chọn `Is Trigger`**.
   - Căn chỉnh kích thước Collider (Bán kính Sphere hoặc Size Box) bao phủ khu vực bạn muốn quái vật xuất hiện.
4. Cấu hình danh sách quái trong Inspector của `LocalEncounterZone`:
   - Bấm vào mục **Spawn Configs** để thêm phần tử.
   - **Enemy Definition**: Kéo ScriptableObject **`EnemySpawnDefinition`** tương ứng của quái vật vào (VD: `Def_Zombie_Standard`).
   - **Min Level / Max Level**: Cấp độ tối thiểu và tối đa của quái vật khi được spawn (VD: Min = 2, Max = 5).
   - **Min Count / Max Count**: Số lượng tối thiểu và tối đa của loại quái này sẽ sinh ra trong zone (VD: Min = 1, Max = 3).
5. **NavMesh Settings**:
   - *Max Spawn Attempts* (Mặc định = 15): Số lần thử tối đa để lấy vị trí ngẫu nhiên trên NavMesh trong bounds của Collider.
   - *NavMesh Search Radius* (Mặc định = 3): Khoảng cách tối đa để warp quái vật xuống mặt lưới NavMesh hợp lệ gần nhất.

> [!NOTE]
> Khi scene được load, `LocalEncounterZone` sẽ chạy hàm `Start()`, tự động tính toán số lượng quái ngẫu nhiên, tính toán level ngẫu nhiên cho từng con, Instantiate các prefab clone của quái vật lên NavMesh, nạp stats cùng các thành phần AI (`CombatEntity`, `TacticalAIController.SetAngered()`) giúp quái sẵn sàng chiến đấu ngay lập tức.

---

## 🛠️ Quy Trình Playtest & Kiểm Tra Nhanh

1. **Kiểm tra World Map**:
   - Di chuyển Player Token trên World Map đi vào vùng Collider của `WorldMapZone`.
   - Di chuyển qua lại cho đến khi roll trúng đụng độ.
   - Kiểm tra xem chữ **"VA CHẠM QUÁI!"** màu đỏ có hiển thị bay lên trên đầu Player không, và log đỏ có xuất hiện góc màn hình không.
   - Game tự động load scene chiến trường trong danh sách. Kết thúc trận đấu, kiểm tra xem Player quay về World Map đúng tọa độ cũ không, và Node đụng độ tạm thời có biến mất hoàn toàn không.

2. **Kiểm tra City/Town**:
   - Load thẳng vào scene City/Town.
   - Quan sát xem số lượng quái vật có được sinh ngẫu nhiên trong vùng Collider quy định và đứng đúng trên mặt lưới NavMesh không.
   - Load lại Scene này lần nữa để kiểm tra xem số lượng và level quái có được thay đổi ngẫu nhiên khác với lần đầu không.

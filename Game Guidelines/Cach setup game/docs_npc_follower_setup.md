# Hướng Dẫn Setup Chuẩn Hệ Thống NPC và Follower/Pet

> Tài liệu này được biên soạn để lưu trữ vĩnh viễn, giúp bạn thiết lập chính xác các phân lớp nhân vật từ Dân Thường (giao Quest, bị móc túi, đánh trả) cho đến Đồng Đội (đi theo, hỗ trợ chiến đấu) mà không bị xung đột vật lý hay thiếu Component.

---

## BỘ CÔNG CỤ 1: SETUP DÂN THƯỜNG / KẺ ĐỊCH (NPC Tuần Tra)
*Tính năng: Đi tuần tự từ A-B-C, kết hợp Hội thoại / Giao Quest, tích hợp hệ thống Móc túi (Pickpocket) bằng Lockpick, tự động nhận diện phe phái, và nổi điên đánh trả nếu bị Player tấn công.*

### Các Component Bắt Buộc Phải Có (Từ trên xuống dưới):

1. **BoxCollider (hoặc CapsuleCollider)**
   - Vô cùng quan trọng. Nếu không bao bọc nhân vật bằng Collider, hệ thống Radar rà quét trận đánh (`Physics.OverlapSphere`) sẽ coi NPC này là tàng hình, không thể bị chĩa súng bắn.
   
2. **Animator**
   - Đảm bảo gán Animator Controller dạng Humanoid chuẩn của Game, có chứa tham số `Speed`, `MotionSpeed` (nếu dùng cơ chế chạy gốc) và Blend Tree. Khoá Root Motion.
   
3. **NavMeshAgent**
   - Không cần quan tâm tới Rigidbody. Unity Navigation chỉ dùng NavMesh.

4. **CombatEntity (Script)**
   - Mục `Base Data`: Kéo 1 Object `CharacterData` vào đây (Nếu tạo Kẻ thù, dùng Data Enemy. Nếu tạo Dân thường, dùng Data Neutral).
   - Mục `Initial Level`: Tuỳ chỉnh.
   
5. **TacticalAIController (Script)**
   - Đây là "Bộ não" trong Combat. Nhờ có nó, Dân thường khi bị bắn trúng mất máu sẽ lập tức kích hoạt cờ "*Nhớ mặt tao đấy*" (`hasPissedMeOff`) và lập tức truy sát người chơi theo đúng chuẩn AI Fallout.
   - Nếu không có script này, NPC đứng im chịu đòn.

6. **NPCMovement (Script)**
   - Gắn các Transform tuần tra vào List `Waypoints` (Điểm A, Điểm B, Điểm C).
   - Chỉnh `Wait Time At Point` = số giây đứng chơi ở mỗi trạm trước khi đi tiếp.
   - *Lưu ý: Tắt hoặc Xóa bỏ script thuần tên là `NPC.cs` cũ đi, vì [NPCMovement](file:///d:/Cong%20Viec/Du%20An%20Game/Survival%20-%20Unity/Rebirth%20Warrior/Assets/Game/Scripts/NPC_System/NPCMovement.cs#11-337) là bản đã được tối ưu chống giật lag vật lý.*

7. **LootContainer (Script)** *(Để Móc Túi/Pickpocket)*
   - Đặt tên `Container ID` (Ví dụ: `npc_danthuong_01`).
   - Tích chọn `Is Locked`.
   - Cài đặt `Lock Difficulty` phù hợp (Sẽ bị cảnh sát vây đánh nếu móc thất bại).
   - Đưa Items vào mục `Initial Contents`. Dù nó là NPC, code vẫn hiểu đây là túi đồ cá nhân để móc lốp.

8. **Tương tác (InteractableLabel + Đối thoại)**
   - Gắn `InteractableLabel` (Tên hiển thị khi re chuột).
   - Gắn tiếp `ActionInteractable` (Hoặc loại Interactable riêng rẽ mà dự án quy định) chứa UnityEvent kích hoạt hàm bật khung chat Dialog System.

---

## BỘ CÔNG CỤ 2: SETUP FOLLOWER VÀ THÚ CƯNG (Đồng Đội)
*Tính năng: Lưu thành Prefab để GameStateManager tự động gọi (Spawn) ra map khi thêm vào Roster. Điền theo Player mượt mà, sẵn sàng ứng chiến mọi lúc.*

> **Bảo hiểm rủi ro:** Kể từ Phase 12 (26/03), hệ thống đã cấy thêm code `Auto-Add` nằm trong lệnh `FollowerController.SetupFromStats()`. Nếu bạn lỡ quên gắn Collider hoặc TacticalAIController cho nó, code sẽ TỰ ĐỘNG dán những component ấy vào cho bạn! Dù vậy, vẫn nên thiết kế từ gốc cho sạch.

### Các Component Cốt Lõi Chung:
- **Animator**
- **BoxCollider** (Chỉnh kích thước cao chuẩn).
- **NavMeshAgent**
- **CombatEntity (Script)** -> *Bỏ trống `Base Data` vì GameStateManager sẽ tự đổ dữ liệu Stats lúc Spawn!*
- **FollowerController (Script)** -> *Bộ não quản lý khoảng cách đứt đuôi (Teleport).*
- **TacticalAIController (Script)** -> *Bộ não đánh theo lượt.*

> **LỖI CHÍ MẠNG CẦN TRÁNH:** 
> TUYỆT ĐỐI KHÔNG BẬT tính năng **Nav Mesh Obstacle** trên đối tượng Follower đang xài NavMeshAgent. Unity cấm thiết lập chặn đường chính chủ thể của nó. Nếu bật, Follower của bạn sẽ đẩy lùi chính mình, nhảy loạn xạ và giật lag lên xuống.

### Phân Nhánh Thêm Component (Rất Quan Trọng):

#### A. Nếu Là NGƯỜI (Human Follower) (VD: Cường, Tuấn)
1. Thêm Script: **[NPCMovement](file:///d:/Cong%20Viec/Du%20An%20Game/Survival%20-%20Unity/Rebirth%20Warrior/Assets/Game/Scripts/NPC_System/NPCMovement.cs#11-337)**
   - Chức năng: Code của FollowerController sẽ tự lấy quyền điều khiển, đặt Player vào chốt `Follow Target`, sau đó để [NPCMovement](file:///d:/Cong%20Viec/Du%20An%20Game/Survival%20-%20Unity/Rebirth%20Warrior/Assets/Game/Scripts/NPC_System/NPCMovement.cs#11-337) vận hành Animator và xoay góc nhìn y hệt 1 NPC bình thường. (Siêu mượt).
2. Follower Controller bỏ qua ô `Is Pet`.

#### B. Nếu Là THÚ CƯNG (Pet / Animals) (VD: Chó, Sói)
1. Thêm Script: **[CreatureMover](file:///d:/Cong%20Viec/Du%20An%20Game/Survival%20-%20Unity/Rebirth%20Warrior/Assets/Game/Resources/Character/Animals_FREE/Scripts/CreatureMover.cs#7-322)** (Có sẵn trong Animals_FREE)
   - Chức năng: CreatureMover sẽ tự quản lý hệ thống CharacterController riêng của Thú. Tôi đã cấu hình lại đầu cắm `axis` của Game đẩy về hệ thống của Animal_FREE, đảm bảo con chó chúi đầu đuổi theo đúng hướng mà không bị lùi ngửa.
2. Follower Controller TÍCH CHỌN ô `Is Pet`.
   - Tích chọn ô này để hệ thống hiểu phải gọi biến Animation `Vert` / [State](file:///d:/Cong%20Viec/Du%20An%20Game/Survival%20-%20Unity/Rebirth%20Warrior/Assets/Game/Scripts/Core/GameStateManager.cs#531-532) (Của động vật) thay vì gọi `Speed` / `Grounded` (Của con người).

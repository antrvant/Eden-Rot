# Hướng dẫn chi tiết: Cách sử dụng Hệ thống Phương tiện di chuyển (Vehicle System)

Tài liệu này hướng dẫn chi tiết cách thiết lập, cấu hình và sử dụng hệ thống phương tiện di chuyển (Vehicle) trong Unity Editor, dành cho người thiết kế màn chơi (Level Designer) hoặc nhà phát triển không cần có kiến thức sâu về lập trình.

---

## 1. Cách tạo một Phương tiện mới (Vehicle Prefab)

Để tạo một chiếc xe hoặc thuyền có thể lái được, hãy làm theo các bước sau:

1. **Chuẩn bị 3D Model:** Kéo Model 3D phương tiện của bạn (xe máy, xe hơi hoặc thuyền) vào trong Scene.
2. **Thêm Component cốt lõi:** Trỏ vào GameObject đó, tại cửa sổ **Inspector**, nhấn **Add Component** và thêm các thành phần sau:
   - **`NavMeshAgent`**: Dùng để tìm đường và di chuyển.
   - **`VehicleController`**: Trực tiếp điều khiển logic của xe.
   - **`VehicleInteractable`**: Cho phép Player tương tác để lên/xuống xe.
   - **`BoxCollider` / `MeshCollider`**: Để có thể click chuột vào xe trên màn hình.
3. **Cấu hình trên `VehicleController`:**
   - **`Vehicle Type`**: Chọn loại xe phù hợp:
     - `Motorbike` (Xe máy): Kích hoạt tư thế ngồi cưỡi dang chân.
     - `Car` (Xe ô-tô): Kích hoạt tư thế ngồi lái tựa lưng.
     - `Boat` (Thuyền): Đi trên mặt nước, tư thế ngồi lái tựa lưng.
   - **`Move Speed`**: Tốc độ di chuyển của xe (ví dụ: `8` hoặc `10`).
   - **`Driver Seat`**: Tạo một **GameObject Empty** con của xe, đặt tên là `Driver_Seat`. Kéo nó tới vị trí mà Player sẽ ngồi lái (trên yên xe hoặc ghế lái). Kéo GameObject này vào trường `Driver Seat` trong Inspector.

---

## 2. Thiết lập Nhiên liệu (Fuel) và Cốp xe (Storage)

### A. Nhiên liệu (Fuel)
- Tích chọn ô **`Use Fuel`** trên `VehicleController`.
- Thiết lập:
  - **`Fuel`**: Lượng xăng hiện tại của xe (ví dụ: `100`).
  - **`Max Fuel`**: Lượng xăng tối đa xe có thể chứa (ví dụ: `100`).
  - **`Fuel Consumption Rate`**: Lượng xăng tiêu hao mỗi giây khi xe di chuyển (ví dụ: `1`).

### B. Cốp xe chứa đồ (Storage)
- Tích chọn ô **`Has Storage`** trên `VehicleController`.
- Nhấn **Add Component** và thêm component **`LootContainer`** vào xe.
- Cấu hình `LootContainer`:
  - Đặt tên cho rương tại ô **`Container ID`** (ví dụ: `Player_Motorbike_Trunk`).
  - Cấu hình các vật phẩm ban đầu hoặc để trống nếu người chơi chỉ dùng để cất đồ.
- Kéo component `LootContainer` này vào ô **`Storage`** của `VehicleController`.

---

## 3. Cấu hình Animator cho Player (Tư thế ngồi lái)

Hệ thống điều khiển phương tiện sử dụng 2 tham số (Parameters) trong Animator Controller để tự động đổi tư thế ngồi lái cho Player:
1. **`InVehicle` (kiểu Bool):** Đánh dấu Player đang ở trong xe.
2. **`VehicleType` (kiểu Int):** Xác định tư thế ngồi tương ứng:
   - `0` = Xe máy (Ngồi cưỡi yên xe, hai tay vươn về phía trước).
   - `1` = Ô-tô (Ngồi ghế lái, tay giữ vô lăng).
   - `2` = Thuyền (Ngồi ghế lái tàu thủy).

### Cách thiết lập trong Unity Animator:
1. Mở Animator Controller của Player.
2. Tại tab **Parameters**, nhấn dấu `+` để thêm:
   - Parameter loại **Bool**, đặt tên là `InVehicle`.
   - Parameter loại **Int**, đặt tên là `VehicleType`.
3. Tạo các State tương ứng với các hoạt ảnh lái xe: `Ride_Motorbike`, `Sit_In_Car`, `Sit_In_Boat`.
4. Tạo Transition đi từ trạng thái mặc định (Locomotion) sang các State lái xe khi `InVehicle == true` và chuyển tiếp ngược lại khi `InVehicle == false`.

---

## 4. Cấu hình Tìm đường và Giới hạn mặt nước (NavMesh)

Để đảm bảo Thuyền chỉ chạy dưới nước và Xe chỉ chạy trên cạn, ta tận dụng **NavMesh Area**:

### Bước 1: Định nghĩa Area trong Unity
- Mở cửa sổ **Window > AI > Navigation** (hoặc `NavMesh` mới).
- Chọn tab **Areas**.
- Thêm một Area mới mang tên **`Water`** (ví dụ: ở hàng thứ 4).

### Bước 2: Gán Area cho Địa hình sông ngòi
- Chọn Mesh đại diện cho mặt nước (sông, biển).
- Trong cấu hình Bake NavMesh, đổi Area Type của Mesh này thành **`Water`**.
- Tiến hành **Bake** lại NavMesh. Toàn bộ vùng nước sẽ hiển thị một màu NavMesh riêng biệt (ví dụ: màu tím hoặc xanh nhạt).

### Bước 3: Tự động chạy logic Area Mask
Hệ thống phương tiện đã tự động xử lý Area Mask:
- Khi game chạy, `VehicleController` sẽ tự động quét Area `Water`:
  - **Boat:** Thiết lập chỉ đi trên vùng `Water`. Cấm chạm cạn.
  - **Car & Motorbike:** Đi trên tất cả các vùng cạn, cấm đi xuống vùng `Water`.
- **Cơ chế lên bờ an toàn:** Khi lái Thuyền và bấm xuống xe, hệ thống sẽ tự tìm bờ đất liền (`Walkable` gần nhất trong bán kính 5m) để warp cả Player và đồng đội lên bờ. Nếu thuyền ở quá xa bờ (ngoài 5m), hệ thống sẽ chặn không cho xuống xe.

---

## 5. Cách thiết lập Xe AI tuần tra tự động (AI Patrol Vehicle)

Nếu bạn muốn tạo các phương tiện chạy tự động trên đường phố và phát thoại như NPC:

1. Kéo Prefab xe vào Scene.
2. Tích chọn ô **`Is Patrol Vehicle`** trong `VehicleController`.
3. Tạo một tuyến tuần tra bằng cách tạo một GameObject có component **`PatrolPath`** (đã có sẵn trong game), đặt các waypoint con.
4. Kéo `PatrolPath` đó vào trường **`Patrol Path`** của `VehicleController`.
5. Thiết lập thời gian nghỉ tại mỗi điểm tại ô **`Wait Time At Point`**.
6. **Cấu hình Barks (Phát thoại bong bóng):**
   - Thêm component **`ChatBubbleUI`** vào vị trí trên nóc xe (dùng để hiện chữ).
   - Kéo nó vào trường **`Chat Bubble`** của `VehicleController`.
   - Tạo một asset **`NPCBarkProfile`** chứa lời thoại cho xe (tiếng động cơ, tiếng còi hú) và kéo vào ô **`Bark Profile`**.

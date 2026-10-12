# SUPER PROMPT - DỰ ÁN GAME UNITY - REBIRTH WARRIOR
**Version:** 4.0 - Updated December 2025
**Unity Version:** 2022.3.3f1 LTS

## PHẦN A: BỐI CẢNH VÀ MỤC TIÊU DỰ ÁN

### 1. Tóm Tắt Dự Án
* **Tên Game:** Rebirth Warrior (Chiến Hồn - Huyền Thoại Trọng Sinh)
* **Thể loại:** Turn-based RPG 2.5D (Isometric View, 8-Direction), pixel art style 32-bit.
* **Platform:** Mobile & PC
* **Mô tả:** Nhân vật chính là người hiện đại chơi game nhiều quá qua đời và được trọng sinh về Việt Nam thời xưa, khi quân Nguyên Trung Quốc đang xâm chiếm. Game có yếu tố fantasy, kết hợp cốt truyện Final Fantasy 4 với yếu tố truyện trọng sinh.

### 2. Vòng Lặp Gameplay Cốt Lõi
Updated Logic:

New Game: Vào CharacterCreation.

Prologue (2025): Load Map_HCMC_2025. Đánh Boss cứu người đẹp -> Scripted Defeat (Thua theo kịch bản).

Time Jump (2100): Chuyển cảnh sang Map_HCMC_2100. Gặp Rebirth Boss -> Scripted Defeat.

Rebirth Event: Chuyển sang Rebirth_UI. Reset Level về 1. Giữ Class. Nhận +20 Unspent Stat Points.

New World (2060): Load Map_HCMC_2060. Bắt đầu gameplay chính thức (World Map hệ thống Fallout).

Người chơi Khám Phá bản đồ Overworld (kiểu Fallout) -> Forest/Dungenon/City -> Va chạm với kẻ địch -> Chuyển sang màn Chiến Đấu -> Đánh bại kẻ địch -> Quay lại màn Forest/Dungenon/City tương ứng -> Thu thập vật phẩm rơi ra -> Lặp lại.


### 3. Overworld, Forest/Dungenon, City, và Battle Scene
GameManager (Core): Đóng vai trò "Supervisor". Tự động phát hiện Scene mới load. Nếu Scene thiếu Player, tự động Instantiate Player từ Prefab (Resources).

WorldManager (WorldMap): Quản lý map thế giới mở (di chuyển token). Chịu trách nhiệm nhận Player từ GameManager và đặt lại vị trí cũ (RestoreSavedPosition) khi load game hoặc quay về từ Battle.

TownManager (Isometric): Quản lý map thị trấn/dungeon (di chuyển 8 hướng). Logic tương tự WorldManager nhưng xử lý SpawnPoint theo ID cổng (Portal System).

Cơ chế lưu vị trí: Sử dụng PlayerPrefs với các key: WorldPositionX, WorldPositionY, ReturnScene, ReturningFromBattle.

* **Overworld (Bản Đồ Thế Giới):**  Thay vì một lục địa giả tưởng, Overworld là bản đồ Trái Đất thực tế nhưng bị tàn phá. Giao diện hiển thị theo phong cách Hologram chiến thuật (do bối cảnh năm 2060). Cơ chế di chuyển: Player điều khiển Main Player (hoặc phương tiện). Phương tiện: Xe máy điện tương lai (E-Bike), Xe bọc thép quân sự, và giai đoạn sau có thể là Máy bay vận tải VTOL (để di chuyển giữa các châu lục).

 * **Khu Vực 1: ĐÔNG NAM Á - VÙNG ĐẤT KHỞI NGUYÊN (The Origin)** 
   * **`Bối cảnh:** Năm 2060, mực nước biển dâng cao kết hợp với thảm họa Zombie khiến Đông Nam Á trở thành một vùng "Venice nhiệt đới" hoang tàn và ẩm ướt. Cây cối bao phủ các tòa nhà chọc trời.
    * **`Cốt truyện:**  Main Player (nhân vật chính) tỉnh dậy tại một hầm trú ẩn sinh học ở TP.HCM sau 5 năm ngủ đông (cryo-sleep). Anh cần tìm Mia (người giữ dữ liệu về nguồn gốc virus).
    * **`Nhân vật:** 
        * **`Mia:**  Được tìm thấy tại khu tị nạn trên cao ở Bangkok. 
        * **`Chú chó (Companion):** Một chú chó Phú Quốc thông minh, tìm thấy khi đang bảo vệ xác chủ cũ tại khu tàn tích Thủ Thiêm.
    * **`Kẻ thù:** 
        * **`Biter/Crawler:**   Dân thường bị nhiễm bệnh.
        * **`Swamp Stalker (Mới):**  Zombie đột biến thích nghi với vùng ngập nước (thay thế cho loại ngụy trang bùn), xuất hiện ở vùng Mekong
    * **`Thành phố:** 
        * **`TP. Hồ Chí Minh (Neo-Saigon):**   Điểm xuất phát. Landmark 81 (đã gãy đôi) là mốc định vị. Khu vực Thủ Thiêm ngập nước, di chuyển bằng thuyền bè.
        * **`Mekong Delta (Vùng Đất Ngập Mặn):**   Nơi tìm nguyên liệu thuốc, nguy hiểm vì tầm nhìn thấp.
        * **`Bangkok (Thành Phố Nổi):**   Các khu chợ nổi trên dòng nước đen ngòm, nơi ẩn náu của các nhóm buôn lậu.
        * **`Singapore (Vườn Địa Đàng Chết):** Một khu vực kính (Dome) bị vỡ, cây cối mọc um tùm, nơi chứa các công nghệ sinh học cũ (tương ứng với "Greenhaven").   

 * **Khu Vực 2: TRUNG QUỐC & NGA - VÙNG ĐẤT SẮT THÉP & BĂNG GIÁ (The Iron & Frost)** 
   * **`Bối cảnh:** Từ khí hậu nhiệt đới chuyển sang vùng đất công nghiệp ô nhiễm nặng nề của Trung Quốc và vùng băng giá vĩnh cửu của Siberia (Nga).
    * **`Cốt truyện:**  Main Player truy đuổi dấu vết của Caleb (Kẻ phản diện) - kẻ đã cướp đi mẫu máu kháng thể đầu tiên. Tại đây, Alex gặp Jax.
    * **`Nhân vật:** 
        * **`Jax:**   Một kỹ sư cơ khí người Nga, đang cố sửa một chiếc xe thiết giáp "Gấu Đen" tại một nhà máy bỏ hoang ở Thẩm Dương. 
        * **`Caleb:**  Xuất hiện lần đầu với tư cách thủ lĩnh băng đảng "Red Dragon", chiếm giữ các mỏ tài nguyên.
    * **`Kẻ thù:** 
        * **`Bloater:**   Zombie chứa khí gas độc hại từ các khu công nghiệp.
        * **`Titan (Hạng III):**   Zombie khổng lồ mặc giáp chống bạo động (còn sót lại từ quân đội) hoặc bị đóng băng một phần (ở Nga), rất trâu bò.
    * **`Thành phố:** 
        * **`Thượng Hải (The Drowned City):**   Các tòa tháp chọc trời nhô lên khỏi mặt nước biển, di chuyển giữa các tòa nhà bằng cầu treo tạm bợ.
        * **`Vạn Lý Trường Thành (The Wall):**  Đã được quân đội gia cố thành pháo đài phòng thủ nhưng đã thất thủ, giờ đầy rẫy xác sống.
        * **`Siberia (The Frozen Wasteland):**   Bão tuyết làm giảm tầm nhìn và tụt máu theo thời gian. Nơi chứa các trạm nghiên cứu quân sự bí mật (Loot vũ khí hạng nặng).

 * **Khu Vực 3: NHẬT BẢN & HÀN QUỐC - VÙNG ĐẤT CÔNG NGHỆ CAO (The High-Tech Ruins)** 
   * **`Bối cảnh:** Các đô thị Cyberpunk với đèn Neon chập chờn. Đây là nơi công nghệ phát triển nhất nhưng cũng là nơi Virus biến đổi mạnh nhất do mật độ dân số cao.
    * **`Cốt truyện:**  Nhóm cần tìm một con tàu hoặc máy bay để vượt đại dương sang phương Tây. Họ phải đối mặt với các Zombie bị cấy ghép máy móc (Cyborg-zombies).
    * **`Nhân vật:** 
        * **`Tsubaki:**  Một nữ kiếm sĩ hiện đại (sử dụng Katana công nghệ cao), sống ẩn dật tại Kyoto. Cô ấy giữ chìa khóa khởi động hệ thống vượt biển.
    * **`Kẻ thù:** 
        * **`Pouncer (Cyber-enhanced):**  Zombie nhanh nhẹn, có thể có các bộ phận cơ khí gắn trên người giúp chúng nhảy cao hơn.
        * **`Mutant (Thủy quái):**  Xuất hiện ở các cảng biển và khu vực ven biển.
    * **`Thành phố:** 
        * **`Seoul (The Neon Graveyard):**  Thành phố không ngủ nay chỉ còn ánh đèn báo động đỏ.
        * **`Tokyo (Shibuya Crossing):**   Khu vực Horde (bầy đàn) lớn nhất game. Hàng ngàn zombie tụ tập tại ngã tư này.
        * **`Busan (The Harbor):**   Cảng biển quân sự kiên cố, nơi người chơi phải thực hiện nhiệm vụ phòng thủ để sửa tàu.

 * **Khu Vực 4: Châu Âu - Tàn Tích Cổ Đại (The Old World)** 
   * **`Bối cảnh:** Những kiến trúc cổ kính (Tháp Eiffel, Đấu trường La Mã) nằm điêu tàn. Đây là nơi các tổ chức thế giới cũ (như WHO, NATO) cố gắng trụ lại cuối cùng nhưng thất bại.
    * **`Cốt truyện:**  Nhóm đến đây để tìm kiếm "Dữ liệu Gốc" (Patient Zero) được đồn là lưu trữ tại Geneva, Thụy Sĩ. Tại đây, họ phát hiện Caleb đã đi trước một bước và đang hướng về Mỹ.
    * **`Nhân vật:** 
        * **`Lyra:**  Một nhà khoa học của tổ chức y tế cũ, đang trốn dưới hầm ngầm Paris (Catacombs). Cô ấy cung cấp công thức chế tạo huyết thanh.
    * **`Kẻ thù:** 
        * **`Screamer:** Thường là các zombie nữ, tiếng hét của chúng gọi bầy đàn từ các ngõ ngách hẹp của thành phố cổ.
        * **`Knight/Guard:** Zombie mặc giáp bảo tàng hoặc giáp chống bạo động Châu Âu.
    * **`Thành phố:** 
        * **`London (The Fog):** Sương mù dày đặc (tương tự Khu vực 5 cũ), tầm nhìn cực thấp.
        * **`Paris (The Catacombs):** Hệ thống Dungeon dưới lòng đất, cực kỳ tối tăm và chật hẹp.
        * **`Geneva (The Sanctuary Ruins):** Từng là vùng an toàn, nay là bẫy chết người với hệ thống an ninh tự động bắn bất cứ thứ gì di chuyển.

 * **Khu Vực 5: NHẬT BẢN & HÀN QUỐC - VÙNG ĐẤT CÔNG NGHỆ CAO (The High-Tech Ruins)** 
   * **`Bối cảnh:** Trung tâm của sự sụp đổ. Từ bờ Đông (New York) hoang tàn đến bờ Tây (Sa mạc Nevada/California) nóng bỏng.
    * **`Cốt truyện:** Cuộc đua cuối cùng đến trụ sở của tập đoàn tạo ra Virus (đặt tại sa mạc Nevada). Caleb đã biến đổi thành một dạng quái vật lai (Hybrid).
    * **`Nhân vật:** 

    * **`Kẻ thù:** 
        * **`The Abomination:** Các thể nghiệm thất bại.
        * **`Quân đội tư nhân:**  Lính đánh thuê của Caleb (kẻ thù con người có súng).
        * **`The Overlord (Caleb biến hình):**  Trùm cuối.
    * **`Thành phố:** 
        * **`New York (Concrete Jungle):**  Các tòa nhà đổ nát tạo thành các mê cung 3D.
        * **`Las Vegas (The Buried City):** Bị chôn vùi một nửa dưới cát sa mạc. Ánh nắng gay gắt làm giảm thể lực.
        * **`Khu vực 51 (Ground Zero):** Dungeon cuối cùng. Cơ sở nghiên cứu ngầm nơi mọi thứ bắt đầu.
    
* **Forest/Dungenon:** Khi di chuyển trên Overworld thì Player sẽ random bị dịch chuyển vào khám phá Forest/Dungenon. Các màn chơi Forest/Dungenon sẽ được tạo sẵn trong Unity và được gọi ra tùy thuộc vào khu vực Player di chuyển trên bản đồ OverWorld. Ứng với mỗi khu vực Overworld sẽ có 1 số màn chơi Forest/Dungenon tạo sẵn và sẽ được random từ số màn chơi đó.  
* **Thành Phố / Làng Mạc (City):** Thành Phố / Làng Mạc (City) sẽ hiển thị cố định trên OverWorld. Player sẽ di chuyển tới nơi thì chọn Enter sẽ được chuyển vào Thành Phố / Làng Mạc (City) đó. Các màn chơi Thành Phố / Làng Mạc (City) sẽ được tạo sẵn trong Unity và được gọi ra khi Player Enter di chuyển vào.
* **Battle Scene:** nơi Player và Enemy sẽ tấn công theo lượt, và lượt chơi bắt đầu là dựa trên tốc độ (agi giữa Player và Enemy, agi cao đi trước. Nếu agi bằng nhau thì random ngẫu nhiên).

### 4. BATTLE & LOOT SYSTEM (Chiến đấu & Vật phẩm)
Logic Drop và điều kiện thắng thua.
EncounterManager: Tự động lưu Scene hiện tại (ReturnScene) trước khi chuyển cảnh sang Battle. Fix lỗi Player bị spawn về điểm bắt đầu game sau khi đánh quái.

BattleRewards: Class trung gian xử lý logic phần thưởng. Hỗ trợ Loot vật phẩm có số lượng (DroppedItemInfo) và tự động cộng Vàng/EXP vào GameStateManager.

VictoryScreen: Hiển thị Loot chi tiết (Icon + Tên + Số lượng). Tự động load lại Scene cũ dựa trên key ReturnScene.

* **1. Drop System (Real-time Loot):**

    * **Trigger:**  Rớt đồ ngay khi Quái chết (Unit Die Animation), không đợi hết trận.

    * **Logic:** Tính toán độc lập cho từng quái.

    * **Quest Item:** Check điều kiện IsQuestActive. Nếu là Item nhiệm vụ, kiểm tra trong túi đã có chưa (để tránh rớt dư thừa nếu cần).

    * **Victory UI:** Tổng hợp (Stack) các item đã rớt trong trận để hiển thị danh sách gọn gàng.
* **2. Defeat Condition:**
    * **Thắng:** Khi Enemy hết máu. Người chơi nhận thưởng, quay lại Forest/Dungenon/City tương ứng, Enemy biến mất (Nếu là có trên MAP).

    * **Thua:**  Tất cả Human Characters (Main + Followers) chết. Player quay lại Forest/Dungenon/City tương ứng sẽ bị dịch chuyển ra khỏi Enemy.

    * Pet: Pet còn sống không tính là team còn sống.

    * Main Player Death: Nếu Main Player chết nhưng thắng trận, khi ra ngoài World sẽ được hồi sinh với 1 HP.


### 5. Stats, kĩ năng và level
* **Stats:** Nhân vật (Player/Partners) và Kẻ thù (Enemy) đều sở hữu bộ chỉ số cơ bản.

Danh sách chỉ số:

HP (Máu): Khởi điểm 100. Mỗi điểm Stat cộng vào = +10 HP Max.

Stamina (Thể lực): (Mới) Dùng cho hành động vật lý/kỹ năng.

Atk (Sức đánh): Khởi điểm 10. Tăng sát thương vật lý.

Def (Phòng thủ): Khởi điểm 10. Giảm sát thương vật lý nhận vào.

Agi (Tốc độ): Khởi điểm 1. Quyết định thứ tự đánh trong Battle.

Luck (May mắn): Khởi điểm 1. Tăng tỷ lệ chí mạng và rơi đồ. (Giới hạn tối đa: 30).

ToxicAtk (Độc công): Sát thương độc.

ToxicResist (Kháng độc): Giảm sát thương độc và tỷ lệ trúng độc.

Cơ chế tăng điểm:

Player/Partners: Mỗi khi lên cấp nhận 5 Unspent Stat Points. Người chơi phải cộng thủ công qua UI.

Enemy: Chỉ số cố định theo Config (Level/Type) trong Unity Editor.
* **Kĩ Năng:** Player sẽ có thanh kỹ năng dựa trên sách kỹ năng lụm được trên đường đi. Sách kỹ năng sẽ được thêm vào trong lúc làm game. Mỗi level sẽ có 5 điểm kĩ năng để tăng vào. Điểm càng cao thì kĩ năng sử dụng càng mạnh. Riêng Partners/Enemy sẽ có kỹ năng cố định, chỉ có thể tăng cấp kĩ năng cố định đó nếu tăng level, chứ không học thêm được kĩ năng mới.
* **Level:** Chỉ riêng Level của Player và Partners ban đầu sẽ là 1, các nhân vật khác sẽ có 1 level cố định được quy định dựa trên hệ thống cấp độ level của tuyến nhân vật Phụ. Level Max của 

Level Cap: Max Level là 100.

Khởi đầu: Player/Partners bắt đầu ở Level 1. NPC/Enemy có level cố định.

Công thức EXP: Công thức tính tổng EXP cần thiết để đạt cấp độ N: EXP_Required = (N-1)^2 * 100 + (N-1) * 1000

Bảng tham khảo:

Lv 1 -> 2: (1)^2*100 + 1*1000 = 1,100 EXP

Lv 2 -> 3: (2)^2*100 + 2*1000 = 2,400 EXP

Lv 3 -> 4: (3)^2*100 + 3*1000 = 3,900 EXP

Lv 9 -> 10: (9)^2*100 + 9*1000 = 8,100 + 9,000 = 17,100 EXP

Lv 99 -> 100: (99)^2*100 + 99*1000 = 980,100 + 99,000 = 1,079,100 EXP
* **Level Up Logic:**
Main Player: Khi lên cấp KHÔNG tự tăng chỉ số. Nhận UnspentStatPoints (Mặc định 5 + Config). Người chơi phải tự cộng điểm thủ công vào (STR, AGI, INT...) thông qua UI.
Followers/Pets: Khi lên cấp TỰ ĐỘNG tăng chỉ số dựa trên GrowthRate trong CharacterData.

### 6. CÔNG THỨC TÍNH SÁT THƯƠNG & CHIẾN ĐẤU (UPDATED)

Hệ thống sát thương được chia thành 2 phần: **Sát thương Vật lý** và **Sát thương Độc (Toxic)**. Tổng sát thương là tổng của hai thành phần này sau khi tính toán riêng biệt.

#### 1. Tính Sát Thương Vật Lý (Physical Damage)
Dựa trên chỉ số Tấn công (Atk) và Phòng thủ (Def).
* **Công thức:** `Physical_Dmg = MAX(0, (Atk - Def * K) * M)`
    * `Atk`: Chỉ số tấn công vật lý.
    * `Def`: Chỉ số phòng thủ vật lý.
    * `K`: Hệ số xuyên giáp (Ví dụ: 0.8). Giúp Atk không bị triệt tiêu hoàn toàn bởi Def.
    * `M`: Hệ số khuếch đại (Ví dụ: 1.5).

#### 2. Tính Sát Thương Độc (Toxic Damage)
Dựa trên chỉ số Độc công (ToxicAtk) và Kháng độc (ToxicResist). Sát thương độc thường xuyên qua giáp vật lý nhưng bị chặn bởi kháng độc.
* **Công thức:** `Toxic_Dmg = MAX(0, ToxicAtk - ToxicResist)`
    * `ToxicAtk`: Chỉ số tấn công độc (từ vũ khí tẩm độc hoặc skill).
    * `ToxicResist`: Chỉ số kháng độc của trang bị hoặc cơ chế sinh tồn.

#### 3. Tổng Sát Thương Cơ Bản
* **Công thức:** `Base_Dmg = Physical_Dmg + Toxic_Dmg`
    * Nếu kết quả <= 0, sát thương tối thiểu luôn là **1**.

#### 4. Cơ Chế Chí Mạng (Critical Hit)
Sử dụng chỉ số May mắn (Luck).
* **Tỷ lệ chí mạng (%):** `Crit_Chance = Luck` (Ví dụ: Luck 15 = 15%).
* **Sát thương chí mạng:** Nếu nổ Crit, Tổng sát thương được nhân đôi (hoặc x1.5 tùy cân bằng).
    * **Công thức:** `Final_Dmg = Base_Dmg * 2`

#### 5. Hiệu Ứng Phụ (Side Effects)
* Nếu `Toxic_Dmg > 0`: Mục tiêu sẽ bị tích luỹ điểm ngộ độc (Poison Buildup), gây mất máu theo thời gian (DoT) ở các lượt sau.
* Hành động tiêu tốn **Stamina**: Các đòn tấn công đặc biệt hoặc Skill sẽ trừ Stamina thay vì MP.

---
**Ví dụ tổng hợp:**
Player có: Atk=150, ToxicAtk=50, Luck=15.
Enemy có: Def=100, ToxicResist=20.
Hệ số: K=0.8, M=1.5.

1. **Vật lý:** `(150 - 100*0.8) * 1.5` = `(150 - 80) * 1.5` = `105` dmg.
2. **Độc:** `50 - 20` = `30` dmg.
3. **Tổng cơ bản:** `105 + 30 = 135` dmg.
4. **Chí mạng:**
   - Nếu không Crit: Gây **135** sát thương (hiển thị 105 cam + 30 tím).
   - Nếu Crit (15%): Gây **270** sát thương.

### 7. Hệ thống nhân vật Phụ
* **Người đồng hành (Partners):** đây là những nhân vật đi theo Players. Những nhân vật này sẽ ở các vị trí cố định. Player chỉ thu phục được các partners khi đáp ứng được các điều kiện quy định. Partners cũng sẽ có Stats, kĩ năng và level như Player. Riêng kĩ năng của Partners sẽ có sẵn và không thể học thêm, chỉ có thể tăng cấp cho kĩ năng đã có sẵn.
 * **`Mia:**  Chuyên gia y tế. Từng là sinh viên y khoa, Mia là người chữa trị và hỗ trợ tinh thần cho nhóm. Cô ấy là hiện thân của lòng nhân ái và hy vọng.
 * **`Jax:**  Thợ máy và chuyên gia vũ khí. Jax là một cựu chiến binh, có kinh nghiệm chế tạo và sửa chữa mọi thứ. Anh ta là người thực tế, đôi khi cộc cằn nhưng đáng tin cậy.
 * **`Tsubaki:**   Một người phụ nữ bí ẩn, có thể là võ sĩ hoặc chuyên gia cận chiến. Cô ấy ít nói nhưng hành động dứt khoát. Tsubaki đại diện cho sức mạnh và sự kiên cường.
 * **`Lyra:**  Một cô bé sống sót một mình, có khả năng đặc biệt cảm nhận được sự hiện diện của zombie hoặc "sự hỗn loạn" trong thế giới. Cô bé đi cùng Alex, cung cấp thông tin và là lời nhắc nhở cho Alex về lý do anh ta chiến đấu.
 * **`Hopper:**  Chú chó trung thành. chú chó có tính cách năng động, thích chạy nhảy.

* **NPC:** NPC sẽ là những nhân vật di chuyển trong 1 khu vực nhất định, hoặc đứng yên tại 1 vị trí nhất định. NPC sẽ bao gồm con người, animal.
* **NPC Quest:** NPC Quest sẽ là những nhân vật di chuyển trong 1 khu vực nhất định, hoặc đứng yên tại 1 vị trí nhất định. NPC Quest sẽ cung cấp nhiệm vụ cho Player làm để được thưởng điểm kinh nghiệm, items, tiền.
* **Merchant/Shopkeeper:** là những nhân vật di chuyển trong 1 khu vực nhất định, hoặc đứng yên tại 1 vị trí nhất định. Player có thể tương tác với các nhân vật này để mua sắm, sửa chửa hoặc nâng cấp vũ khí/áo giáp.
* **Enemy:** Nhân vật phản diện, Zombie, quái, Boss. Tất cả nhân vật này khi va chạm với Player sẽ chuyển sang chế độ Battle Scene.
    * **Biter:** **(Zombie Hạng I)**      Zombie cơ bản, chậm chạp, dễ bị hạ gục. Số điểm Exp Player đạt được khi giết 50 EXP
    * **Crawler:** **(Zombie Hạng I)**    Bị cụt chân, di chuyển bằng cách bò. Chúng bất ngờ và khó phát hiện. Số điểm Exp Player đạt được khi giết 75 EXP
    * **Screamer:** **(Zombie Hạng I)**   Zombie tạo ra tiếng kêu chói tai để thu hút đồng loại. Số điểm Exp Player đạt được khi giết 100 EXP
    * **Pouncer:** **(Zombie Hạng II)**   Zombie nhanh nhẹn, có thể nhảy vọt và tấn công bất ngờ. Số điểm Exp Player đạt được khi giết 200 EXP
    * **Spitter:** **(Zombie Hạng II)**   Có khả năng phun ra dịch độc. Số điểm Exp Player đạt được khi giết 250 XP
    * **Bloater:** **(Zombie Hạng II)**   Zombie béo phì, khi bị hạ gục sẽ phát nổ, gây sát thương diện rộng. Số điểm Exp Player đạt được khi giết 300 XP
    * **Titan:** **(Zombie Hạng III)**    Zombie khổng lồ, chậm nhưng cực kỳ mạnh mẽ. Số điểm Exp Player đạt được khi giết 1000 XP
    * **Hunter:**  **(Zombie Hạng III)**  Loại zombie thông minh, có thể đặt bẫy và săn lùng con mồi theo nhóm. Số điểm Exp Player đạt được khi giết 1200 XP
    * **The Abomination:** **(Boss)**     Một quái vật lai tạo từ nhiều xác sống, có nhiều chi và khả năng tấn công đa dạng. Số điểm Exp Player đạt được khi giết 200000 XP
    * **The Overlord:** **(Boss)**        Một con người bị biến đổi, vẫn giữ được trí thông minh nhưng có sức mạnh phi thường. Số điểm Exp Player đạt được khi giết 400000 XP
    * **Caleb:**  **(Boss)**              Một cựu lãnh đạo quân đội, tin rằng để sống sót, con người phải hy sinh đạo đức. Hắn ta điều hành một phe phái tàn bạo, sẵn sàng cướp bóc và giết chóc để duy trì quyền lực. Caleb đại diện cho sự tuyệt vọng và tàn bạo của con người. Số điểm Exp Player đạt được khi giết 1500000 XP

### 8. Core Mechanics
* **Turn-based Combat:** Dựa trên Speed/Agility để quyết định lượt
* **Party System:** Max 4 characters + 1 pet
* **15 Character Classes:** Warrior, Mage, Healer, Archer, etc.
* **Rebirth System:** Unique mechanic - chuyển đổi class khi chết
* **Skills System:** Học skills từ sách kỹ năng
* **Equipment System:** Weapon, Armor, Accessory slots
* **Quest System:** Main quests + Side quests
* **Save/Load System:** JSON-based persistence

### 9. WORLD & NAVIGATION (Di chuyển & Bản đồ)
* **World Map:** Di chuyển trên bản đồ thế giới lớn (giống Fallout 2)
* **Town/Village:** Khám phá thành phố, mua bán, nhận quest
* **Battle Scene:** Turn-based combat riêng biệt
* **Dialogue:** Hệ thống Dialouge quản lý nói chuyện, câu thoại giữa player và các npc, boss

* **1. Portal System (ID Matching):**

Không dùng tọa độ cứng (X,Y) để spawn.

Cơ chế: Cổng ra (TownExit) gửi đi một TargetSpawnID. Scene mới (TownManager/WorldManager) tìm GameObject có tên trùng với ID đó và đặt Player tại đó.

Scripts: TownEntrance, TownExit, TownManager, WorldManager (được nâng cấp để hỗ trợ ID).

* **2. Quest Navigation (Chỉ đường thông minh):**

Data: Sử dụng QuestLocationDatabase (ScriptableObject).

Lưu vị trí mục tiêu (TargetID -> Scene + Coordinate).

Lưu kết nối cổng (FromScene -> ToScene -> PortalPosition).

Logic Mũi tên (QuestNavigator):

Nếu cùng Scene: Chỉ thẳng vào mục tiêu.

Nếu khác Scene: Tra cứu Database để tìm tọa độ Cổng dẫn tới Scene tiếp theo -> Chỉ vào Cổng.

Visual: Mũi tên xoay quanh nhân vật, Sorting Layer = UI (để không bị map che).

## PHẦN B: CẤU TRÚC PROJECT & FOLDERS

### 1. Kiến Trúc Tổng Thể & Design Patterns
* **Singleton Pattern:** Vẫn là kiến trúc xương sống cho các hệ thống quản lý toàn cục.
* **Data-Driven Design (ScriptableObjects):**
    * **`WeaponInfo` & `EnemyData`:** Tách biệt dữ liệu vũ khí và kẻ thù khỏi logic.
    * **`SceneBackgroundDatabase`:** **(MỚI)** Một ScriptableObject đóng vai trò cơ sở dữ liệu trung tâm, quản lý ảnh nền chiến đấu cho tất cả các scene, giúp loại bỏ sự phụ thuộc vào các script riêng lẻ trong từng scene.
* **Interface-based Design:** Sử dụng interface `IWeapon` và `IEnemy` để tạo các hệ thống có tính mở rộng.
* **Unity's New Input System:** Quản lý input qua file `Player Controls.inputactions`.

### 2. Cấu Trúc Hệ Thống (Systems)
```
Assets/
├── Game/
│   ├── Scripts/
│   │   ├── Battle/           # Combat system scripts
│   │   │   ├── BattleAction.cs
│   │   │   ├── BattleItemButtonUI.cs
│   │   │   ├── BattleLoader.cs
│   │   │   ├── BattleManager.cs
│   │   │   ├── BattleRewards.cs
│   │   │   ├── BattleStation.cs
│   │   │   ├── BattleTypes.cs
│   │   │   ├── BattleUI.cs
│   │   │   ├── BattleUnitClickable.cs
│   │   │   ├── BattleUnitHUD.cs
│   │   │   ├── BattleVisualController.cs
│   │   │   ├── DamageCalculator.cs
│   │   │   ├── DefeatPenalty.cs
│   │   │   ├── DefeatScreen.cs
│   │   │   ├── EnemyAI.cs
│   │   │   ├── EnemyUI.cs
│   │   │   ├── GameManager.cs
│   │   │   ├── PartyMemberUI.cs
│   │   │   ├── PetAI.cs
│   │   │   ├── ScriptedBattleContext.cs
│   │   │   ├── SelectionManager.cs
│   │   │   ├── SkillButtonUI.cs
│   │   │   ├── TargetSelector.cs
│   │   │   ├── VictoryScreen.cs
│   │   │   └── VictorySlotUI.cs
│   │   │
│   │   ├── Character/        # Character-related scripts
│   │   │   ├── CharacterAppearanceData.cs
│   │   │   ├── CharacterData.cs
│   │   │   ├── CharacterStats.cs
│   │   │   └── PlayerAnimation.cs
│   │   │
│   │   ├── Core/             # Core managers
│   │   │   ├── CanvasResetter.cs
│   │   │   ├── DialogueManager.cs
│   │   │   ├── GameInitializer.cs
│   │   │   ├── GameStateManager.cs
│   │   │   ├── LocalizationManager.cs
│   │   │   ├── SceneEventSystemDestroyer.cs
│   │   │   └── SingletonEventSystem.cs
│   │   │
│   │   ├── Dialogue/        # Dialogue
│   │   │   ├── DialogueActions.cs
│   │   │   ├── DialogueNode.cs
│   │   │   └── DialogueUIInitializer.cs
│   │   │
│   │   ├── Editor/        # Import Editor
│   │   │   └── GameDataImporter.cs
│   │   │
│   │   ├── Inventory/        # Inventory
│   │   │   ├── InventoryManager.cs
│   │   │   └── InventorySlot.cs
│   │   │
│   │   ├── Items/             # Items
│   │   │   └── Item.cs
│   │   │
│   │   ├── NPC_System/             # Quest managers
│   │   │   ├── Data/
│   │   │   │   └── SocialExchangeProfile.cs
│   │   │   ├── ChatBubbleUI.cs
│   │   │   ├── NPCBarkProfile.cs
│   │   │   ├── NPCMovement.cs
│   │   │   └── PatrolPath.cs
│   │   │
│   │   ├── Quests/             # Quest managers
│   │   │   ├── Quest.cs
│   │   │   ├── QuestData.cs
│   │   │   ├── QuestLocationDatabase.cs
│   │   │   ├── QuestManager.cs
│   │   │   ├── QuestNavigator.cs
│   │   │   └── QuestObjective.cs
│   │   │
│   │   ├── Rebirth/           # Rebirth system
│   │   │   ├── RebirthManager.cs
│   │   │   └── TutorialRebirthTrigger.cs
│   │   │
│   │   ├── SaveLoad/           # Save Load system
│   │   │   ├── GameSaveData.cs
│   │   │   └── SaveSystem.cs
│   │   │
│   │   ├── Skills/           # Skills system
│   │   │   ├── Skill.cs
│   │   │   └── SkillManager.cs
│   │   │
│   │   ├── UI/               # UI components
│   │   │   ├── ButtonHoverSound.cs
│   │   │   ├── CharacterCreationManager.cs
│   │   │   ├── CharacterSelectionPanel.cs
│   │   │   ├── CharacterStatsUI.cs
│   │   │   ├── ChoiceButtonUI.cs
│   │   │   ├── DamagePopup.cs
│   │   │   ├── EquipSlotUI.cs
│   │   │   ├── InventoryUI.cs
│   │   │   ├── ItemSlotUI.cs
│   │   │   ├── MainMenu.cs
│   │   │   ├── MenuIntroController.cs
│   │   │   ├── PartyManagementUI.cs
│   │   │   ├── PartySlotButton.cs
│   │   │   ├── PartyStatusUI.cs
│   │   │   ├── PartyUIBuilderSafe.cs
│   │   │   ├── PetManagementUI.cs
│   │   │   ├── PetSlotUI.cs
│   │   │   ├── QuestLogSlot.cs
│   │   │   ├── QuestLogUI.cs
│   │   │   ├── QuestObjectiveUI.cs
│   │   │   ├── SaveLoadManager.cs
│   │   │   ├── SaveSlotUI.cs
│   │   │   ├── UISetupHelper.cs
│   │   │   └── WorldUIManager.cs
│   │   │
│   │   └── World/            # World & town scripts
│   │       ├── CameraController.cs
│   │       ├── CameraFollow.cs
│   │       ├── CraftingRecipe.cs
│   │       ├── EncounterManager.cs
│   │       ├── EncounterZone.cs
│   │       ├── GameTimeManager.cs
│   │       ├── InnManager.cs
│   │       ├── LootSystem.cs
│   │       ├── MapBossController.cs
│   │       ├── MapLocation.cs
│   │       ├── NPC.cs
│   │       ├── PlayerController.cs
│   │       ├── ShopManager.cs
│   │       ├── TownEntrance.cs
│   │       ├── TownExit.cs
│   │       ├── TownManager.cs
│   │       ├── WorldMapManager.cs
│   │       ├── WorldMapPlayer.cs
│   │       └── WorldMapZone.cs
│   │
│   ├── Prefabs/
│   │   ├── Player.prefab
│   │   ├── Battle/       # Battle prefabs
│   │   │   ├── Character_Base_Battle.prefab
│   │   │   └── Enemy_Base_Battle.prefab
│   │   └── UI/              # UI prefabs
│   │       ├── BattleItemSlot.prefab
│   │       ├── BattleItemSlot 1.prefab
│   │       ├── BattleStation_Prefab.prefab
│   │       ├── CharacterSlot.prefab
│   │       ├── ChoiceButton_Prefab.prefab
│   │       ├── Dialog_Panel_NPC.prefab
│   │       ├── Dialog_Panel_Player.prefab
│   │       ├── dmagepopup.prefab
│   │       ├── DropSlotUI.prefab
│   │       ├── EquipSlotUI.prefab
│   │       ├── ItemButton.prefab
│   │       ├── ItemSlot.prefab
│   │       ├── Location_Prefab.prefab
│   │       ├── Panel_SaveLoad.prefab
│   │       ├── PartyMemberIcon.prefab
│   │       ├── PartySlotButton.prefab
│   │       ├── PetSlot.prefab
│   │       ├── QuestListSlot_Prefab.prefab
│   │       ├── QuestObjectiveUI_Prefab.prefab
│   │       ├── saveslot.prefab
│   │       ├── SkillButton_Prefab.prefab
│   │       └── VictorySlot.prefab
│   │
│   ├── Sprites/
│   │   ├── Characters/      # Character sprites
│   │   ├── UI/             # UI sprites
│   │   ├── Enemies/          # Enemies sprites
│   │   └── Tiles/    # Tiles images
│   │
│   ├── Scenes/
│   │   ├── WorldScene.unity
│   │   ├── CharacterCreation.unity
│   │   ├── Battle.unity
│   │   ├── MainMenu.unity
│   │   └── TownScene.unity
│   │
│   └── Resources/
│       ├── Animation
│       │    ├── Attack_NE.anim
│       │    ├── Run E.anim
│       │    ├── Run N.anim
│       │    ├── Run NE.anim
│       │    ├── Run NW.anim
│       │    ├── Run S.anim
│       │    ├── Run SE.anim
│       │    ├── Run SW.anim
│       │    ├── Run W.anim
│       │    ├── Static E.anim
│       │    ├── Static NE.anim
│       │    ├── Static NW.anim
│       │    ├── Static S.anim
│       │    ├── Static SE.anim
│       │    ├── Static SW.anim
│       │    └── Static W.anim
│       ├── Data/
│       │   ├── Characters
│       │   │    ├── Boss_rebirthmain.asset
│       │   │    ├── Mage.asset
│       │   │    ├── main_player.asset
│       │   │    ├── Pet_Wolf.asset
│       │   │    ├── rebirth_main_player.asset
│       │   │    ├── villager_001.asset
│       │   │    ├── Warrior.asset
│       │   │    └── Zombie.asset
│       │   ├── Dialogue/   
│       │   │    ├── Dg_BossRebirth.jasset
│       │   │    ├── Dg_Villager_Q.jasset
│       │   │    └── ShopKeeper.asset
│       │   ├── Library/   
│       │   │    └── Armor_Library.spriteLib
│       │   ├── Localization/    # JSON localization files
│       │   │    ├── English.json
│       │   │    └── Vietnamese.
│       │   ├── Main Player/   
│       │   │    └── Main Player.asset
│       │   └── Quest/   
│       │        ├── Game_QuestData.asset
│       │        └── Q_001_Kill_Goblins.asset
│       ├── Items
│       │    ├── Egg_Wolf.asset
│       │    ├── gaybongchay.asset
│       │    ├── Giap_CanhSat.asset
│       │    ├── HP_thithop.asset
│       │    ├── HP_tuicuuthuong.asset
│       │    ├── IT_Book_Fireball.asset
│       │    ├── MP_Nuocsuoi.asset
│       │    ├── Mu_CanhSat.asset
│       │    └── sung_pistol.asset
│       └── Skills
│            └── SK_Fireball.asset
└── PrefabsParty
    └── UI
        ├── PartyMemberSlot.prefab
        └── WorldPartyMemberSlot.prefab
```

## PHẦN C: SCRIPTS CHI TIẾT

### C1. Battle Scripts

#### BattleAction.cs
```csharp
using UnityEngine;
using RebirthWarrior.Skills; // <-- THÊM DÒNG NÀY

namespace RebirthWarrior.Battle
{
    public enum BattleActionType
    {
        Attack,
        Skill,
        Defend,
        Item,
        Escape
    }

    /// <summary>
    /// Data class cho một action trong battle
    /// Version 2.0 - Hỗ trợ Skill Data
    /// </summary>
    [System.Serializable]
    public class BattleAction
    {
        public BattleUnit actor;
        public BattleUnit target;
        public BattleActionType actionType;

        // THAY ĐỔI: Chuyển 'object' thành 'Skill'
        public Skill skillData; // <-- THAY ĐỔI TỪ 'object'
        public object itemData; // (Giữ nguyên)

        /// <summary>
        /// Constructor cho attack action
        /// </summary>
        public static BattleAction CreateAttack(BattleUnit actor, BattleUnit target)
        {
            return new BattleAction
            {
                actor = actor,
                target = target,
                actionType = BattleActionType.Attack
            };
        }

        /// <summary>
        /// Constructor cho skill action
        /// </summary>
        // THAY ĐỔI: Chuyển 'object' thành 'Skill'
        public static BattleAction CreateSkill(BattleUnit actor, BattleUnit target, Skill skillData)
        {
            return new BattleAction
            {
                actor = actor,
                target = target,
                actionType = BattleActionType.Skill,
                skillData = skillData // <-- THAY ĐỔI TỪ 'object'
            };
        }

        /// <summary>
        /// Constructor cho defend action
        /// </summary>
        public static BattleAction CreateDefend(BattleUnit actor)
        {
            return new BattleAction
            {
                actor = actor,
                target = actor, // Defend self
                actionType = BattleActionType.Defend
            };
        }

        // ... (Các hàm CreateItem, CreateEscape, IsValid, ToString không đổi) ...

        public static BattleAction CreateItem(BattleUnit actor, BattleUnit target, object itemData)
        {
            return new BattleAction
            {
                actor = actor,
                target = target,
                actionType = BattleActionType.Item,
                itemData = itemData
            };
        }

        public static BattleAction CreateEscape(BattleUnit actor)
        {
            return new BattleAction
            {
                actor = actor,
                actionType = BattleActionType.Escape
            };
        }

        public bool IsValid()
        {
            if (actor == null || !actor.IsAlive())
            {
                Debug.LogWarning("[BattleAction] Actor is null or dead!");
                return false;
            }

            // Attack, Skill, Item cần mục tiêu (trừ khi skill/item là AOE)
            if (actionType == BattleActionType.Attack ||
                actionType == BattleActionType.Skill ||
                actionType == BattleActionType.Item)
            {
                // TODO: Xử lý AOE (không cần target)
                if (target == null || !target.IsAlive())
                {
                    Debug.LogWarning("[BattleAction] Target is null or dead!");
                    return false;
                }
            }

            return true;
        }

        public override string ToString()
        {
            return $"[BattleAction] {actor?.stats.characterName} -> {actionType} -> {target?.stats.characterName}";
        }
    }
}
```

#### BattleItemButtonUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Items;

namespace RebirthWarrior.Battle
{
    public class BattleItemButtonUI : MonoBehaviour
    {
        [SerializeField] private Button button;
        [SerializeField] private Image icon;
        [SerializeField] private TextMeshProUGUI nameText;
        [SerializeField] private TextMeshProUGUI quantityText;

        private Item assignedItem;
        private BattleUI battleUI;

        public void Initialize(Item item, int quantity, BattleUI ui)
        {
            assignedItem = item;
            battleUI = ui;

            if (icon != null)
            {
                icon.sprite = item.icon;
                icon.enabled = item.icon != null;
            }

            if (nameText != null) nameText.text = item.itemName;
            if (quantityText != null) quantityText.text = $"x{quantity}";

            button.onClick.RemoveAllListeners();
            button.onClick.AddListener(OnClicked);
        }

        private void OnClicked()
        {
            if (battleUI != null && assignedItem != null)
            {
                battleUI.OnItemSelected(assignedItem);
            }
        }
    }
}
```

#### BattleLoader.cs
```csharp
using UnityEngine;
using RebirthWarrior.Character;
using RebirthWarrior.Battle;
using RebirthWarrior.Core;
using RebirthWarrior.Dialogue;
using System.Collections;
using System.Collections.Generic;

public class BattleLoader : MonoBehaviour
{
    [SerializeField] private BattleUI battleUI;

    IEnumerator Start()
    {
        Time.timeScale = 1f;

        // Tìm BattleUI để đảm bảo có reference (nếu cần dùng cho việc khác)
        if (battleUI == null) battleUI = FindObjectOfType<BattleUI>();

        var gameState = GameStateManager.Instance;

        List<CharacterStats> playerParty = gameState.GetBattleParty();
        List<CharacterStats> enemyParty = gameState.nextEnemies;

        // 1. Khởi tạo Battle: Spawn Visual 3D/2D, Setup HUD máu, v.v.
        // Hàm này trong BattleManager giờ đã tự lo việc hiển thị nhân vật.
        BattleManager.Instance.InitializeBattle(playerParty, enemyParty);

        // [ĐÃ SỬA] XÓA DÒNG NÀY ĐI VÌ BATTLE UI KHÔNG CÒN QUẢN LÝ VISUAL NỮA
        // if (battleUI != null) { battleUI.InitializePartyUI(playerParty); battleUI.InitializeEnemyUI(enemyParty); }

        gameState.nextEnemies = null;

        // === XỬ LÝ HỘI THOẠI MỞ ĐẦU (NẾU CÓ) ===
        DialogueData data = gameState.battleStartingData;
        if (data != null && DialogueManager.Instance != null)
        {
            Debug.Log("[BattleLoader] Playing Intro Dialogue...");
            DialogueManager.Instance.StartDialogue(data, "Default");

            // Chờ hội thoại kết thúc
            yield return null;
            while (DialogueManager.Instance.IsDialogueActive()) yield return null;
        }
        gameState.ClearBattleDialogue();

        // Lưu ý: Trong code BattleManager trước đó, hàm InitializeBattle đã gọi StartNextTurn() ở cuối.
        // Nếu bạn thấy trận đấu bắt đầu ngay cả khi đang hội thoại, hãy vào BattleManager xóa dòng StartNextTurn() ở cuối hàm InitializeBattle,
        // rồi uncomment dòng dưới đây để BattleLoader tự kích hoạt khi xong việc.

        // BattleManager.Instance.StartNextTurn(); 
    }
}
```

#### BattleManager.cs
```csharp
using System.Collections;
using System.Collections.Generic;
using System.Linq;
using UnityEngine;
using RebirthWarrior.Character;
using RebirthWarrior.Skills;
using RebirthWarrior.Core;
using RebirthWarrior.Items;
using RebirthWarrior.Inventory;
using RebirthWarrior.Quests;
using RebirthWarrior.WorldMap;
using UnityEngine.SceneManagement;

namespace RebirthWarrior.Battle
{
    public class BattleManager : MonoBehaviour
    {
        public static BattleManager Instance { get; private set; }

        [Header("Enemy AI")]
        private EnemyAI enemyAI = new EnemyAI();

        [Header("Containers")]
        [SerializeField] public Transform playerPartyContainer;
        [SerializeField] public Transform enemyPartyContainer;

        [Header("--- STATION CONFIGURATION ---")]
        [SerializeField] private List<BattleStation> playerStations;
        [SerializeField] private List<BattleStation> enemyStations;

        [Header("Battle State")]
        private BattleState currentState;
        private List<BattleUnit> allUnits = new List<BattleUnit>();
        private Queue<BattleUnit> turnQueue = new Queue<BattleUnit>();
        private BattleUnit currentTurnUnit;

        [Header("Battle End UI")]
        [SerializeField] private VictoryScreen victoryScreen;
        [SerializeField] private DefeatScreen defeatScreen;

        // Events
        public System.Action<BattleState> OnBattleStateChanged;
        public System.Action<BattleUnit> OnUnitTurnStart;
        public System.Action<BattleUnit, BattleUnit, int, bool> OnDamageDealt;
        public System.Action<BattleUnit, BattleUnit, int> OnHealDealt;
        public System.Action<BattleResult> OnBattleEnd;
        public System.Action<List<BattleUnit>> OnBattleUnitsCreated;

        private Dictionary<CharacterStats, BattleVisualController> visualMap = new Dictionary<CharacterStats, BattleVisualController>();
        private List<DroppedItemInfo> currentBattleDrops = new List<DroppedItemInfo>();

        private void Awake()
        {
            if (Instance == null) { Instance = this; }
            else { Destroy(gameObject); }
        }

        public void InitializeBattle(List<CharacterStats> playerParty, List<CharacterStats> enemies)
        {
            Time.timeScale = 1f;
            foreach (var member in playerParty)
            {
                if (member.characterData.type == CharacterType.MainPlayerCharacter && member.currentHP <= 0)
                {
                    member.currentHP = 1;
                }
            }

            allUnits.Clear();
            turnQueue.Clear();
            visualMap.Clear();
            currentBattleDrops.Clear();

            foreach (var station in playerStations) station.ClearStation();
            foreach (var station in enemyStations) station.ClearStation();

            // Lọc danh sách Humans và Pets
            var humans = playerParty.Where(c => c.characterData.type != CharacterType.Pet).ToList();
            var pets = playerParty.Where(c => c.characterData.type == CharacterType.Pet).ToList();

            List<CharacterStats> sortedParty = new List<CharacterStats>();
            sortedParty.AddRange(humans);
            sortedParty.AddRange(pets);

            SpawnTeamIntoStations(sortedParty, playerStations, UnitType.Player);
            SpawnTeamIntoStations(enemies, enemyStations, UnitType.Enemy);

            OnBattleUnitsCreated?.Invoke(allUnits);
            CalculateTurnOrder();
            ChangeState(BattleState.BattleStart);
            StartNextTurn();
        }

        private void SpawnTeamIntoStations(List<CharacterStats> members, List<BattleStation> stations, UnitType type)
        {
            for (int i = 0; i < members.Count; i++)
            {
                if (i >= stations.Count) break;
                var member = members[i];
                var station = stations[i];
                BattleUnit unit = new BattleUnit(member, type);
                allUnits.Add(unit);

                // --- KEY POINT: Kiểm tra kỹ Data và Prefab ---
                if (member.characterData != null && member.characterData.battlePrefab != null)
                {
                    GameObject visuals = Instantiate(member.characterData.battlePrefab, station.spawnPoint.position, Quaternion.identity);
                    var visualCtrl = visuals.GetComponent<BattleVisualController>();
                    if (visualCtrl != null)
                    {
                        visualCtrl.Setup(member.characterData, type == UnitType.Player);
                        visualCtrl.LinkBattleUnit(unit);
                        visualMap.Add(member, visualCtrl);
                    }
                    unit.visual = visuals;
                    station.Initialize(unit);
                }
                else
                {
                    Debug.LogError($"[BattleManager] Character {member.characterName} (Type: {type}) không có Prefab hoặc CharacterData! Visual sẽ bị null.");
                }
            }
        }

        private void CalculateTurnOrder()
        {
            var sortedUnits = allUnits
                .Where(u => u.stats.isAlive)
                .OrderByDescending(u => u.stats.speed)
                .ThenBy(u => Random.value)
                .ToList();
            turnQueue = new Queue<BattleUnit>(sortedUnits);
        }

        public void StartNextTurn()
        {
            if (CheckBattleEnd()) return;
            if (turnQueue.Count == 0) CalculateTurnOrder();
            if (turnQueue.Count == 0) return;

            currentTurnUnit = turnQueue.Dequeue();
            if (!currentTurnUnit.IsAlive()) { StartNextTurn(); return; }

            OnUnitTurnStart?.Invoke(currentTurnUnit);

            if (currentTurnUnit.unitType == UnitType.Enemy)
            {
                ChangeState(BattleState.EnemyTurn);
                StartCoroutine(EnemyTurnCoroutine());
            }
            else
            {
                if (currentTurnUnit.stats.characterData.type == CharacterType.Pet)
                {
                    ChangeState(BattleState.PlayerTurn);
                    StartCoroutine(PetTurnCoroutine());
                }
                else
                {
                    ChangeState(BattleState.PlayerTurn);
                }
            }
        }

        private IEnumerator PetTurnCoroutine()
        {
            yield return new WaitForSeconds(0.5f);
            var enemies = GetEnemies(aliveOnly: true);
            PetAI petAI = new PetAI();
            BattleAction action = petAI.DetermineAction(currentTurnUnit, enemies, GetPartyMembers());
            if (action != null) ExecuteAction(action);
            else StartNextTurn();
        }

        private IEnumerator EnemyTurnCoroutine()
        {
            yield return new WaitForSeconds(0.5f);
            var playerUnits = GetPartyMembers(aliveOnly: true);
            if (playerUnits.Count == 0) { StartNextTurn(); yield break; }

            BattleUnit target = enemyAI.SelectTarget(playerUnits) ?? playerUnits[0];
            ExecuteAction(BattleAction.CreateAttack(currentTurnUnit, target));
        }

        public void ExecuteAction(BattleAction action)
        {
            if (action == null || !action.IsValid()) { StartNextTurn(); return; }
            ChangeState(BattleState.Processing);
            StartCoroutine(ExecuteActionRoutine(action));
        }

        private IEnumerator ExecuteActionRoutine(BattleAction action)
        {
            visualMap.TryGetValue(action.actor.stats, out var actorVisual);

            switch (action.actionType)
            {
                case BattleActionType.Attack:
                    yield return StartCoroutine(PerformAttackRoutine(action.actor, action.target));
                    break;
                case BattleActionType.Skill:
                    if (actorVisual != null) actorVisual.PlaySkillAnimation();
                    PerformSkill(action.actor, action.target, action.skillData);
                    float waitTime = (actorVisual != null) ? actorVisual.GetCurrentAnimationLength() : 1f;
                    yield return new WaitForSeconds(waitTime);
                    break;
                case BattleActionType.Defend:
                    PerformDefend(action.actor);
                    yield return new WaitForSeconds(0.5f);
                    break;
                case BattleActionType.Item:
                    if (action.itemData is Item item) PerformUseItem(action.actor, action.target, item);
                    yield return new WaitForSeconds(1f);
                    break;
                case BattleActionType.Escape:
                    PerformEscape(action.actor);
                    yield break;
            }

            if (CheckBattleEnd()) yield break;
            yield return new WaitForSeconds(0.2f);
            StartNextTurn();
        }

        // --- FIX CRASH HERE: PerformAttackRoutine ---
        private IEnumerator PerformAttackRoutine(BattleUnit attacker, BattleUnit target)
        {
            visualMap.TryGetValue(attacker.stats, out var attackerVisual);
            visualMap.TryGetValue(target.stats, out var targetVisual);

            bool isRanged = false;
            float finalStopDistance = 1.5f;

            if (attacker.stats.characterData != null)
            {
                if (attacker.stats.characterData.basicAttackType == AttackType.Ranged ||
                    attacker.stats.characterData.basicAttackType == AttackType.Cast)
                {
                    isRanged = true;
                }
                finalStopDistance = attacker.stats.characterData.stopDistance;
                if (finalStopDistance <= 0.1f) finalStopDistance = (isRanged ? 8f : 1.5f);
            }

            RebirthWarrior.Items.Item weapon = attacker.stats.GetItemInSlot(RebirthWarrior.Items.EquipmentSlot.Weapon);
            if (weapon != null)
            {
                if (weapon.rangeType == RebirthWarrior.Items.AttackRangeType.Ranged) isRanged = true;
                else isRanged = false;
                if (weapon.attackDistance > 0) finalStopDistance = weapon.attackDistance;
            }

            if (attackerVisual != null)
            {
                attackerVisual.SetAttackType(isRanged);
                attackerVisual.SetStopDistance(finalStopDistance);
            }

            bool isCritical = false;
            int physicalDmg = Mathf.Max(0, attacker.stats.attack - target.stats.defense);
            int toxicDmg = Mathf.Max(0, attacker.stats.toxicAttack - target.stats.toxicResist);
            int totalDamage = physicalDmg + toxicDmg;

            if (Random.value < (attacker.stats.luck * 0.01f))
            {
                isCritical = true;
                totalDamage += (physicalDmg / 2);
            }

            // --- FIX: Kiểm tra Target Visual trước khi truy cập Transform ---
            if (attackerVisual != null && target.visual != null)
            {
                yield return StartCoroutine(attackerVisual.PerformAttackRoutine(target.visual.transform, () =>
                {
                    ApplyDamage(target, totalDamage, toxicDmg, isCritical, targetVisual);
                }));
            }
            else
            {
                // Fallback: Nếu 1 trong 2 không có visual (tàng hình), đánh luôn không cần animation chạy tới
                Debug.LogWarning($"[BattleManager] Skip animation move. AttackerVisual: {attackerVisual != null}, TargetVisual: {target.visual != null}");
                yield return new WaitForSeconds(0.5f);
                ApplyDamage(target, totalDamage, toxicDmg, isCritical, targetVisual);
            }
        }

        private void ApplyDamage(BattleUnit target, int damage, int toxicDmg, bool isCritical, BattleVisualController targetVisual)
        {
            target.stats.TakeDamage(damage);
            if (toxicDmg > 0) target.stats.AddToxic(5);

            OnDamageDealt?.Invoke(currentTurnUnit, target, damage, isCritical);
            UpdateStationUI(target);
            if (targetVisual != null)
            {
                if (target.stats.currentHP <= 0)
                {
                    targetVisual.PlayDeathAnimation();
                    if (target.unitType == UnitType.Enemy)
                    {
                        if (QuestManager.Instance)
                            QuestManager.Instance.OnEnemyKilled(target.stats.characterData.characterID);
                        DropLootForUnit(target);
                    }
                }
                else targetVisual.PlayHitAnimation();
            }
        }

        private void PerformSkill(BattleUnit user, BattleUnit target, Skill skill)
        {
            if (skill == null) return;
            skill.PayCost(user.stats);
        }

        private void PerformUseItem(BattleUnit user, BattleUnit target, Item item)
        {
            if (InventoryManager.Instance != null) InventoryManager.Instance.RemoveItem(item, 1);
            if (item.healAmount > 0)
            {
                target.stats.Heal(item.healAmount);
                OnHealDealt?.Invoke(user, target, item.healAmount);
                UpdateStationUI(target);
            }
        }

        private void PerformDefend(BattleUnit defender)
        {
            Debug.Log($"[Defend] {defender.stats.characterName}");
        }

        private void PerformEscape(BattleUnit runner)
        {
            if (GameStateManager.Instance != null && GameStateManager.Instance.isScriptedRebirthBattle)
            {
                StartCoroutine(EndTurnDelay());
                return;
            }

            float escapeChance = 0.5f;
            if (Random.value < escapeChance) EndBattle(BattleResult.Escaped);
            else StartCoroutine(EndTurnDelay());
        }

        private IEnumerator EndTurnDelay()
        {
            yield return new WaitForSeconds(1f);
            if (currentState != BattleState.BattleEnd) StartNextTurn();
        }

        private void UpdateStationUI(BattleUnit unit)
        {
            foreach (var s in playerStations) if (s.CurrentUnit == unit) s.hud.UpdateHP();
            foreach (var s in enemyStations) if (s.CurrentUnit == unit) s.hud.UpdateHP();
        }

        private void EndBattle(BattleResult result)
        {
            ChangeState(BattleState.BattleEnd);
            OnBattleEnd?.Invoke(result);

            if (result == BattleResult.Victory) OnBattleVictory();
            else if (result == BattleResult.Defeat) OnBattleDefeat();
            else if (result == BattleResult.Escaped)
            {
                WorldMapManager.ReturnToWorld();
            }
        }

        private void OnBattleVictory()
        {
            if (victoryScreen)
            {
                int totalGold = 0;
                int totalExp = 0;
                var enemies = GetEnemies(false);

                foreach (var e in enemies)
                {
                    if (e.stats.characterData != null)
                    {
                        totalGold += e.stats.characterData.killGoldReward;
                        totalExp += e.stats.characterData.killExpReward;
                    }
                }
                BattleRewards.ApplyRewardsToGameState(totalGold, totalExp);
                BattleRewardResult result = new BattleRewardResult
                {
                    goldGained = totalGold,
                    expGained = totalExp,
                    droppedItems = currentBattleDrops
                };
                var partyStats = GetPartyMembers(true).Select(u => u.stats).ToList();
                victoryScreen.ShowVictory(result, partyStats);
            }
        }

        private void OnBattleDefeat()
        {
            var gameState = GameStateManager.Instance;
            if (gameState != null && gameState.currentBattleContext != null && gameState.currentBattleContext.isScriptedDefeat)
            {
                StartCoroutine(HandleScriptedDefeatRoutine(gameState.currentBattleContext));
                return;
            }
            if (defeatScreen) defeatScreen.Show();
        }

        private IEnumerator HandleScriptedDefeatRoutine(ScriptedBattleContext context)
        {
            yield return new WaitForSeconds(2.0f);
            if (context.healPlayerAfterBattle)
            {
                var player = GameStateManager.Instance.GetMainPlayer();
                if (player != null) player.currentHP = Mathf.Max(1, player.maxHP / 2);
            }
            if (!string.IsNullOrEmpty(context.sceneToLoadOnDefeat))
            {
                if (context.sceneToLoadOnDefeat == "REBIRTH_EVENT")
                {
                    if (RebirthWarrior.Rebirth.RebirthManager.Instance)
                        RebirthWarrior.Rebirth.RebirthManager.Instance.PerformTheRebirth();
                }
                else
                {
                    UnityEngine.SceneManagement.SceneManager.LoadScene(context.sceneToLoadOnDefeat);
                }
            }
            else
            {
                WorldMapManager.ReturnToWorld();
            }
            if (GameStateManager.Instance) GameStateManager.Instance.currentBattleContext = null;
        }

        private bool CheckBattleEnd()
        {
            if (GetEnemies(true).Count == 0)
            {
                EndBattle(BattleResult.Victory);
                return true;
            }
            var aliveHumans = allUnits.Where(u =>
                u.unitType == UnitType.Player &&
                u.stats.isAlive &&
                u.stats.characterData.type != CharacterType.Pet
            ).ToList();

            if (aliveHumans.Count == 0)
            {
                EndBattle(BattleResult.Defeat);
                return true;
            }
            return false;
        }

        private void DropLootForUnit(BattleUnit unit)
        {
            if (unit.stats.characterData == null || unit.stats.characterData.potentialDrops == null) return;
            foreach (var loot in unit.stats.characterData.potentialDrops)
            {
                if (loot.isQuestItem)
                {
                    if (QuestManager.Instance == null || !QuestManager.Instance.IsQuestActive(loot.requiredQuestID)) continue;
                    if (InventoryManager.Instance != null && InventoryManager.Instance.HasItem(loot.item)) continue;
                }
                if (Random.Range(0f, 100f) <= loot.dropChance)
                {
                    int amount = Random.Range(loot.minAmount, loot.maxAmount + 1);
                    if (InventoryManager.Instance != null) InventoryManager.Instance.AddItem(loot.item, amount);
                    AddDropToDisplayList(loot.item, amount);
                }
            }
        }

        private void AddDropToDisplayList(RebirthWarrior.Items.Item item, int amount)
        {
            var existing = currentBattleDrops.Find(x => x.item == item);
            if (existing != null) existing.quantity += amount;
            else currentBattleDrops.Add(new DroppedItemInfo { item = item, quantity = amount });
        }

        public List<BattleUnit> GetEnemies(bool aliveOnly = true) => allUnits.Where(u => u.unitType == UnitType.Enemy && (!aliveOnly || u.IsAlive())).ToList();
        public List<BattleUnit> GetPartyMembers(bool aliveOnly = true) => allUnits.Where(u => u.unitType == UnitType.Player && (!aliveOnly || u.IsAlive())).ToList();
        private void ChangeState(BattleState newState) { currentState = newState; OnBattleStateChanged?.Invoke(newState); }
        public BattleState GetCurrentState() => currentState;
        public BattleUnit GetCurrentTurnUnit() => currentTurnUnit;
    }
}
```

#### BattleRewards.cs
```csharp
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.Battle
{
    // 1. Định nghĩa item rơi (Dùng chung cho cả hệ thống)
    [System.Serializable]
    public class DroppedItemInfo
    {
        public RebirthWarrior.Items.Item item;
        public int quantity;
    }

    // 2. Class chứa kết quả trận đấu (Dùng để truyền dữ liệu sang VictoryScreen)
    [System.Serializable]
    public class BattleRewardResult
    {
        public int goldGained;
        public int expGained;
        public List<DroppedItemInfo> droppedItems = new List<DroppedItemInfo>();
    }

    /// <summary>
    /// Class tiện ích để tính toán và apply phần thưởng
    /// </summary>
    public class BattleRewards
    {
        /// <summary>
        /// Cộng tiền và Exp trực tiếp vào GameState
        /// </summary>
        public static void ApplyRewardsToGameState(int gold, int exp)
        {
            var gameState = Core.GameStateManager.Instance;
            if (gameState)
            {
                gameState.AddGold(gold);
                gameState.AddExpToParty(exp);
            }
        }
    }
}
```



#### BattleStation.cs
```csharp
using UnityEngine;
using RebirthWarrior.Character; // Để dùng CharacterStats

namespace RebirthWarrior.Battle
{
    public class BattleStation : MonoBehaviour
    {
        [Header("Settings")]
        public UnitType stationType; // Hero hoặc Enemy
        public Transform spawnPoint; // Vị trí đứng thực tế (Child object)

        [Header("UI Reference")]
        // Kéo UI thanh máu/tên tương ứng trên đầu vị trí này vào đây
        public BattleUnitHUD hud;

        // Biến lưu unit đang đứng ở trạm này
        public BattleUnit CurrentUnit { get; private set; }

        private void Awake()
        {
            // Nếu chưa gán spawnPoint, lấy chính transform của object này
            if (spawnPoint == null) spawnPoint = transform;
        }

        public void Initialize(BattleUnit unit)
        {
            CurrentUnit = unit;

            // 1. Đặt vị trí visual về đúng SpawnPoint
            if (unit.visual != null)
            {
                // Truy cập vào visual.transform thay vì unit.transform
                unit.visual.transform.position = spawnPoint.position;
                unit.visual.transform.rotation = spawnPoint.rotation;
            }

            // 2. Setup UI (Thanh máu, tên)
            if (hud != null && unit.stats != null)
            {
                // Gọi hàm Setup bên HUD, truyền stats vào
                hud.Setup(unit.stats);

                // Bật HUD lên (nếu đang tắt)
                hud.gameObject.SetActive(true);
            }
        }

        // Hàm để ẩn HUD khi unit chết hoặc không có người
        public void ClearStation()
        {
            CurrentUnit = null;
            if (hud != null) hud.gameObject.SetActive(false);
        }
    }
}
```



#### BattleTypes.cs
```csharp
using UnityEngine;
using RebirthWarrior.Character; // Cần để dùng CharacterStats

namespace RebirthWarrior.Battle
{
    // Class đại diện cho một đơn vị trong trận đấu (Logic + Visual)
    [System.Serializable]
    public class BattleUnit
    {
        public CharacterStats stats;
        public UnitType unitType;
        public GameObject visual; // GameObject chứa BattleVisualController

        // Constructor
        public BattleUnit(CharacterStats stats, UnitType type)
        {
            this.stats = stats;
            this.unitType = type;
        }

        // Helper properties
        public bool isPlayerUnit { get { return unitType == UnitType.Player; } }
        public bool IsAlive() { return stats != null && stats.currentHP > 0 && stats.isAlive; }

        // Helper để lấy Visual Controller nhanh
        public BattleVisualController GetVisualController()
        {
            if (visual != null) return visual.GetComponent<BattleVisualController>();
            return null;
        }
    }

    // Các Enum dùng chung
    public enum UnitType
    {
        Player,
        Enemy
    }

    public enum BattleState
    {
        BattleStart,
        PlayerTurn,
        EnemyTurn,
        Processing, // Đang diễn ra animation/skill
        BattleEnd
    }

    public enum BattleResult
    {
        Victory,
        Defeat,
        Escaped
    }
}
```



#### BattleUI.cs
```csharp
using RebirthWarrior.Character;
using RebirthWarrior.Core;
using RebirthWarrior.Inventory;
using RebirthWarrior.Items;
using RebirthWarrior.Skills;
using RebirthWarrior.UI;
using System.Collections;
using System.Collections.Generic;
using System.Linq;
using TMPro;
using UnityEngine;
using UnityEngine.UI;

namespace RebirthWarrior.Battle
{
    public class BattleUI : MonoBehaviour
    {
        public static BattleUI Instance { get; private set; }

        [Header("Action Buttons")]
        [SerializeField] private Button attackButton;
        [SerializeField] private Button skillButton;
        [SerializeField] private Button defendButton;
        [SerializeField] private Button itemButton;
        [SerializeField] private Button escapeButton;

        [Header("Action Button Text")]
        [SerializeField] private TextMeshProUGUI attackText;
        [SerializeField] private TextMeshProUGUI skillText;
        [SerializeField] private TextMeshProUGUI defendText;
        [SerializeField] private TextMeshProUGUI itemText;
        [SerializeField] private TextMeshProUGUI escapeText;

        [Header("--- CHARACTER DETAIL PANEL (FULL INFO) ---")]
        [SerializeField] private GameObject characterDetailPanel;
        [SerializeField] private Image detailAvatar;
        [SerializeField] private TextMeshProUGUI detailNameText;
        [SerializeField] private TextMeshProUGUI detailLevelText;
        [SerializeField] private TextMeshProUGUI detailStatsText;
        [SerializeField] private Button closeDetailButton;

        [Header("Battle Log")]
        [SerializeField] private TextMeshProUGUI battleLogText;
        [SerializeField] private ScrollRect battleLogScrollRect;
        private Queue<string> battleLogQueue = new Queue<string>();
        private const int MAX_LOG_LINES = 5;

        [Header("Panels")]
        [SerializeField] private GameObject actionPanel;
        [SerializeField] private GameObject itemPanel;
        [SerializeField] private GameObject enemyTurnPanel;
        [SerializeField] private GameObject skillPanel;

        [Header("Skill Panel UI")]
        [SerializeField] private Transform skillGridContainer;
        [SerializeField] private GameObject skillButtonPrefab;
        [SerializeField] private Button skillPanelCloseButton;

        [Header("Selection")]
        [SerializeField] private SelectionManager selectionManager;

        [Header("Item Panel UI")]
        [SerializeField] private Transform itemGridContainer;
        [SerializeField] private GameObject itemButtonPrefab;
        [SerializeField] private Button itemPanelCloseButton;

        [Header("Damage Popups")]
        [SerializeField] private GameObject damagePopupPrefab;
        [SerializeField] private Transform worldCanvasParent;

        private BattleManager battleManager;

        private void Awake()
        {
            if (Instance == null) Instance = this;
            battleManager = BattleManager.Instance;
            if (attackButton) attackButton.onClick.AddListener(OnAttackButtonPressed);
            if (skillButton) skillButton.onClick.AddListener(OnSkillButtonPressed);
            if (defendButton) defendButton.onClick.AddListener(OnDefendButtonPressed);
            if (itemButton) itemButton.onClick.AddListener(OnItemButtonPressed);
            if (escapeButton) escapeButton.onClick.AddListener(OnEscapeButtonPressed);
            if (skillPanelCloseButton) skillPanelCloseButton.onClick.AddListener(CloseSkillPanel);
            if (itemPanelCloseButton) itemPanelCloseButton.onClick.AddListener(CloseItemPanel);
            if (closeDetailButton) closeDetailButton.onClick.AddListener(CloseDetailPanel);
            if (selectionManager == null) selectionManager = FindObjectOfType<SelectionManager>();
            if (selectionManager != null)
            {
                selectionManager.OnEnemySelected.AddListener(OnUnitSelected);
            }
            if (characterDetailPanel) characterDetailPanel.SetActive(false);
        }

        private void Start()
        {
            InitializeLocalization();
            if (battleManager != null)
            {
                battleManager.OnBattleStateChanged += OnBattleStateChanged;
                battleManager.OnUnitTurnStart += OnUnitTurnStart;
                battleManager.OnDamageDealt += OnDamageDealt;
            }
        }

        private void OnDestroy()
        {
            if (battleManager != null)
            {
                battleManager.OnBattleStateChanged -= OnBattleStateChanged;
                battleManager.OnUnitTurnStart -= OnUnitTurnStart;
                battleManager.OnDamageDealt -= OnDamageDealt;
            }
        }

        private void InitializeLocalization() { }

        public void ShowCharacterDetailPanel(CharacterStats stats)
        {
            if (characterDetailPanel == null || stats == null) return;
            if (detailNameText) detailNameText.text = stats.characterName;
            if (detailLevelText) detailLevelText.text = $"Lv. {stats.level}";
            if (detailAvatar && stats.characterData != null)
            {
                detailAvatar.sprite = stats.characterData.icon;
                detailAvatar.preserveAspect = true;
            }
            if (detailStatsText)
            {
                string info = "";
                info += $"❤️ HP: {stats.currentHP}/{stats.maxHP}\n";
                info += $"💧 STM: {stats.currentStamina}/{stats.maxStamina}\n";
                info += $"⚔️ Atk: {stats.attack} | 🛡️ Def: {stats.defense}\n";
                info += $"☣️ Tox: {stats.toxicAttack} | 😷 Res: {stats.toxicResist}\n";
                info += $"⚡ Spd: {stats.speed} | 🍀 Luk: {stats.luck}";
                detailStatsText.text = info;
            }
            characterDetailPanel.SetActive(true);
        }

        public void CloseDetailPanel() { if (characterDetailPanel != null) characterDetailPanel.SetActive(false); }
        private void OnUnitSelected(BattleUnit unit) { }

        private void OnBattleStateChanged(BattleState newState)
        {
            switch (newState)
            {
                case BattleState.BattleStart: AddBattleLog("⚔️ Battle Start!"); break;
                case BattleState.PlayerTurn:
                    ShowActionPanel(true);
                    if (enemyTurnPanel) enemyTurnPanel.SetActive(false);
                    if (selectionManager) selectionManager.AutoSelectFirstEnemy();
                    break;
                case BattleState.EnemyTurn:
                    ShowActionPanel(false);
                    if (enemyTurnPanel) enemyTurnPanel.SetActive(true);
                    break;
                case BattleState.BattleEnd:
                    ShowActionPanel(false);
                    if (enemyTurnPanel) enemyTurnPanel.SetActive(false);
                    break;
            }
        }

        private void OnUnitTurnStart(BattleUnit unit) { AddBattleLog($"🎯 {unit.stats.characterName}'s Turn"); }

        private void OnDamageDealt(BattleUnit attacker, BattleUnit target, int damage, bool isCritical)
        {
            string msg = $"{attacker.stats.characterName} hits {target.stats.characterName} for {damage}";
            if (isCritical) msg += " (CRIT!)";
            AddBattleLog(msg);
            if (target.visual != null)
            {
                StartCoroutine(SpawnMultiDamagePopups(target.visual.transform, damage, isCritical));
            }
        }

        private IEnumerator SpawnMultiDamagePopups(Transform targetTransform, int totalDamage, bool isCritical)
        {
            if (totalDamage < 10 || isCritical)
            {
                CreatePopup(targetTransform.position, totalDamage, isCritical);
                yield break;
            }
            int damageLeft = totalDamage;
            int split = 3;
            for (int i = 0; i < split - 1; i++)
            {
                int part = damageLeft / 2;
                if (part < 1) part = 1;
                CreatePopup(targetTransform.position, part, false);
                damageLeft -= part;
                yield return new WaitForSeconds(0.15f);
            }
            if (damageLeft > 0) CreatePopup(targetTransform.position, damageLeft, false);
        }

        private void CreatePopup(Vector3 pos, int amt, bool crit)
        {
            if (!damagePopupPrefab) return;
            var go = Instantiate(damagePopupPrefab, worldCanvasParent);
            go.transform.position = pos + Vector3.up * 1.5f;

            // --- FIX ERROR: Sử dụng PopupType.Normal thay vì Damage ---
            // Nếu vẫn báo lỗi, hãy mở file DamagePopup.cs để xem tên đúng là gì (ví dụ: Hit, Regular...)
            PopupType type = crit ? PopupType.Critical : PopupType.Normal;

            go.GetComponent<DamagePopup>()?.Setup(amt, type);
        }

        private void AddBattleLog(string msg)
        {
            battleLogQueue.Enqueue(msg);
            if (battleLogQueue.Count > MAX_LOG_LINES) battleLogQueue.Dequeue();
            if (battleLogText) battleLogText.text = string.Join("\n", battleLogQueue);
        }

        private void ShowActionPanel(bool show) { if (actionPanel) actionPanel.SetActive(show); }

        private void OnAttackButtonPressed()
        {
            if (battleManager.GetCurrentState() != BattleState.PlayerTurn) return;
            if (!selectionManager.HasSelection()) { AddBattleLog("Select a target first!"); return; }
            var target = selectionManager.GetSelectedEnemy();
            var unit = battleManager.GetCurrentTurnUnit();
            battleManager.ExecuteAction(BattleAction.CreateAttack(unit, target));
            ShowActionPanel(false);
        }

        private void OnSkillButtonPressed() { if (battleManager.GetCurrentState() == BattleState.PlayerTurn) OpenSkillPanel(); }
        private void OnDefendButtonPressed()
        {
            if (battleManager.GetCurrentState() == BattleState.PlayerTurn)
            {
                battleManager.ExecuteAction(BattleAction.CreateDefend(battleManager.GetCurrentTurnUnit()));
                ShowActionPanel(false);
            }
        }
        public void OnItemButtonPressed() { if (battleManager.GetCurrentState() == BattleState.PlayerTurn) OpenItemPanel(); }
        private void OnEscapeButtonPressed()
        {
            if (battleManager.GetCurrentState() == BattleState.PlayerTurn)
            {
                battleManager.ExecuteAction(BattleAction.CreateEscape(battleManager.GetCurrentTurnUnit()));
                ShowActionPanel(false);
            }
        }

        private void OpenSkillPanel()
        {
            if (!skillPanel) return;
            foreach (Transform t in skillGridContainer) Destroy(t.gameObject);
            var unit = battleManager.GetCurrentTurnUnit();
            if (unit != null)
            {
                foreach (var s in unit.stats.learnedSkills)
                {
                    var btnObj = Instantiate(skillButtonPrefab, skillGridContainer);
                    btnObj.GetComponent<SkillButtonUI>()?.Initialize(s, this);
                }
            }
            skillPanel.SetActive(true);
            actionPanel.SetActive(false);
        }

        private void CloseSkillPanel() { if (skillPanel) skillPanel.SetActive(false); if (actionPanel) actionPanel.SetActive(true); }
        public void OnSkillSelected(Skill s)
        {
            CloseSkillPanel();
            var t = selectionManager.GetSelectedEnemy() ?? battleManager.GetEnemies(true).FirstOrDefault();
            if (t != null)
            {
                battleManager.ExecuteAction(BattleAction.CreateSkill(battleManager.GetCurrentTurnUnit(), t, s));
                ShowActionPanel(false);
            }
        }

        private void OpenItemPanel()
        {
            if (!itemPanel) return;
            foreach (Transform t in itemGridContainer) Destroy(t.gameObject);
            if (InventoryManager.Instance)
            {
                foreach (var slot in InventoryManager.Instance.GetAllItems())
                {
                    if (slot?.item?.itemType == ItemType.Consumable && slot.item.usableInBattle)
                    {
                        var btnObj = Instantiate(itemButtonPrefab, itemGridContainer);
                        btnObj.GetComponent<BattleItemButtonUI>()?.Initialize(slot.item, slot.quantity, this);
                    }
                }
            }
            itemPanel.SetActive(true);
            actionPanel.SetActive(false);
        }
        private void CloseItemPanel() { if (itemPanel) itemPanel.SetActive(false); if (actionPanel) actionPanel.SetActive(true); }
        public void OnItemSelected(Item i)
        {
            CloseItemPanel();
            var unit = battleManager.GetCurrentTurnUnit();
            battleManager.ExecuteAction(BattleAction.CreateItem(unit, unit, i));
            ShowActionPanel(false);
        }
    }
}
```



#### BattleUnitClickable.cs
```csharp
using UnityEngine;
using RebirthWarrior.Battle;

public class BattleUnitClickable : MonoBehaviour
{
    private TargetSelector targetSelector;
    private SelectionManager selectionManager;
    private BattleVisualController visualController;

    void Start()
    {
        targetSelector = FindObjectOfType<TargetSelector>();
        selectionManager = FindObjectOfType<SelectionManager>();
        visualController = GetComponent<BattleVisualController>();
    }

    void OnMouseDown()
    {
        if (visualController == null) return;

        BattleUnit myUnit = visualController.GetBattleUnit();
        if (myUnit == null) return;

        // Debug.Log($"Click: {myUnit.stats.characterName}");

        // 1. Skill Target Mode
        if (targetSelector != null && targetSelector.IsSelecting())
        {
            targetSelector.OnTargetClicked(myUnit);
            return;
        }

        // 2. Normal Attack Selection
        if (myUnit.unitType == UnitType.Enemy && BattleManager.Instance.GetCurrentState() == BattleState.PlayerTurn)
        {
            if (selectionManager != null)
            {
                // --- SỬA LỖI: Chỉ truyền 1 tham số ---
                selectionManager.OnEnemyClicked(myUnit);
            }
        }
    }
}
```



#### BattleUnitHUD.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;

namespace RebirthWarrior.Battle
{
    public class BattleUnitHUD : MonoBehaviour
    {
        [Header("UI Components")]
        [SerializeField] private TextMeshProUGUI nameText;
        [SerializeField] private TextMeshProUGUI levelText;
        [SerializeField] private Slider hpSlider;
        [SerializeField] private Slider mpSlider; // Giờ là Stamina Slider

        [Header("Selection Visuals")]
        [Tooltip("Kéo Game Object hình khung viền/mũi tên vào đây")]
        [SerializeField] private GameObject selectionIndicator;

        private CharacterStats _targetStats;

        // Hàm Setup mà BattleStation đang gọi
        public void Setup(CharacterStats stats)
        {
            _targetStats = stats;

            if (nameText != null) nameText.text = stats.characterName;
            if (levelText != null) levelText.text = "Lv." + stats.level;

            UpdateHP();
            UpdateMP(); // Hàm này giờ sẽ update Stamina

            SetSelected(false);

            // Đổi màu thanh Stamina sang màu vàng (Optional)
            if (mpSlider != null && mpSlider.fillRect != null)
            {
                var img = mpSlider.fillRect.GetComponent<Image>();
                if (img) img.color = new Color(1f, 0.8f, 0f); // Vàng cam
            }
        }

        public void SetSelected(bool isSelected)
        {
            if (selectionIndicator != null)
            {
                selectionIndicator.SetActive(isSelected);
            }
        }

        // Cập nhật máu
        public void UpdateHP()
        {
            if (_targetStats == null || hpSlider == null) return;
            float hpPercent = (float)_targetStats.currentHP / _targetStats.maxHP;
            hpSlider.value = hpPercent;
        }

        // [FIX ERROR] Cập nhật Stamina (Thay vì MP)
        public void UpdateMP()
        {
            if (_targetStats == null || mpSlider == null) return;

            // Sửa lỗi dòng 63: Dùng maxStamina và currentStamina
            float mpPercent = (float)_targetStats.currentStamina / _targetStats.maxStamina;
            mpSlider.value = mpPercent;
        }

        public CharacterStats GetCharacterStats()
        {
            return _targetStats;
        }

        private void Update()
        {
            if (_targetStats != null)
            {
                UpdateHP();
                UpdateMP();
            }
        }
    }
}
```



#### BattleVisualController.cs
```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.Rendering;
using RebirthWarrior.Character;
using RebirthWarrior.Items;

namespace RebirthWarrior.Battle
{
    [RequireComponent(typeof(Animator))]
    [RequireComponent(typeof(SpriteRenderer))]
    public class BattleVisualController : MonoBehaviour
    {
        [Header("References")]
        [SerializeField] private Animator animator;
        [SerializeField] private SpriteRenderer spriteRenderer;
        private SortingGroup sortingGroup;

        [Header("Runtime Settings")]
        private float moveSpeedIso = 8f;
        private float stopDistance = 1.5f;
        private bool isRangedUnit = false;

        private Vector3 originalPosition;
        private bool isFacingLeft = false;

        private AudioSource audioSource;
        private CharacterData _data;
        private BattleUnit linkedBattleUnit;

        private void Awake()
        {
            if (animator == null) animator = GetComponent<Animator>();
            if (spriteRenderer == null) spriteRenderer = GetComponent<SpriteRenderer>();
            sortingGroup = GetComponent<SortingGroup>();
            audioSource = GetComponent<AudioSource>();
            if (audioSource == null) audioSource = gameObject.AddComponent<AudioSource>();
            audioSource.playOnAwake = false;
        }

        public void Setup(CharacterData data, bool isPlayerSide)
        {
            _data = data;
            this.originalPosition = transform.position;
            if (data != null)
            {
                this.moveSpeedIso = data.battleMoveSpeed > 0 ? data.battleMoveSpeed : 8f;
                this.stopDistance = 1.5f;
            }
            this.isFacingLeft = !isPlayerSide;
            spriteRenderer.flipX = isFacingLeft;
        }

        public void SetAttackType(bool isRanged) => this.isRangedUnit = isRanged;
        public void SetStopDistance(float distance) => this.stopDistance = distance;

        // --- FIX: Hàm lấy độ dài Animation chuẩn xác ---
        public float GetCurrentAnimationLength()
        {
            if (animator == null) return 1f;
            AnimatorStateInfo stateInfo = animator.GetCurrentAnimatorStateInfo(0);
            return stateInfo.length > 0 ? stateInfo.length : 1f;
        }

        public void PlaySkillAnimation()
        {
            if (animator) animator.SetTrigger("Skill");
            // Lưu ý: Animator cần có Trigger "Skill", nếu chưa có hãy thêm vào Animator Controller
        }

        // --- COROUTINE TẤN CÔNG ĐÃ FIX TIMING ---
        public IEnumerator PerformAttackRoutine(Transform targetTransform, System.Action onHitCallback)
        {
            Vector3 targetPos = targetTransform.position;
            Vector3 direction = (targetPos - transform.position).normalized;
            Vector3 attackPos = targetPos - (direction * stopDistance);

            // 1. DI CHUYỂN
            spriteRenderer.flipX = (targetPos.x < transform.position.x);
            float currentDist = Vector3.Distance(transform.position, targetPos);

            if (currentDist > stopDistance)
            {
                animator.SetBool("IsRunning", true);
                yield return StartCoroutine(MoveToPosition(attackPos));
                animator.SetBool("IsRunning", false);
            }

            // 2. TẤN CÔNG
            int oldOrder = SetSortingOrder(100);
            animator.SetTrigger("Attack");
            PlaySFX(_data != null ? _data.sfxAttack : null);

            // --- FIX TIMING ---
            // Đợi 1 frame để Animator chuyển state
            yield return null;

            float animLength = GetCurrentAnimationLength();
            // Impact point thường ở khoảng 40-50% animation
            float impactTime = animLength * 0.4f;
            float remainingTime = animLength - impactTime;

            yield return new WaitForSeconds(impactTime);

            if (_data != null && _data.hitVFXPrefab != null)
            {
                Instantiate(_data.hitVFXPrefab, targetPos, Quaternion.identity);
                PlaySFX(_data.sfxHit);
            }

            onHitCallback?.Invoke();

            yield return new WaitForSeconds(remainingTime);

            SetSortingOrder(oldOrder);

            // 3. QUAY VỀ
            if (Vector3.Distance(transform.position, originalPosition) > 0.1f)
            {
                spriteRenderer.flipX = (originalPosition.x < transform.position.x);
                animator.SetBool("IsRunning", true);
                yield return StartCoroutine(MoveToPosition(originalPosition));
                animator.SetBool("IsRunning", false);
                spriteRenderer.flipX = isFacingLeft;
            }
        }

        private IEnumerator MoveToPosition(Vector3 target)
        {
            animator.SetBool("IsRunning", true);
            while (Vector3.Distance(transform.position, target) > 0.05f)
            {
                transform.position = Vector3.MoveTowards(transform.position, target, moveSpeedIso * Time.deltaTime);
                UpdateSortingOrder();
                yield return null;
            }
            transform.position = target;
            UpdateSortingOrder();
            animator.SetBool("IsRunning", false);
        }

        private void UpdateSortingOrder()
        {
            int newOrder = Mathf.RoundToInt(transform.position.y * -100);
            if (sortingGroup) sortingGroup.sortingOrder = newOrder;
            else if (spriteRenderer) spriteRenderer.sortingOrder = newOrder;
        }

        private int SetSortingOrder(int order)
        {
            int old = 0;
            if (sortingGroup) { old = sortingGroup.sortingOrder; sortingGroup.sortingOrder = order; }
            else if (spriteRenderer) { old = spriteRenderer.sortingOrder; spriteRenderer.sortingOrder = order; }
            return old;
        }

        private void PlaySFX(AudioClip clip)
        {
            if (audioSource && clip) audioSource.PlayOneShot(clip);
        }

        public void PlayHitAnimation()
        {
            if (animator) animator.SetTrigger("Hit");
            PlaySFX(_data != null ? _data.sfxHit : null);
        }

        public void PlayDeathAnimation()
        {
            if (animator) animator.SetTrigger("Die");
            PlaySFX(_data != null ? _data.sfxDie : null);
        }

        public void LinkBattleUnit(BattleUnit unit) => this.linkedBattleUnit = unit;
        public BattleUnit GetBattleUnit() => linkedBattleUnit;
    }
}
```




#### DamageCalculator.cs
```csharp
using UnityEngine;
using RebirthWarrior.Character;
using RebirthWarrior.Skills; // Cần dòng này để dùng SurvivalSkillType

namespace RebirthWarrior.Battle
{
    /// <summary>
    /// Tính toán damage cho tất cả loại tấn công
    /// Version 3.0 - Đã chuyển đổi sang hệ thống Survival (Toxic/Medicine)
    /// </summary>
    public static class DamageCalculator
    {
        private const float CRITICAL_MULTIPLIER = 1.5f;
        private const float DEFENSE_REDUCTION_RATE = 0.5f;

        /// <summary>
        /// Tính sát thương vật lý
        /// </summary>
        public static int CalculatePhysicalDamage(CharacterStats attacker, CharacterStats defender, out bool isCritical)
        {
            float baseDamage = attacker.attack - (defender.defense * DEFENSE_REDUCTION_RATE);
            baseDamage = Mathf.Max(1, baseDamage);

            float variance = Random.Range(0.9f, 1.1f);
            baseDamage *= variance;

            isCritical = CheckCriticalHit(attacker.luck);
            if (isCritical)
            {
                baseDamage *= CRITICAL_MULTIPLIER;
                Debug.Log("🎯 CHÍ MẠNG (Physical)!");
            }

            return Mathf.RoundToInt(baseDamage);
        }

        /// <summary>
        /// Tính sát thương Độc (Thay cho Magic cũ)
        /// </summary>
        public static int CalculateToxicDamage(CharacterStats attacker, CharacterStats defender, float skillPower, out bool isCritical)
        {
            // Logic Mới: Toxic Attack vs Toxic Resist
            float baseDamage = attacker.toxicAttack - (defender.toxicResist * DEFENSE_REDUCTION_RATE);
            baseDamage = Mathf.Max(1, baseDamage);

            baseDamage *= skillPower;

            float variance = Random.Range(0.95f, 1.05f);
            baseDamage *= variance;

            isCritical = CheckCriticalHit(attacker.luck);
            if (isCritical)
            {
                baseDamage *= CRITICAL_MULTIPLIER;
                Debug.Log("🎯 CHÍ MẠNG (Toxic)!");
            }

            return Mathf.RoundToInt(baseDamage);
        }

        /// <summary>
        /// Tính lượng hồi máu (Dựa trên Skill Medicine + Base Attack)
        /// </summary>
        public static int CalculateHealing(CharacterStats healer, float healPower = 1.0f)
        {
            // Logic Mới: Hồi máu dựa trên level kỹ năng Medicine + Attack cơ bản
            // Nếu không có skill Medicine, coi như level 1
            int medicineLevel = healer.GetSkillLevel(SurvivalSkillType.Medicine);

            // Công thức: (Attack * 0.5 + MedicineLevel * 5) * Power
            float baseHeal = (healer.attack * 0.5f) + (medicineLevel * 5f);

            float healAmount = baseHeal * healPower;
            float variance = Random.Range(0.95f, 1.05f);
            healAmount *= variance;

            return Mathf.RoundToInt(healAmount);
        }

        private static bool CheckCriticalHit(int luck)
        {
            float critChance = (float)luck;
            critChance = Mathf.Min(critChance, 30f);
            return Random.Range(0f, 100f) < critChance;
        }

        public static bool CheckEvasion(CharacterStats defender)
        {
            float evasionChance = 5f + (defender.agility * 0.3f);
            evasionChance = Mathf.Min(evasionChance, 30f);
            return Random.Range(0f, 100f) < evasionChance;
        }
    }
}
```


#### DefeatPenalty.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Inventory; // Cần namespace này
using RebirthWarrior.Items;

namespace RebirthWarrior.Battle
{
    public class DefeatPenalty
    {
        private const float GOLD_LOSS_PERCENT = 0.2f; // Mất 20% vàng
        private const float EXP_LOSS_PERCENT = 0.1f;  // Mất 10% kinh nghiệm hiện có

        public static DefeatPenaltyResult ApplyPenalties()
        {
            var gameState = Core.GameStateManager.Instance;
            var inventory = InventoryManager.Instance;

            if (gameState == null) return new DefeatPenaltyResult();

            // 1. XỬ LÝ VÀNG
            int currentGold = gameState.GetGold();
            int goldLoss = Mathf.RoundToInt(currentGold * GOLD_LOSS_PERCENT);
            if (goldLoss > 0) gameState.RemoveGold(goldLoss);

            // 2. XỬ LÝ EXP (Chỉ trừ Exp hiện tại, không rớt cấp)
            int totalExpLost = 0;
            var party = gameState.GetBattleParty();
            foreach (var member in party)
            {
                if (member != null)
                {
                    int expLoss = Mathf.RoundToInt(member.currentExp * EXP_LOSS_PERCENT);
                    member.currentExp = Mathf.Max(0, member.currentExp - expLoss);
                    totalExpLost += expLoss;
                }
            }

            // 3. XỬ LÝ RỚT ITEM (MỚI)
            List<string> lostItemNames = new List<string>();
            if (inventory != null)
            {
                // Random số lượng item bị rớt (1 đến 3)
                int itemsToDrop = Random.Range(1, 4);

                // Lấy danh sách các slot có đồ
                var filledSlots = new List<int>();
                var allSlots = inventory.GetAllItems();
                for (int i = 0; i < allSlots.Length; i++)
                {
                    // Chỉ rớt đồ Consumable hoặc Material, tránh rớt KeyItem hoặc Trang bị xịn
                    if (allSlots[i] != null && allSlots[i].item != null &&
                        allSlots[i].item.itemType != ItemType.KeyItem)
                    {
                        filledSlots.Add(i);
                    }
                }

                // Random xóa
                for (int k = 0; k < itemsToDrop; k++)
                {
                    if (filledSlots.Count == 0) break;

                    int randomIndex = Random.Range(0, filledSlots.Count);
                    int slotIndex = filledSlots[randomIndex];

                    InventorySlot slot = allSlots[slotIndex];
                    if (slot != null && slot.item != null)
                    {
                        lostItemNames.Add(slot.item.itemName);
                        // Xóa 1 cái hoặc xóa cả stack? -> Ở đây xóa cả stack cho đau
                        inventory.RemoveItem(slot.item, slot.quantity);

                        filledSlots.RemoveAt(randomIndex); // Không xóa lại slot này nữa
                    }
                }
            }

            return new DefeatPenaltyResult
            {
                goldLost = goldLoss,
                expLost = totalExpLost,
                lostItems = lostItemNames
            };
        }
    }

    public class DefeatPenaltyResult
    {
        public int goldLost;
        public int expLost;
        public List<string> lostItems; // Danh sách tên item bị mất
    }
}
```



#### DefeatScreen.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using System.Collections;
using System.Text;
using UnityEngine.SceneManagement; // Thêm cái này

namespace RebirthWarrior.Battle
{
    public class DefeatScreen : MonoBehaviour
    {
        [Header("UI References")]
        [SerializeField] private GameObject defeatPanel;
        [SerializeField] private TextMeshProUGUI titleText;
        [SerializeField] private TextMeshProUGUI messageText;

        [Header("Penalty Info")]
        [SerializeField] private TextMeshProUGUI penaltyText;
        [SerializeField] private TextMeshProUGUI lostItemsText;

        [SerializeField] private Button returnButton;

        [Header("Audio")]
        [SerializeField] private AudioClip defeatMusic;

        private void Awake()
        {
            if (defeatPanel != null) defeatPanel.SetActive(false);
            if (returnButton != null) returnButton.onClick.AddListener(OnReturnClicked);
            if (penaltyText != null) penaltyText.gameObject.SetActive(false);
            if (lostItemsText != null) lostItemsText.gameObject.SetActive(false);
        }

        public void Show()
        {
            if (defeatPanel != null) defeatPanel.SetActive(true);
            StartCoroutine(ShowDefeatSequence());
        }

        public IEnumerator ShowDefeatSequence()
        {
            if (titleText != null) titleText.text = "THẤT BẠI";

            // Xử lý hình phạt (Giữ nguyên logic cũ)
            var penalty = DefeatPenalty.ApplyPenalties();

            if (penaltyText != null)
            {
                string msg = "";
                if (penalty.goldLost > 0) msg += $"<color=red>- {penalty.goldLost} Vàng</color>\n";
                if (penalty.expLost > 0) msg += $"<color=red>- {penalty.expLost} Kinh nghiệm</color>";

                if (!string.IsNullOrEmpty(msg))
                {
                    penaltyText.text = msg;
                    penaltyText.gameObject.SetActive(true);
                }
            }

            if (lostItemsText != null && penalty.lostItems != null && penalty.lostItems.Count > 0)
            {
                StringBuilder sb = new StringBuilder();
                sb.AppendLine("Vật phẩm bị rơi:");
                foreach (var itemName in penalty.lostItems)
                {
                    sb.AppendLine($"<color=grey>- {itemName}</color>");
                }
                lostItemsText.text = sb.ToString();
                lostItemsText.gameObject.SetActive(true);
            }
            else if (lostItemsText != null)
            {
                lostItemsText.text = "";
            }

            yield return new WaitForSeconds(0.5f);
            if (returnButton != null) returnButton.interactable = true;
        }

        private void OnReturnClicked()
        {
            if (defeatPanel != null) defeatPanel.SetActive(false);

            // === [FIX LOGIC TRẢ VỀ MAP CŨ] ===
            // Nếu thua thì có thể về làng (TownScene) hoặc về map cũ tùy game design.
            // Ở đây tôi để về map cũ nhưng ở vị trí an toàn (hoặc vị trí cũ)
            string sceneToLoad = PlayerPrefs.GetString("ReturnScene", "WorldScene");

            // (Optional) Nếu muốn thua thì về TownScene luôn:
            // sceneToLoad = "TownScene"; 

            Debug.Log($"[Defeat] Đang quay về: {sceneToLoad}");
            SceneManager.LoadScene(sceneToLoad);
        }
    }
}
```



#### EnemyAI.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using System.Linq;

namespace RebirthWarrior.Battle
{
    public class EnemyAI
    {
        public BattleUnit SelectTarget(List<BattleUnit> availableTargets)
        {
            // Debug thô
            if (availableTargets == null)
            {
                Debug.LogError("[EnemyAI] List targets is NULL");
                return null;
            }

            Debug.Log($"[EnemyAI] Số mục tiêu tiềm năng: {availableTargets.Count}");

            // Lọc người sống
            var aliveTargets = new List<BattleUnit>();
            foreach (var t in availableTargets)
            {
                if (t != null && t.IsAlive()) aliveTargets.Add(t);
            }

            if (aliveTargets.Count == 0)
            {
                Debug.LogWarning("[EnemyAI] Không có mục tiêu nào còn sống!");
                return null;
            }

            // Chọn người đầu tiên (Đơn giản nhất để test)
            return aliveTargets[0];
        }
    }
}
```



#### EnemyUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;

namespace RebirthWarrior.Battle
{
    public class EnemyUI : MonoBehaviour
    {
        [Header("Components")]
        [SerializeField] private Image avatarImage;
        [SerializeField] private TextMeshProUGUI nameText;
        [SerializeField] private Slider hpSlider;
        [SerializeField] private Image turnHighlightBorder; // Viền báo lượt (Vàng)
        [SerializeField] private Image selectionBorder;     // Viền báo chọn (Đỏ) - Kéo thêm 1 image vào đây hoặc dùng chung

        private CharacterStats _stats;

        public void Initialize(CharacterStats stats)
        {
            _stats = stats;
            UpdateUI();

            // Tắt hết các hiệu ứng ban đầu
            if (turnHighlightBorder) turnHighlightBorder.enabled = false;
            if (selectionBorder) selectionBorder.enabled = false;
        }

        public CharacterStats GetCharacterStats() => _stats;

        public void UpdateUI()
        {
            if (_stats == null) return;

            if (nameText) nameText.text = _stats.characterName;

            if (avatarImage && _stats.characterData != null)
            {
                avatarImage.sprite = _stats.characterData.icon;
                avatarImage.preserveAspect = true;
            }

            if (hpSlider)
            {
                hpSlider.maxValue = _stats.maxHP;
                hpSlider.value = _stats.currentHP;
            }
        }

        // --- CÁC HÀM FIX LỖI SELECTION MANAGER ---

        /// <summary>
        /// Được gọi bởi BattleUI để báo hiệu đến lượt quái này
        /// </summary>
        public void SetTurnHighlight(bool isActive)
        {
            if (turnHighlightBorder)
            {
                turnHighlightBorder.enabled = isActive;
                turnHighlightBorder.color = Color.yellow; // Màu vàng cho lượt
            }

            // Scale nhẹ lên khi đến lượt
            if (isActive) transform.localScale = Vector3.one * 1.1f;
            else transform.localScale = Vector3.one;
        }

        /// <summary>
        /// Được gọi bởi SelectionManager khi người chơi click chọn quái này làm mục tiêu
        /// </summary>
        public void SetSelected(bool isSelected)
        {
            if (selectionBorder)
            {
                selectionBorder.enabled = isSelected;
                selectionBorder.color = Color.red; // Màu đỏ khi bị khóa mục tiêu
            }
            else if (turnHighlightBorder)
            {
                // Fallback: Nếu không có viền riêng thì dùng chung viền lượt nhưng đổi màu
                turnHighlightBorder.enabled = isSelected;
                if (isSelected) turnHighlightBorder.color = Color.red;
            }
        }

        /// <summary>
        /// Được gọi bởi TargetSelector khi rê chuột hoặc chọn skill AOE
        /// </summary>
        public void SetHighlight(bool isHighlighted)
        {
            // Hiệu ứng nhẹ hơn, ví dụ làm sáng avatar hoặc hiện viền trắng
            if (selectionBorder)
            {
                selectionBorder.enabled = isHighlighted;
                selectionBorder.color = Color.white;
            }
            else if (turnHighlightBorder)
            {
                turnHighlightBorder.enabled = isHighlighted;
                if (isHighlighted) turnHighlightBorder.color = Color.white;
            }
        }

        public void ShowDamage(int damage)
        {
            StartCoroutine(FlashRed());
        }

        private System.Collections.IEnumerator FlashRed()
        {
            if (avatarImage) avatarImage.color = Color.red;
            yield return new WaitForSeconds(0.1f);
            if (avatarImage) avatarImage.color = Color.white;
        }
    }
}
```



#### GameManager.cs
```csharp
using UnityEngine;
using UnityEngine.SceneManagement;
using RebirthWarrior.Character;
using RebirthWarrior.World;

namespace RebirthWarrior.Core
{
    public class GameManager : MonoBehaviour
    {
        public static GameManager Instance { get; private set; }

        [Header("System Config")]
        [Tooltip("Kéo file Prefab Player vào đây")]
        [SerializeField] private GameObject playerPrefab;

        private void Awake()
        {
            if (Instance == null) Instance = this;
        }

        private void OnEnable() => SceneManager.sceneLoaded += OnSceneLoaded;
        private void OnDisable() => SceneManager.sceneLoaded -= OnSceneLoaded;

        private void OnSceneLoaded(Scene scene, LoadSceneMode mode)
        {
            if (scene.name == "MainMenu" || scene.name == "Battle" ||
                scene.name == "CharacterCreation" || scene.name == "LoadingScene")
                return;

            GameObject pObj = GameObject.FindGameObjectWithTag("Player");
            if (pObj == null)
            {
                SpawnPlayer();
            }
            else
            {
                NotifyManager(pObj);
            }
        }

        private void SpawnPlayer()
        {
            // Kiểm tra nếu đang ở WorldMap thì KHÔNG spawn Player WASD
            // (Vì WorldMap dùng Token riêng do WorldMapManager quản lý)
            if (FindObjectOfType<RebirthWarrior.WorldMap.WorldMapManager>() != null)
            {
                return;
            }

            if (playerPrefab == null) playerPrefab = Resources.Load<GameObject>("Prefabs/Player");

            if (playerPrefab != null)
            {
                Debug.Log($"[GameManager] ✨ Auto-Spawn Player tại: {SceneManager.GetActiveScene().name}");
                GameObject p = Instantiate(playerPrefab, Vector3.zero, Quaternion.identity);
                p.name = "Player";
                p.tag = "Player";
                NotifyManager(p);
            }
            else
            {
                Debug.LogError("⛔ LỖI: Thiếu Player Prefab trong GameManager!");
            }
        }

        private void NotifyManager(GameObject playerObj)
        {
            var ctrl = playerObj.GetComponent<PlayerController>();
            if (ctrl == null) return;

            // FIX: Xóa khối lệnh gọi WorldManager cũ vì đã thay thế bằng WorldMapManager.
            // Nếu là Map Town/Isometric thì dùng TownManager
            if (TownManager.Instance != null)
            {
                TownManager.Instance.OnPlayerReady(ctrl);
                return;
            }

            // Nếu Scene này không có TownManager (và không phải WorldMap), chỉ cảnh báo nhẹ
            // Debug.LogWarning("Scene này có Player nhưng không có Manager để set vị trí.");
        }
    }
}
```



#### PartyMemberUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;

namespace RebirthWarrior.Battle
{
    public class PartyMemberUI : MonoBehaviour
    {
        [Header("Components")]
        [SerializeField] private Image avatarImage;
        [SerializeField] private TextMeshProUGUI nameText;
        [SerializeField] private Slider hpSlider;
        [SerializeField] private Slider mpSlider; // Bây giờ là Stamina Slider
        [SerializeField] private Image turnHighlightBorder;

        [Header("Animation")]
        [SerializeField] private Animator uiAnimator;

        private CharacterStats _stats;

        public void Initialize(CharacterStats stats)
        {
            _stats = stats;
            UpdateUI();
            if (turnHighlightBorder) turnHighlightBorder.enabled = false;

            // Đổi màu thanh MP cũ (thường màu xanh) sang màu Vàng cho Stamina
            if (mpSlider != null)
            {
                Image fill = mpSlider.fillRect.GetComponent<Image>();
                if (fill != null) fill.color = new Color(1f, 0.8f, 0f); // Màu vàng
            }
        }

        public CharacterStats GetCharacterStats() => _stats;

        public void UpdateUI()
        {
            if (_stats == null) return;

            if (nameText) nameText.text = _stats.characterName;

            if (avatarImage && _stats.characterData != null)
            {
                avatarImage.sprite = _stats.characterData.icon;
                avatarImage.preserveAspect = true;
            }

            if (hpSlider)
            {
                hpSlider.maxValue = _stats.maxHP;
                hpSlider.value = _stats.currentHP;
            }

            // === [FIX LỖI TẠI ĐÂY] ===
            if (mpSlider)
            {
                // Dùng maxStamina và currentStamina thay vì MP
                mpSlider.maxValue = _stats.maxStamina;
                mpSlider.value = _stats.currentStamina;
            }
        }

        public void SetTurnHighlight(bool isActive)
        {
            if (turnHighlightBorder)
            {
                turnHighlightBorder.enabled = isActive;
                turnHighlightBorder.color = Color.yellow;
            }
            if (isActive) transform.localScale = Vector3.one * 1.1f;
            else transform.localScale = Vector3.one;
        }

        public void SetHighlight(bool isHighlighted)
        {
            if (turnHighlightBorder)
            {
                turnHighlightBorder.enabled = isHighlighted;
                if (isHighlighted) turnHighlightBorder.color = Color.green;
            }
        }

        public void SetSelected(bool isSelected)
        {
            if (turnHighlightBorder)
            {
                turnHighlightBorder.enabled = isSelected;
                if (isSelected) turnHighlightBorder.color = Color.green;
            }
        }

        public void PlayDamageAnimation()
        {
            if (uiAnimator) uiAnimator.SetTrigger("Shake");
            else StartCoroutine(ShakeRoutine());
        }

        private System.Collections.IEnumerator ShakeRoutine()
        {
            Vector3 originalPos = transform.localPosition;
            for (int i = 0; i < 5; i++)
            {
                transform.localPosition = originalPos + Random.insideUnitSphere * 5f;
                yield return new WaitForSeconds(0.05f);
            }
            transform.localPosition = originalPos;
        }
    }
}
```



#### PetAI.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using System.Linq;
using RebirthWarrior.Character;

namespace RebirthWarrior.Battle
{
    public class PetAI
    {
        /// <summary>
        /// Pet tự quyết định hành động
        /// </summary>
        public BattleAction DetermineAction(BattleUnit petUnit, List<BattleUnit> enemies, List<BattleUnit> allies)
        {
            // 1. Tìm mục tiêu (Mặc định đánh kẻ thù yếu máu nhất)
            var aliveEnemies = enemies.Where(e => e.IsAlive()).OrderBy(e => e.stats.currentHP).ToList();

            if (aliveEnemies.Count == 0) return null; // Không còn địch

            BattleUnit target = aliveEnemies[0];

            // 2. Kiểm tra Skill (Nếu Pet có Skill và đủ MP)
            // TODO: Mở rộng logic này để Pet dùng skill buff/heal
            foreach (var skill in petUnit.stats.learnedSkills)
            {
                if (skill.CanUse(petUnit.stats) && skill.targetType == RebirthWarrior.Skills.TargetType.SingleEnemy)
                {
                    Debug.Log($"[PetAI] {petUnit.stats.characterName} dùng skill: {skill.skillNameKey}");
                    return BattleAction.CreateSkill(petUnit, target, skill);
                }
            }

            // 3. Đánh thường (Mặc định)
            Debug.Log($"[PetAI] {petUnit.stats.characterName} tấn công thường.");
            return BattleAction.CreateAttack(petUnit, target);
        }
    }
}
```



#### ScriptedBattleContext.cs
```csharp
using UnityEngine;
using System;

namespace RebirthWarrior.Battle
{
    [Serializable]
    public class ScriptedBattleContext
    {
        [Header("Scripted Defeat Settings")]
        public bool isScriptedDefeat = false; // Nếu True: Thua không bị phạt
        public string sceneToLoadOnDefeat;    // Tên Scene chuyển tới sau khi thua
        public string spawnPointIDOnDefeat;   // Vị trí spawn ở scene mới (nếu có)

        [Header("After Battle (Win/Lose)")]
        public bool healPlayerAfterBattle = true; // Hồi máu sau khi xong cutscene
    }
}
```



#### SelectionManager.cs
```csharp
using UnityEngine;
using UnityEngine.Events;
using System.Collections.Generic;

namespace RebirthWarrior.Battle
{
    public class SelectionManager : MonoBehaviour
    {
        [Header("Events")]
        public UnityEvent<BattleUnit> OnEnemySelected;
        public UnityEvent OnSelectionCleared;

        [Header("Current Selection")]
        private BattleUnit currentSelectedEnemy;
        private BattleUnitHUD currentSelectedHUD;

        private BattleManager battleManager;

        private void Awake()
        {
            battleManager = BattleManager.Instance;
        }

        // --- SỬA LỖI TẠI ĐÂY: Chỉ nhận BattleUnit, tự đi tìm HUD ---
        public void OnEnemyClicked(BattleUnit enemy)
        {
            // Tự tìm HUD tương ứng với Unit này
            BattleUnitHUD hud = FindHUDForUnit(enemy);
            SelectEnemy(enemy, hud);
        }

        private void SelectEnemy(BattleUnit enemy, BattleUnitHUD hud)
        {
            // 1. Tắt highlight cái cũ
            if (currentSelectedHUD != null)
            {
                currentSelectedHUD.SetSelected(false);
            }

            // 2. Gán cái mới
            currentSelectedEnemy = enemy;
            currentSelectedHUD = hud;

            // 3. Bật highlight cái mới
            if (currentSelectedHUD != null)
            {
                currentSelectedHUD.SetSelected(true);
            }
            else
            {
                Debug.LogWarning($"Không tìm thấy HUD cho {enemy.stats.characterName} để hiện khung chọn!");
            }

            OnEnemySelected?.Invoke(enemy);
            Debug.Log($"[SelectionManager] Selected: {enemy.stats.characterName}");
        }

        // Hàm Helper tìm HUD trong scene
        private BattleUnitHUD FindHUDForUnit(BattleUnit unit)
        {
            var allHUDs = FindObjectsOfType<BattleUnitHUD>();
            foreach (var hud in allHUDs)
            {
                // Giả sử BattleUnitHUD có hàm lấy stats (đã thêm ở bước trước)
                if (hud.GetCharacterStats() == unit.stats)
                {
                    return hud;
                }
            }
            return null;
        }

        public void DeselectEnemy()
        {
            if (currentSelectedHUD != null) currentSelectedHUD.SetSelected(false);
            currentSelectedEnemy = null;
            currentSelectedHUD = null;
            OnSelectionCleared?.Invoke();
        }

        public BattleUnit GetSelectedEnemy() => currentSelectedEnemy;

        public bool HasSelection() => currentSelectedEnemy != null && currentSelectedEnemy.IsAlive();

        public void OnEnemyDeath(BattleUnit enemy)
        {
            if (currentSelectedEnemy == enemy)
            {
                AutoSelectFirstEnemy();
            }
        }

        public void AutoSelectFirstEnemy()
        {
            if (battleManager == null) return;
            var enemies = battleManager.GetEnemies(aliveOnly: true);
            if (enemies.Count == 0)
            {
                DeselectEnemy();
                return;
            }
            OnEnemyClicked(enemies[0]); // Tái sử dụng hàm logic ở trên
        }
    }
}
```

#### SkillButtonUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Skills;
using System.Text;

namespace RebirthWarrior.Battle
{
    public class SkillButtonUI : MonoBehaviour
    {
        [SerializeField] private Button button;
        [SerializeField] private Image icon;
        [SerializeField] private TextMeshProUGUI skillNameText;
        [SerializeField] private TextMeshProUGUI mpCostText;

        private Skill assignedSkill;
        private BattleUI battleUI;

        /// <summary>
        /// Gán dữ liệu skill vào nút này
        /// </summary>
        public void Initialize(Skill skill, BattleUI ui)
        {
            assignedSkill = skill;
            battleUI = ui;

            if (icon != null)
            {
                icon.sprite = skill.icon;
                icon.enabled = (skill.icon != null);
            }
            if (skillNameText != null)
            {
                // TODO: Dùng LocalizationManager
                skillNameText.text = skill.skillNameKey;
            }
            if (mpCostText != null)
            {
                // [FIX LỖI] Đổi hiển thị MP -> STM (Stamina)
                mpCostText.text = $"STM: {skill.staminaCost}";
            }

            button.onClick.AddListener(OnSkillClicked);
        }

        /// <summary>
        /// Khi người chơi bấm nút skill này
        /// </summary>
        private void OnSkillClicked()
        {
            if (battleUI != null)
            {
                // Báo cho BattleUI biết skill nào được chọn
                battleUI.OnSkillSelected(assignedSkill);
            }
        }
    }
}
```



#### TargetSelector.cs
```csharp
using RebirthWarrior.Character;
using RebirthWarrior.Skills;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.Events;

namespace RebirthWarrior.Battle
{
    public class TargetSelector : MonoBehaviour
    {
        // ... (Giữ nguyên các biến Events và State) ...
        [Header("Events")]
        public UnityEvent<BattleUnit> OnTargetSelected;
        public UnityEvent OnSelectionCancelled;

        private BattleUnit currentTarget;
        private List<BattleUnit> availableTargets = new List<BattleUnit>();
        private bool isSelectingTarget = false;

        public void StartTargetSelection(TargetType targetType, List<BattleUnit> targets)
        {
            if (targets == null || targets.Count == 0) return;

            isSelectingTarget = true;
            availableTargets = new List<BattleUnit>(targets);

            foreach (var target in availableTargets)
            {
                if (target.IsAlive()) HighlightTarget(target, true);
            }
        }

        public void CancelTargetSelection()
        {
            if (!isSelectingTarget) return;
            foreach (var target in availableTargets) HighlightTarget(target, false);
            isSelectingTarget = false;
            availableTargets.Clear();
            currentTarget = null;
            OnSelectionCancelled?.Invoke();
        }

        public void OnTargetClicked(BattleUnit target)
        {
            if (!isSelectingTarget) return;
            if (!availableTargets.Contains(target) || !target.IsAlive()) return;

            currentTarget = target;
            foreach (var t in availableTargets) HighlightTarget(t, false);

            isSelectingTarget = false;
            OnTargetSelected?.Invoke(currentTarget);
        }

        // --- SỬA LOGIC HIGHLIGHT ---
        private void HighlightTarget(BattleUnit target, bool highlight)
        {
            // Tìm HUD chung cho cả Player và Enemy
            var hud = FindHUD(target);
            if (hud != null)
            {
                hud.SetSelected(highlight); // Tái sử dụng khung chọn làm highlight
            }
        }

        private BattleUnitHUD FindHUD(BattleUnit unit)
        {
            var allHUDs = FindObjectsOfType<BattleUnitHUD>();
            foreach (var ui in allHUDs)
            {
                if (ui.GetCharacterStats() == unit.stats) return ui;
            }
            return null;
        }

        public bool IsSelecting() => isSelectingTarget;
        public BattleUnit GetCurrentTarget() => currentTarget;
    }

    // (Giữ enum TargetType nếu có)
}
```



#### VictoryScreen.cs
```csharp
using RebirthWarrior.Character;
using RebirthWarrior.World;
using System.Collections;
using System.Collections.Generic;
using TMPro;
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

namespace RebirthWarrior.Battle
{
    public class VictoryScreen : MonoBehaviour
    {
        [Header("UI References")]
        [SerializeField] private GameObject victoryPanel;
        [SerializeField] private TextMeshProUGUI titleText;
        [SerializeField] private Button continueButton;

        [Header("Reward Info")]
        [SerializeField] private TextMeshProUGUI goldText;
        [SerializeField] private Transform characterListContainer;
        [SerializeField] private GameObject victorySlotPrefab;
        [SerializeField] private Transform dropsContainer;
        [SerializeField] private GameObject dropSlotPrefab;

        private void Awake()
        {
            if (victoryPanel != null) victoryPanel.SetActive(false);
            if (continueButton != null) continueButton.onClick.AddListener(OnContinueClicked);
        }

        public void ShowVictory(BattleRewardResult rewards, List<CharacterStats> party)
        {
            if (victoryPanel != null) victoryPanel.SetActive(true);
            if (continueButton != null) continueButton.interactable = false;

            StartCoroutine(ShowSequence(rewards, party));
        }

        private IEnumerator ShowSequence(BattleRewardResult rewards, List<CharacterStats> party)
        {
            // 1. Hiển thị Vàng
            if (goldText != null) goldText.text = $"+{rewards.goldGained} Gold";

            // 2. Hiển thị Vật phẩm (ĐÃ FIX)
            foreach (Transform child in dropsContainer) Destroy(child.gameObject);

            if (rewards.droppedItems != null)
            {
                foreach (var drop in rewards.droppedItems)
                {
                    if (drop.item == null) continue;
                    GameObject obj = Instantiate(dropSlotPrefab, dropsContainer);

                    // --- LOGIC TÌM UI THÔNG MINH HƠN ---

                    // A. Tìm Image Icon (Tìm object con có tên "Icon", nếu không thấy thì tìm Image thứ 2)
                    Image iconImg = null;
                    Transform iconTrans = obj.transform.Find("Icon"); // Tìm theo tên "Icon" trong Prefab
                    if (iconTrans) iconImg = iconTrans.GetComponent<Image>();

                    // Fallback: Nếu không đặt tên là Icon, tìm component Image (thường cái đầu là BG, cái sau là Icon)
                    if (iconImg == null)
                    {
                        var images = obj.GetComponentsInChildren<Image>();
                        if (images.Length > 1) iconImg = images[1]; // Lấy cái thứ 2 (Icon)
                        else if (images.Length == 1) iconImg = images[0]; // Lấy cái duy nhất
                    }

                    // Gán Sprite Item
                    if (iconImg != null && drop.item.icon != null)
                    {
                        iconImg.sprite = drop.item.icon;
                        iconImg.enabled = true;
                    }

                    // B. Tìm Text (Hiển thị Tên + Số lượng)
                    var txt = obj.GetComponentInChildren<TextMeshProUGUI>();
                    if (txt)
                    {
                        // Hiển thị: "Potion x2"
                        string qtyStr = drop.quantity > 1 ? $" <color=yellow>x{drop.quantity}</color>" : "";
                        txt.text = $"{drop.item.itemName}{qtyStr}";
                    }
                }
            }

            // 3. Hiển thị EXP
            foreach (Transform child in characterListContainer) Destroy(child.gameObject);
            List<VictorySlotUI> slots = new List<VictorySlotUI>();

            foreach (var member in party)
            {
                GameObject obj = Instantiate(victorySlotPrefab, characterListContainer);
                var slotUI = obj.GetComponent<VictorySlotUI>();
                if (slotUI)
                {
                    slotUI.Setup(member);
                    slots.Add(slotUI);
                }
            }

            yield return new WaitForSeconds(0.5f);

            foreach (var slot in slots)
            {
                if (slot) StartCoroutine(slot.AnimateExp(rewards.expGained));
            }

            yield return new WaitForSeconds(1.0f);
            if (continueButton != null) continueButton.interactable = true;
        }

        private void OnContinueClicked()
        {
            if (victoryPanel != null) victoryPanel.SetActive(false);
            string sceneToLoad = PlayerPrefs.GetString("ReturnScene", "WorldScene");
            SceneManager.LoadScene(sceneToLoad);
        }
    }
}
```


#### VictorySlotUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;
using System.Collections;

namespace RebirthWarrior.Battle
{
    public class VictorySlotUI : MonoBehaviour
    {
        [Header("UI References")]
        [SerializeField] private Image portrait;
        [SerializeField] private TextMeshProUGUI nameText;
        [SerializeField] private TextMeshProUGUI levelText;
        [SerializeField] private Slider expSlider;
        [SerializeField] private TextMeshProUGUI expGainText;
        [SerializeField] private GameObject levelUpVFX; // Text hoặc Particle "Level Up!"

        private CharacterStats stats;

        public void Setup(CharacterStats character)
        {
            stats = character;

            if (portrait != null && character.characterData != null)
                portrait.sprite = character.characterData.portraitSprite;

            if (nameText != null) nameText.text = character.characterName;

            // Set trạng thái ban đầu (Trước khi cộng EXP)
            UpdateLevelInfo();

            if (levelUpVFX != null) levelUpVFX.SetActive(false);
            if (expGainText != null) expGainText.text = "";
        }

        private void UpdateLevelInfo()
        {
            if (levelText != null) levelText.text = $"Lv.{stats.level}";

            if (expSlider != null)
            {
                // Tính % EXP
                // Cần công thức EXP từ CharacterStats để hiển thị chính xác thanh slider
                // Tạm thời dùng current / max
                float current = stats.currentExp;
                float max = stats.expToNextLevel; // Bạn cần đảm bảo biến này public trong CharacterStats
                expSlider.value = current / max;
            }
        }

        public IEnumerator AnimateExp(int expGained)
        {
            if (expGainText != null) expGainText.text = $"+{expGained} EXP";

            // Logic chạy thanh EXP đơn giản
            // Để làm chuẩn xác (tăng level giữa chừng), cần logic phức tạp hơn trong CharacterStats
            // Ở đây ta giả lập hiệu ứng visual

            float startVal = expSlider.value;
            float targetVal = (float)(stats.currentExp) / stats.expToNextLevel; // Giá trị sau khi đã cộng (vì BattleRewards đã cộng rồi)

            // Nếu vừa lên cấp, currentExp sẽ nhỏ hơn startVal (tương đối), ta cần xử lý visual đặc biệt
            // Tuy nhiên để đơn giản cho Phase này:

            float timer = 0;
            while (timer < 1f)
            {
                timer += Time.deltaTime;
                expSlider.value = Mathf.Lerp(startVal, targetVal, timer);
                yield return null;
            }

            // Check level up (So sánh level hiện tại với level lúc Setup - cần lưu biến oldLevel nếu muốn chính xác)
            // Tạm thời check visual
            UpdateLevelInfo();
        }

        public void ShowLevelUp()
        {
            if (levelUpVFX != null)
            {
                levelUpVFX.SetActive(true);
                // Play sound level up
            }
        }
    }
}
```


### C2. Character Scripts

#### CharacterAppearanceData.cs
```csharp
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.Character
{
    [CreateAssetMenu(menuName = "Rebirth Warrior/Character/Appearance Data")]
    public class CharacterAppearanceData : ScriptableObject
    {
        [Header("GENDER BASE (Cơ thể gốc - Thay đổi theo Giới Tính)")]
        public Sprite maleBaseSkin;   // Ảnh nam khỏa thân/cơ bản (150x150)
        public Sprite femaleBaseSkin; // Ảnh nữ khỏa thân/cơ bản (150x150)

        [Header("MALE OPTIONS (Nam)")]
        public List<Sprite> maleOutfits;    // <-- Body/Quần áo cho nam
        public List<Sprite> maleHairStyles; // Tóc nam
        public List<Sprite> maleEyes;       // Mắt nam

        [Header("FEMALE OPTIONS (Nữ)")]
        public List<Sprite> femaleOutfits;  // <-- Body/Quần áo cho nữ
        public List<Sprite> femaleHairStyles; // Tóc nữ
        public List<Sprite> femaleEyes;       // Mắt nữ
    }
}
```



#### CharacterData.cs
Logic: Mở rộng dữ liệu để hỗ trợ Battle Visuals:

public GameObject battlePrefab: Prefab vật lý (đã Rigging) sẽ được spawn trong Battle Scene.

public AudioClip sfxAttack/sfxHit/sfxDie: Cấu hình âm thanh.

```csharp
using UnityEngine;
using RebirthWarrior.Skills;
using System.Collections.Generic;

namespace RebirthWarrior.Character
{
    [CreateAssetMenu(fileName = "New Character", menuName = "Rebirth Warrior/Character Data")]
    public class CharacterData : ScriptableObject
    {
        [Header("Character Identity")]
        public string characterID;
        public string characterNameKey; // Localization key
        public Sprite characterSprite;  // 32-bit pixel art sprite
        public Sprite portraitSprite;   // Portrait cho UI

        [Header("UI Display")]
        public Sprite icon; // Ảnh đại diện hiển thị trên thanh máu và bảng info (200x200px)

        [Header("Character Type")]
        public CharacterType type;
        public CharacterClass characterClass;

        [Header("Base Stats (Level 1)")]
        public int baseMaxHP = 100;
        public int baseMaxStamina = 50; // [ĐỔI] Thay cho baseMaxMP
        public int baseAttack = 10;
        public int baseDefense = 5;
        public int baseToxicAttack = 10; // [ĐỔI] Thay cho baseMagic
        public int baseToxicResist = 5;  // [ĐỔI] Thay cho baseMagicDefense
        public int baseSpeed = 10;
        public int baseAgility = 10;
        public int baseLuck = 5;

        [Header("--- 2.5D BATTLE SETTINGS (NEW) ---")]
        [Tooltip("Loại tấn công cơ bản của nhân vật")]
        public AttackType basicAttackType = AttackType.Melee;

        [Tooltip("Khoảng cách dừng lại trước mặt kẻ thù khi tấn công cận chiến")]
        public float stopDistance = 1.5f;

        [Tooltip("Tốc độ di chuyển khi lao tới tấn công")]
        public float battleMoveSpeed = 10f;

        [Tooltip("Projectile Prefab (Dành cho Ranged/Mage)")]
        public GameObject projectilePrefab;

        [Header("Growth Rates (per level)")]
        [Tooltip("Số điểm Stats nhận được mỗi level (CHỈ DÙNG cho MainPlayerCharacter)")]
        public int statPointsPerLevel = 5;

        [Tooltip("Tỷ lệ tăng HP tự động")]
        [Range(1f, 10f)] public float hpGrowth = 5f;
        [Tooltip("Tỷ lệ tăng Stamina tự động")]
        [Range(1f, 5f)] public float staminaGrowth = 3f; // [ĐỔI] Thay cho mpGrowth
        [Tooltip("Tỷ lệ tăng Attack tự động")]
        [Range(0.5f, 3f)] public float attackGrowth = 2f;
        [Tooltip("Tỷ lệ tăng Defense tự động")]
        [Range(0.5f, 2f)] public float defenseGrowth = 1.5f;

        [Tooltip("Tỷ lệ tăng Toxic Attack tự động")]
        [Range(0.5f, 3f)] public float toxicAttackGrowth = 2f; // [ĐỔI] Thay magicGrowth

        [Tooltip("Tỷ lệ tăng Toxic Resist tự động")]
        [Range(0.5f, 2f)] public float toxicResistGrowth = 1.5f; // [ĐỔI] Thay magicDefenseGrowth

        [Tooltip("Tỷ lệ tăng Speed tự động")]
        [Range(0.5f, 2f)] public float speedGrowth = 1.5f;

        [Header("Skills")]
        public List<Skill> learnableSkills;

        [Header("--- BATTLE VISUALS (QUAN TRỌNG) ---")]
        [Tooltip("Prefab nhân vật sẽ sinh ra trong Battle")]
        public GameObject battlePrefab;

        [Header("--- VISUAL CONFIG (MẶC ĐỊNH) ---")]
        [Tooltip("Sprite ảnh 2D cơ bản của nhân vật")]
        public Sprite defaultBattleSprite;

        [Header("Audio Config")]
        public AudioClip sfxAttack;
        public AudioClip sfxHit;
        public AudioClip sfxDie;
        public AudioClip sfxCastSkill;

        [Header("VFX Config")]
        [Tooltip("Hiệu ứng nổ ra trên người đối thủ khi nhân vật này tấn công trúng")]
        public GameObject hitVFXPrefab;

        [Tooltip("Vị trí bắn đạn (nếu là cung thủ/pháp sư)")]
        public Vector3 projectileSpawnOffset;

        [Header("Rewards (Khi bị giết)")]
        [Tooltip("Số EXP nhận được khi giết quái này")]
        public int killExpReward = 50;

        [Tooltip("Số Vàng nhận được khi giết quái này")]
        public int killGoldReward = 10;

        [Header("Loot Table (Vật phẩm rơi ra)")]
        public List<LootItem> potentialDrops;

        [Header("Character Story")]
        [TextArea(3, 6)]
        public string backstoryKey;

        [Header("PET SYSTEM (Chỉ dùng nếu Type = Pet)")]
        [Tooltip("Pet này có cưỡi được không?")]
        public bool isMountable;

        [Tooltip("Tốc độ di chuyển cộng thêm khi cưỡi")]
        public float mountSpeedBonus = 2.0f;

        [Tooltip("Sprite khi Player cưỡi lên Pet")]
        public Sprite mountedSprite;

        [Header("EVOLUTION (Tiến Hóa)")]
        [Tooltip("Item cần thiết để tiến hóa")]
        public RebirthWarrior.Items.Item evolutionItem;

        [Tooltip("Level tối thiểu để tiến hóa")]
        public int evolutionLevelReq = 10;

        [Tooltip("Hình dạng tiếp theo sau khi tiến hóa")]
        public CharacterData nextEvolutionForm;

        /// <summary>
        /// Tạo CharacterStats instance từ data này
        /// </summary>
        public CharacterStats CreateStats(int level = 1)
        {
            CharacterStats stats = new CharacterStats(characterID, characterNameKey);

            stats.characterData = this;
            stats.level = level;

            // [FIX ERROR] Map các biến mới sang CharacterStats
            stats.baseMaxHP = baseMaxHP;
            stats.baseMaxStamina = baseMaxStamina;
            stats.baseAttack = baseAttack;
            stats.baseDefense = baseDefense;
            stats.baseToxicAttack = baseToxicAttack;
            stats.baseToxicResist = baseToxicResist;
            stats.baseSpeed = baseSpeed;
            stats.baseAgility = baseAgility;
            stats.baseLuck = baseLuck;

            // Logic tăng level tự động khi khởi tạo (dành cho Followers/Enemies)
            if (level > 1 && type != CharacterType.MainPlayerCharacter)
            {
                int levelsToGrow = level - 1;
                stats.baseMaxHP += Mathf.RoundToInt(hpGrowth * levelsToGrow);

                // [FIX] Dùng staminaGrowth
                stats.baseMaxStamina += Mathf.RoundToInt(staminaGrowth * levelsToGrow);

                stats.baseAttack += Mathf.RoundToInt(attackGrowth * levelsToGrow);
                stats.baseDefense += Mathf.RoundToInt(defenseGrowth * levelsToGrow);

                // [FIX] Dùng toxic growth
                stats.baseToxicAttack += Mathf.RoundToInt(toxicAttackGrowth * levelsToGrow);
                stats.baseToxicResist += Mathf.RoundToInt(toxicResistGrowth * levelsToGrow);

                stats.baseSpeed += Mathf.RoundToInt(speedGrowth * levelsToGrow);
            }
            else if (type == CharacterType.MainPlayerCharacter)
            {
                stats.unspentStatPoints = 20;
            }

            // [FIX ERROR] Dùng Stamina thay vì MP
            stats.currentHP = stats.maxHP;
            stats.currentStamina = stats.maxStamina; // Sửa dòng gây lỗi 165

            if (learnableSkills != null)
            {
                foreach (var skill in learnableSkills)
                {
                    if (skill != null && level >= skill.requiredLevel)
                    {
                        stats.LearnSkill(skill);
                    }
                }
            }

            return stats;
        }
    }

    // Enums
    public enum CharacterType
    {
        MainPlayerCharacter,
        PlayerCharacter,
        Enemy,
        Pet,
        NPC
    }

    public enum AttackType
    {
        Melee,
        Ranged,
        Cast
    }

    public enum CharacterClass
    {
        Warrior, Spearman, Archer,
        Mage, Priest, Shaman,
        BladeDancer, BeastMaster, Strategist,
        DragonKnight, PhoenixMage, ImmortalMonk,
        TuongQuan, ThienBinh, SonLinh
    }

    [System.Serializable]
    public class LootItem
    {
        public RebirthWarrior.Items.Item item;
        [Range(0f, 100f)] public float dropChance;
        public int minAmount = 1;
        public int maxAmount = 1;

        [Header("Quest Condition")]
        public bool isQuestItem;
        public string requiredQuestID;
    }
}
```



#### CharacterStats.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Items;
using System.Linq;
using RebirthWarrior.Skills;
using System;

namespace RebirthWarrior.Character
{
    [System.Serializable]
    public class CharacterStats
    {
        public static event Action<int> OnLevelUp;

        [Header("Identity")]
        public CharacterData characterData;
        public string characterID;
        public string characterName;
        public int level = 1;

        [Header("Experience")]
        public int currentExp = 0;
        public int expToNextLevel = 100;
        public int unspentStatPoints = 0;

        [Header("Health & Stamina")]
        public int currentHP = 100;
        public int currentStamina = 100; // Thay cho MP
        public int currentToxic = 0;     // Thanh nhiễm độc (0-100)

        [Header("Base Stats (Raw)")]
        public int baseMaxHP = 100;
        public int baseMaxStamina = 100; // Thay cho baseMaxMP
        public int baseAttack = 10;
        public int baseDefense = 5;
        public int baseToxicAttack = 0;  // Thay cho Magic (Sát thương độc)
        public int baseToxicResist = 0;  // Thay cho MagicDefense (Kháng độc)
        public int baseSpeed = 10;
        public int baseAgility = 10;
        public int baseLuck = 5;

        [Header("Visual Appearance")]
        public bool isCustomCharacter = false;
        public int genderIndex;
        public int bodyIndex;
        public int hairIndex;
        public int eyesIndex;

        [Header("Skills & Equipment")]
        public List<Skill> learnedSkills = new List<Skill>();
        public Dictionary<EquipmentSlot, Item> equippedItems = new Dictionary<EquipmentSlot, Item>();

        [Header("Survival Skills (Mới)")]
        public List<SurvivalSkillData> survivalSkills = new List<SurvivalSkillData>();

        [Header("Status")]
        public bool isAlive = true;
        public StatusEffect currentStatus = StatusEffect.None;

        // --- PROPERTIES (BASE + BONUS) ---
        public int maxHP { get { return baseMaxHP + GetEquipmentBonus(StatType.MaxHP); } }
        public int maxStamina { get { return baseMaxStamina + GetEquipmentBonus(StatType.MaxStamina); } }
        public int attack { get { return baseAttack + GetEquipmentBonus(StatType.Attack); } }
        public int defense { get { return baseDefense + GetEquipmentBonus(StatType.Defense); } }

        // Toxic Attack thay thế Magic
        public int toxicAttack { get { return baseToxicAttack + GetEquipmentBonus(StatType.ToxicAttack); } }

        // Toxic Resist thay thế Magic Defense
        public int toxicResist { get { return baseToxicResist + GetEquipmentBonus(StatType.ToxicResist); } }

        public int speed { get { return baseSpeed + GetEquipmentBonus(StatType.Speed); } }
        public int agility { get { return baseAgility + GetEquipmentBonus(StatType.Agility); } }
        public int luck { get { return baseLuck + GetEquipmentBonus(StatType.Luck); } }

        // --- CONSTRUCTOR ---
        public CharacterStats(string id, string name)
        {
            characterID = id;
            characterName = name;
            equippedItems = new Dictionary<EquipmentSlot, Item>();
            learnedSkills = new List<Skill>();
            isAlive = true;

            // Khởi tạo 5 kỹ năng sinh tồn mặc định
            foreach (SurvivalSkillType type in System.Enum.GetValues(typeof(SurvivalSkillType)))
            {
                survivalSkills.Add(new SurvivalSkillData { type = type });
            }
        }

        // --- TIME SYSTEM HOOK ---
        public static void OnHourPassed()
        {
            if (RebirthWarrior.Core.GameStateManager.Instance == null) return;
            var player = RebirthWarrior.Core.GameStateManager.Instance.GetMainPlayer();
            if (player != null) player.ProcessTimeEffects();
        }

        public void ProcessTimeEffects()
        {
            // 1. Trừ Stamina (Đói/Khát)
            UseStamina(5); // Mất 5 Stamina mỗi giờ game

            // 2. Nếu Stamina = 0 -> Trừ máu (Dehydrated)
            if (currentStamina <= 0)
            {
                TakeDamage(2);
                Debug.LogWarning($"{characterName} đang mất máu do kiệt sức!");
            }

            // 3. Nếu nhiễm độc (Toxic > 50) -> Trừ máu
            if (currentToxic > 50)
            {
                TakeDamage(5);
            }
        }

        // --- REBIRTH ---
        public void ApplyRebirth(CharacterData newClassData)
        {
            if (newClassData == null) return;
            Debug.Log($"[CharacterStats] Trọng sinh thành {newClassData.characterNameKey}...");
            level = 1;
            currentExp = 0;
            expToNextLevel = CalculateExpForNextLevel(1);
            unspentStatPoints = 0;

            characterData = newClassData;
            characterID = newClassData.characterID;

            baseMaxHP = newClassData.baseMaxHP;
            baseMaxStamina = newClassData.baseMaxStamina; // [FIX] Dùng baseMaxStamina
            baseAttack = newClassData.baseAttack;
            baseDefense = newClassData.baseDefense;
            baseToxicAttack = newClassData.baseToxicAttack; // [FIX] Dùng baseToxicAttack
            baseToxicResist = newClassData.baseToxicResist; // [FIX] Dùng baseToxicResist
            baseSpeed = newClassData.baseSpeed;
            baseAgility = newClassData.baseAgility;
            baseLuck = newClassData.baseLuck;

            learnedSkills.Clear();
            CheckForNewSkills();
            equippedItems.Clear();

            Revive();
            currentHP = maxHP;
            currentStamina = maxStamina;
        }

        public void LearnSkill(Skill skill) { if (skill && !learnedSkills.Contains(skill)) learnedSkills.Add(skill); }
        public bool KnowsSkill(Skill skill) => learnedSkills.Contains(skill);

        private void CheckForNewSkills()
        {
            if (characterData && characterData.learnableSkills != null)
                foreach (var s in characterData.learnableSkills) if (s && level >= s.requiredLevel && !KnowsSkill(s)) LearnSkill(s);
        }

        private int GetEquipmentBonus(StatType stat)
        {
            if (equippedItems == null) return 0;
            int bonus = 0;
            foreach (var item in equippedItems.Values)
            {
                if (item == null) continue;
                switch (stat)
                {
                    case StatType.MaxHP: bonus += item.maxHPBonus; break;
                    case StatType.MaxStamina: bonus += item.maxStaminaBonus; break;
                    case StatType.Attack: bonus += item.attackBonus; break;
                    case StatType.Defense: bonus += item.defenseBonus; break;
                    case StatType.ToxicAttack: bonus += item.toxicAttackBonus; break;
                    case StatType.ToxicResist: bonus += item.toxicResistBonus; break;
                    case StatType.Speed: bonus += item.speedBonus; break;
                }
            }
            return bonus;
        }

        public Item EquipItem(Item item, EquipmentSlot slot)
        {
            if (!item || !item.IsEquipment()) return null;
            Item old = null;
            if (equippedItems.TryGetValue(slot, out old)) { }
            equippedItems[slot] = item;
            ValidateCurrentHPMP();
            return old;
        }

        public Item UnequipItem(EquipmentSlot slot)
        {
            if (equippedItems.TryGetValue(slot, out Item item))
            {
                equippedItems[slot] = null;
                ValidateCurrentHPMP();
                return item;
            }
            return null;
        }

        public Item GetItemInSlot(EquipmentSlot slot) { equippedItems.TryGetValue(slot, out Item item); return item; }
        private void ValidateCurrentHPMP() { currentHP = Mathf.Min(currentHP, maxHP); currentStamina = Mathf.Min(currentStamina, maxStamina); }

        public void TakeDamage(int dmg) { currentHP = Mathf.Max(0, currentHP - dmg); if (currentHP <= 0) { isAlive = false; currentHP = 0; } }
        public void Heal(int amt) { if (isAlive) currentHP = Mathf.Min(maxHP, currentHP + amt); }

        public bool UseStamina(int amt)
        {
            if (currentStamina >= amt) { currentStamina -= amt; return true; }
            currentStamina = 0;
            return false;
        }
        public void RestoreStamina(int amt) => currentStamina = Mathf.Min(maxStamina, currentStamina + amt);

        public void AddToxic(int amt) { currentToxic = Mathf.Min(100, currentToxic + amt); }
        public void ReduceToxic(int amt) { currentToxic = Mathf.Max(0, currentToxic - amt); }

        public int GetSkillLevel(SurvivalSkillType type)
        {
            var skill = survivalSkills.Find(s => s.type == type);
            return skill != null ? skill.level : 1;
        }
        public void AddSkillExp(SurvivalSkillType type, int amount)
        {
            var skill = survivalSkills.Find(s => s.type == type);
            if (skill != null) skill.AddExp(amount);
        }

        public void GainExperience(int amt) { if (amt <= 0) return; currentExp += amt; while (currentExp >= expToNextLevel) LevelUp(); }

        private void LevelUp()
        {
            level++;
            currentExp -= expToNextLevel;
            expToNextLevel = CalculateExpForNextLevel(level);

            if (characterData != null && characterData.type == CharacterType.MainPlayerCharacter)
            {
                unspentStatPoints += characterData.statPointsPerLevel;
                baseMaxHP += 5;
                baseMaxStamina += 2;
            }
            else
            {
                if (characterData != null)
                {
                    baseMaxHP += Mathf.RoundToInt(characterData.hpGrowth);

                    // [FIX] Sửa tên biến ở đây để khớp với CharacterData.cs
                    baseMaxStamina += Mathf.RoundToInt(characterData.staminaGrowth); // Đã sửa mpGrowth -> staminaGrowth

                    baseAttack += Mathf.RoundToInt(characterData.attackGrowth);
                    baseDefense += Mathf.RoundToInt(characterData.defenseGrowth);

                    // [FIX] Sửa magicGrowth -> toxicAttackGrowth
                    baseToxicAttack += Mathf.RoundToInt(characterData.toxicAttackGrowth);

                    // [FIX] Sửa magicDefenseGrowth -> toxicResistGrowth
                    baseToxicResist += Mathf.RoundToInt(characterData.toxicResistGrowth);

                    baseSpeed += Mathf.RoundToInt(characterData.speedGrowth);
                }
                else
                {
                    baseMaxHP += 10;
                    baseAttack += 1;
                }
            }

            currentHP = maxHP;
            currentStamina = maxStamina;
            OnLevelUp?.Invoke(level);
            CheckForNewSkills();
        }

        private int CalculateExpForNextLevel(int lv) => (int)Mathf.Pow(lv, 2) * 100 + lv * 1000;

        public void Revive() { isAlive = true; currentHP = maxHP / 2; currentStamina = maxStamina / 2; currentStatus = StatusEffect.None; }
        public void ApplyStatusEffect(StatusEffect e) => currentStatus = e;
        public void ClearStatusEffect() => currentStatus = StatusEffect.None;
        public float GetHPPercentage() => (float)currentHP / maxHP;
        public float GetStaminaPercentage() => (float)currentStamina / maxStamina;
    }

    public enum StatType { MaxHP, MaxStamina, Attack, Defense, ToxicAttack, ToxicResist, Speed, Agility, Luck }
    public enum StatusEffect { None, Poison, Burn, Paralysis, Sleep, Confusion, Silence, Blind, Stun }
}
```

#### PlayerAnimation.cs
```csharp
using UnityEngine;

namespace RebirthWarrior.Character
{
    public class PlayerAnimation : MonoBehaviour
    {
        private Animator anim;

        // Tên các State trong Animator (Phải đặt tên chính xác y hệt thế này)
        // Thứ tự mảng cực kỳ quan trọng: N -> NW -> W -> SW -> S -> SE -> E -> NE
        // Tương ứng với vòng tròn ngược chiều kim đồng hồ bắt đầu từ hướng Bắc (North)
        public string[] staticDirections = { "Static N", "Static NW", "Static W", "Static SW", "Static S", "Static SE", "Static E", "Static NE" };
        public string[] runDirections = { "Run N", "Run NW", "Run W", "Run SW", "Run S", "Run SE", "Run E", "Run NE" };

        private int lastDirectionIndex;

        private void Awake()
        {
            anim = GetComponent<Animator>();
        }

        public void SetDirection(Vector2 _direction)
        {
            string[] directionArray = null;

            // Nếu vận tốc gần như bằng 0 -> Đứng yên
            if (_direction.sqrMagnitude < 0.01f)
            {
                directionArray = staticDirections;
            }
            else
            {
                directionArray = runDirections;
                // Chỉ tính toán hướng mới khi nhân vật di chuyển
                lastDirectionIndex = DirectionToIndex(_direction);
            }

            // Gọi tên Animation để Play
            anim.Play(directionArray[lastDirectionIndex]);
        }

        // HÀM TÍNH TOÁN GÓC (Logic cốt lõi từ file tham khảo)
        private int DirectionToIndex(Vector2 _direction)
        {
            // Chuẩn hóa vector để chỉ lấy hướng
            Vector2 norDir = _direction.normalized;

            // Chia 360 độ thành 8 phần => mỗi phần 45 độ
            float step = 360f / 8f;

            // Offset một nửa bước (22.5 độ) để hướng Bắc nằm giữa lát cắt
            float offset = step / 2f;

            // Tính góc giữa hướng di chuyển và hướng Bắc (Vector2.up)
            float angle = Vector2.SignedAngle(Vector2.up, norDir);

            // Cộng offset để căn chỉnh
            angle += offset;

            // Xử lý số âm (SignedAngle trả về -180 đến 180) -> chuyển thành 0 đến 360
            if (angle < 0)
            {
                angle += 360;
            }

            // Tính ra index (0 đến 7)
            float stepCount = angle / step;
            return Mathf.FloorToInt(stepCount) % 8; // % 8 để đảm bảo an toàn
        }
    }
}
```



### C3. Core Scripts

#### CanvasResetter.cs
```csharp
using UnityEngine;
using UnityEngine.SceneManagement;

public class CanvasResetter : MonoBehaviour
{
    private Canvas canvas;

    private void Awake()
    {
        DontDestroyOnLoad(gameObject);
        canvas = GetComponent<Canvas>();
        SceneManager.sceneLoaded += OnSceneLoaded;
    }

    private void OnSceneLoaded(Scene scene, LoadSceneMode mode)
    {
        if (canvas != null)
        {
            if (canvas.renderMode == RenderMode.ScreenSpaceCamera)
                canvas.worldCamera = Camera.main;
            else
                canvas.worldCamera = null;

            // Đặt lại vị trí
            RectTransform rect = GetComponent<RectTransform>();
            rect.anchoredPosition = Vector2.zero;
            rect.localScale = Vector3.one;
        }
    }

    private void OnDestroy()
    {
        SceneManager.sceneLoaded -= OnSceneLoaded;
    }
}

``````



#### DialogueManager.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using System;
using RebirthWarrior.Dialogue;
using RebirthWarrior.Quests;
using RebirthWarrior.World;

namespace RebirthWarrior.Core
{
    public class DialogueManager : MonoBehaviour
    {
        public static DialogueManager Instance { get; private set; }

        [Header("Runtime UI References")]
        [SerializeField] private GameObject npcContainer;
        [SerializeField] private GameObject playerContainer;

        private TextMeshProUGUI npcNameText;
        private TextMeshProUGUI npcDialogueText;
        private Image npcAvatarImage;
        private TextMeshProUGUI playerNameText;
        private TextMeshProUGUI playerDialogueText;
        private Image playerAvatarImage;
        private Transform choicesContainer;
        private GameObject choiceButtonPrefab;
        private Button continueButton;

        private DialogueData currentData;
        private DialogueState currentState;
        private int currentLineIndex;
        private bool isDialogueActive;
        private Action onDialogueComplete;

        private void Awake()
        {
            if (Instance == null) { Instance = this; }
            else { Destroy(gameObject); }
        }

        public void SetupUI(
            GameObject npcPanel, TextMeshProUGUI npcName, TextMeshProUGUI npcText, Image npcAvatar,
            GameObject playerPanel, TextMeshProUGUI playerName, TextMeshProUGUI playerText, Image playerAvatar,
            Transform choices, GameObject btnPrefab, Button contBtn)
        {
            npcContainer = npcPanel;
            npcNameText = npcName;
            npcDialogueText = npcText;
            npcAvatarImage = npcAvatar;

            playerContainer = playerPanel;
            playerNameText = playerName;
            playerDialogueText = playerText;
            playerAvatarImage = playerAvatar;

            if (choices != null) choicesContainer = choices;
            if (btnPrefab != null) choiceButtonPrefab = btnPrefab;
            if (contBtn != null) continueButton = contBtn;
        }

        public bool IsDialogueActive() => isDialogueActive;

        public void StartDialogue(DialogueData data, Action onComplete)
        {
            if (data == null) return;
            this.onDialogueComplete = onComplete;
            BeginDialogueLogic(data, "Default");
        }

        public void StartDialogue(DialogueData data, string startStateID = "Default")
        {
            if (data == null) return;
            this.onDialogueComplete = null;
            BeginDialogueLogic(data, startStateID);
        }

        public void StartDialogue(DialogueData data, string startStateID, Action onComplete)
        {
            if (data == null) return;
            this.onDialogueComplete = onComplete;
            BeginDialogueLogic(data, startStateID);
        }

        private void BeginDialogueLogic(DialogueData data, string startID)
        {
            currentData = data;
            ChangeState(startID);
            isDialogueActive = true;

            var p = FindObjectOfType<PlayerController>();
            if (p != null) p.DisableMovement();

            if (npcContainer) npcContainer.SetActive(false);
            if (playerContainer) playerContainer.SetActive(false);

            DisplayLine();
        }

        private void ChangeState(string id)
        {
            currentState = currentData.GetState(id);
            if (currentState == null && currentData.states.Count > 0) currentState = currentData.states[0];
            currentLineIndex = 0;
        }

        private void DisplayLine()
        {
            if (currentState == null || currentLineIndex >= currentState.lines.Count) { EndDialogue(); return; }

            DialogueLine line = currentState.lines[currentLineIndex];
            bool hasChoices = (line.choices != null && line.choices.Count > 0);
            string textToShow = line.text;

            if (line.isPlayerSpeaking && hasChoices) textToShow = "";

            UpdateSpeakerUI(line.isPlayerSpeaking, textToShow, hasChoices);
            ExecuteAction(line.actionOnShow);

            if (choicesContainer != null) foreach (Transform t in choicesContainer) Destroy(t.gameObject);

            if (hasChoices)
            {
                if (continueButton != null) continueButton.gameObject.SetActive(false);
                if (choicesContainer != null) choicesContainer.gameObject.SetActive(true);

                foreach (var c in line.choices)
                {
                    if (CheckChoiceCondition(c))
                    {
                        if (choiceButtonPrefab != null && choicesContainer != null)
                        {
                            var btn = Instantiate(choiceButtonPrefab, choicesContainer);
                            btn.GetComponentInChildren<TextMeshProUGUI>().text = c.text;
                            btn.GetComponent<Button>().onClick.AddListener(() => OnChoiceSelected(c));
                            btn.gameObject.SetActive(true);
                        }
                    }
                }
            }
            else
            {
                if (choicesContainer != null) choicesContainer.gameObject.SetActive(false);
                if (continueButton != null)
                {
                    continueButton.gameObject.SetActive(true);
                    continueButton.interactable = true;
                    continueButton.onClick.RemoveAllListeners();
                    continueButton.onClick.AddListener(() => { currentLineIndex++; DisplayLine(); });
                }
            }
        }

        private void UpdateSpeakerUI(bool isPlayer, string textContent, bool hasChoices)
        {
            bool hasContent = !string.IsNullOrEmpty(textContent);

            if (isPlayer)
            {
                SetPlayerPanelVisibility(true, true);
                if (npcContainer) npcContainer.SetActive(false);
                if (playerDialogueText) playerDialogueText.text = textContent;
                UpdatePlayerAvatar();
            }
            else
            {
                if (npcContainer) npcContainer.SetActive(true);
                if (npcDialogueText) npcDialogueText.text = textContent;
                UpdateNPCAvatar();

                if (hasChoices)
                {
                    SetPlayerPanelVisibility(true, true);
                    UpdatePlayerAvatar();
                    if (playerDialogueText) playerDialogueText.text = "";
                }
                else
                {
                    SetPlayerPanelVisibility(false, false);
                }
            }
        }

        private void SetPlayerPanelVisibility(bool containerActive, bool contentActive)
        {
            if (playerContainer) playerContainer.SetActive(containerActive);
            if (containerActive)
            {
                if (playerNameText) playerNameText.gameObject.SetActive(contentActive);
                if (playerDialogueText) playerDialogueText.gameObject.SetActive(contentActive);
                if (playerAvatarImage) playerAvatarImage.gameObject.SetActive(contentActive);
            }
        }

        private void UpdatePlayerAvatar()
        {
            if (GameStateManager.Instance)
            {
                var mainPlayer = GameStateManager.Instance.GetMainPlayer();
                if (mainPlayer != null)
                {
                    if (playerNameText) playerNameText.text = mainPlayer.characterName;
                    if (playerAvatarImage != null)
                    {
                        playerAvatarImage.enabled = true;
                        if (mainPlayer.characterData != null)
                            playerAvatarImage.sprite = mainPlayer.characterData.portraitSprite;
                    }
                }
            }
        }

        private void UpdateNPCAvatar()
        {
            string name = currentData.speakerName;
            Sprite sprite = null;
            if (currentData.speaker)
            {
                name = currentData.speaker.characterNameKey;
                sprite = currentData.speaker.portraitSprite;
            }
            if (npcNameText) npcNameText.text = name;
            if (npcAvatarImage) { npcAvatarImage.sprite = sprite; npcAvatarImage.enabled = (sprite != null); }
        }

        private bool CheckChoiceCondition(DialogueChoice c)
        {
            if (string.IsNullOrEmpty(c.requiredQuestID)) return true;
            if (QuestManager.Instance == null) return true;

            // [FIX LỖI 1] Gọi trực tiếp GetQuestByID thay vì GetQuestDatabase
            var quest = QuestManager.Instance.GetQuestByID(c.requiredQuestID);

            if (quest == null) return false; // Không tìm thấy quest -> Ẩn lựa chọn

            QuestState currentState = QuestManager.Instance.GetQuestState(quest);
            bool conditionMet = (currentState == c.requiredState);
            if (c.reverseCondition) return !conditionMet;
            return conditionMet;
        }

        private void OnChoiceSelected(DialogueChoice c)
        {
            ExecuteAction(c.actionOnSelect);
            if (c.closeDialogue) EndDialogue();
            else if (!string.IsNullOrEmpty(c.nextStateID)) { ChangeState(c.nextStateID); DisplayLine(); }
            else { currentLineIndex++; DisplayLine(); }
        }

        private void ExecuteAction(DialogueAction action)
        {
            if (action == null || action.type == DialogueActionType.None) return;
            if (action.type == DialogueActionType.HealParty && GameStateManager.Instance) GameStateManager.Instance.HealPartyFull();

            if (action.type == DialogueActionType.StartQuest && QuestManager.Instance)
            {
                // [FIX LỖI 2] Dùng AcceptQuest (String ID)
                QuestManager.Instance.AcceptQuest(action.parameter);
            }
            if (action.type == DialogueActionType.CompleteQuest && QuestManager.Instance)
            {
                // [FIX LỖI 3] Dùng CompleteQuest (String ID)
                QuestManager.Instance.CompleteQuest(action.parameter);
            }
        }

        public void EndDialogue()
        {
            isDialogueActive = false;
            if (npcContainer != null) npcContainer.SetActive(false);
            if (playerContainer != null) playerContainer.SetActive(false);
            if (continueButton != null) continueButton.gameObject.SetActive(false);
            if (choicesContainer != null) choicesContainer.gameObject.SetActive(false);

            var p = FindObjectOfType<PlayerController>();
            if (p != null) p.EnableMovement();

            if (onDialogueComplete != null) { onDialogueComplete.Invoke(); onDialogueComplete = null; }
        }
    }
}
``````


#### GameInitializer.cs
```csharp
using UnityEngine;
using RebirthWarrior.Character;
using RebirthWarrior.Core;
using System.Collections.Generic;

/// <summary>
/// Script này khởi tạo party MỘT LẦN KHI GAME CHẠY
/// và đảm bảo party này tồn tại xuyên suốt.
/// </summary>
public class GameInitializer : MonoBehaviour
{
    [Header("Party Khởi Đầu")]
    [SerializeField] private List<CharacterData> startingPartyData;

    // --- FIX RACE CONDITION: Chuyển từ Awake sang Start ---
    // Awake dùng để khởi tạo chính nó, Start dùng để gọi Manager khác.
    void Start()
    {
        var gameState = GameStateManager.Instance;
        if (gameState == null)
        {
            Debug.LogError("[GameInitializer] Không tìm thấy GameStateManager! Hãy đảm bảo Scene có chứa GameStateManager.");
            return;
        }

        // Chỉ tạo party nếu danh sách TỔNG (Master Roster) đang rỗng.
        if (gameState.GetMasterRoster().Count == 0)
        {
            Debug.Log("[GameInitializer] Roster rỗng. Đang tạo party khởi đầu...");

            if (startingPartyData != null && startingPartyData.Count > 0)
            {
                CreatePartyFromData(gameState);
            }
            else
            {
                Debug.LogWarning("[GameInitializer] Không có CharacterData. Tạo party mặc định.");
                CreateDefaultParty(gameState);
            }
        }
        else
        {
            Debug.Log("[GameInitializer] Roster đã có dữ liệu. Bỏ qua việc tạo party.");
        }
    }

    private void CreatePartyFromData(GameStateManager gameState)
    {
        foreach (var data in startingPartyData)
        {
            if (data != null)
            {
                CharacterStats member = data.CreateStats(1); // Tạo nhân vật level 1
                gameState.AddCharacterToRoster(member);
            }
        }
    }

    private void CreateDefaultParty(GameStateManager gameState)
    {
        gameState.AddCharacterToRoster(new CharacterStats("hero1_main", "Warrior") { level = 5, baseAttack = 20, baseMaxHP = 150 });
        gameState.AddCharacterToRoster(new CharacterStats("hero2_main", "Mage") { level = 5, baseToxicAttack = 25, baseMaxHP = 90 });
    }
}
``````


#### GameStateManager.cs
```csharp
using RebirthWarrior.Battle;
using RebirthWarrior.Character;
using RebirthWarrior.Dialogue;
using RebirthWarrior.Items;
using RebirthWarrior.SaveLoad;
using RebirthWarrior.Skills;
using System.Collections.Generic;
using System.Linq;
using UnityEngine;

namespace RebirthWarrior.Core
{
    public class GameStateManager : MonoBehaviour
    {
        [Header("Gold & Resources")]
        [SerializeField] private int currentGold = 1000;

        [Header("Party Management")]
        [SerializeField] private int maxBattlePartySize = 7;

        private List<CharacterStats> masterCharacterRoster = new List<CharacterStats>();
        private List<CharacterStats> battleParty = new List<CharacterStats>();

        [Header("Rebirth")]
        public bool isScriptedRebirthBattle = false;
        public bool hasBeenReborn = false;

        [Header("Current Battle Config")]
        public RebirthWarrior.Battle.ScriptedBattleContext currentBattleContext;

        [HideInInspector] public List<CharacterStats> nextEnemies;
        [HideInInspector] public DialogueData battleStartingData;

        public bool isGameActive { get; private set; } = false;
        private static GameStateManager instance;

        public string nextSpawnPointID;
        public static GameStateManager Instance
        {
            get
            {
                if (instance == null)
                {
                    instance = FindObjectOfType<GameStateManager>();
                    if (instance == null) Debug.LogWarning("[GameStateManager] Instance not found.");
                }
                return instance;
            }
        }

        private void Awake()
        {
            if (instance != null && instance != this) { Destroy(gameObject); return; }
            instance = this;
            DontDestroyOnLoad(gameObject);
        }

        // --- GOLD MANAGEMENT ---
        public int GetGold() { return currentGold; }
        public void AddGold(int amount) { if (amount >= 0) currentGold += amount; }
        public bool RemoveGold(int amount) { if (amount < 0 || currentGold < amount) return false; currentGold -= amount; return true; }
        public bool HasEnoughGold(int amount) { return currentGold >= amount; }
        public void SetGold(int amount) { currentGold = Mathf.Max(0, amount); }

        // --- PARTY MANAGEMENT ---

        public CharacterStats GetMainPlayer()
        {
            if (masterCharacterRoster.Count > 0) return masterCharacterRoster[0];
            return null;
        }

        public void ClearAllFollowers()
        {
            if (masterCharacterRoster.Count == 0) return;
            CharacterStats mainPlayer = GetMainPlayer();
            masterCharacterRoster.Clear();
            battleParty.Clear();
            if (mainPlayer != null)
            {
                masterCharacterRoster.Add(mainPlayer);
                battleParty.Add(mainPlayer);
            }
        }

        public List<CharacterStats> GetBattleParty() { return battleParty; }
        public List<CharacterStats> GetMasterRoster() { return masterCharacterRoster; }

        public void AddCharacterToRoster(CharacterStats newCharacter)
        {
            if (newCharacter == null) return;
            if (!masterCharacterRoster.Contains(newCharacter))
            {
                masterCharacterRoster.Add(newCharacter);
                if (battleParty.Count < maxBattlePartySize)
                {
                    AddCharacterToBattleParty(newCharacter);
                }
            }
        }

        public bool AddCharacterToBattleParty(CharacterStats character)
        {
            if (battleParty.Contains(character)) return false;
            if (battleParty.Count >= maxBattlePartySize) return false;

            battleParty.Add(character);
            return true;
        }

        public void RemoveCharacterFromBattleParty(CharacterStats character)
        {
            if (battleParty.Contains(character))
            {
                battleParty.Remove(character);
            }
        }

        public bool IsFollowerRecruited(string characterID)
        {
            if (string.IsNullOrEmpty(characterID)) return false;
            return masterCharacterRoster.Any(c => c.characterID == characterID);
        }

        public List<CharacterStats> GetReserveCharacters()
        {
            return masterCharacterRoster.Where(c => !battleParty.Contains(c)).ToList();
        }

        public int GetPartySize() { return battleParty.Count; }
        public void HealPartyFull() { foreach (var m in battleParty) if (m != null) { m.currentHP = m.maxHP; m.currentStamina = m.maxStamina; } }

        public void AddExpToParty(int exp)
        {
            foreach (var member in battleParty)
            {
                if (member != null && member.isAlive)
                {
                    member.GainExperience(exp);
                }
            }
        }

        public CharacterStats GetActivePet()
        {
            return battleParty.FirstOrDefault(c => c != null && c.characterData != null && c.characterData.type == CharacterType.Pet);
        }

        public void SetActivePet(CharacterStats pet)
        {
            if (pet == null) return;
            AddCharacterToRoster(pet);
            bool added = AddCharacterToBattleParty(pet);
            if (added) Debug.Log($"[GameStateManager] Pet {pet.characterName} đã tham gia đội hình!");
            else Debug.Log($"[GameStateManager] Đội hình đầy! Pet {pet.characterName} ở hàng dự bị.");
        }

        public void LoadFromData(GameSaveData data)
        {
            currentGold = data.gold;
            hasBeenReborn = data.hasBeenReborn;
            masterCharacterRoster.Clear();
            battleParty.Clear();

            foreach (var cData in data.partyMembers)
            {
                string path = $"Data/Characters/{cData.charID}";
                CharacterData asset = Resources.Load<CharacterData>(path);
                if (asset == null) asset = Resources.Load<CharacterData>(cData.charID);

                if (asset != null)
                {
                    CharacterStats newStats = asset.CreateStats(cData.level);
                    newStats.characterName = cData.customName;
                    newStats.currentExp = cData.currentExp;
                    newStats.currentHP = cData.curHP;

                    // MAPPING DATA CŨ -> STATS MỚI
                    newStats.currentStamina = cData.curMP; // MP cũ -> Stamina mới
                    newStats.baseMaxStamina = cData.baseMaxMP;
                    newStats.baseToxicAttack = cData.baseMag; // Magic cũ -> Toxic Attack
                    newStats.baseToxicResist = cData.baseMDef; // MDef cũ -> Toxic Resist

                    newStats.baseAttack = cData.baseAtk;
                    newStats.baseDefense = cData.baseDef;
                    newStats.baseSpeed = cData.baseSpd;
                    newStats.baseAgility = cData.baseAgi;
                    newStats.baseLuck = cData.baseLuck;
                    newStats.baseMaxHP = cData.baseMaxHP;
                    newStats.unspentStatPoints = cData.unspentPoints;

                    newStats.isCustomCharacter = cData.isCustom;
                    newStats.genderIndex = cData.genderIdx;
                    newStats.bodyIndex = cData.bodyIdx;
                    newStats.hairIndex = cData.hairIdx;
                    newStats.eyesIndex = cData.eyesIdx;

                    if (cData.equippedItems != null)
                    {
                        foreach (var eData in cData.equippedItems)
                        {
                            Item item = Resources.Load<Item>($"Items/{eData.itemID}");
                            if (item == null) item = Resources.Load<Item>(eData.itemID);

                            if (item != null)
                            {
                                EquipmentSlot slot = (EquipmentSlot)eData.slotIndex;
                                newStats.EquipItem(item, slot);
                            }
                        }
                    }

                    if (cData.learnedSkillIDs != null)
                    {
                        foreach (string skillName in cData.learnedSkillIDs)
                        {
                            Skill skill = Resources.Load<Skill>($"Skills/{skillName}");
                            if (skill == null) skill = Resources.Load<Skill>(skillName);
                            if (skill != null) newStats.LearnSkill(skill);
                        }
                    }

                    AddCharacterToRoster(newStats);
                }
            }
        }

        public void ClearBattleDialogue()
        {
            battleStartingData = null;
            isScriptedRebirthBattle = false;
        }
    }
}
``````


#### LocalizationManager.cs
```csharp
using System.Collections.Generic;
using UnityEngine;
using System.IO;

namespace RebirthWarrior.Core
{
    public class LocalizationManager : MonoBehaviour
    {
        public static LocalizationManager Instance { get; private set; }

        [Header("Language Settings")]
        [SerializeField] private SystemLanguage defaultLanguage = SystemLanguage.Vietnamese;
        private SystemLanguage currentLanguage;

        private Dictionary<string, string> localizedText;
        private const string LOCALIZATION_PATH = "Data/Localization/";
        private bool isInitialized = false;

        private void Awake()
        {
            if (Instance == null)
            {
                Instance = this;
                DontDestroyOnLoad(gameObject);
                InitializeLocalization();
            }
            else { Destroy(gameObject); }
        }

        private void InitializeLocalization()
        {
            string savedLanguage = PlayerPrefs.GetString("GameLanguage", defaultLanguage.ToString());
            if (System.Enum.TryParse(savedLanguage, out SystemLanguage lang)) currentLanguage = lang;
            else currentLanguage = defaultLanguage;

            LoadLocalizedText(currentLanguage);
        }

        private void LoadLocalizedText(SystemLanguage language)
        {
            localizedText = new Dictionary<string, string>();
            string fileName = GetLanguageFileName(language);

            TextAsset jsonFile = Resources.Load<TextAsset>(LOCALIZATION_PATH + fileName.Replace(".json", ""));

            if (jsonFile != null)
            {
                LocalizationData data = JsonUtility.FromJson<LocalizationData>(jsonFile.text);
                foreach (var item in data.items)
                {
                    if (!localizedText.ContainsKey(item.key))
                        localizedText.Add(item.key, item.value);
                }
                isInitialized = true;
                Debug.Log($"[LocalizationManager] Loaded {language}");
            }
            else
            {
                Debug.LogError($"[LocalizationManager] Cannot find localization file: {fileName}");
            }
        }

        private string GetLanguageFileName(SystemLanguage language)
        {
            switch (language)
            {
                case SystemLanguage.Vietnamese: return "Vietnamese.json";
                case SystemLanguage.English: return "English.json";
                case SystemLanguage.Chinese: return "Chinese.json";
                default: return "English.json";
            }
        }

        // === FIX QUAN TRỌNG TẠI ĐÂY ===
        public string GetLocalizedText(string key)
        {
            // 1. Bảo vệ chống Null Key
            if (string.IsNullOrEmpty(key)) return "";

            if (!isInitialized) return key;

            if (localizedText != null && localizedText.ContainsKey(key))
            {
                return localizedText[key];
            }
            else
            {
                // Debug.LogWarning($"[LocalizationManager] Key not found: {key}");
                return key; // Trả về chính key đó nếu không tìm thấy (Fallback)
            }
        }

        public void ChangeLanguage(SystemLanguage newLanguage)
        {
            if (currentLanguage == newLanguage) return;
            currentLanguage = newLanguage;
            PlayerPrefs.SetString("GameLanguage", currentLanguage.ToString());
            PlayerPrefs.Save();
            LoadLocalizedText(currentLanguage);
            OnLanguageChanged?.Invoke();
        }

        public System.Action OnLanguageChanged;
        public SystemLanguage GetCurrentLanguage() => currentLanguage;
    }

    [System.Serializable] public class LocalizationData { public LocalizationItem[] items; }
    [System.Serializable] public class LocalizationItem { public string key; public string value; }
}
``````


#### SceneEventSystemDestroyer.cs
```csharp
using UnityEngine;
using UnityEngine.EventSystems;

namespace RebirthWarrior.Core
{
    // Gắn script này vào EventSystem của các Scene: Town, World, Battle
    // KHÔNG GẮN vào EventSystem của MainMenu/InventoryUI_Persistent
    public class SceneEventSystemDestroyer : MonoBehaviour
    {
        private void Awake()
        {
            // Tìm xem có EventSystem nào khác đang sống không (Cái DontDestroyOnLoad)
            var systems = FindObjectsOfType<EventSystem>();

            if (systems.Length > 1)
            {
                // Nếu tìm thấy hơn 1 cái, nghĩa là "Sếp tổng" đã đến.
                // Mình (EventSystem local) phải biến mất ngay.
                gameObject.SetActive(false); // Tắt ngay để Unity không báo lỗi
                Destroy(gameObject);
            }
        }
    }
}
``````


#### SingletonEventSystem.cs
```csharp
using UnityEngine;
using UnityEngine.EventSystems;

namespace RebirthWarrior.Core
{
    public class SingletonEventSystem : MonoBehaviour
    {
        public static SingletonEventSystem Instance { get; private set; }

        private void Awake()
        {
            // 1. Kiểm tra Singleton của chính script này
            if (Instance != null && Instance != this)
            {
                // Tắt ngay lập tức để tránh Unity báo lỗi trong Frame này
                gameObject.SetActive(false);
                Destroy(gameObject);
                return;
            }

            // 2. Kiểm tra EventSystem của Unity (Double check)
            // Nếu đã có một EventSystem khác đang chạy (DontDestroyOnLoad từ scene trước)
            if (EventSystem.current != null && EventSystem.current.gameObject != gameObject)
            {
                gameObject.SetActive(false);
                Destroy(gameObject);
                return;
            }

            // 3. Nếu chưa có ai -> Mình là trùm
            Instance = this;
            DontDestroyOnLoad(gameObject);
        }
    }
}
``````



### C4. Dialogue SCripts

#### DialogueActions.cs
```csharp
using UnityEngine;

namespace RebirthWarrior.Dialogue
{
    public enum DialogueActionType
    {
        None,
        StartQuest,     // Giao Quest
        CompleteQuest,  // Trả Quest
        OpenShop,       // Mở Shop
        HealParty,      // Hồi máu (Inn)
        StartBattle     // Đánh nhau
    }

    [System.Serializable]
    public class DialogueAction
    {
        public DialogueActionType type;
        [Tooltip("ID của Quest, Shop, hoặc Enemy")]
        public string parameter;
    }
}
```


#### DialogueData.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Character;
using RebirthWarrior.Quests; // Cần namespace này

namespace RebirthWarrior.Dialogue
{
    [CreateAssetMenu(fileName = "New Dialogue Data", menuName = "Rebirth Warrior/Dialogue/Dialogue Data V2")]
    public class DialogueData : ScriptableObject
    {
        [Header("Speaker Info")]
        public CharacterData speaker;
        public string speakerName;

        [Header("States")]
        public List<DialogueState> states;

        public DialogueState GetState(string stateID)
        {
            return states.Find(s => s.stateID == stateID);
        }
    }

    [System.Serializable]
    public class DialogueState
    {
        public string stateID;
        public List<DialogueLine> lines;
    }

    [System.Serializable]
    public class DialogueLine
    {
        [TextArea(3, 5)] public string text;
        public bool isPlayerSpeaking;

        [Header("Lựa chọn")]
        public List<DialogueChoice> choices;

        [Header("Auto Action")]
        public DialogueAction actionOnShow;
    }

    [System.Serializable]
    public class DialogueChoice
    {
        public string text;
        public string nextStateID;
        public DialogueAction actionOnSelect;
        public bool closeDialogue;

        // === NÂNG CẤP: ĐIỀU KIỆN HIỂN THỊ (VISIBILITY CONDITION) ===
        [Header("Điều kiện hiển thị (Optional)")]
        [Tooltip("Nếu gán Quest vào đây, lựa chọn này chỉ hiện khi Quest đạt trạng thái bên dưới")]
        public string requiredQuestID;
        public QuestState requiredState;

        [Tooltip("Đảo ngược điều kiện? (Ví dụ: Hiện khi Quest CHƯA hoàn thành)")]
        public bool reverseCondition;
    }
}
```


#### DialogueUIInitializer.cs
```csharp
using UnityEngine;
using RebirthWarrior.Core;
using TMPro;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

namespace RebirthWarrior.Dialogue
{
    public class DialogueUIInitializer : MonoBehaviour
    {
        [Header("NPC / BOSS UI")]
        [SerializeField] private GameObject npcContainer;
        [SerializeField] private TextMeshProUGUI npcNameText;
        [SerializeField] private TextMeshProUGUI npcDialogueText;
        [SerializeField] private Image npcAvatarImage;

        [Header("PLAYER UI")]
        [SerializeField] private GameObject playerContainer;
        [SerializeField] private TextMeshProUGUI playerNameText;
        [SerializeField] private TextMeshProUGUI playerDialogueText;
        [SerializeField] private Image playerAvatarImage;

        [Header("Common UI")]
        [SerializeField] private Transform choicesContainer;
        [SerializeField] private GameObject choiceButtonPrefab;
        [SerializeField] private Button continueButton;

        private void OnEnable()
        {
            SceneManager.sceneLoaded += OnSceneLoaded;
            // Gọi ForceSetup ngay khi Object này được bật
            ForceSetup();
        }

        private void OnDisable()
        {
            SceneManager.sceneLoaded -= OnSceneLoaded;
        }

        private void OnSceneLoaded(Scene scene, LoadSceneMode mode)
        {
            ForceSetup();
        }

        private void Start()
        {
            ForceSetup();
        }

        public void ForceSetup()
        {
            // 1. Tự động ẩn các Panel đi khi bắt đầu game (Để Sếp cứ để Active trong Editor cho dễ nhìn)
            if (npcContainer != null) npcContainer.SetActive(false);
            if (playerContainer != null) playerContainer.SetActive(false);
            if (continueButton != null) continueButton.gameObject.SetActive(false);

            // 2. Kết nối với Manager
            if (DialogueManager.Instance != null)
            {
                DialogueManager.Instance.SetupUI(
                    npcContainer, npcNameText, npcDialogueText, npcAvatarImage,
                    playerContainer, playerNameText, playerDialogueText, playerAvatarImage,
                    choicesContainer, choiceButtonPrefab, continueButton
                );
            }
            else
            {
                // Thử lại sau nếu Manager chưa kịp sinh ra
                Invoke(nameof(ForceSetup), 0.1f);
            }
        }
    }
}
```


### C5. Editor Script

#### GameDataImporter.cs
```csharp
using RebirthWarrior.Character;
using RebirthWarrior.Dialogue;
using RebirthWarrior.Items;
using RebirthWarrior.Quests;
using System.Collections.Generic;
using System.IO;
using UnityEditor;
using UnityEngine;

public class GameDataImporter : EditorWindow
{
    // [SỬA LẠI ĐƯỜNG DẪN] Trỏ về Data/CSV thay vì Resources
    private static string CSVPath => Application.dataPath + "/Game/Resources/Data/CSV/";

    [MenuItem("Rebirth Tools/Import All Data")]
    public static void ImportAll()
    {
        ImportItems();
        ImportQuests();
        ImportEnemies();
        AssetDatabase.SaveAssets();
        AssetDatabase.Refresh();
        Debug.Log("✅ IMPORT XONG! Dữ liệu đã được cập nhật vào thư mục Game/Data.");
    }

    // 1. IMPORT ITEMS
    [MenuItem("Rebirth Tools/Import Items (CSV)")]
    public static void ImportItems()
    {
        string path = CSVPath + "Items.csv";
        if (!File.Exists(path)) { Debug.LogError("❌ Không tìm thấy file: " + path); return; }

        string[] lines = File.ReadAllLines(path);
        for (int i = 1; i < lines.Length; i++)
        {
            string[] data = ParseCSVLine(lines[i]);
            if (data.Length < 3) continue;

            string id = data[0];
            // [SỬA ĐƯỜNG DẪN] Lưu vào Assets/Game/Resources/Data/Items
            Item item = CreateOrLoadAsset<Item>("Assets/Game/Resources/Items", id);

            item.itemID = id;
            item.itemName = data[1];
            if (System.Enum.TryParse(data[2], out ItemType type)) item.itemType = type;

            item.buyPrice = int.Parse(data[3]);
            item.attackBonus = int.Parse(data[4]);
            item.defenseBonus = int.Parse(data[5]);
            item.toxicAttackBonus = int.Parse(data[6]);
            item.speedBonus = int.Parse(data[7]);
            item.healAmount = int.Parse(data[8]);
            item.staminaAmount = int.Parse(data[9]);
            item.description = data[10];

            string iconName = data[11];
            if (!string.IsNullOrEmpty(iconName)) item.icon = Resources.Load<Sprite>("Icons/" + iconName); // Icon vẫn nên để Resources hoặc gán tay sau

            if (item.IsEquipment() && data.Length > 12)
            {
                if (System.Enum.TryParse(data[12], out EquipmentSlot slot)) item.equipmentSlot = slot;
            }
            EditorUtility.SetDirty(item);
        }
        Debug.Log("✅ Import Items (Data/Items) Xong!");
    }

    // 2. IMPORT QUESTS
    [MenuItem("Rebirth Tools/Import Quests (CSV)")]
    public static void ImportQuests()
    {
        string path = CSVPath + "Quests.csv";
        if (!File.Exists(path)) return;

        string[] lines = File.ReadAllLines(path);
        for (int i = 1; i < lines.Length; i++)
        {
            string[] data = ParseCSVLine(lines[i]);
            if (data.Length < 3) continue;

            string id = data[0];
            // [SỬA ĐƯỜNG DẪN] Lưu vào Assets/Game/Resources/Data/Quests
            Quest quest = CreateOrLoadAsset<Quest>("Assets/Game/Resources/Data/Quests", id);

            quest.questID = id;
            quest.questName = data[1];
            quest.description = data[2];

            QuestObjective obj = new QuestObjective();
            if (System.Enum.TryParse(data[3], out ObjectiveType type)) obj.type = type;
            obj.objectiveID = data[4];
            obj.requiredAmount = int.Parse(data[5]);
            quest.objectives = new List<QuestObjective> { obj };

            quest.rewardGold = int.Parse(data[6]);
            quest.rewardExp = int.Parse(data[7]);

            EditorUtility.SetDirty(quest);
        }
        Debug.Log("✅ Import Quests (Data/Quests) Xong!");
    }

    // 3. IMPORT ENEMIES
    [MenuItem("Rebirth Tools/Import Enemies (CSV)")]
    public static void ImportEnemies()
    {
        string path = CSVPath + "Enemies.csv";
        if (!File.Exists(path)) return;

        string[] lines = File.ReadAllLines(path);
        for (int i = 1; i < lines.Length; i++)
        {
            string[] data = ParseCSVLine(lines[i]);
            if (data.Length < 3) continue;

            string id = data[0];
            // [SỬA ĐƯỜNG DẪN] Lưu vào Assets/Game/Resources/Data/Characters
            CharacterData charData = CreateOrLoadAsset<CharacterData>("Assets/Game/Resources/Data/Characters", id);

            charData.characterID = id;
            charData.characterNameKey = data[1];
            charData.type = CharacterType.Enemy;
            charData.baseMaxHP = int.Parse(data[2]);
            charData.baseMaxStamina = int.Parse(data[3]);
            charData.baseAttack = int.Parse(data[4]);
            charData.baseDefense = int.Parse(data[5]);
            charData.baseToxicAttack = int.Parse(data[6]);
            charData.baseSpeed = int.Parse(data[7]);
            charData.killExpReward = int.Parse(data[8]);
            charData.killGoldReward = int.Parse(data[9]);

            string spriteName = data[10];
            if (!string.IsNullOrEmpty(spriteName))
            {
                // Sprite thì bắt buộc phải Load từ Resources hoặc gán tay
                charData.characterSprite = Resources.Load<Sprite>("Sprites/Enemies/" + spriteName);
                charData.defaultBattleSprite = charData.characterSprite;
            }
            EditorUtility.SetDirty(charData);
        }
        Debug.Log("✅ Import Enemies (Data/Characters) Xong!");
    }

    private static T CreateOrLoadAsset<T>(string folderPath, string assetName) where T : ScriptableObject
    {
        if (!Directory.Exists(folderPath)) Directory.CreateDirectory(folderPath);
        string fullPath = $"{folderPath}/{assetName}.asset";
        T asset = AssetDatabase.LoadAssetAtPath<T>(fullPath);
        if (asset == null)
        {
            asset = ScriptableObject.CreateInstance<T>();
            AssetDatabase.CreateAsset(asset, fullPath);
        }
        return asset;
    }

    private static string[] ParseCSVLine(string line) => line.Split(',');
}
```


### C6. Inventory Scripts

#### InventoryManager.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using System.Linq;
using RebirthWarrior.Items;
using RebirthWarrior.Character;
using System;
using RebirthWarrior.Core;

namespace RebirthWarrior.Inventory
{
    public class InventoryManager : MonoBehaviour
    {
        [Header("Inventory Settings")]
        [SerializeField] public int inventoryGridSize = 28;
        [SerializeField] public int columns = 7;

        [Header("Starting Items")]
        [SerializeField] private List<Items.Item> startingItems;
        [SerializeField] private List<int> startingQuantities;

        private InventorySlot[] inventory;
        private static InventoryManager instance;
        public event Action<Item, int> OnItemAdded;
        public event System.Action OnInventoryChanged;
        private static bool isShuttingDown = false;

        public static InventoryManager Instance
        {
            get
            {
                if (isShuttingDown) return null;
                if (instance == null) instance = FindObjectOfType<InventoryManager>();
                return instance;
            }
        }
        public void OnApplicationQuit() { isShuttingDown = true; }

        private void Awake()
        {
            if (instance != null && instance != this) { Destroy(gameObject); return; }
            instance = this;
            inventory = new InventorySlot[inventoryGridSize];
            AddStartingItems();
        }

        private void AddStartingItems()
        {
            if (startingItems == null) return;
            for (int i = 0; i < startingItems.Count; i++)
            {
                if (startingItems[i] != null)
                {
                    int quantity = i < startingQuantities.Count ? startingQuantities[i] : 1;
                    AddItem(startingItems[i], quantity);
                }
            }
        }

        public bool IsInventoryFull() { return !inventory.Any(s => s == null); }

        public bool AddItem(Items.Item item, int quantity = 1)
        {
            if (item == null || quantity <= 0) return false;

            // Logic Stack Item
            if (item.maxStack > 1)
            {
                for (int i = 0; i < inventory.Length; i++)
                {
                    if (quantity <= 0) break;
                    if (inventory[i] != null && !inventory[i].isGhost && inventory[i].item == item && inventory[i].quantity < item.maxStack)
                    {
                        int space = item.maxStack - inventory[i].quantity;
                        int add = Mathf.Min(quantity, space);
                        inventory[i].quantity += add;
                        quantity -= add;
                    }
                }
            }

            // Logic Add Item mới vào ô trống
            while (quantity > 0)
            {
                int bestIndex = FindSpaceForItem(item);
                if (bestIndex == -1) { OnInventoryChanged?.Invoke(); return false; }
                int add = Mathf.Min(quantity, item.maxStack);
                AddItemAt(bestIndex, item, add);
                quantity -= add;

                // [FIX ERROR 1] Truyền object 'item' thay vì 'item.itemID'
                if (RebirthWarrior.Quests.QuestManager.Instance != null)
                    RebirthWarrior.Quests.QuestManager.Instance.OnItemCollected(item, add);
            }
            OnInventoryChanged?.Invoke();
            return true;
        }

        public bool TryMoveItem(int fromIndex, int toIndex)
        {
            if (fromIndex == toIndex) return false;
            if (fromIndex < 0 || fromIndex >= inventory.Length) return false;
            if (toIndex < 0 || toIndex >= inventory.Length) return false;

            if (inventory[fromIndex] != null && inventory[fromIndex].isGhost) fromIndex = inventory[fromIndex].anchorIndex;
            if (inventory[toIndex] != null && inventory[toIndex].isGhost) toIndex = inventory[toIndex].anchorIndex;

            if (fromIndex == toIndex) return false;

            InventorySlot slotA = inventory[fromIndex];
            InventorySlot slotB = inventory[toIndex];

            if (slotA == null) return false;

            Item itemA = slotA.item; int qtyA = slotA.quantity;
            Item itemB = (slotB != null) ? slotB.item : null; int qtyB = (slotB != null) ? slotB.quantity : 0;

            ClearItemAt(fromIndex);
            if (slotB != null) ClearItemAt(toIndex);

            if (CheckAvailableSpace(toIndex, itemA.width, itemA.height))
            {
                AddItemAt(toIndex, itemA, qtyA);
                if (itemB != null)
                {
                    if (CheckAvailableSpace(fromIndex, itemB.width, itemB.height))
                    {
                        AddItemAt(fromIndex, itemB, qtyB);
                        OnInventoryChanged?.Invoke();
                        return true;
                    }
                    else
                    {
                        ClearItemAt(toIndex);
                        AddItemAt(fromIndex, itemA, qtyA);
                        AddItemAt(toIndex, itemB, qtyB);
                        return false;
                    }
                }
                else
                {
                    OnInventoryChanged?.Invoke();
                    return true;
                }
            }
            else
            {
                AddItemAt(fromIndex, itemA, qtyA);
                if (itemB != null) AddItemAt(toIndex, itemB, qtyB);
                return false;
            }
        }

        private void AddItemAt(int index, Item item, int quantity)
        {
            inventory[index] = new InventorySlot(item, quantity);
            OccupySlots(index, item.width, item.height);
        }

        private int FindSpaceForItem(Item item)
        {
            for (int i = 0; i < inventory.Length; i++) { if (CheckAvailableSpace(i, item.width, item.height)) return i; }
            return -1;
        }

        private bool CheckAvailableSpace(int index, int width, int height)
        {
            int startX = index % columns; int startY = index / columns;
            if (startX + width > columns) return false;
            if (startY + height > (inventoryGridSize / columns)) return false;

            for (int x = 0; x < width; x++)
            {
                for (int y = 0; y < height; y++)
                {
                    int idx = (startY + y) * columns + (startX + x);
                    if (idx >= inventory.Length || inventory[idx] != null) return false;
                }
            }
            return true;
        }

        private void OccupySlots(int anchor, int w, int h)
        {
            int startX = anchor % columns; int startY = anchor / columns;
            for (int x = 0; x < w; x++)
            {
                for (int y = 0; y < h; y++)
                {
                    if (x == 0 && y == 0) continue;
                    int idx = (startY + y) * columns + (startX + x);
                    inventory[idx] = new InventorySlot(anchor);
                }
            }
        }

        private void ClearItemAt(int index)
        {
            if (inventory[index] == null) return;
            if (inventory[index].isGhost) index = inventory[index].anchorIndex;
            Item item = inventory[index].item;
            if (item == null) { inventory[index] = null; return; }

            int w = item.width; int h = item.height;
            int startX = index % columns; int startY = index / columns;
            for (int x = 0; x < w; x++)
            {
                for (int y = 0; y < h; y++)
                {
                    int idx = (startY + y) * columns + (startX + x);
                    if (idx < inventory.Length) inventory[idx] = null;
                }
            }
        }

        public bool RemoveItem(Items.Item item, int quantity = 1)
        {
            if (item == null) return false;
            if (GetItemQuantity(item) < quantity) return false;
            for (int i = inventory.Length - 1; i >= 0; i--)
            {
                if (quantity <= 0) break;
                if (inventory[i] != null && !inventory[i].isGhost && inventory[i].item == item)
                {
                    if (inventory[i].quantity > quantity) { inventory[i].quantity -= quantity; quantity = 0; }
                    else { quantity -= inventory[i].quantity; ClearItemAt(i); }
                }
            }
            OnInventoryChanged?.Invoke();
            return true;
        }

        public bool HasItem(Items.Item item) { return inventory.Any(s => s != null && !s.isGhost && s.item == item); }
        public int GetItemQuantity(Items.Item item) { return inventory.Where(s => s != null && !s.isGhost && s.item == item).Sum(s => s.quantity); }
        public InventorySlot[] GetAllItems() { return inventory; }

        public bool UseItem(Items.Item item, CharacterStats target)
        {
            if (!HasItem(item)) return false;
            if (item.petToSpawn != null && GameStateManager.Instance)
            {
                GameStateManager.Instance.SetActivePet(item.petToSpawn.CreateStats(1));
                RemoveItem(item, 1); return true;
            }
            if (target != null)
            {
                if (item.healAmount > 0) target.Heal(item.healAmount);
                if (item.staminaAmount > 0) target.RestoreStamina(item.staminaAmount);
                if (item.toxicReduction > 0) target.ReduceToxic(item.toxicReduction);
                RemoveItem(item, 1); return true;
            }
            return false;
        }

        public bool EquipItem(Item item, CharacterStats target)
        {
            if (item == null || !item.IsEquipment()) return false;
            if (!RemoveItem(item, 1)) return false;
            Item old = target.EquipItem(item, item.equipmentSlot);
            if (old != null) AddItem(old, 1);
            OnInventoryChanged?.Invoke();
            return true;
        }
        public bool UnequipItem(EquipmentSlot slot, CharacterStats target)
        {
            Item old = target.UnequipItem(slot);
            if (old == null) return false;
            if (!AddItem(old, 1)) { target.EquipItem(old, slot); return false; }
            OnInventoryChanged?.Invoke();
            return true;
        }
        public void LoadFromData(RebirthWarrior.SaveLoad.GameSaveData data)
        {
            for (int i = 0; i < inventory.Length; i++) inventory[i] = null;
            foreach (var iData in data.inventoryItems)
            {
                Item item = Resources.Load<Item>($"Items/{iData.itemID}");
                if (item == null) item = Resources.Load<Item>(iData.itemID);
                if (item != null) AddItem(item, iData.amount);
            }
            OnInventoryChanged?.Invoke();
        }

        // --- CRAFTING HELPERS ---
        public bool HasIngredients(List<RebirthWarrior.Crafting.Ingredient> ingredients)
        {
            foreach (var ing in ingredients)
            {
                if (GetItemQuantity(ing.item) < ing.amount) return false;
            }
            return true;
        }

        public void ConsumeIngredients(List<RebirthWarrior.Crafting.Ingredient> ingredients)
        {
            foreach (var ing in ingredients)
            {
                RemoveItem(ing.item, ing.amount);
            }
        }
    }
}
```


#### InventorySlot.cs
```csharp
using RebirthWarrior.Items; // Đảm bảo bạn có using này

namespace RebirthWarrior.Inventory
{
    /// <summary>
    /// Định nghĩa một Ô chứa đồ trong Inventory
    /// </summary>
    [System.Serializable]
    public class InventorySlot
    {
        public Item item;     // Vật phẩm chứa trong ô
        public int quantity;  // Số lượng (sẽ là 1 cho trang bị)

        // === [MỚI] HỖ TRỢ MULTI-SLOT ===
        public bool isGhost; // Có phải là ô bị chiếm bởi thằng khác không?
        public int anchorIndex; // Index của ô chủ sở hữu (nếu đây là ghost)

        public InventorySlot(Item item, int quantity)
        {
            this.item = item;
            this.quantity = quantity;
            this.isGhost = false;
            this.anchorIndex = -1;
        }

        // Constructor cho Ghost Slot
        public InventorySlot(int anchorIndex)
        {
            this.item = null;
            this.quantity = 0;
            this.isGhost = true;
            this.anchorIndex = anchorIndex;
        }
    }
}
```


### C7. Item Scripts

#### Item.cs
```csharp
using RebirthWarrior.Character;
using RebirthWarrior.Skills;
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.Items
{
    public enum ItemType { Consumable, Weapon, Armor, KeyItem, Material, Tool }
    public enum AttackRangeType { Melee, Ranged }
    public enum EquipmentSlot { Weapon, Shield, Head, Hands, Feet, Armor, Ring }
    public enum WeaponType { None, Sword, Gun, Bow, Staff }

    [CreateAssetMenu(fileName = "New Item", menuName = "Rebirth Warrior/Items/Item")]
    public class Item : ScriptableObject
    {
        [Header("Basic Info")]
        public string itemID;
        public string itemName = "New Item";
        [TextArea(3, 5)] public string description = "Item description";
        public Sprite icon;

        [Header("Item Type")]
        public ItemType itemType = ItemType.Consumable;

        [Header("Durability")]
        public int maxDurability = 100;
        public int currentDurability = 100;

        [Header("Inventory Grid Size")]
        [Range(1, 10)] public int width = 1;
        [Range(1, 10)] public int height = 1;

        [Header("Shop")]
        public int buyPrice = 100;
        public int sellPrice = 50;

        [Header("Consumable Effects")]
        public int healAmount = 0;
        public int staminaAmount = 0; // Stamina thay MP
        public int toxicReduction = 0;
        public StatusEffect curesStatus = StatusEffect.None;

        [Header("Skill Book")]
        public Skill skillToLearn;
        public List<CharacterClass> requiredClasses = new List<CharacterClass>();

        [Header("Equipment Stats")]
        public EquipmentSlot equipmentSlot = EquipmentSlot.Weapon;
        public int attackBonus = 0;
        public int defenseBonus = 0;
        public int toxicAttackBonus = 0;
        public int toxicResistBonus = 0;
        public int speedBonus = 0;
        public int maxHPBonus = 0;
        public int maxStaminaBonus = 0;

        [Header("Restrictions")]
        public bool usableInBattle = true;
        public bool usableInWorld = true;
        public int maxStack = 99;

        [Header("Pet System")]
        public CharacterData petToSpawn;

        [Header("Battle Config")]
        public WeaponType weaponType;
        public AttackRangeType rangeType = AttackRangeType.Melee;
        public float attackDistance = 1.5f;
        public Sprite weaponSprite;
        public string armorLibraryLabel;

        public bool IsConsumable() { return itemType == ItemType.Consumable; }
        public bool IsEquipment() { return itemType == ItemType.Weapon || itemType == ItemType.Armor; }
        public bool IsTool() { return itemType == ItemType.Tool; }

        public bool CanUseOnCharacter(CharacterStats target)
        {
            if (target == null) return false;
            if (skillToLearn != null)
            {
                if (target.KnowsSkill(skillToLearn)) return false;
                if (requiredClasses.Count > 0 && !requiredClasses.Contains(target.characterData.characterClass)) return false;
            }
            return true;
        }

        // === [FIX LỖI 2] THÊM HÀM NÀY ĐỂ INVENTORY UI GỌI ĐƯỢC ===
        public string GetTypeDisplayName()
        {
            if (itemType == ItemType.Armor) return "Armor";
            if (itemType == ItemType.Weapon) return "Weapon";
            if (itemType == ItemType.Consumable) return "Consumable";
            if (itemType == ItemType.Tool) return "Tool";
            return itemType.ToString();
        }
        // ========================================================

        public string GetEquipmentStats()
        {
            if (!IsEquipment()) return "";
            string stats = "";
            if (attackBonus > 0) stats += $"ATK +{attackBonus}\n";
            if (defenseBonus > 0) stats += $"DEF +{defenseBonus}\n";
            if (toxicAttackBonus > 0) stats += $"TOXIC ATK +{toxicAttackBonus}\n";
            if (toxicResistBonus > 0) stats += $"RESIST +{toxicResistBonus}\n";
            return stats.TrimEnd('\n');
        }

        public string GetConsumableEffects()
        {
            if (!IsConsumable()) return "";
            string effects = "";
            if (healAmount > 0) effects += $"Hồi {healAmount} HP\n";
            if (staminaAmount > 0) effects += $"Hồi {staminaAmount} Stamina\n";
            if (toxicReduction > 0) effects += $"Giảm {toxicReduction} Độc\n";
            return effects.TrimEnd('\n');
        }
    }
}
```



### C8. NPC_System Scripts

#### SocialExchangeProfile.cs
```csharp
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.NPCSystem
{
    [System.Serializable]
    public class DialogueLineSimple
    {
        public bool isInitiator; // True = Người bắt chuyện nói, False = Người nghe nói
        [TextArea] public string text;
        public float duration = 3f;
    }

    [CreateAssetMenu(fileName = "NewSocialExchange", menuName = "Rebirth Warrior/NPC/Social Exchange")]
    public class SocialExchangeProfile : ScriptableObject
    {
        [Header("Điều kiện")]
        [Tooltip("Cuộc hội thoại này chỉ xảy ra nếu người kia có Profile ID này (VD: villager_B)")]
        public string targetProfileID;

        [Header("Nội dung hội thoại")]
        public List<DialogueLineSimple> lines;
    }
}
```


#### ChatBubbleUI.cs
```csharp
using UnityEngine;
using TMPro;
using System.Collections;
using UnityEngine.UI;

namespace RebirthWarrior.UI
{
    public class ChatBubbleUI : MonoBehaviour
    {
        [Header("References")]
        [Tooltip("Kéo đối tượng TextMeshPro vào đây")]
        [SerializeField] private TextMeshProUGUI textComp;

        [Tooltip("Kéo cái GameObject chứa Hình Nền (Image) vào đây")]
        [SerializeField] private GameObject bubbleContainer;

        [Tooltip("Kéo Canvas gốc vào đây (nếu có)")]
        [SerializeField] private Canvas canvas;

        private Transform mainCameraTransform;

        private void Start()
        {
            if (Camera.main != null) mainCameraTransform = Camera.main.transform;

            // Setup Canvas WorldSpace
            if (canvas == null) canvas = GetComponent<Canvas>();
            if (canvas && canvas.renderMode != RenderMode.WorldSpace)
                canvas.renderMode = RenderMode.WorldSpace;

            // Đảm bảo ẩn ngay từ đầu
            Hide();
        }

        private void LateUpdate()
        {
            // Billboard: Luôn quay về phía camera
            if (bubbleContainer.activeSelf && mainCameraTransform != null)
            {
                transform.rotation = mainCameraTransform.rotation;
            }
        }

        public void ShowText(string content, float duration)
        {
            if (bubbleContainer == null || textComp == null) return;

            textComp.text = content;

            // Bật Container lên (Chứa cả ảnh nền và chữ)
            bubbleContainer.SetActive(true);

            // Layout Rebuild (để khung background tự co giãn theo chữ nếu Sếp dùng ContentSizeFitter)
            LayoutRebuilder.ForceRebuildLayoutImmediate(bubbleContainer.GetComponent<RectTransform>());

            StopAllCoroutines();
            StartCoroutine(HideAfterTime(duration));
        }

        public void Hide()
        {
            // Tắt Container là tắt hết (nếu Text là con của Container)
            if (bubbleContainer) bubbleContainer.SetActive(false);
        }

        private IEnumerator HideAfterTime(float time)
        {
            yield return new WaitForSeconds(time);
            Hide();
        }

        // Hàm Validate để Sếp đỡ quên kéo reference
        private void OnValidate()
        {
            if (textComp == null) textComp = GetComponentInChildren<TextMeshProUGUI>();
            // Tự tìm BubbleContainer nếu chưa gán (giả sử nó là con đầu tiên)
            if (bubbleContainer == null && transform.childCount > 0)
                bubbleContainer = transform.GetChild(0).gameObject;
        }
    }
}
```



#### NPCBarkProfile.cs
```csharp
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.NPCSystem
{
    [CreateAssetMenu(fileName = "NewBarkProfile", menuName = "Rebirth Warrior/NPC/Bark Profile")]
    public class NPCBarkProfile : ScriptableObject
    {
        [Header("Cấu hình")]
        public string profileID; // Ví dụ: "villager_poor"

        [Header("Danh sách câu thoại")]
        [TextArea(2, 5)]
        public List<string> sentences; // Có thể nâng cấp thành List<LocalizationKey> sau này

        public string GetRandomSentence()
        {
            if (sentences == null || sentences.Count == 0) return "...";
            return sentences[Random.Range(0, sentences.Count)];
        }

        [Header("Social Settings (Mới)")]
        public string myProfileID; // Ví dụ: "guard_A"
        public List<SocialExchangeProfile> socialExchanges; // Danh sách các cuộc hội thoại có thể xảy ra
    }
}
```



#### NPCMovement.cs
```csharp
using UnityEngine;
using System.Collections;
using System.Collections.Generic;
using RebirthWarrior.World;
using RebirthWarrior.UI;

namespace RebirthWarrior.NPCSystem
{
    public enum PatrolType { Loop, PingPong, OneWay }

    [RequireComponent(typeof(NPC))]
    public class NPCMovement : MonoBehaviour
    {
        [Header("Path Settings")]
        [SerializeField] private PatrolPath patrolPath;
        [SerializeField] private PatrolType patrolType = PatrolType.Loop;

        [Header("Movement Config")]
        [SerializeField] private float moveSpeed = 2f;
        [SerializeField] private float waitTimeAtPoint = 2f;

        [Header("Bark & Social System")]
        [SerializeField] public NPCBarkProfile barkProfile; // Để Public để các NPC khác đọc được
        [SerializeField] private ChatBubbleUI chatBubble;
        [SerializeField] private float minBarkInterval = 5f;
        [SerializeField] private float maxBarkInterval = 15f;

        [Header("Social Config")]
        [SerializeField] private float socialScanRadius = 3f; // Bán kính tìm bạn
        [SerializeField] private float socialCooldown = 30f;  // Gặp nhau xong thì 30s sau mới nói tiếp đỡ nhảm
        [SerializeField] private LayerMask npcLayer;          // Layer của NPC để quét

        [Header("Components")]
        [SerializeField] private Animator animator;

        // Runtime vars
        private List<Transform> waypoints;
        private int currentPointIndex = 0;
        private bool isMovingForward = true;
        private bool isWaiting = false;
        private bool isInteracting = false; // Player tương tác HOẶC đang nói chuyện với NPC khác
        private float barkTimer;
        private float socialTimer; // Đếm ngược cooldown xã hội

        private void Start()
        {
            if (patrolPath != null)
            {
                waypoints = patrolPath.GetWaypoints();
                if (waypoints.Count > 0) transform.position = waypoints[0].position;
            }
            barkTimer = Random.Range(minBarkInterval, maxBarkInterval);
            socialTimer = 5f; // Đợi 5s đầu game rồi mới bắt đầu quét
        }

        private void Update()
        {
            if (isInteracting) return;

            // Đếm ngược cooldown xã hội
            if (socialTimer > 0) socialTimer -= Time.deltaTime;

            HandleMovement();
            HandleBarking();

            // Chỉ quét tìm bạn khi đang KHÔNG cooldown
            if (socialTimer <= 0) HandleSocialScan();
        }

        // ... (Hàm HandleMovement và WaitAtPoint GIỮ NGUYÊN như phiên bản cũ chuẩn nhất) ...
        private void HandleMovement()
        {
            if (waypoints == null || waypoints.Count < 2) { UpdateAnimator(Vector2.zero); return; }
            if (isWaiting) return;

            Transform targetPoint = waypoints[currentPointIndex];
            float distance = Vector2.Distance(transform.position, targetPoint.position);

            if (distance < 0.1f) { UpdateAnimator(Vector2.zero); StartCoroutine(WaitAtPoint()); }
            else
            {
                float step = moveSpeed * Time.deltaTime;
                transform.position = Vector2.MoveTowards(transform.position, targetPoint.position, step);
                Vector2 direction = (targetPoint.position - transform.position).normalized;
                UpdateAnimator(direction);
            }
        }

        private IEnumerator WaitAtPoint()
        {
            isWaiting = true;
            UpdateAnimator(Vector2.zero);
            yield return new WaitForSeconds(waitTimeAtPoint);
            switch (patrolType)
            {
                case PatrolType.Loop: currentPointIndex = (currentPointIndex + 1) % waypoints.Count; break;
                case PatrolType.PingPong:
                    if (isMovingForward) { if (currentPointIndex >= waypoints.Count - 1) { isMovingForward = false; currentPointIndex--; } else currentPointIndex++; }
                    else { if (currentPointIndex <= 0) { isMovingForward = true; currentPointIndex++; } else currentPointIndex--; }
                    break;
                case PatrolType.OneWay: if (currentPointIndex < waypoints.Count - 1) currentPointIndex++; break;
            }
            isWaiting = false;
        }

        private void UpdateAnimator(Vector2 dir)
        {
            if (animator == null) return;
            bool isMoving = dir.sqrMagnitude > 0.01f;
            animator.SetBool("IsMoving", isMoving);
            if (isMoving) { animator.SetFloat("InputX", dir.x); animator.SetFloat("InputY", dir.y); }
        }

        // ========================================================================
        // LOGIC MỚI: HỆ THỐNG XÃ HỘI (SOCIAL SYSTEM)
        // ========================================================================

        private void HandleBarking()
        {
            if (barkProfile == null || chatBubble == null || isInteracting) return;
            barkTimer -= Time.deltaTime;
            if (barkTimer <= 0)
            {
                // Chỉ nói nhảm 1 mình nếu không đang trong thời gian "chờ xã hội"
                string text = barkProfile.GetRandomSentence();
                chatBubble.ShowText(text, 3f);
                barkTimer = Random.Range(minBarkInterval, maxBarkInterval);
            }
        }

        private void HandleSocialScan()
        {
            // Quét xung quanh
            Collider2D[] hits = Physics2D.OverlapCircleAll(transform.position, socialScanRadius, npcLayer);

            foreach (var hit in hits)
            {
                if (hit.gameObject == gameObject) continue; // Bỏ qua chính mình

                NPCMovement otherNPC = hit.GetComponent<NPCMovement>();
                // === THÊM DÒNG NÀY ĐỂ SOI ===
                if (otherNPC != null)
                {
                    Debug.Log($"[Social] Tìm thấy {otherNPC.name}. ID của nó là: '{otherNPC.barkProfile.myProfileID}'. ID mình cần là: 'merchant'");
                }
                // ============================
                if (otherNPC != null && !otherNPC.isInteracting && otherNPC.barkProfile != null)
                {
                    // Kiểm tra xem mình có kịch bản nào nói chuyện với thằng này không
                    var exchange = GetMatchingExchange(otherNPC.barkProfile.myProfileID);

                    if (exchange != null)
                    {
                        // BẮT ĐẦU HỘI THOẠI!
                        StartCoroutine(ProcessSocialDialogue(exchange, otherNPC));
                        return; // Chỉ nói với 1 người thôi
                    }
                }
            }
        }

        private SocialExchangeProfile GetMatchingExchange(string otherID)
        {
            if (barkProfile == null || barkProfile.socialExchanges == null) return null;
            foreach (var ex in barkProfile.socialExchanges)
            {
                if (ex.targetProfileID == otherID) return ex;
            }
            return null;
        }

        // Coroutine điều phối hội thoại giữa 2 NPC
        private IEnumerator ProcessSocialDialogue(SocialExchangeProfile exchange, NPCMovement partner)
        {
            // 1. Dừng cả 2 lại (Gọi hàm PauseForSocial đã sửa bên dưới)
            this.PauseForSocial(partner.transform);
            partner.PauseForSocial(this.transform);

            // 2. Chạy kịch bản
            foreach (var line in exchange.lines)
            {
                if (line.isInitiator)
                {
                    // Mình nói
                    if (this.chatBubble) this.chatBubble.ShowText(line.text, line.duration);
                }
                else
                {
                    // Bạn nói
                    if (partner.chatBubble) partner.chatBubble.ShowText(line.text, line.duration);
                }

                // Chờ người này nói xong mới tới người kia
                yield return new WaitForSeconds(line.duration + 0.5f);
            }

            // 3. Kết thúc -> Đi tiếp
            this.ResumeFromSocial();
            partner.ResumeFromSocial();
        }

        // === [FIX QUAN TRỌNG TẠI ĐÂY] ===
        public void PauseForSocial(Transform target)
        {
            isInteracting = true;

            // [ĐÃ XÓA] StopAllCoroutines(); 
            // TUYỆT ĐỐI KHÔNG GỌI StopAllCoroutines() Ở ĐÂY
            // Vì nó sẽ giết chết luôn cái Coroutine hội thoại đang chạy trên người NPC này.

            if (chatBubble) chatBubble.Hide(); // Tắt bark cũ nếu có

            // Quay mặt về phía đối phương
            if (target != null && animator != null)
            {
                Vector2 dir = (target.position - transform.position).normalized;
                animator.SetFloat("InputX", dir.x);
                animator.SetFloat("InputY", dir.y);
                animator.SetBool("IsMoving", false);
            }
        }

        public void ResumeFromSocial()
        {
            isInteracting = false;
            socialTimer = socialCooldown; // Set cooldown để không nói lại ngay
            isWaiting = false; // Reset để Update tự kích hoạt đi lại
        }

        // --- Hàm cũ cho Player Interact (Giữ nguyên) ---
        public void PauseMovement(Transform playerTransform)
        {
            isInteracting = true;
            StopAllCoroutines();
            isWaiting = false;
            if (chatBubble) chatBubble.Hide();
            if (playerTransform != null && animator != null)
            {
                Vector2 dir = (playerTransform.position - transform.position).normalized;
                animator.SetFloat("InputX", dir.x);
                animator.SetFloat("InputY", dir.y);
                animator.SetBool("IsMoving", false);
            }
        }

        public void ResumeMovement()
        {
            isInteracting = false;
            // Cho phép Update chạy lại
        }

        private void OnDrawGizmosSelected()
        {
            Gizmos.color = Color.cyan;
            Gizmos.DrawWireSphere(transform.position, socialScanRadius);
        }
    }
}
```



#### PatrolPath.cs
```csharp
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.NPCSystem
{
    public class PatrolPath : MonoBehaviour
    {
        [Header("Visual Debug")]
        public Color pathColor = Color.yellow;
        public float pointRadius = 0.2f;

        // Tự động lấy các child làm điểm mốc
        public List<Transform> GetWaypoints()
        {
            List<Transform> points = new List<Transform>();
            foreach (Transform child in transform)
            {
                if (child != transform) points.Add(child);
            }
            return points;
        }

        private void OnDrawGizmos()
        {
            Gizmos.color = pathColor;
            List<Transform> points = GetWaypoints();

            if (points.Count < 2) return;

            for (int i = 0; i < points.Count; i++)
            {
                Vector3 current = points[i].position;
                Vector3 next = points[(i + 1) % points.Count].position; // Nối vòng tròn

                Gizmos.DrawSphere(current, pointRadius);
                Gizmos.DrawLine(current, next);
            }
        }
    }
}
```



### C8. Quest Scripts

#### Quest.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Items;
using RebirthWarrior.Character;

namespace RebirthWarrior.Quests
{
    [CreateAssetMenu(fileName = "New Quest", menuName = "Rebirth Warrior/Quest v12")]
    public class Quest : ScriptableObject
    {
        [Header("Info")]
        public string questID;
        public string questName; // Tên hiển thị
        public string titleKey;  // Key Localization (Hỗ trợ script cũ)
        [TextArea(3, 5)]
        public string description;

        [Header("Prerequisites (Điều kiện nhận)")] // <-- Đã thêm lại
        public int requiredLevel;
        public List<Quest> prerequisiteQuests;
        public List<CharacterData> requiredFollowers;

        [Header("Repetition (Lặp lại)")] // <-- Đã thêm lại
        public bool isRepeatable;
        public int maxRepeats;

        [Header("State (Runtime)")]
        public QuestState state;
        public bool isCompleted;

        [Header("Objectives")]
        public List<QuestObjective> objectives;

        [Header("Rewards")]
        public int rewardGold;
        public int rewardExp;
        public List<Item> rewardItems;
        public CharacterData rewardFollower;
    }

    public enum QuestState { NotStarted, Active, ReadyToComplete, Completed, Failed }
}
```


#### QuestData.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Items;

namespace RebirthWarrior.Quests
{
    [CreateAssetMenu(fileName = "New Quest", menuName = "Rebirth Warrior/Quest Data")]
    public class QuestData : ScriptableObject
    {
        [Header("Quest Info")]
        public string questID;
        public string title;
        [TextArea(3, 5)] public string description;

        [Header("Objectives")]
        public List<QuestObjective> objectives;

        [Header("Rewards")]
        public int goldReward;
        public int expReward;
        public List<Item> itemRewards;

        [Header("Quest Chain")]
        [Tooltip("Quest tiếp theo sẽ tự động mở khi làm xong quest này")]
        public QuestData nextQuest;

        [Tooltip("Điều kiện để nhận quest này (Quest trước đó phải xong)")]
        public QuestData prerequisiteQuest;

        public QuestData CreateRuntimeCopy()
        {
            QuestData copy = Instantiate(this);
            copy.questID = this.questID;
            return copy;
        }
    }
}
```



#### QuestLocationDatabase.cs
```csharp
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.Quests
{
    [CreateAssetMenu(fileName = "QuestLocationDB", menuName = "Rebirth Warrior/Quest/Location Database")]
    public class QuestLocationDatabase : ScriptableObject
    {
        [Header("Target Locations")]
        public List<QuestLocationData> locations;

        [Header("Scene Connections")]
        public List<SceneConnectionData> portals;

        public QuestLocationData GetLocationByID(string targetID)
        {
            return locations.Find(x => x.targetID == targetID);
        }

        // --- HÀM TÌM CỔNG (ĐỂ NAVIGATOR DÙNG) ---
        public Vector2 GetPortalPosition(string fromScene, string toScene)
        {
            // Tìm trong danh sách Portals xem có đường đi từ A -> B không
            foreach (var portal in portals)
            {
                if (portal.currentScene == fromScene && portal.targetScene == toScene)
                {
                    return portal.portalPosition;
                }
            }
            return Vector2.zero; // Không tìm thấy
        }
    }

    [System.Serializable]
    public class QuestLocationData
    {
        public string targetID;
        public string sceneName;
        public Vector2 position;
    }

    [System.Serializable]
    public class SceneConnectionData
    {
        public string currentScene;   // Từ đâu
        public string targetScene;    // Đến đâu
        public Vector2 portalPosition; // Vị trí cổng
    }
}
```



#### QuestManager.cs
```csharp
using UnityEngine;
using System.Collections;
using System.Collections.Generic;
using RebirthWarrior.Core;
using RebirthWarrior.Inventory;
using RebirthWarrior.Items;
using RebirthWarrior.SaveLoad;

#if UNITY_EDITOR
using UnityEditor; // Chỉ dùng trong Editor để tự tìm file
#endif

namespace RebirthWarrior.Quests
{
    public class QuestManager : MonoBehaviour
    {
        public static QuestManager Instance { get; private set; }

        [Header("Quest List")]
        [Tooltip("Danh sách này sẽ tự động được điền khi chạy trong Editor")]
        [SerializeField] private List<Quest> allQuests = new List<Quest>();

        private Dictionary<string, Quest> questMap = new Dictionary<string, Quest>();
        private Dictionary<string, QuestStatus> questLog = new Dictionary<string, QuestStatus>();
        private Dictionary<string, int> questRepeatCounts = new Dictionary<string, int>();

        public System.Action<Quest> OnQuestStarted;
        public System.Action<Quest> OnQuestCompleted;
        public System.Action<Quest, QuestObjective, int> OnObjectiveProgress;

        private void Awake()
        {
            if (Instance == null) { Instance = this; DontDestroyOnLoad(gameObject); }
            else Destroy(gameObject);

            InitializeQuestDatabase();
        }

        private void Start()
        {
            StartCoroutine(SubscribeToEvents());
        }

        // --- TỰ ĐỘNG LOAD QUEST TỪ THƯ MỤC DATA ---
        private void InitializeQuestDatabase()
        {
            // Nếu list trống, thử tự động tìm trong Editor
            if (allQuests == null || allQuests.Count == 0)
            {
#if UNITY_EDITOR
                Debug.Log("[QuestManager] Đang tìm Quest trong thư mục Assets/Game/Resources/Data/Quests...");
                string[] guids = AssetDatabase.FindAssets("t:Quest", new[] { "Assets/Game/Resources/Data/Quests" });
                allQuests = new List<Quest>();
                foreach (string guid in guids)
                {
                    string path = AssetDatabase.GUIDToAssetPath(guid);
                    Quest q = AssetDatabase.LoadAssetAtPath<Quest>(path);
                    if (q != null) allQuests.Add(q);
                }
#endif
            }

            // Map vào Dictionary để tra cứu nhanh
            questMap.Clear();
            foreach (var q in allQuests)
            {
                if (q != null && !questMap.ContainsKey(q.questID))
                {
                    questMap.Add(q.questID, q);
                }
            }
            Debug.Log($"[QuestManager] Đã load {questMap.Count} nhiệm vụ từ hệ thống.");
        }

        // ... (CÁC PHẦN DƯỚI GIỮ NGUYÊN NHƯ CŨ) ...
        public Quest GetQuestByID(string id)
        {
            if (questMap.ContainsKey(id)) return questMap[id];
            return null;
        }

        public QuestStatus GetQuestStatus(string questID)
        {
            if (questLog.ContainsKey(questID)) return questLog[questID];
            return null;
        }

        private IEnumerator SubscribeToEvents()
        {
            yield return null;
            if (InventoryManager.Instance) InventoryManager.Instance.OnItemAdded += OnItemCollected;
        }

        public void AcceptQuest(string questID)
        {
            Quest quest = GetQuestByID(questID);
            if (quest != null) StartQuest(quest);
        }

        public void StartQuest(Quest quest)
        {
            if (GetQuestState(quest) != QuestState.NotStarted) return;

            QuestStatus newStatus = new QuestStatus(quest);
            questLog[quest.questID] = newStatus;

            Debug.Log($"[QuestManager] Nhận nhiệm vụ: {quest.questName}");
            OnQuestStarted?.Invoke(quest);

            CheckQuestObjectives(quest, newStatus);
        }

        public void CheckQuestObjectives(Quest quest, QuestStatus status)
        {
            if (status.state != QuestState.Active) return;
            bool allCompleted = true;

            foreach (var obj in quest.objectives)
            {
                int current = 0;
                switch (obj.type)
                {
                    case ObjectiveType.Fetch:
                        if (InventoryManager.Instance && obj.itemData != null)
                            current = InventoryManager.Instance.GetItemQuantity(obj.itemData);
                        break;
                    default:
                        if (status.objectiveProgress.ContainsKey(obj.targetID))
                            current = status.objectiveProgress[obj.targetID];
                        break;
                }

                status.objectiveProgress[obj.targetID] = current;
                obj.currentProgress = current;

                if (current < obj.requiredAmount) allCompleted = false;
            }

            if (allCompleted)
            {
                status.state = QuestState.ReadyToComplete;
            }
        }

        public void CompleteQuest(string questID)
        {
            Quest quest = GetQuestByID(questID);
            if (quest == null) return;

            QuestState state = GetQuestState(quest);
            if (state == QuestState.ReadyToComplete)
            {
                foreach (var obj in quest.objectives)
                {
                    if (obj.type == ObjectiveType.Fetch && obj.itemData != null)
                    {
                        if (InventoryManager.Instance)
                            InventoryManager.Instance.RemoveItem(obj.itemData, obj.requiredAmount);
                    }
                }

                if (GameStateManager.Instance)
                {
                    GameStateManager.Instance.AddGold(quest.rewardGold);
                    GameStateManager.Instance.AddExpToParty(quest.rewardExp);
                }
                if (InventoryManager.Instance && quest.rewardItems != null)
                {
                    foreach (var item in quest.rewardItems)
                        if (item != null) InventoryManager.Instance.AddItem(item, 1);
                }

                questLog[quest.questID].state = QuestState.Completed;
                if (questRepeatCounts.ContainsKey(quest.questID)) questRepeatCounts[quest.questID]++;
                else questRepeatCounts[quest.questID] = 1;

                OnQuestCompleted?.Invoke(quest);
            }
        }

        public void OnItemCollected(Item item, int quantity) => UpdateObjectiveProgress(ObjectiveType.Fetch, item.itemID, quantity);
        public void OnEnemyKilled(string enemyID) => UpdateObjectiveProgress(ObjectiveType.Kill, enemyID, 1);
        public void OnTalkToNPC(string npcID) => UpdateObjectiveProgress(ObjectiveType.TalkTo, npcID, 1);
        public void OnLocationReached(string locationID) => UpdateObjectiveProgress(ObjectiveType.GoTo, locationID, 1);

        private void UpdateObjectiveProgress(ObjectiveType type, string targetID, int amountToAdd)
        {
            foreach (var kvp in questLog)
            {
                QuestStatus status = kvp.Value;
                if (status.state != QuestState.Active) continue;
                Quest quest = GetQuestByID(status.questID);
                if (quest == null) continue;

                bool questUpdated = false;
                foreach (var obj in quest.objectives)
                {
                    string objTarget = obj.targetID;
                    if (obj.type == ObjectiveType.Fetch && obj.itemData != null) objTarget = obj.itemData.itemID;

                    if (obj.type == type && objTarget == targetID)
                    {
                        if (!status.objectiveProgress.ContainsKey(obj.targetID)) status.objectiveProgress[obj.targetID] = 0;
                        if (type == ObjectiveType.Fetch && InventoryManager.Instance)
                            status.objectiveProgress[obj.targetID] = InventoryManager.Instance.GetItemQuantity(obj.itemData);
                        else
                            status.objectiveProgress[obj.targetID] += amountToAdd;

                        if (status.objectiveProgress[obj.targetID] > obj.requiredAmount)
                            status.objectiveProgress[obj.targetID] = obj.requiredAmount;

                        questUpdated = true;
                        OnObjectiveProgress?.Invoke(quest, obj, status.objectiveProgress[obj.targetID]);
                    }
                }
                if (questUpdated) CheckQuestObjectives(quest, status);
            }
        }

        public QuestState GetQuestState(Quest quest)
        {
            if (quest == null) return QuestState.NotStarted;
            if (questLog.ContainsKey(quest.questID)) return questLog[quest.questID].state;
            return QuestState.NotStarted;
        }

        public bool CanOfferQuest(Quest quest)
        {
            if (GetQuestState(quest) != QuestState.NotStarted) return false;
            if (quest.prerequisiteQuests != null)
                foreach (var pre in quest.prerequisiteQuests)
                    if (GetQuestState(pre) != QuestState.Completed) return false;
            return true;
        }

        public bool IsQuestActive(string questID)
        {
            if (!questLog.ContainsKey(questID)) return false;
            return questLog[questID].state == QuestState.Active || questLog[questID].state == QuestState.ReadyToComplete;
        }

        public List<Quest> GetActiveQuests()
        {
            List<Quest> list = new List<Quest>();
            foreach (var kvp in questLog)
            {
                if (kvp.Value.state == QuestState.Active || kvp.Value.state == QuestState.ReadyToComplete)
                {
                    var q = GetQuestByID(kvp.Key);
                    if (q) list.Add(q);
                }
            }
            return list;
        }

        public List<Quest> GetCompletedQuests()
        {
            List<Quest> list = new List<Quest>();
            foreach (var kvp in questLog)
            {
                if (kvp.Value.state == QuestState.Completed)
                {
                    var q = GetQuestByID(kvp.Key);
                    if (q) list.Add(q);
                }
            }
            return list;
        }

        public void LoadFromData(GameSaveData data)
        {
            questLog.Clear();
            questRepeatCounts.Clear();
            InitializeQuestDatabase();

            if (data.activeQuests != null)
            {
                foreach (var qData in data.activeQuests)
                {
                    Quest q = GetQuestByID(qData.questID);
                    if (q != null)
                    {
                        QuestStatus status = new QuestStatus(q);
                        foreach (var progressStr in qData.objectivesProgress)
                        {
                            var parts = progressStr.Split(':');
                            if (parts.Length == 2) status.objectiveProgress[parts[0]] = int.Parse(parts[1]);
                        }
                        questLog[q.questID] = status;
                        CheckQuestObjectives(q, status);
                    }
                }
            }

            if (data.completedQuests != null)
            {
                foreach (string qID in data.completedQuests)
                {
                    Quest q = GetQuestByID(qID);
                    if (q != null)
                    {
                        QuestStatus status = new QuestStatus(q);
                        status.state = QuestState.Completed;
                        questLog[qID] = status;
                        questRepeatCounts[qID] = 1;
                    }
                }
            }
        }
    }

    [System.Serializable]
    public class QuestStatus
    {
        public string questID;
        public QuestState state;
        public Dictionary<string, int> objectiveProgress = new Dictionary<string, int>();

        public QuestStatus(Quest quest)
        {
            this.questID = quest.questID;
            this.state = QuestState.Active;
            this.objectiveProgress = new Dictionary<string, int>();

            if (quest.objectives != null)
            {
                foreach (var obj in quest.objectives)
                {
                    if (obj != null) objectiveProgress[obj.targetID] = 0;
                }
            }
        }
        public QuestStatus() { }
    }
}
```



#### QuestNavigator.cs
```csharp
using UnityEngine;
using UnityEngine.SceneManagement;
using RebirthWarrior.World;

namespace RebirthWarrior.Quests
{
    public class QuestNavigator : MonoBehaviour
    {
        // ... (Các biến Singleton, Data giữ nguyên) ...
        public static QuestNavigator Instance { get; private set; }
        [SerializeField] private QuestLocationDatabase locationDB;

        [Header("Visuals")]
        [SerializeField] private GameObject directionArrow;
        [SerializeField] private float orbitRadius = 1.5f;

        // [MỚI] Biến để chỉnh góc xoay thủ công nếu mũi tên bị lệch
        // Nếu Sprite của bạn hướng sang PHẢI -> Để 0
        // Nếu Sprite hướng lên TRÊN -> Để -90
        [SerializeField] private float rotationOffset = 0f;

        private Transform playerTransform;
        private Vector2 currentTargetPos;
        private bool isTracking = false;
        private string currentTargetID_Cache;

        // ... (Awake, Start, OnEnable... GIỮ NGUYÊN) ...
        private void Awake() { if (Instance == null) { Instance = this; DontDestroyOnLoad(gameObject); } else { Destroy(gameObject); } }
        private void Start()
        {
            if (directionArrow)
            {
                if (directionArrow.scene.rootCount == 0) directionArrow = Instantiate(directionArrow, transform);
                directionArrow.SetActive(false);
                var sr = directionArrow.GetComponent<SpriteRenderer>();
                if (sr) { sr.sortingLayerName = "UI"; sr.sortingOrder = 100; }
            }
        }
        private void OnEnable() => SceneManager.sceneLoaded += OnSceneLoaded;
        private void OnDisable() => SceneManager.sceneLoaded -= OnSceneLoaded;
        private void OnSceneLoaded(Scene scene, LoadSceneMode mode) { if (!string.IsNullOrEmpty(currentTargetID_Cache)) StartTracking(currentTargetID_Cache); }

        private void Update()
        {
            if (!isTracking) return;
            if (playerTransform == null)
            {
                var player = FindObjectOfType<PlayerController>();
                if (player != null) playerTransform = player.transform;
                else return;
            }
            UpdateArrowPosition();
        }

        // ... (Hàm StartTracking, StopTracking, EnableArrow GIỮ NGUYÊN) ...
        public void StartTracking(string targetID)
        {
            if (locationDB == null) return;
            var targetData = locationDB.GetLocationByID(targetID);
            if (targetData == null) { StopTracking(); return; }

            currentTargetID_Cache = targetID;
            string currentScene = SceneManager.GetActiveScene().name;
            string targetScene = targetData.sceneName;

            if (currentScene == targetScene)
            {
                currentTargetPos = targetData.position;
                EnableArrow(true);
            }
            else
            {
                Vector2 portalPos = locationDB.GetPortalPosition(currentScene, targetScene);
                if (portalPos != Vector2.zero)
                {
                    currentTargetPos = portalPos;
                    EnableArrow(true);
                }
                else
                {
                    StopTracking();
                }
            }
        }

        public void StopTracking() { isTracking = false; currentTargetID_Cache = ""; if (directionArrow) directionArrow.SetActive(false); }
        private void EnableArrow(bool enable) { isTracking = enable; if (directionArrow) directionArrow.SetActive(enable); }

        // --- [HÀM QUAN TRỌNG ĐÃ SỬA] ---
        private void UpdateArrowPosition()
        {
            if (directionArrow == null || playerTransform == null) return;

            Vector2 playerPos = playerTransform.position;

            // Tính hướng từ Player đến Mục tiêu
            Vector2 direction = (currentTargetPos - playerPos).normalized;

            // Atan2 trả về góc tính từ trục X dương (Hướng phải)
            float angle = Mathf.Atan2(direction.y, direction.x) * Mathf.Rad2Deg;

            // 1. Cập nhật vị trí xoay quanh nhân vật
            Vector3 finalPos = playerPos + (direction * orbitRadius);
            finalPos.z = -5f; // Nổi lên trên map
            directionArrow.transform.position = finalPos;

            // 2. Xoay mũi tên (Cộng thêm rotationOffset để bạn tùy chỉnh)
            // Vì Sprite của bạn hướng PHẢI, nên để offset mặc định là 0 là đúng.
            directionArrow.transform.rotation = Quaternion.Euler(0, 0, angle + rotationOffset);
        }
    }
}
```


#### QuestObjective.cs
```csharp
using UnityEngine;
using RebirthWarrior.Items;

namespace RebirthWarrior.Quests
{
    // Giữ nguyên ObjectiveType cho hệ thống cũ
    public enum ObjectiveType
    {
        Kill,
        Fetch,
        TalkTo,
        GoTo
    }

    [System.Serializable]
    public class QuestObjective
    {
        public string description;
        public string objectiveNameKey;

        // ID của mục tiêu
        public string objectiveID;

        // Alias 'targetID' cho Importer
        public string targetID
        {
            get { return objectiveID; }
            set { objectiveID = value; }
        }

        public ObjectiveType type;

        [Tooltip("Item cần thu thập (Nếu là Fetch Quest)")]
        public Item itemData;

        public int requiredAmount;

        // Alias cho UI
        public int requireProgress { get { return requiredAmount; } set { requiredAmount = value; } }

        public int currentAmount;
        public int currentProgress { get { return currentAmount; } set { currentAmount = value; } }

        public bool isCompleted;
    }
}
```


### C9. REBIRTH Scripts

#### RebirthManager.cs
```csharp
using UnityEngine;
using RebirthWarrior.Core;
using RebirthWarrior.Character;
using UnityEngine.SceneManagement;

namespace RebirthWarrior.Rebirth
{
    public class RebirthManager : MonoBehaviour
    {
        public static RebirthManager Instance { get; private set; }

        [Header("Rebirth Settings")]
        [SerializeField] private CharacterData startingClassData;
        [Tooltip("Map 2060 sẽ load sau khi trọng sinh")]
        [SerializeField] private string sceneAfterRebirth = "Map_HCMC_2060";

        private void Awake()
        {
            if (Instance == null) { Instance = this; }
            else { Destroy(gameObject); }
        }

        public void PerformTheRebirth()
        {
            Debug.Log("[RebirthManager] Bắt đầu quy trình Trọng Sinh...");

            var gameState = GameStateManager.Instance;
            if (gameState == null) return;

            CharacterStats mainPlayer = gameState.GetMainPlayer();
            if (mainPlayer != null && startingClassData != null)
            {
                // 1. Reset Stats
                mainPlayer.ApplyRebirth(startingClassData);

                // 2. --- QUAN TRỌNG: Gán CharacterData mới để BattleManager biết Prefab nào mà spawn ---
                mainPlayer.characterData = startingClassData;

                // 3. Cộng điểm tiềm năng
                mainPlayer.unspentStatPoints = 20;

                Debug.Log($"[RebirthManager] Đã chuyển sinh thành công class: {startingClassData.characterNameKey}");
            }
            else
            {
                Debug.LogError("[RebirthManager] LỖI: Không tìm thấy Main Player hoặc chưa gán Starting Class Data!");
            }

            // 4. Xóa Followers
            gameState.ClearAllFollowers();
            gameState.hasBeenReborn = true;

            // 5. Load Map
            Debug.Log($"[RebirthManager] Đang chuyển đến {sceneAfterRebirth}...");
            SceneManager.LoadScene(sceneAfterRebirth);
        }
    }
}
```


#### TutorialRebirthTrigger.cs
```csharp
using UnityEngine;
using RebirthWarrior.Core;
using RebirthWarrior.UI;
using RebirthWarrior.Dialogue;
using System.Collections;

namespace RebirthWarrior.World
{
    public class TutorialRebirthTrigger : MonoBehaviour
    {
        [Header("Dialogue Giới Thiệu")]
        [SerializeField] private DialogueData rebirthIntroDialogue;

        private const string TUTORIAL_DONE_KEY = "Tutorial_Rebirth_Completed";

        private IEnumerator Start()
        {
            // CHECK 1: Chỉ chạy nếu đã Reborn (từ RebirthManager)
            if (GameStateManager.Instance == null || !GameStateManager.Instance.hasBeenReborn)
            {
                yield break;
            }

            // CHECK 2: Kiểm tra xem đã chạy Tutorial này bao giờ chưa (Fix lỗi lặp lại khi quay lại map)
            if (PlayerPrefs.GetInt(TUTORIAL_DONE_KEY, 0) == 1)
            {
                yield break;
            }

            // --- BẮT ĐẦU TUTORIAL ---

            // 1. Đợi màn hình load xong và ổn định
            yield return new WaitForSeconds(1f);

            // 2. Chạy Dialogue dẫn truyện
            if (rebirthIntroDialogue != null && DialogueManager.Instance != null)
            {
                DialogueManager.Instance.StartDialogue(rebirthIntroDialogue);

                // Đợi cho đến khi Dialogue đóng hẳn
                while (DialogueManager.Instance.IsDialogueActive())
                {
                    yield return null;
                }
            }

            // 3. Đánh dấu đã xong Tutorial NGAY LẬP TỨC để không lặp lại
            PlayerPrefs.SetInt(TUTORIAL_DONE_KEY, 1);
            PlayerPrefs.Save();

            // 4. Mở bảng Stats (Fix lỗi UI không hiện & Kẹt nhân vật)
            Debug.Log("[Tutorial] Mở bảng Stats...");

            if (InventoryUI.Instance != null)
            {
                // Mở Inventory tổng trước
                InventoryUI.Instance.OpenInventory();

                // --- FIX: Đợi 0.2s để UI Canvas cập nhật layout ---
                yield return new WaitForSeconds(0.2f);

                // Mở tab Stats
                InventoryUI.Instance.OpenStatsPanel();
            }
            else
            {
                Debug.LogError("[Tutorial] Không tìm thấy InventoryUI!");
            }

            // 5. --- QUAN TRỌNG: MỞ KHÓA DI CHUYỂN ---
            // Đề phòng trường hợp Dialogue tắt xong nhưng chưa trả lại quyền điều khiển
            if (TownManager.Instance != null && TownManager.Instance.player != null)
            {
                TownManager.Instance.player.SetControlEnabled(true);
            }
        }
    }
}
```


### C10. SaveLoad Scripts

#### GameSaveData.cs
```csharp
using System.Collections.Generic;

namespace RebirthWarrior.SaveLoad
{
    [System.Serializable]
    public class GameSaveData
    {
        // ... (Giữ nguyên các biến chung: saveDate, gold, locationName...)
        public string saveDate;
        public string locationName;
        public int gold;
        public string playTime;
        public string currentScene;
        public float posX, posY;
        public float worldReturnX, worldReturnY;
        public string playerName;
        public int playerLevel;
        public bool hasBeenReborn;

        public List<CharSaveData> partyMembers = new List<CharSaveData>();
        public List<string> completedQuests = new List<string>();
        public List<QuestSaveData> activeQuests = new List<QuestSaveData>();
        public List<ItemSaveData> inventoryItems = new List<ItemSaveData>();
    }

    [System.Serializable]
    public class CharSaveData
    {
        public string charID;
        public string customName;
        public int level;
        public int currentExp;
        public int curHP;
        public int curMP;

        // Base Stats
        public int baseAtk;
        public int baseDef;
        public int baseMag;
        public int baseMDef;
        public int baseSpd;
        public int baseAgi;
        public int baseLuck;
        public int baseMaxHP;
        public int baseMaxMP;
        public int unspentPoints;

        // Customization
        public bool isCustom;
        public int genderIdx;
        public int bodyIdx;
        public int hairIdx;
        public int eyesIdx;

        // Equipment
        public List<EquipSaveData> equippedItems = new List<EquipSaveData>();

        // [MỚI] Danh sách Skill đã học
        public List<string> learnedSkillIDs = new List<string>();
    }

    // ... (Giữ nguyên EquipSaveData, ItemSaveData, QuestSaveData)
    [System.Serializable] public class EquipSaveData { public int slotIndex; public string itemID; }
    [System.Serializable] public class ItemSaveData { public string itemID; public int amount; }
    [System.Serializable] public class QuestSaveData { public string questID; public List<string> objectivesProgress = new List<string>(); }
}
```

#### SaveSystem.cs
```csharp
using UnityEngine;
using System.IO;

namespace RebirthWarrior.SaveLoad
{
    public static class SaveSystem
    {
        private static string SaveFolder => Application.persistentDataPath + "/Saves/";

        public static void Init()
        {
            if (!Directory.Exists(SaveFolder)) Directory.CreateDirectory(SaveFolder);
        }

        public static void SaveGame(GameSaveData data, int slotIndex, Texture2D screenshot)
        {
            Init();
            string json = JsonUtility.ToJson(data, true);
            string path = SaveFolder + $"save_{slotIndex}.json";
            File.WriteAllText(path, json);

            if (screenshot != null)
            {
                byte[] bytes = screenshot.EncodeToPNG();
                File.WriteAllBytes(SaveFolder + $"thumb_{slotIndex}.png", bytes);
            }
            Debug.Log($"[SaveSystem] Saved to slot {slotIndex}");
        }

        // === FIX: Đổi tên thành LoadGameData ===
        public static GameSaveData LoadGameData(int slotIndex)
        {
            string path = SaveFolder + $"save_{slotIndex}.json";
            if (File.Exists(path))
            {
                string json = File.ReadAllText(path);
                return JsonUtility.FromJson<GameSaveData>(json);
            }
            return null;
        }

        public static Sprite LoadScreenshot(int slotIndex)
        {
            string path = SaveFolder + $"thumb_{slotIndex}.png";
            if (File.Exists(path))
            {
                byte[] bytes = File.ReadAllBytes(path);
                Texture2D tex = new Texture2D(2, 2);
                tex.LoadImage(bytes);
                return Sprite.Create(tex, new Rect(0, 0, tex.width, tex.height), new Vector2(0.5f, 0.5f));
            }
            return null;
        }

        public static void DeleteSave(int slotIndex)
        {
            string jsonPath = SaveFolder + $"save_{slotIndex}.json";
            string imgPath = SaveFolder + $"thumb_{slotIndex}.png";
            if (File.Exists(jsonPath)) File.Delete(jsonPath);
            if (File.Exists(imgPath)) File.Delete(imgPath);
        }
    }
}
```


### C11. SKILLS Scripts

#### Skill.cs 
```csharp
using UnityEngine;
using UnityEngine.Serialization; // Cần dòng này để giữ dữ liệu cũ
using RebirthWarrior.Character;
using RebirthWarrior.Battle;

namespace RebirthWarrior.Skills
{
    [CreateAssetMenu(fileName = "NewSkill", menuName = "Rebirth Warrior/Skill")]
    public class Skill : ScriptableObject
    {
        [Header("Basic Info")]
        public string skillID;
        public string skillNameKey;
        public string descriptionKey;
        public Sprite icon;

        [Header("Skill Type")]
        public SkillType skillType;
        public TargetType targetType;
        public ElementType element;

        [Header("Cost")]
        // [FIX] Đổi tên biến nhưng giữ lại giá trị cũ đã nhập trong Inspector
        [FormerlySerializedAs("mpCost")]
        public int staminaCost;

        public int hpCost;

        [Header("Power")]
        public float basePower;
        public int statusDuration;

        [Header("Effects")]
        public StatusEffect appliesStatus = StatusEffect.None;
        [Range(0, 100)]
        public int statusChance;

        [Header("Requirements")]
        public int requiredLevel;

        public bool CanUse(CharacterStats user)
        {
            if (user.level < requiredLevel) return false;

            // [FIX ERROR 1] currentMP -> currentStamina
            if (user.currentStamina < staminaCost) return false;

            if (user.currentHP <= hpCost) return false;
            return true;
        }

        public void PayCost(CharacterStats user)
        {
            // [FIX ERROR 2] UseMP -> UseStamina
            user.UseStamina(staminaCost);

            user.TakeDamage(hpCost);
        }

        public int CalculateDamage(CharacterStats user, CharacterStats target)
        {
            int value = 0;
            bool dummyCritical;

            switch (skillType)
            {
                case SkillType.Physical:
                    int physicalPower = user.attack + (int)basePower;
                    // Tạo stats ảo để tính damage vật lý tăng cường
                    CharacterStats physicalUser = new CharacterStats(user.characterID, user.characterName);
                    physicalUser.baseAttack = physicalPower;
                    physicalUser.baseLuck = user.luck; // Copy Luck để tính Crit

                    value = DamageCalculator.CalculatePhysicalDamage(physicalUser, target, out dummyCritical);
                    break;

                case SkillType.Magical:
                    // [FIX ERROR 3] CalculateMagicDamage -> CalculateToxicDamage
                    // Trong hệ thống mới, Skill Phép (Magical) sẽ tính là Sát thương Độc (Toxic)
                    value = DamageCalculator.CalculateToxicDamage(user, target, basePower, out dummyCritical);
                    break;

                case SkillType.Healing:
                    // Healing giờ dựa trên Medicine Skill (đã update trong DamageCalculator)
                    value = DamageCalculator.CalculateHealing(user, basePower);
                    break;
            }
            return value;
        }

        public void ApplyEffect(CharacterStats user, CharacterStats target)
        {
            // (Logic Effect đã được chuyển sang BattleManager, hàm này giữ trống để tương thích)
        }
    }

    // Các Enum giữ nguyên
    public enum SkillType { Physical, Magical, Healing, Buff, Debuff, Status, Special }
    public enum TargetType { Self, SingleAlly, SingleEnemy, AllAllies, AllEnemies, Random }
    public enum ElementType { None, Fire, Water, Wood, Earth, Metal, Light, Dark }
}
```


#### SkillManager.cs
```csharp
using UnityEngine;
using System.Collections.Generic;

namespace RebirthWarrior.Skills
{
    public enum SurvivalSkillType
    {
        Lockpicking, // Mở khóa
        Pickpocketing, // Móc túi
        Cooking, // Nấu ăn
        Medicine, // Chế thuốc
        Crafting // Chế tạo & Sửa chữa
    }

    [System.Serializable]
    public class SurvivalSkillData
    {
        public SurvivalSkillType type;
        public int level = 1;
        public int currentExp = 0;
        public int expToNextLevel = 100;

        public void AddExp(int amount)
        {
            currentExp += amount;
            if (currentExp >= expToNextLevel)
            {
                level++;
                currentExp -= expToNextLevel;
                expToNextLevel = level * 150; // Công thức tăng khó
                Debug.Log($"Skill {type} lên cấp {level}!");
            }
        }
    }
}
```


### C12. UI SYSTEM

#### CharacterCreationManager.cs
```csharp
using UnityEngine;
using UnityEngine.EventSystems; // Bắt buộc để dùng sự kiện chuột
using UnityEngine.UI;

public class ButtonHoverSound : MonoBehaviour, IPointerEnterHandler
{
    [Header("Settings")]
    public AudioSource sourceToPlay; // Kéo cái AudioSource (SFX) từ GameManager vào đây
    public AudioClip hoverSound;     // File âm thanh "tít" hoặc "bụp" nhẹ
    [Range(0f, 1f)] public float volume = 1f;

    // Biến để kiểm tra xem nút có đang ẩn không
    private CanvasGroup canvasGroup;

    void Start()
    {
        // Tự động tìm CanvasGroup trên nút này
        canvasGroup = GetComponent<CanvasGroup>();
    }

    // Hàm này tự động chạy khi chuột lướt vào (Hover)
    public void OnPointerEnter(PointerEventData eventData)
    {
        // 1. Kiểm tra quan trọng: Nếu nút chưa hiện (interactable = false) thì KHÔNG phát tiếng
        if (canvasGroup != null && !canvasGroup.interactable)
        {
            return;
        }

        // 2. Nếu nút đã hiện, phát âm thanh
        if (sourceToPlay != null && hoverSound != null)
        {
            sourceToPlay.PlayOneShot(hoverSound, volume);
        }
    }
}
```



#### CharacterCreationManager.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;
using RebirthWarrior.Core;
using UnityEngine.SceneManagement;
using System.Collections.Generic;
using System.Collections;

namespace RebirthWarrior.UI
{
    public class CharacterCreationManager : MonoBehaviour
    {
        [Header("Data")]
        [SerializeField] private CharacterData mainPlayerData;
        [SerializeField] private CharacterAppearanceData appearanceData;

        [Header("Avatar Layers")]
        [SerializeField] private Image baseSkinImage;
        [SerializeField] private Image outfitImage;
        [SerializeField] private Image eyesImage;
        [SerializeField] private Image hairImage;

        [Header("UI Inputs")]
        [SerializeField] private TMP_InputField characterNameInput;
        [SerializeField] private TextMeshProUGUI genderText;
        [SerializeField] private TextMeshProUGUI bodyText;
        [SerializeField] private TextMeshProUGUI hairText;
        [SerializeField] private TextMeshProUGUI eyesText;
        [SerializeField] private Button startGameButton;

        [Header("UI Stats")]
        [SerializeField] private TextMeshProUGUI pointsRemainingText;
        [SerializeField] private List<StatUIElements> statUIList;

        [Header("Game Flow Settings")]
        [SerializeField] private string startingSceneName = "Map_HCMC_2025";

        private CharacterStats tempStats;
        private int pointsRemaining = 20;
        private Dictionary<StatType, int> baseStats = new Dictionary<StatType, int>();

        private int genderIndex = 0;
        private int bodyIndex = 0;
        private int hairIndex = 0;
        private int eyesIndex = 0;

        [System.Serializable]
        public class StatUIElements
        {
            public StatType statType;
            public TextMeshProUGUI statValueText;
            public Button increaseButton;
            public Button decreaseButton;
        }

        void Start()
        {
            if (mainPlayerData != null)
            {
                tempStats = mainPlayerData.CreateStats(1);
                pointsRemaining = tempStats.unspentStatPoints;
                StoreBaseStats();
            }

            genderIndex = 0;
            ValidateIndices();
            UpdateAvatar();
            UpdateStatUI();
            StartCoroutine(SetFocusToNameInput());
        }

        IEnumerator SetFocusToNameInput()
        {
            yield return null;
            if (characterNameInput != null)
            {
                characterNameInput.Select();
                characterNameInput.ActivateInputField();
            }
        }

        private List<Sprite> GetCurrentOutfitList()
        {
            if (appearanceData == null) return null;
            return (genderIndex == 0) ? appearanceData.maleOutfits : appearanceData.femaleOutfits;
        }
        private List<Sprite> GetCurrentHairList()
        {
            if (appearanceData == null) return null;
            return (genderIndex == 0) ? appearanceData.maleHairStyles : appearanceData.femaleHairStyles;
        }
        private List<Sprite> GetCurrentEyesList()
        {
            if (appearanceData == null) return null;
            return (genderIndex == 0) ? appearanceData.maleEyes : appearanceData.femaleEyes;
        }

        public void ChangeGender(int direction)
        {
            genderIndex += direction;
            if (genderIndex > 1) genderIndex = 0;
            if (genderIndex < 0) genderIndex = 1;
            bodyIndex = 0; hairIndex = 0; eyesIndex = 0;
            UpdateAvatar();
        }

        public void ChangeBody(int direction)
        {
            var list = GetCurrentOutfitList();
            if (list == null || list.Count == 0) return;
            bodyIndex += direction;
            if (bodyIndex >= list.Count) bodyIndex = 0;
            if (bodyIndex < 0) bodyIndex = list.Count - 1;
            UpdateAvatar();
        }

        public void ChangeHair(int direction)
        {
            var list = GetCurrentHairList();
            if (list == null || list.Count == 0) return;
            hairIndex += direction;
            if (hairIndex >= list.Count) hairIndex = 0;
            if (hairIndex < 0) hairIndex = list.Count - 1;
            UpdateAvatar();
        }

        public void ChangeEyes(int direction)
        {
            var list = GetCurrentEyesList();
            if (list == null || list.Count == 0) return;
            eyesIndex += direction;
            if (eyesIndex >= list.Count) eyesIndex = 0;
            if (eyesIndex < 0) eyesIndex = list.Count - 1;
            UpdateAvatar();
        }

        private void ValidateIndices()
        {
            var outfits = GetCurrentOutfitList();
            if (outfits != null && outfits.Count > 0) bodyIndex = Mathf.Clamp(bodyIndex, 0, outfits.Count - 1);
            else bodyIndex = 0;
        }

        private void UpdateAvatar()
        {
            if (genderText) genderText.text = (genderIndex == 0) ? "Nam" : "Nữ";
            if (bodyText) bodyText.text = $"Trang phục {bodyIndex + 1}";
            if (hairText) hairText.text = $"Kiểu {hairIndex + 1}";
            if (eyesText) eyesText.text = $"Kiểu {eyesIndex + 1}";

            if (appearanceData == null) return;

            if (baseSkinImage != null)
            {
                Sprite baseSprite = (genderIndex == 0) ? appearanceData.maleBaseSkin : appearanceData.femaleBaseSkin;
                SetImageSprite(baseSkinImage, baseSprite);
            }

            var outfits = GetCurrentOutfitList();
            if (outfitImage != null)
            {
                if (outfits != null && outfits.Count > 0)
                    SetImageSprite(outfitImage, outfits[Mathf.Clamp(bodyIndex, 0, outfits.Count - 1)]);
                else
                    outfitImage.enabled = false;
            }

            var eyes = GetCurrentEyesList();
            if (eyesImage != null)
            {
                if (eyes != null && eyes.Count > 0)
                    SetImageSprite(eyesImage, eyes[Mathf.Clamp(eyesIndex, 0, eyes.Count - 1)]);
                else
                    eyesImage.enabled = false;
            }

            var hairs = GetCurrentHairList();
            if (hairImage != null)
            {
                if (hairs != null && hairs.Count > 0)
                    SetImageSprite(hairImage, hairs[Mathf.Clamp(hairIndex, 0, hairs.Count - 1)]);
                else
                    hairImage.enabled = false;
            }
        }

        private void SetImageSprite(Image targetImage, Sprite sprite)
        {
            if (targetImage == null) return;
            if (sprite != null)
            {
                targetImage.sprite = sprite;
                targetImage.enabled = true;
                targetImage.SetNativeSize();
            }
            else targetImage.enabled = false;
        }

        public void OnStartGame()
        {
            if (string.IsNullOrEmpty(characterNameInput.text)) return;

            tempStats.characterName = characterNameInput.text;
            tempStats.unspentStatPoints = 0;

            tempStats.isCustomCharacter = true;
            tempStats.genderIndex = genderIndex;
            tempStats.bodyIndex = bodyIndex;
            tempStats.hairIndex = hairIndex;
            tempStats.eyesIndex = eyesIndex;

            tempStats.currentHP = tempStats.maxHP;
            tempStats.currentStamina = tempStats.maxStamina; // Sửa
            tempStats.isAlive = true;
            tempStats.level = 1;

            if (GameStateManager.Instance)
                GameStateManager.Instance.AddCharacterToRoster(tempStats);

            Debug.Log($"[CharacterCreation] Đang vào game: {startingSceneName}");
            SceneManager.LoadScene(startingSceneName);
        }

        void StoreBaseStats()
        {
            baseStats.Clear();
            baseStats.Add(StatType.MaxHP, tempStats.baseMaxHP);
            baseStats.Add(StatType.MaxStamina, tempStats.baseMaxStamina); // Sửa
            baseStats.Add(StatType.Attack, tempStats.baseAttack);
            baseStats.Add(StatType.Defense, tempStats.baseDefense);
            baseStats.Add(StatType.ToxicAttack, tempStats.baseToxicAttack); // Sửa
            baseStats.Add(StatType.ToxicResist, tempStats.baseToxicResist); // Sửa
            baseStats.Add(StatType.Speed, tempStats.baseSpeed);
            baseStats.Add(StatType.Agility, tempStats.baseAgility);
            baseStats.Add(StatType.Luck, tempStats.baseLuck);
        }

        public void OnStatIncrease(int statIndex) => ChangeStatValue(statIndex, 1);
        public void OnStatDecrease(int statIndex) => ChangeStatValue(statIndex, -1);
        private void ChangeStatValue(int statIndex, int amount) { StatType type = (StatType)statIndex; if (amount > 0) { if (pointsRemaining <= 0) return; if (type == StatType.Luck && GetCurrentStat(type) >= 30) return; ApplyStat(type, 1); pointsRemaining--; } else { if (GetCurrentStat(type) <= baseStats[type]) return; ApplyStat(type, -1); pointsRemaining++; } UpdateStatUI(); }

        void ApplyStat(StatType type, int dir)
        {
            switch (type)
            {
                case StatType.MaxHP: tempStats.baseMaxHP += dir * 10; break;
                case StatType.MaxStamina: tempStats.baseMaxStamina += dir * 5; break;
                case StatType.Attack: tempStats.baseAttack += dir; break;
                case StatType.Defense: tempStats.baseDefense += dir; break;
                case StatType.ToxicAttack: tempStats.baseToxicAttack += dir; break;
                case StatType.ToxicResist: tempStats.baseToxicResist += dir; break;
                case StatType.Speed: tempStats.baseSpeed += dir; break;
                case StatType.Agility: tempStats.baseAgility += dir; break;
                case StatType.Luck: tempStats.baseLuck += dir; break;
            }
        }

        int GetCurrentStat(StatType type)
        {
            switch (type)
            {
                case StatType.MaxHP: return tempStats.baseMaxHP;
                case StatType.MaxStamina: return tempStats.baseMaxStamina;
                case StatType.Attack: return tempStats.baseAttack;
                case StatType.Defense: return tempStats.baseDefense;
                case StatType.ToxicAttack: return tempStats.baseToxicAttack;
                case StatType.ToxicResist: return tempStats.baseToxicResist;
                case StatType.Speed: return tempStats.baseSpeed;
                case StatType.Agility: return tempStats.baseAgility;
                case StatType.Luck: return tempStats.baseLuck;
                default: return 0;
            }
        }

        void UpdateStatUI() { if (pointsRemainingText) pointsRemainingText.text = $"ĐIỂM: {pointsRemaining}"; foreach (var ui in statUIList) { if (ui.statValueText) ui.statValueText.text = GetCurrentStat(ui.statType).ToString(); if (ui.increaseButton) { bool maxLuck = (ui.statType == StatType.Luck && GetCurrentStat(ui.statType) >= 30); ui.increaseButton.interactable = (pointsRemaining > 0 && !maxLuck); } if (ui.decreaseButton) { ui.decreaseButton.interactable = (GetCurrentStat(ui.statType) > baseStats[ui.statType]); } } if (startGameButton != null) { bool hasName = !string.IsNullOrEmpty(characterNameInput.text); bool pointsUsed = (pointsRemaining == 0); startGameButton.interactable = hasName && pointsUsed; var txt = startGameButton.GetComponentInChildren<TextMeshProUGUI>(); if (txt) { if (!hasName) txt.text = "Nhập tên..."; else if (!pointsUsed) txt.text = "Phân phối hết điểm!"; else txt.text = "BẮT ĐẦU"; } } }
        public void OnNameChanged() => UpdateStatUI();
        public void IncreaseStat(int statIdx) => ChangeStatValue(statIdx, 1);
        public void DecreaseStat(int statIdx) => ChangeStatValue(statIdx, -1);
    }
}
```



#### CharacterSelectionPanel.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using System;
using System.Collections.Generic;
using RebirthWarrior.Character;
using RebirthWarrior.Items;
using RebirthWarrior.Core;

namespace RebirthWarrior.UI
{
    /// <summary>
    /// Version 3.0 - Đã cập nhật sang hệ thống Stamina/Toxic
    /// </summary>
    public class CharacterSelectionPanel : MonoBehaviour
    {
        [Header("UI References")]
        [SerializeField] private GameObject panel;
        [SerializeField] private TextMeshProUGUI titleText;
        [SerializeField] private Transform characterGrid;
        [SerializeField] private GameObject characterSlotPrefab;
        [SerializeField] private Button cancelButton;

        private List<GameObject> characterSlots = new List<GameObject>();
        private Item currentItem;
        private Action<CharacterStats> onCharacterSelected;

        private void Awake()
        {
            if (panel != null) panel.SetActive(false);
            if (cancelButton != null) cancelButton.onClick.AddListener(Hide);
        }

        public void Show(Item item, Action<CharacterStats> callback)
        {
            currentItem = item;
            onCharacterSelected = callback;

            if (panel != null) panel.SetActive(true);

            if (titleText != null)
            {
                if (item.itemType == ItemType.Consumable)
                    titleText.text = $"Dùng {item.itemName} lên:";
                else if (item.IsEquipment())
                    titleText.text = $"Trang bị {item.itemName} cho:";
            }
            PopulateCharacters();
            Time.timeScale = 0f;
        }

        public void Hide()
        {
            if (panel != null) panel.SetActive(false);
            currentItem = null;
            onCharacterSelected = null;
            Time.timeScale = 1f;
        }

        private void PopulateCharacters()
        {
            if (characterGrid == null || characterSlotPrefab == null) return;
            foreach (var slot in characterSlots) { Destroy(slot); }
            characterSlots.Clear();

            var gameState = GameStateManager.Instance;
            if (gameState == null) return;

            var party = gameState.GetBattleParty();

            foreach (var character in party)
            {
                CreateCharacterSlot(character);
            }
        }

        private void CreateCharacterSlot(CharacterStats character)
        {
            // Lọc bỏ Pet (trừ khi sau này có item riêng cho Pet)
            if (character.characterData != null && character.characterData.type == CharacterType.Pet)
            {
                return;
            }

            GameObject slotObj = Instantiate(characterSlotPrefab, characterGrid);
            var button = slotObj.GetComponent<Button>();
            var nameText = slotObj.transform.Find("CharacterName")?.GetComponent<TextMeshProUGUI>();

            var hpBar = slotObj.transform.Find("HPBar")?.GetComponent<Slider>();
            var hpText = slotObj.transform.Find("HPText")?.GetComponent<TextMeshProUGUI>();

            // [FIX] MPBar giờ hiển thị Stamina
            var mpBar = slotObj.transform.Find("MPBar")?.GetComponent<Slider>();
            var mpText = slotObj.transform.Find("MPText")?.GetComponent<TextMeshProUGUI>();

            if (nameText != null) nameText.text = character.characterName;

            if (hpBar != null) { hpBar.maxValue = character.maxHP; hpBar.value = character.currentHP; }
            if (hpText != null) hpText.text = $"{character.currentHP}/{character.maxHP}";

            // [FIX] Đổi hiển thị MP -> Stamina
            if (mpBar != null)
            {
                mpBar.maxValue = character.maxStamina;
                mpBar.value = character.currentStamina;
                // Đổi màu thanh sang vàng cho hợp Stamina
                var fill = mpBar.fillRect.GetComponent<Image>();
                if (fill) fill.color = new Color(1f, 0.8f, 0f);
            }
            if (mpText != null) mpText.text = $"{character.currentStamina}/{character.maxStamina}";

            bool isValidTarget = IsValidTarget(character);

            if (button != null)
            {
                button.interactable = isValidTarget;
                if (isValidTarget)
                {
                    button.onClick.AddListener(() => OnCharacterClicked(character));
                }
                else
                {
                    var canvasGroup = slotObj.GetComponent<CanvasGroup>();
                    if (canvasGroup == null) canvasGroup = slotObj.AddComponent<CanvasGroup>();
                    canvasGroup.alpha = 0.5f;
                }
            }
            characterSlots.Add(slotObj);
        }

        private bool IsValidTarget(CharacterStats character)
        {
            if (currentItem == null) return true;

            // 1. Kiểm tra Trang bị (Equipment)
            if (currentItem.IsEquipment())
            {
                return true;
            }

            // 2. Kiểm tra Vật phẩm (Consumable)
            if (currentItem.itemType == ItemType.Consumable)
            {
                // Không thể dùng item lên nhân vật đã chết
                if (character.currentHP <= 0 || !character.isAlive)
                {
                    return false;
                }

                // Logic Skill Book
                if (currentItem.skillToLearn != null)
                {
                    if (character.KnowsSkill(currentItem.skillToLearn)) return false;

                    if (currentItem.requiredClasses.Count > 0 &&
                        !currentItem.requiredClasses.Contains(character.characterData.characterClass))
                        return false;
                }

                // Logic hồi Máu
                if (currentItem.healAmount > 0)
                {
                    // Chỉ cho dùng nếu máu chưa đầy
                    if (character.currentHP >= character.maxHP) return false;
                }

                // [FIX LỖI TẠI ĐÂY] Logic hồi Stamina (Thay cho Mana)
                if (currentItem.staminaAmount > 0)
                {
                    // Chỉ cho dùng nếu Stamina chưa đầy
                    if (character.currentStamina >= character.maxStamina) return false;
                }

                // Logic giảm Độc (Toxic)
                if (currentItem.toxicReduction > 0)
                {
                    if (character.currentToxic <= 0) return false;
                }
            }

            return true;
        }

        private void OnCharacterClicked(CharacterStats character)
        {
            onCharacterSelected?.Invoke(character);
            Hide();
        }
    }
}
```




#### CharacterStatsUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;
using RebirthWarrior.Skills;
using RebirthWarrior.Battle;
using System.Collections.Generic;

namespace RebirthWarrior.UI
{
    public class CharacterStatsUI : MonoBehaviour
    {
        [Header("Main UI References")]
        [SerializeField] private GameObject panelRoot;
        [SerializeField] private Button closeButton;
        [SerializeField] private TextMeshProUGUI characterNameText;
        [SerializeField] private TextMeshProUGUI levelText;

        [Header("Attribute Allocation")]
        [SerializeField] private TextMeshProUGUI unspentPointsText;
        [SerializeField] private List<StatAttributeRow> statRows;

        [Header("Avatar Display")]
        [SerializeField] private CharacterAppearanceData appearanceData;
        [SerializeField] private Image characterPortrait;
        [SerializeField] private Image portraitOutfit;
        [SerializeField] private Image portraitHair;
        [SerializeField] private Image portraitEyes;

        [Header("Skill List")]
        [SerializeField] private GameObject skillScrollView;
        [SerializeField] private Transform skillListContainer;
        [SerializeField] private GameObject skillButtonPrefab;
        [SerializeField] private int skillPoolSize = 10;

        private CharacterStats currentCharacter;
        private InventoryUI inventoryUI;
        private List<SkillButtonUI> skillButtonPool = new List<SkillButtonUI>();

        [System.Serializable]
        public class StatAttributeRow
        {
            public string rowLabel;
            public StatType statType;
            public TextMeshProUGUI valueText;
            public Button increaseButton;
        }

        private void Awake()
        {
            inventoryUI = GetComponentInParent<InventoryUI>();
            if (closeButton != null) closeButton.onClick.AddListener(Hide);

            if (statRows != null)
            {
                foreach (var row in statRows)
                {
                    if (row.increaseButton != null)
                    {
                        StatType type = row.statType;
                        row.increaseButton.onClick.AddListener(() => OnIncreaseStat(type));
                    }
                }
            }

            CreateSkillButtonPool();
            if (panelRoot != null) panelRoot.SetActive(false);
        }

        private void CreateSkillButtonPool()
        {
            if (skillListContainer == null || skillButtonPrefab == null) return;
            for (int i = 0; i < skillPoolSize; i++)
            {
                GameObject skillButtonObj = Instantiate(skillButtonPrefab, skillListContainer);
                SkillButtonUI skillButtonUI = skillButtonObj.GetComponent<SkillButtonUI>();
                if (skillButtonUI != null)
                {
                    skillButtonPool.Add(skillButtonUI);
                    skillButtonObj.SetActive(false);
                }
            }
        }

        public void Show(CharacterStats character)
        {
            if (character == null) return;
            currentCharacter = character;
            if (panelRoot != null) panelRoot.SetActive(true);

            UpdateAllUI();
            PopulateSkills();
        }

        public void Hide()
        {
            if (panelRoot != null) panelRoot.SetActive(false);
            if (inventoryUI != null) inventoryUI.ShowMainPanels();
        }

        public bool IsShowing() => panelRoot != null && panelRoot.activeSelf;

        private void UpdateAllUI()
        {
            if (currentCharacter == null) return;
            if (characterNameText) characterNameText.text = currentCharacter.characterName;
            if (levelText) levelText.text = $"Lv.{currentCharacter.level} ({currentCharacter.characterData?.characterClass})";
            if (unspentPointsText)
                unspentPointsText.text = $"Điểm tiềm năng: <color=yellow>{currentCharacter.unspentStatPoints}</color>";

            UpdateAvatarDisplay();
            UpdateStatRows();
        }

        private void UpdateStatRows()
        {
            if (statRows == null) return;
            bool canSpend = currentCharacter.unspentStatPoints > 0;
            bool isMainPlayer = (currentCharacter.characterData != null && currentCharacter.characterData.type == CharacterType.MainPlayerCharacter);

            foreach (var row in statRows)
            {
                int val = GetStatValue(row.statType);
                if (row.valueText) row.valueText.text = val.ToString();
                if (row.increaseButton)
                {
                    row.increaseButton.gameObject.SetActive(isMainPlayer);
                    bool isMaxed = (row.statType == StatType.Luck && val >= 30);
                    row.increaseButton.interactable = (canSpend && !isMaxed);
                }
            }
        }

        private void OnIncreaseStat(StatType type)
        {
            if (currentCharacter == null || currentCharacter.unspentStatPoints <= 0) return;

            switch (type)
            {
                case StatType.MaxHP: currentCharacter.baseMaxHP += 10; break;
                case StatType.MaxStamina: currentCharacter.baseMaxStamina += 5; break;  // Sửa
                case StatType.Attack: currentCharacter.baseAttack += 1; break;
                case StatType.Defense: currentCharacter.baseDefense += 1; break;
                case StatType.ToxicAttack: currentCharacter.baseToxicAttack += 1; break; // Sửa
                case StatType.ToxicResist: currentCharacter.baseToxicResist += 1; break; // Sửa
                case StatType.Speed: currentCharacter.baseSpeed += 1; break;
                case StatType.Agility: currentCharacter.baseAgility += 1; break;
                case StatType.Luck:
                    if (currentCharacter.baseLuck < 30) currentCharacter.baseLuck += 1;
                    else return;
                    break;
            }

            currentCharacter.unspentStatPoints--;
            currentCharacter.currentHP = Mathf.Min(currentCharacter.currentHP, currentCharacter.maxHP);
            currentCharacter.currentStamina = Mathf.Min(currentCharacter.currentStamina, currentCharacter.maxStamina); // Sửa

            UpdateAllUI();
        }

        private int GetStatValue(StatType type)
        {
            switch (type)
            {
                case StatType.MaxHP: return currentCharacter.maxHP;
                case StatType.MaxStamina: return currentCharacter.maxStamina; // Sửa
                case StatType.Attack: return currentCharacter.attack;
                case StatType.Defense: return currentCharacter.defense;
                case StatType.ToxicAttack: return currentCharacter.toxicAttack; // Sửa
                case StatType.ToxicResist: return currentCharacter.toxicResist; // Sửa
                case StatType.Speed: return currentCharacter.speed;
                case StatType.Agility: return currentCharacter.agility;
                case StatType.Luck: return currentCharacter.luck;
                default: return 0;
            }
        }

        private void UpdateAvatarDisplay()
        {
            if (characterPortrait == null) return;
            if (currentCharacter.isCustomCharacter && appearanceData != null)
            {
                characterPortrait.enabled = true;
                var bodies = (currentCharacter.genderIndex == 0) ? appearanceData.maleBaseSkin : appearanceData.femaleBaseSkin;
                if (bodies != null) characterPortrait.sprite = bodies;

                if (portraitOutfit != null)
                {
                    var list = (currentCharacter.genderIndex == 0) ? appearanceData.maleOutfits : appearanceData.femaleOutfits;
                    if (list != null && currentCharacter.bodyIndex < list.Count)
                    {
                        portraitOutfit.sprite = list[currentCharacter.bodyIndex];
                        portraitOutfit.gameObject.SetActive(true);
                        portraitOutfit.SetNativeSize();
                    }
                    else portraitOutfit.gameObject.SetActive(false);
                }

                if (portraitHair != null)
                {
                    var list = (currentCharacter.genderIndex == 0) ? appearanceData.maleHairStyles : appearanceData.femaleHairStyles;
                    if (list != null && currentCharacter.hairIndex < list.Count)
                    {
                        portraitHair.sprite = list[currentCharacter.hairIndex];
                        portraitHair.gameObject.SetActive(true);
                        portraitHair.SetNativeSize();
                    }
                    else portraitHair.gameObject.SetActive(false);
                }

                if (portraitEyes != null)
                {
                    var list = (currentCharacter.genderIndex == 0) ? appearanceData.maleEyes : appearanceData.femaleEyes;
                    if (list != null && currentCharacter.eyesIndex < list.Count)
                    {
                        portraitEyes.sprite = list[currentCharacter.eyesIndex];
                        portraitEyes.gameObject.SetActive(true);
                        portraitEyes.SetNativeSize();
                    }
                    else portraitEyes.gameObject.SetActive(false);
                }
            }
            else if (currentCharacter.characterData != null)
            {
                characterPortrait.sprite = currentCharacter.characterData.portraitSprite;
                characterPortrait.enabled = (characterPortrait.sprite != null);
                if (portraitOutfit) portraitOutfit.gameObject.SetActive(false);
                if (portraitHair) portraitHair.gameObject.SetActive(false);
                if (portraitEyes) portraitEyes.gameObject.SetActive(false);
            }
        }

        private void PopulateSkills()
        {
            if (skillScrollView == null) return;
            skillScrollView.SetActive(false);
            var learnedSkills = currentCharacter.learnedSkills;

            while (learnedSkills.Count > skillButtonPool.Count)
            {
                GameObject obj = Instantiate(skillButtonPrefab, skillListContainer);
                skillButtonPool.Add(obj.GetComponent<SkillButtonUI>());
            }

            for (int i = 0; i < skillButtonPool.Count; i++)
            {
                if (i < learnedSkills.Count)
                {
                    skillButtonPool[i].Initialize(learnedSkills[i], null);
                    skillButtonPool[i].gameObject.SetActive(true);
                }
                else
                {
                    skillButtonPool[i].gameObject.SetActive(false);
                }
            }
            skillScrollView.SetActive(true);
        }
    }
}
```



#### ChoiceButtonUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Dialogue; // Cần namespace này

namespace RebirthWarrior.UI
{
    public class ChoiceButtonUI : MonoBehaviour
    {
        [SerializeField] private Button button;
        [SerializeField] private TextMeshProUGUI text;

        public void Setup(DialogueChoice choice, System.Action onClick)
        {
            if (text) text.text = choice.text;
            if (button)
            {
                button.onClick.RemoveAllListeners();
                button.onClick.AddListener(() => onClick?.Invoke());
            }
        }
    }
}
```



#### DamagePopup.cs
```csharp
using UnityEngine;
using TMPro;

namespace RebirthWarrior.UI
{
    // Định nghĩa các loại Popup
    public enum PopupType
    {
        Normal,     // Màu cam/trắng
        Critical,   // Màu đỏ, chữ to
        Toxic,      // Màu tím/xanh lá đậm
        Heal,       // Màu xanh lá tươi
        Miss,       // Màu xám
        StaminaLoss // Màu vàng nhạt (nếu cần hiện trừ thể lực)
    }

    public class DamagePopup : MonoBehaviour
    {
        private TextMeshProUGUI textMesh;
        private float disappearTimer;
        private Color textColor;
        private Vector3 moveVector;

        private const float DISAPPEAR_TIMER_MAX = 1f;

        private void Awake()
        {
            textMesh = GetComponent<TextMeshProUGUI>();
            if (textMesh == null) textMesh = gameObject.AddComponent<TextMeshProUGUI>();
        }

        // Hàm Setup mới hỗ trợ Type
        public void Setup(int amount, PopupType type)
        {
            textMesh.fontStyle = FontStyles.Bold;

            switch (type)
            {
                case PopupType.Normal:
                    textMesh.fontSize = 28;
                    textMesh.color = new Color(1f, 0.6f, 0f); // Cam vàng
                    textMesh.text = amount.ToString();
                    break;

                case PopupType.Critical:
                    textMesh.fontSize = 38;
                    textMesh.color = Color.red; // Đỏ tươi
                    textMesh.text = "CRIT! " + amount;
                    // Phóng to ra một chút lúc đầu
                    transform.localScale = Vector3.one * 1.2f;
                    break;

                case PopupType.Toxic:
                    textMesh.fontSize = 28;
                    textMesh.color = new Color(0.6f, 0f, 1f); // Tím độc
                    // Hoặc dùng màu xanh lục bảo: new Color(0f, 0.8f, 0.2f);
                    textMesh.text = "-" + amount;
                    break;

                case PopupType.Heal:
                    textMesh.fontSize = 30;
                    textMesh.color = Color.green;
                    textMesh.text = "+" + amount;
                    break;

                case PopupType.Miss:
                    textMesh.fontSize = 26;
                    textMesh.color = Color.gray;
                    textMesh.text = "MISS";
                    break;

                case PopupType.StaminaLoss:
                    textMesh.fontSize = 24;
                    textMesh.color = Color.yellow;
                    textMesh.text = "-" + amount + " SP";
                    break;
            }

            textColor = textMesh.color;
            disappearTimer = DISAPPEAR_TIMER_MAX;

            // Random hướng bay
            moveVector = new Vector3(Random.Range(-0.5f, 0.5f), 1f) * 30f; // Tốc độ bay lên
        }

        private void Update()
        {
            // Bay lên
            transform.position += moveVector * Time.deltaTime;
            moveVector -= moveVector * 3f * Time.deltaTime; // Giảm tốc dần

            if (disappearTimer > DISAPPEAR_TIMER_MAX * 0.5f)
            {
                // Nửa đầu: Phóng to nhẹ
                float increaseScaleAmount = 0.5f;
                transform.localScale += Vector3.one * increaseScaleAmount * Time.deltaTime;
            }
            else
            {
                // Nửa sau: Thu nhỏ lại
                float decreaseScaleAmount = 0.5f;
                transform.localScale -= Vector3.one * decreaseScaleAmount * Time.deltaTime;
            }

            disappearTimer -= Time.deltaTime;
            if (disappearTimer < 0)
            {
                // Mờ dần
                float disappearSpeed = 3f;
                textColor.a -= disappearSpeed * Time.deltaTime;
                textMesh.color = textColor;

                if (textColor.a < 0) Destroy(gameObject);
            }
        }
    }
}
```


#### EquipSlotUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Items;
using RebirthWarrior.Character; // Cần cho CharacterStats

namespace RebirthWarrior.UI
{
    public class EquipSlotUI : MonoBehaviour
    {
        [Header("Loại Slot này")]
        [SerializeField] private EquipmentSlot slotType; // GÁN TRONG INSPECTOR

        [Header("Tham chiếu con")]
        [SerializeField] private Image icon;
        [SerializeField] private TextMeshProUGUI slotNameText;
        [SerializeField] private Button button;

        private CharacterStats currentCharacter;
        private InventoryUI inventoryUI;

        private void Awake()
        {
            // Tìm InventoryUI cha
            inventoryUI = GetComponentInParent<InventoryUI>();
            if (button == null) button = GetComponent<Button>();

            button.onClick.AddListener(OnSlotClicked);
        }

        /// <summary>
        /// Gán nhân vật và cập nhật UI
        /// </summary>
        public void SetCharacter(CharacterStats character)
        {
            currentCharacter = character;
            UpdateSlot();
        }

        /// <summary>
        /// Cập nhật hình ảnh dựa trên item
        /// </summary>
        public void UpdateSlot()
        {
            if (currentCharacter == null) return;

            Item item = currentCharacter.GetItemInSlot(slotType);

            if (item != null)
            {
                // CÓ ĐỒ
                icon.sprite = item.icon;
                icon.color = Color.white;
                icon.enabled = true;
                slotNameText.enabled = false; // Ẩn tên slot
                button.interactable = true; // Cho phép gỡ đồ
            }
            else
            {
                // SLOT TRỐNG
                icon.sprite = null;
                icon.enabled = false;
                slotNameText.enabled = true; // Hiện tên slot (HEAD, CHEST...)
                button.interactable = false; // Không cho bấm
            }
        }

        /// <summary>
        /// Khi bấm vào slot (để gỡ đồ)
        /// </summary>
        private void OnSlotClicked()
        {
            if (currentCharacter == null) return;

            // Gọi hàm gỡ đồ trong InventoryUI
            inventoryUI.RequestUnequip(currentCharacter, slotType);
        }
    }
}
```




#### InventoryUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using System.Collections.Generic;
using RebirthWarrior.Items;
using RebirthWarrior.Character;
using RebirthWarrior.Inventory;
using RebirthWarrior.Core;
using UnityEngine.EventSystems;

namespace RebirthWarrior.UI
{
    public class InventoryUI : MonoBehaviour
    {
        [Header("UI References")]
        [SerializeField] private GameObject inventoryPanel;
        [SerializeField] private Button closeButton;
        [SerializeField] private TextMeshProUGUI goldText;

        [Header("Item Bag")]
        [SerializeField] private GameObject itemPanelRoot;
        [SerializeField] private Transform itemGridContainer;
        [SerializeField] private GameObject itemSlotPrefab;

        [Header("Equipment Panel")]
        [SerializeField] private GameObject equipmentPanelRoot;
        [SerializeField] private TextMeshProUGUI characterNameText;
        [SerializeField] private TextMeshProUGUI characterStatsText;
        [SerializeField] private Button prevCharacterButton;
        [SerializeField] private Button nextCharacterButton;

        [Header("Character Appearance")]
        [SerializeField] private CharacterAppearanceData appearanceData;
        [SerializeField] private Image portraitBody;
        [SerializeField] private Image portraitOutfit;
        [SerializeField] private Image portraitHair;
        [SerializeField] private Image portraitEyes;

        [Header("Equipment Slots")]
        [SerializeField] private EquipSlotUI headSlot;
        [SerializeField] private EquipSlotUI handsSlot;
        [SerializeField] private EquipSlotUI feetSlot;
        [SerializeField] private EquipSlotUI weaponSlot;
        [SerializeField] private EquipSlotUI shieldSlot;
        [SerializeField] private EquipSlotUI armorSlot;
        [SerializeField] private EquipSlotUI ringSlot;

        [Header("Panels")]
        [SerializeField] private Button statsButton;
        [SerializeField] private CharacterStatsUI statsPanel;
        [SerializeField] private Button partyMgmtButton;
        [SerializeField] private PartyManagementUI partyManagementPanel;
        [SerializeField] private Button petMgmtButton;
        [SerializeField] private PetManagementUI petManagementPanel;

        [Header("Item Details")]
        [SerializeField] private GameObject itemDetailsPanel;
        [SerializeField] private TextMeshProUGUI itemNameText;
        [SerializeField] private TextMeshProUGUI itemDescriptionText;
        [SerializeField] private TextMeshProUGUI itemTypeText;
        [SerializeField] private Image itemIcon;
        [SerializeField] private Button actionButton;
        [SerializeField] private TextMeshProUGUI actionButtonText;
        [SerializeField] private Button dropButton;

        [Header("Character Selection")]
        [SerializeField] private CharacterSelectionPanel characterSelectionPanel;

        [Header("Drag & Drop")]
        [SerializeField] private Image dragIcon;

        [Header("Quest Log")]
        [SerializeField] private Button questLogButton;

        [Header("Feedback")]
        [SerializeField] private GameObject feedbackPanel;
        [SerializeField] private TextMeshProUGUI feedbackText;
        [SerializeField] private Button closeFeedbackButton;

        private List<ItemSlotUI> itemSlots = new List<ItemSlotUI>();
        private List<EquipSlotUI> allEquipSlots = new List<EquipSlotUI>();
        private Items.Item selectedItem;
        private CharacterStats currentCharacter;
        private int currentCharacterIndex = 0;
        private List<CharacterStats> party;

        private bool isDragging = false;
        private int draggedSlotIndex = -1;

        private static InventoryUI instance;
        public static InventoryUI Instance { get { return instance; } }

        private void Awake()
        {
            if (instance != null && instance != this) { Destroy(gameObject); return; }
            instance = this;
            DontDestroyOnLoad(gameObject);

            if (actionButton) actionButton.onClick.AddListener(OnActionButtonClicked);
            if (dropButton) dropButton.onClick.AddListener(OnDropButtonClicked);
            if (closeButton) closeButton.onClick.AddListener(CloseInventory);
            if (prevCharacterButton) prevCharacterButton.onClick.AddListener(PreviousCharacter);
            if (nextCharacterButton) nextCharacterButton.onClick.AddListener(NextCharacter);
            if (statsButton) statsButton.onClick.AddListener(OpenStatsPanel);
            if (partyMgmtButton) partyMgmtButton.onClick.AddListener(OpenPartyManagementPanel);
            if (questLogButton) questLogButton.onClick.AddListener(OnQuestLogButtonClicked);
            if (petMgmtButton) petMgmtButton.onClick.AddListener(OpenPetManagementPanel);
            if (closeFeedbackButton) closeFeedbackButton.onClick.AddListener(HideFeedback);

            if (inventoryPanel) inventoryPanel.SetActive(false);
            if (statsPanel) statsPanel.Hide();
            if (dragIcon) dragIcon.gameObject.SetActive(false);
            if (petManagementPanel) petManagementPanel.gameObject.SetActive(false);
            if (feedbackPanel) feedbackPanel.SetActive(false);

            StartCoroutine(SubscribeToInventoryManager());
            PopulateEquipSlotList();
            CreateItemSlotPool();
        }

        private IEnumerator<WaitForEndOfFrame> SubscribeToInventoryManager()
        {
            yield return new WaitForEndOfFrame();
            if (InventoryManager.Instance) InventoryManager.Instance.OnInventoryChanged += OnInventoryChanged;
        }
        private void OnDestroy() { if (InventoryManager.Instance) InventoryManager.Instance.OnInventoryChanged -= OnInventoryChanged; }
        private void OnInventoryChanged() { if (inventoryPanel && inventoryPanel.activeSelf) { RefreshInventoryDisplay(); RefreshEquipmentDisplay(); } }

        private void CreateItemSlotPool()
        {
            if (!itemSlotPrefab || !itemGridContainer || !InventoryManager.Instance) return;
            foreach (Transform child in itemGridContainer) Destroy(child.gameObject);
            itemSlots.Clear();
            int poolSize = InventoryManager.Instance.inventoryGridSize;
            for (int i = 0; i < poolSize; i++)
            {
                GameObject slotObj = Instantiate(itemSlotPrefab, itemGridContainer);
                ItemSlotUI slotUI = slotObj.GetComponent<ItemSlotUI>();
                slotUI.BindData(this, null, i);
                itemSlots.Add(slotUI);
            }
        }

        public void ToggleInventory() { if (inventoryPanel.activeSelf) CloseInventory(); else OpenInventory(); }

        public void OpenInventory()
        {
            if (inventoryPanel) inventoryPanel.SetActive(true);
            UpdateGoldDisplay();
            party = GameStateManager.Instance.GetBattleParty();
            if (party == null || party.Count == 0) { CloseInventory(); return; }
            LoadCharacter(currentCharacterIndex);

            ShowMainPanels();
            if (statsPanel) statsPanel.Hide();
            if (partyManagementPanel) partyManagementPanel.Hide();
            if (QuestLogUI.Instance) QuestLogUI.Instance.ClosePanel();

            RefreshInventoryDisplay();
            Time.timeScale = 0f;
        }

        public void CloseInventory()
        {
            if (statsPanel) statsPanel.Hide();
            if (partyManagementPanel) partyManagementPanel.Hide();
            if (petManagementPanel) petManagementPanel.gameObject.SetActive(false);
            if (itemDetailsPanel) itemDetailsPanel.SetActive(false);
            if (feedbackPanel) feedbackPanel.SetActive(false);
            if (itemPanelRoot) itemPanelRoot.SetActive(true);
            if (inventoryPanel) inventoryPanel.SetActive(false);
            Time.timeScale = 1f;
        }

        public void OpenStatsPanel() { if (statsPanel && currentCharacter != null) { if (itemPanelRoot) itemPanelRoot.SetActive(false); statsPanel.Show(currentCharacter); } }
        public void OpenPartyManagementPanel() { if (partyManagementPanel) { if (itemPanelRoot) itemPanelRoot.SetActive(false); partyManagementPanel.Show(); } }
        public void OnQuestLogButtonClicked() { CloseInventory(); if (WorldUIManager.Instance) WorldUIManager.Instance.ToggleQuestLogPanel(); }
        public void OpenPetManagementPanel() { if (petManagementPanel) { if (itemPanelRoot) itemPanelRoot.SetActive(false); petManagementPanel.gameObject.SetActive(true); petManagementPanel.Show(); } }
        public void ShowMainPanels() { if (itemPanelRoot) itemPanelRoot.SetActive(true); if (equipmentPanelRoot) equipmentPanelRoot.SetActive(true); }

        public void NextCharacter() { if (party == null) return; currentCharacterIndex = (currentCharacterIndex + 1) % party.Count; LoadCharacter(currentCharacterIndex); }
        public void PreviousCharacter() { if (party == null) return; currentCharacterIndex--; if (currentCharacterIndex < 0) currentCharacterIndex = party.Count - 1; LoadCharacter(currentCharacterIndex); }
        private void LoadCharacter(int index) { if (party == null || index < 0 || index >= party.Count) return; currentCharacterIndex = index; currentCharacter = party[index]; RefreshEquipmentDisplay(); if (statsPanel && statsPanel.IsShowing()) statsPanel.Show(currentCharacter); }

        private void RefreshInventoryDisplay()
        {
            if (!itemPanelRoot || itemSlots.Count == 0) return;
            itemPanelRoot.SetActive(false);
            GridLayoutGroup gridLayout = itemGridContainer.GetComponent<GridLayoutGroup>();
            if (gridLayout != null) { gridLayout.enabled = true; gridLayout.constraint = GridLayoutGroup.Constraint.FixedColumnCount; gridLayout.constraintCount = InventoryManager.Instance.columns; }
            Vector2 cellSize = gridLayout ? gridLayout.cellSize : new Vector2(100, 100);
            Vector2 spacing = gridLayout ? gridLayout.spacing : new Vector2(5, 5);
            InventorySlot[] inventory = InventoryManager.Instance.GetAllItems();
            if (itemSlots.Count != inventory.Length) CreateItemSlotPool();
            for (int i = 0; i < itemSlots.Count; i++)
            {
                ItemSlotUI uiSlot = itemSlots[i];
                uiSlot.transform.SetSiblingIndex(i);
                if (i < inventory.Length && inventory[i] != null)
                {
                    InventorySlot data = inventory[i];
                    uiSlot.BindData(this, data, i);
                    if (data.isGhost) uiSlot.SetGhostMode(true);
                    else
                    {
                        uiSlot.ResizeIcon(data.item.width, data.item.height, cellSize, spacing);
                        if (data.item.width > 1 || data.item.height > 1) uiSlot.SetIconSorting(true);
                        else uiSlot.SetIconSorting(false);
                    }
                }
                else { uiSlot.BindData(this, null, i); uiSlot.ResetIconSize(); }
            }
            LayoutRebuilder.ForceRebuildLayoutImmediate(itemGridContainer.GetComponent<RectTransform>());
            itemPanelRoot.SetActive(true);
        }

        private void RefreshEquipmentDisplay() { if (equipmentPanelRoot == null || currentCharacter == null) return; bool isPet = (currentCharacter.characterData != null && currentCharacter.characterData.type == CharacterType.Pet); foreach (var slotUI in allEquipSlots) { slotUI.gameObject.SetActive(!isPet); if (!isPet) slotUI.SetCharacter(currentCharacter); } if (portraitBody != null) portraitBody.gameObject.SetActive(false); if (characterNameText) characterNameText.text = $"{currentCharacter.characterName} - Lv.{currentCharacter.level}"; }
        private void PopulateEquipSlotList() { allEquipSlots = new List<EquipSlotUI> { headSlot, handsSlot, feetSlot, weaponSlot, shieldSlot, armorSlot, ringSlot }; allEquipSlots.RemoveAll(item => item == null); }
        public void RequestUnequip(CharacterStats m, EquipmentSlot s) { InventoryManager.Instance.UnequipItem(s, m); }
        public void OnItemClicked(Items.Item item) { selectedItem = item; ShowItemDetails(item); }

        private void ShowItemDetails(Items.Item item)
        {
            if (itemDetailsPanel == null) return;
            itemDetailsPanel.SetActive(true);
            if (itemNameText) itemNameText.text = item.itemName;
            if (itemDescriptionText) itemDescriptionText.text = item.description;

            // [FIX] HÀM NÀY SẼ HẾT LỖI KHI CẬP NHẬT ITEM.CS
            if (itemTypeText) itemTypeText.text = item.GetTypeDisplayName();

            if (itemIcon) { itemIcon.sprite = item.icon; itemIcon.enabled = (item.icon != null); }
            if (actionButton) { bool showButton = false; string btnLabel = ""; if (item.IsConsumable()) { btnLabel = "Dùng"; showButton = true; } else if (item.IsEquipment()) { btnLabel = "Trang bị"; showButton = true; } if (actionButtonText) actionButtonText.text = btnLabel; actionButton.gameObject.SetActive(showButton); }
            if (dropButton) dropButton.gameObject.SetActive(true);
        }

        private void OnActionButtonClicked() { if (selectedItem) { if (selectedItem.petToSpawn != null) { if (InventoryManager.Instance.UseItem(selectedItem, null)) HandleItemActionSuccess(); return; } if (selectedItem.IsConsumable()) characterSelectionPanel.Show(selectedItem, OnCharacterSelected_Use); else if (selectedItem.IsEquipment()) OnCharacterSelected_Equip(currentCharacter); } }
        private void OnCharacterSelected_Use(CharacterStats target) { if (selectedItem == null) return; if (!selectedItem.CanUseOnCharacter(target)) { ShowFeedback("Không thể dùng!", Color.red); return; } if (InventoryManager.Instance.UseItem(selectedItem, target)) { HandleItemActionSuccess(); } }
        private void ShowFeedback(string msg, Color color) { if (feedbackPanel && feedbackText) { feedbackText.text = msg; feedbackText.color = color; feedbackPanel.SetActive(true); CancelInvoke(nameof(HideFeedback)); Invoke(nameof(HideFeedback), 2.0f); } }
        public void HideFeedback() { if (feedbackPanel) feedbackPanel.SetActive(false); }
        private void OnCharacterSelected_Equip(CharacterStats target) { if (InventoryManager.Instance.EquipItem(selectedItem, target)) HandleItemActionSuccess(); }
        private void HandleItemActionSuccess() { if (itemDetailsPanel) itemDetailsPanel.SetActive(false); selectedItem = null; }
        private void OnDropButtonClicked() { if (InventoryManager.Instance.RemoveItem(selectedItem, 1)) HandleItemActionSuccess(); }
        private void UpdateGoldDisplay() { if (GameStateManager.Instance && goldText) goldText.text = $"Gold: {GameStateManager.Instance.GetGold()}"; }
        public void OnDragStart(int index) { draggedSlotIndex = index; isDragging = true; var inventory = InventoryManager.Instance.GetAllItems(); if (index >= 0 && index < inventory.Length && inventory[index] != null) { Item item = inventory[index].item; if (dragIcon) { dragIcon.sprite = item.icon; dragIcon.gameObject.SetActive(true); dragIcon.transform.SetAsLastSibling(); } } }
        public void OnDrag(PointerEventData eventData) { if (isDragging && dragIcon) dragIcon.transform.position = eventData.position; }
        public void OnDragEnd() { isDragging = false; draggedSlotIndex = -1; if (dragIcon) dragIcon.gameObject.SetActive(false); }
        public void OnDropOnSlot(int dropIndex) { if (draggedSlotIndex == -1 || dropIndex == -1) return; bool success = InventoryManager.Instance.TryMoveItem(draggedSlotIndex, dropIndex); if (!success) ShowFeedback("Không vừa chỗ!", Color.red); }
    }
}
```





#### ItemSlotUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using UnityEngine.EventSystems;
using RebirthWarrior.Inventory;
using RebirthWarrior.Items;

namespace RebirthWarrior.UI
{
    [RequireComponent(typeof(CanvasGroup))]
    public class ItemSlotUI : MonoBehaviour, IBeginDragHandler, IDragHandler, IEndDragHandler, IDropHandler
    {
        [Header("Components")]
        [SerializeField] private Image icon;
        [SerializeField] private TextMeshProUGUI quantityText;
        [SerializeField] private Button button;
        [SerializeField] private CanvasGroup canvasGroup;

        private InventoryUI inventoryUI;
        private int slotIndex = -1;
        private InventorySlot slotData;

        private void OnValidate()
        {
            if (icon == null) icon = transform.Find("Icon")?.GetComponent<Image>();
            if (quantityText == null) quantityText = transform.Find("Quantity")?.GetComponent<TextMeshProUGUI>();
            if (button == null) button = GetComponent<Button>();
            if (canvasGroup == null) canvasGroup = GetComponent<CanvasGroup>();
        }

        public void BindData(InventoryUI ui, InventorySlot data, int index)
        {
            inventoryUI = ui;
            slotIndex = index;
            slotData = data;

            // Reset trạng thái trước khi bind mới
            if (icon)
            {
                icon.enabled = false;
                SetIconSorting(false); // Tắt Canvas override cũ
            }
            if (quantityText) quantityText.gameObject.SetActive(false);
            if (button) { button.interactable = false; button.onClick.RemoveAllListeners(); }
            if (canvasGroup) { canvasGroup.alpha = 1f; canvasGroup.blocksRaycasts = true; }

            ResetIconTransform();

            if (data != null && data.item != null)
            {
                Item item = data.item;
                int quantity = data.quantity;

                if (icon)
                {
                    icon.sprite = item.icon;
                    icon.color = Color.white;
                    icon.enabled = true;
                }

                if (quantityText)
                {
                    quantityText.text = $"x{quantity}";
                    quantityText.gameObject.SetActive(quantity > 1);
                }

                if (button)
                {
                    button.interactable = true;
                    button.onClick.AddListener(() => OnSlotClicked(item));
                }
            }
        }

        private void OnSlotClicked(Item item)
        {
            if (inventoryUI != null) inventoryUI.OnItemClicked(item);
        }

        public void SetGhostMode(bool isGhost)
        {
            if (isGhost)
            {
                if (icon) icon.enabled = false;
                if (quantityText) quantityText.gameObject.SetActive(false);
                if (button) button.interactable = false;
                if (canvasGroup) canvasGroup.blocksRaycasts = true; // Vẫn cho phép drop vào
            }
        }

        public void ResizeIcon(int width, int height, Vector2 cellSize, Vector2 spacing)
        {
            if (icon == null) return;

            float finalW = (cellSize.x * width) + (spacing.x * (width - 1));
            float finalH = (cellSize.y * height) + (spacing.y * (height - 1));

            RectTransform rect = icon.rectTransform;
            rect.pivot = new Vector2(0, 1); // Pivot Top-Left
            rect.anchorMin = new Vector2(0, 1);
            rect.anchorMax = new Vector2(0, 1);
            rect.anchoredPosition = Vector2.zero;
            rect.sizeDelta = new Vector2(finalW, finalH);
        }

        public void ResetIconSize() { ResetIconTransform(); }

        private void ResetIconTransform()
        {
            if (icon == null) return;
            RectTransform rect = icon.rectTransform;
            rect.anchorMin = Vector2.zero;
            rect.anchorMax = Vector2.one;
            rect.pivot = new Vector2(0.5f, 0.5f);
            rect.offsetMin = Vector2.zero;
            rect.offsetMax = Vector2.zero;
        }

        // === [FIX LỖI CAN'T REMOVE CANVAS] ===
        public void SetIconSorting(bool bringToFront)
        {
            if (icon == null) return;

            // Lấy các component
            Canvas c = icon.GetComponent<Canvas>();
            GraphicRaycaster gr = icon.GetComponent<GraphicRaycaster>();

            if (bringToFront)
            {
                // Thêm Canvas nếu chưa có
                if (c == null) c = icon.gameObject.AddComponent<Canvas>();
                c.overrideSorting = true;
                c.sortingLayerName = "UI";
                c.sortingOrder = 10;

                // Thêm Raycaster nếu chưa có (để click được)
                if (gr == null) icon.gameObject.AddComponent<GraphicRaycaster>();
            }
            else
            {
                // [QUAN TRỌNG] Xóa Raycaster TRƯỚC, rồi mới xóa Canvas
                if (gr != null) DestroyImmediate(gr); // Dùng Immediate cho chắc chắn
                if (c != null) DestroyImmediate(c);
            }
        }

        // ================= DRAG & DROP =================
        public void OnBeginDrag(PointerEventData eventData)
        {
            if (slotData == null || inventoryUI == null) return;
            inventoryUI.OnDragStart(slotIndex);
            if (canvasGroup) { canvasGroup.alpha = 0.5f; canvasGroup.blocksRaycasts = false; }
        }
        public void OnDrag(PointerEventData eventData) { if (inventoryUI != null) inventoryUI.OnDrag(eventData); }
        public void OnEndDrag(PointerEventData eventData)
        {
            if (inventoryUI != null) inventoryUI.OnDragEnd();
            if (canvasGroup) { canvasGroup.alpha = 1f; canvasGroup.blocksRaycasts = true; }
        }
        public void OnDrop(PointerEventData eventData) { if (inventoryUI != null) inventoryUI.OnDropOnSlot(slotIndex); }
    }
}
```




#### MainMenu.cs
```csharp
using UnityEngine;
using UnityEngine.SceneManagement;
using UnityEngine.UI;

namespace RebirthWarrior.UI
{
    public class MainMenu : MonoBehaviour
    {
        [Header("Scene Tải")]
        [SerializeField] private string characterCreationScene = "CharacterCreation";

        [Header("Các Nút Bấm")]
        [SerializeField] private Button newGameButton;
        [SerializeField] private Button loadGameButton;
        [SerializeField] private Button optionsButton;

        private void Start()
        {
            if (newGameButton != null) newGameButton.onClick.AddListener(OnNewGameClicked);
            if (loadGameButton != null) loadGameButton.onClick.AddListener(OnLoadGameClicked);
            if (optionsButton != null) optionsButton.onClick.AddListener(OnOptionsClicked);
        }

        public void OnNewGameClicked()
        {
            Debug.Log($"[MainMenu] New Game -> {characterCreationScene}");
            SceneManager.LoadScene(characterCreationScene);
        }

        public void OnLoadGameClicked()
        {
            Debug.Log("[MainMenu] -> Bấm nút Load Game");

            // Code tự tìm Manager, không cần kéo thả tay
            if (SaveLoadManager.Instance != null)
            {
                SaveLoadManager.Instance.OpenLoadPanel();
            }
            else
            {
                Debug.LogError("[MainMenu] LỖI: Không tìm thấy SaveLoadManager.Instance!");
                Debug.LogError("=> Hãy kiểm tra xem Prefab 'InventoryUI_Persistent' đã có trong Scene MainMenu chưa?");
            }
        }

        public void OnOptionsClicked()
        {
            Debug.Log("Options clicked (Chưa cài đặt)");
        }
    }
}
```



#### MenuIntroController.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.Video;
using System.Collections;
using System.Collections.Generic;

public class MenuIntroController : MonoBehaviour
{
    [Header("Components")]
    public VideoPlayer introVideo;
    public GameObject introObject;
    public Button skipButton; // <--- KÉO NÚT SKIP VÀO ĐÂY

    [Header("Menu Buttons")]
    public List<CanvasGroup> menuButtons;

    [Header("Settings")]
    public float fadeDuration = 0.5f;
    public float delayBetweenButtons = 0.3f;

    [Header("Audio SFX")]
    public AudioSource sfxSource;
    public AudioClip popSound;
    [Range(0f, 1f)] public float sfxVolume = 1f;

    [Header("Background Music")]
    public AudioSource musicSource;
    public AudioClip bgMusic;
    [Range(0f, 1f)] public float musicVolume = 0.5f;

    private bool isSkipped = false;

    void Start()
    {
        // 0. Setup nút Skip
        if (skipButton != null)
        {
            skipButton.onClick.AddListener(SkipIntro);
            skipButton.gameObject.SetActive(true);
        }

        // 1. Setup các nút ẩn
        foreach (var btn in menuButtons)
        {
            btn.alpha = 0;
            btn.interactable = false;
            btn.blocksRaycasts = false;
        }

        // 2. Setup nhạc nền
        if (musicSource != null && bgMusic != null)
        {
            musicSource.clip = bgMusic;
            musicSource.loop = true;
            musicSource.volume = musicVolume;
            musicSource.playOnAwake = false;
        }

        // 3. Chạy Video
        if (introVideo != null)
        {
            introVideo.loopPointReached += OnVideoFinished;
            introVideo.Play();
        }
        else
        {
            SkipIntro(); // Không có video thì skip luôn
        }
    }

    void OnVideoFinished(VideoPlayer vp)
    {
        if (!isSkipped) FinishIntroSequence();
    }

    // === HÀM SKIP ===
    public void SkipIntro()
    {
        if (isSkipped) return;
        isSkipped = true;

        if (introVideo != null) introVideo.Stop();

        FinishIntroSequence();
    }

    private void FinishIntroSequence()
    {
        // Tắt Video & Nút Skip
        if (introObject != null) introObject.SetActive(false);
        if (skipButton != null) skipButton.gameObject.SetActive(false);

        // Phát nhạc ngay lập tức (Không fade nếu skip để vào nhanh)
        if (musicSource != null && bgMusic != null)
        {
            musicSource.volume = musicVolume;
            if (!musicSource.isPlaying) musicSource.Play();
        }

        // Hiện nút Menu ngay lập tức
        StopAllCoroutines();
        foreach (var btn in menuButtons)
        {
            btn.gameObject.SetActive(true);
            btn.alpha = 1f;
            btn.interactable = true;
            btn.blocksRaycasts = true;
        }
    }

    // Giữ lại hàm cũ phòng khi không Skip
    IEnumerator ShowButtonsSequence()
    {
        foreach (CanvasGroup btn in menuButtons)
        {
            if (sfxSource != null && popSound != null) sfxSource.PlayOneShot(popSound, sfxVolume);
            yield return StartCoroutine(FadeInButton(btn));
            yield return new WaitForSeconds(delayBetweenButtons);
        }
    }

    private IEnumerator FadeInButton(CanvasGroup cg)
    {
        if (cg == null) yield break;
        float duration = 0.5f;
        float elapsedTime = 0f;
        cg.alpha = 0f;
        cg.gameObject.SetActive(true);

        while (elapsedTime < duration)
        {
            if (cg == null || cg.gameObject == null) yield break;
            elapsedTime += Time.deltaTime;
            cg.alpha = Mathf.Lerp(0f, 1f, elapsedTime / duration);
            yield return null;
        }

        if (cg != null)
        {
            cg.alpha = 1f;
            cg.interactable = true;
            cg.blocksRaycasts = true;
        }
    }

    IEnumerator FadeMusicIn()
    {
        float timer = 0f;
        float targetVolume = musicVolume;
        float duration = 2.0f;

        while (timer < duration)
        {
            timer += Time.deltaTime;
            if (musicSource != null) musicSource.volume = Mathf.Lerp(0f, targetVolume, timer / duration);
            yield return null;
        }
        if (musicSource != null) musicSource.volume = targetVolume;
    }
}
```



#### PartyManagementUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;
using RebirthWarrior.Core;
using System.Collections.Generic;

namespace RebirthWarrior.UI
{
    /// <summary>
    /// Version 2.2 - Sửa lỗi Nút Remove (Dùng SetSlotType)
    /// </summary>
    public class PartyManagementUI : MonoBehaviour
    {
        [Header("UI References")]
        [SerializeField] private GameObject panelRoot;
        [SerializeField] private Button closeButton;
        [SerializeField] private Transform battleTeamContainer;
        [SerializeField] private Transform reserveTeamContainer;
        [SerializeField] private GameObject partySlotButtonPrefab;

        [Header("Pool Settings")]
        [SerializeField] private int initialPoolSize = 15;

        private List<PartySlotButton> battleSlotPool = new List<PartySlotButton>();
        private List<PartySlotButton> reserveSlotPool = new List<PartySlotButton>();

        private GameStateManager gameState;
        private InventoryUI inventoryUI;

        private CharacterStats selectedBattleChar = null;
        private CharacterStats selectedReserveChar = null;

        private void Start()
        {
            gameState = GameStateManager.Instance;
            inventoryUI = GetComponentInParent<InventoryUI>();

            if (closeButton != null)
                closeButton.onClick.AddListener(Hide);

            CreatePools();

            if (panelRoot != null)
                panelRoot.SetActive(false);
        }

        private void CreatePools()
        {
            if (partySlotButtonPrefab == null) { return; }

            // 1. TẠO 4 SLOT CHIẾN ĐẤU (Battle Team)
            for (int i = 0; i < 4; i++)
            {
                GameObject slotObj = Instantiate(partySlotButtonPrefab, battleTeamContainer);
                var slotUI = slotObj.GetComponent<PartySlotButton>();

                // SỬA LỖI: Nói cho nút này biết nó là slot "Chiến Đấu"
                slotUI.SetSlotType(true);

                battleSlotPool.Add(slotUI);
            }

            // 2. TẠO POOL DỰ BỊ (Reserve Team)
            for (int i = 0; i < initialPoolSize; i++)
            {
                GameObject slotObj = Instantiate(partySlotButtonPrefab, reserveTeamContainer);
                var slotUI = slotObj.GetComponent<PartySlotButton>();

                // SỬA LỖI: Nói cho nút này biết nó là slot "Dự Bị"
                slotUI.SetSlotType(false);

                reserveSlotPool.Add(slotUI);
                slotObj.SetActive(false);
            }
        }

        public void Show()
        {
            if (panelRoot != null)
                panelRoot.SetActive(true);
            RefreshUI();
        }

        public void Hide()
        {
            if (panelRoot != null)
                panelRoot.SetActive(false);

            if (inventoryUI != null)
                inventoryUI.ShowMainPanels();
        }

        public bool IsShowing()
        {
            return panelRoot != null && panelRoot.activeSelf;
        }

        private void RefreshUI()
        {
            if (gameState == null) { gameState = GameStateManager.Instance; if (gameState == null) return; }
            var battleParty = gameState.GetBattleParty();
            var reserveParty = gameState.GetReserveCharacters();

            for (int i = 0; i < battleSlotPool.Count; i++)
            {
                if (i < battleParty.Count)
                {
                    battleSlotPool[i].Setup(battleParty[i], this);
                    battleSlotPool[i].gameObject.SetActive(true);
                }
                else
                {
                    battleSlotPool[i].Setup(null, this);
                    battleSlotPool[i].gameObject.SetActive(true);
                }
            }

            while (reserveParty.Count > reserveSlotPool.Count)
            {
                GameObject slotObj = Instantiate(partySlotButtonPrefab, reserveTeamContainer);
                var slotUI = slotObj.GetComponent<PartySlotButton>();
                slotUI.SetSlotType(false); // Đảm bảo slot mới cũng là 'Reserve'
                reserveSlotPool.Add(slotUI);
            }

            // === [SỬA ĐỔI] LỌC PET KHỎI DANH SÁCH DỰ BỊ ===
            // 1. Tạo list tạm chỉ chứa NGƯỜI (Human Characters)
            List<CharacterStats> humanReserves = new List<CharacterStats>();
            foreach (var character in reserveParty)
            {
                // Nếu là Pet -> Bỏ qua, không đưa vào UI Dự Bị
                if (character.characterData != null && character.characterData.type == CharacterType.Pet)
                    continue;

                humanReserves.Add(character);
            }

            // 2. Logic hiển thị UI (Sử dụng humanReserves thay vì reserveParty)
            while (humanReserves.Count > reserveSlotPool.Count)
            {
                GameObject slotObj = Instantiate(partySlotButtonPrefab, reserveTeamContainer);
                var slotUI = slotObj.GetComponent<PartySlotButton>();
                slotUI.SetSlotType(false);
                reserveSlotPool.Add(slotUI);
            }

            for (int i = 0; i < reserveSlotPool.Count; i++)
            {
                if (i < humanReserves.Count)
                {
                    reserveSlotPool[i].Setup(humanReserves[i], this);
                    reserveSlotPool[i].gameObject.SetActive(true);
                }
                else
                {
                    reserveSlotPool[i].gameObject.SetActive(false);
                }
            }
            DeselectAll();
        }

        public void RequestRemoveFromBattleParty(CharacterStats character)
        {
            if (character == null) return;
            gameState.RemoveCharacterFromBattleParty(character);
            RefreshUI();
        }

        #region Selection Logic
        public void OnBattleSlotClicked(PartySlotButton button)
        {
            selectedBattleChar = button.characterData;
            HighlightButtons(battleSlotPool, button);
            AttemptSwap();
        }
        public void OnReserveSlotClicked(PartySlotButton button)
        {
            selectedReserveChar = button.characterData;
            HighlightButtons(reserveSlotPool, button);
            AttemptSwap();
        }
        private void AttemptSwap()
        {
            // Hoán đổi (Có người <-> Dự bị)
            if (selectedBattleChar != null && selectedReserveChar != null)
            {
                gameState.RemoveCharacterFromBattleParty(selectedBattleChar);
                bool added = gameState.AddCharacterToBattleParty(selectedReserveChar);
                if (added) RefreshUI();
            }
            // Thêm vào (Trống <-> Dự bị)
            else if (selectedBattleChar == null && selectedReserveChar != null)
            {
                bool added = gameState.AddCharacterToBattleParty(selectedReserveChar);
                if (added) RefreshUI();
            }
        }
        private void DeselectAll()
        {
            selectedBattleChar = null;
            selectedReserveChar = null;
            HighlightButtons(battleSlotPool, null);
            HighlightButtons(reserveSlotPool, null);
        }
        private void HighlightButtons(List<PartySlotButton> pool, PartySlotButton selectedButton)
        {
            foreach (var button in pool)
            {
                if (button.gameObject.activeSelf)
                    button.SetHighlight(button == selectedButton);
            }
        }
        #endregion
    }
}
```




#### PartySlotButton.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;

namespace RebirthWarrior.UI
{
    /// <summary>
    /// Version 2.1 - Sửa lỗi Nút Remove (Dùng biến isBattleSlot)
    /// </summary>
    public class PartySlotButton : MonoBehaviour
    {
        [Header("Trạng thái CÓ NHÂN VẬT")]
        [SerializeField] private GameObject inUseVisuals;
        [SerializeField] private Image portrait;
        [SerializeField] private TextMeshProUGUI nameText;
        [SerializeField] private TextMeshProUGUI levelText;
        [SerializeField] private Button removeButton;
        [SerializeField] private Image highlightBorder;

        [Header("Trạng thái TRỐNG")]
        [SerializeField] private GameObject emptySlotVisuals;

        [HideInInspector]
        public CharacterStats characterData;

        private PartyManagementUI manager;
        private Button mainButton;

        // BIẾN MỚI: Lưu trữ loại slot
        private bool isBattleSlot = false;

        private void Awake()
        {
            mainButton = GetComponent<Button>();

            mainButton.onClick.AddListener(OnSlotClicked);
            if (removeButton != null)
                removeButton.onClick.AddListener(OnRemoveClicked);
        }

        /// <summary>
        /// (HÀM MỚI) Được gọi bởi PartyManagementUI để gán loại slot
        /// </summary>
        public void SetSlotType(bool isBattleSlot)
        {
            this.isBattleSlot = isBattleSlot;
        }

        /// <summary>
        /// Gán dữ liệu cho slot
        /// </summary>
        public void Setup(CharacterStats stats, PartyManagementUI manager)
        {
            this.characterData = stats;
            this.manager = manager;

            if (stats != null)
            {
                // === CÓ NHÂN VẬT ===
                if (inUseVisuals != null) inUseVisuals.SetActive(true);
                if (emptySlotVisuals != null) emptySlotVisuals.SetActive(false);

                if (portrait != null && stats.characterData != null)
                {
                    portrait.sprite = stats.characterData.portraitSprite;
                    portrait.enabled = (portrait.sprite != null);
                }
                if (nameText != null) nameText.text = stats.characterName;
                if (levelText != null) levelText.text = $"Lv. {stats.level}";

                // SỬA LỖI: Hiển thị nút "Remove" DỰA TRÊN BIẾN isBattleSlot
                if (removeButton != null)
                {
                    removeButton.gameObject.SetActive(isBattleSlot);
                }
            }
            else
            {
                // === Ô TRỐNG ===
                if (inUseVisuals != null) inUseVisuals.SetActive(false);
                if (emptySlotVisuals != null) emptySlotVisuals.SetActive(true);
            }

            SetHighlight(false);
        }

        public void SetHighlight(bool highlighted)
        {
            if (highlightBorder != null)
                highlightBorder.enabled = highlighted;
        }

        /// <summary>
        /// Khi bấm vào ô (dùng để CHỌN)
        /// </summary>
        private void OnSlotClicked()
        {
            if (manager == null) return;

            // SỬA LỖI: Dùng biến isBattleSlot để báo cáo
            if (isBattleSlot)
            {
                manager.OnBattleSlotClicked(this);
            }
            else
            {
                manager.OnReserveSlotClicked(this);
            }
        }

        /// <summary>
        /// Khi bấm vào nút "Remove" (dùng để XÓA)
        /// </summary>
        private void OnRemoveClicked()
        {
            if (manager != null && characterData != null)
            {
                manager.RequestRemoveFromBattleParty(characterData);
            }
        }
    }
}
```



#### PartyStatusUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using System.Collections.Generic;

namespace RebirthWarrior.UI
{
    public class PartyStatusUI : MonoBehaviour
    {
        [Header("UI References")]
        [SerializeField] private GameObject partyPanel;
        [SerializeField] private Transform memberContainer;
        [SerializeField] private GameObject memberSlotPrefab;

        [Header("Gold & EXP")]
        [SerializeField] private TextMeshProUGUI goldText;
        [SerializeField] private TextMeshProUGUI expText;

        [Header("Update Settings")]
        [SerializeField] private float updateInterval = 0.5f;

        private List<PartyMemberSlot> memberSlots = new List<PartyMemberSlot>();
        private float updateTimer = 0f;

        private void Start()
        {
            InitializePartyUI();
        }

        private void Update()
        {
            updateTimer += Time.deltaTime;
            if (updateTimer >= updateInterval)
            {
                UpdatePartyUI();
                updateTimer = 0f;
            }
        }

        private void InitializePartyUI()
        {
            var gameState = Core.GameStateManager.Instance;
            if (gameState == null) return;

            var party = gameState.GetBattleParty();
            if (party == null || party.Count == 0) return;

            foreach (var slot in memberSlots) { if (slot.slotObject != null) Destroy(slot.slotObject); }
            memberSlots.Clear();

            foreach (var member in party) CreateMemberSlot(member);
            UpdateGoldExpDisplay();
        }

        private void CreateMemberSlot(Character.CharacterStats member)
        {
            if (memberSlotPrefab == null || memberContainer == null) return;

            GameObject slotObj = Instantiate(memberSlotPrefab, memberContainer);

            PartyMemberSlot slot = new PartyMemberSlot
            {
                member = member,
                slotObject = slotObj,
                nameText = slotObj.transform.Find("NameText")?.GetComponent<TextMeshProUGUI>(),
                levelText = slotObj.transform.Find("LevelText")?.GetComponent<TextMeshProUGUI>(),
                hpText = slotObj.transform.Find("HPText")?.GetComponent<TextMeshProUGUI>(),

                // [LƯU Ý] Trong Prefab cũ, đây là MPText/MPBar. Giờ nó sẽ hiển thị Stamina.
                mpText = slotObj.transform.Find("MPText")?.GetComponent<TextMeshProUGUI>(),
                hpBar = slotObj.transform.Find("HPBar/Fill")?.GetComponent<Image>(),
                mpBar = slotObj.transform.Find("MPBar/Fill")?.GetComponent<Image>()
            };

            memberSlots.Add(slot);
            UpdateMemberSlot(slot);
        }

        private void UpdatePartyUI()
        {
            foreach (var slot in memberSlots) UpdateMemberSlot(slot);
            UpdateGoldExpDisplay();
        }

        private void UpdateMemberSlot(PartyMemberSlot slot)
        {
            if (slot.member == null) return;
            if (slot.nameText != null) slot.nameText.text = slot.member.characterName;
            if (slot.levelText != null) slot.levelText.text = $"Lv.{slot.member.level}";
            if (slot.hpText != null) slot.hpText.text = $"{slot.member.currentHP}/{slot.member.maxHP}";

            if (slot.hpBar != null)
            {
                float hpPercent = slot.member.GetHPPercentage();
                slot.hpBar.fillAmount = hpPercent;
                if (hpPercent > 0.5f) slot.hpBar.color = Color.green;
                else if (hpPercent > 0.25f) slot.hpBar.color = Color.yellow;
                else slot.hpBar.color = Color.red;
            }

            // === [FIX LỖI HIỂN THỊ STAMINA] ===
            if (slot.mpText != null)
                slot.mpText.text = $"{slot.member.currentStamina}/{slot.member.maxStamina}"; // Đổi MP -> Stamina

            if (slot.mpBar != null)
            {
                // Dùng hàm GetStaminaPercentage (đã có trong CharacterStats mới)
                slot.mpBar.fillAmount = slot.member.GetStaminaPercentage();
                slot.mpBar.color = Color.yellow; // Đổi màu vàng cho Stamina
            }
        }

        private void UpdateGoldExpDisplay()
        {
            var gameState = Core.GameStateManager.Instance;
            if (gameState == null) return;
            if (goldText != null) goldText.text = $"💰 {gameState.GetGold()}";
            if (expText != null)
            {
                int totalExp = 0;
                var party = gameState.GetBattleParty();
                if (party != null) foreach (var member in party) if (member != null) totalExp += member.currentExp;
                expText.text = $"⭐ {totalExp}";
            }
        }

        public void RefreshUI() { InitializePartyUI(); }
    }

    [System.Serializable]
    public class PartyMemberSlot
    {
        public Character.CharacterStats member;
        public GameObject slotObject;
        public TextMeshProUGUI nameText;
        public TextMeshProUGUI levelText;
        public TextMeshProUGUI hpText;
        public TextMeshProUGUI mpText; // Tên biến giữ nguyên để khớp prefab, nhưng hiển thị Stamina
        public Image hpBar;
        public Image mpBar;
    }
}
```




#### PartyUIBuilderSafe.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;

namespace RebirthWarrior.UI
{
    /// <summary>
    /// Party UI Builder V2 - SAFE VERSION
    /// Only creates World/Town UI, doesn't touch Battle prefabs!
    /// </summary>
    public class PartyUIBuilderSafe : MonoBehaviour
    {
        [Header("Settings")]
        [SerializeField] private bool buildOnStart = false;
        
        // SAFE: Only creates in specific path
        private const string SAFE_PREFAB_PATH = "Assets/Prefabs/UI/WorldPartyMemberSlot.prefab";
        
        [ContextMenu("Build Party UI (Safe)")]
        public void BuildPartyUI()
        {
            Debug.Log("[PartyUIBuilderSafe] Building Party UI (Safe mode)...");
            
            // Find or create Canvas
            Canvas canvas = FindObjectOfType<Canvas>();
            if (canvas == null)
            {
                Debug.LogError("[PartyUIBuilderSafe] No Canvas found! Create Canvas first.");
                return;
            }
            
            // Create main panel
            GameObject partyPanel = CreatePartyPanel(canvas.transform);
            
            // Create header (Gold & EXP)
            CreateHeader(partyPanel.transform);
            
            // Create member container
            GameObject memberContainer = CreateMemberContainer(partyPanel.transform);
            
            // Create member slot prefab (SAFE PATH)
            CreateMemberSlotPrefab();
            
            // Add PartyStatusUI component
            PartyStatusUI statusUI = partyPanel.GetComponent<PartyStatusUI>();
            if (statusUI == null)
            {
                statusUI = partyPanel.AddComponent<PartyStatusUI>();
            }
            
            // Auto-assign references
            AssignReferences(statusUI, partyPanel);
            
            Debug.Log("[PartyUIBuilderSafe] ✅ Party UI created successfully! (Battle prefabs untouched)");
        }
        
        private GameObject CreatePartyPanel(Transform parent)
        {
            // Check if already exists
            Transform existing = parent.Find("PartyStatusPanel");
            if (existing != null)
            {
                Debug.Log("[PartyUIBuilderSafe] PartyStatusPanel already exists, using existing...");
                return existing.gameObject;
            }
            
            GameObject panel = new GameObject("PartyStatusPanel");
            panel.transform.SetParent(parent, false);
            
            RectTransform rect = panel.AddComponent<RectTransform>();
            rect.anchorMin = new Vector2(0, 1);
            rect.anchorMax = new Vector2(0, 1);
            rect.pivot = new Vector2(0, 1);
            rect.anchoredPosition = new Vector2(20, -20);
            rect.sizeDelta = new Vector2(400, 350);
            
            Image image = panel.AddComponent<Image>();
            image.color = new Color(0, 0, 0, 0.8f);
            
            Outline outline = panel.AddComponent<Outline>();
            outline.effectColor = new Color(1, 1, 1, 0.5f);
            outline.effectDistance = new Vector2(2, -2);
            
            return panel;
        }
        
        private void CreateHeader(Transform parent)
        {
            GameObject header = new GameObject("Header");
            header.transform.SetParent(parent, false);
            
            RectTransform headerRect = header.AddComponent<RectTransform>();
            headerRect.anchorMin = new Vector2(0, 1);
            headerRect.anchorMax = new Vector2(1, 1);
            headerRect.pivot = new Vector2(0.5f, 1);
            headerRect.anchoredPosition = new Vector2(0, -10);
            headerRect.sizeDelta = new Vector2(-20, 40);
            
            HorizontalLayoutGroup layout = header.AddComponent<HorizontalLayoutGroup>();
            layout.childAlignment = TextAnchor.MiddleCenter;
            layout.spacing = 20;
            layout.childForceExpandWidth = true;
            layout.childControlWidth = true;
            
            CreateGoldText(header.transform);
            CreateExpText(header.transform);
        }
        
        private void CreateGoldText(Transform parent)
        {
            GameObject goldObj = new GameObject("GoldText");
            goldObj.transform.SetParent(parent, false);
            
            TextMeshProUGUI goldText = goldObj.AddComponent<TextMeshProUGUI>();
            goldText.text = "💰 1000";
            goldText.fontSize = 24;
            goldText.color = Color.yellow;
            goldText.alignment = TextAlignmentOptions.Center;
            goldText.fontStyle = FontStyles.Bold;
        }
        
        private void CreateExpText(Transform parent)
        {
            GameObject expObj = new GameObject("ExpText");
            expObj.transform.SetParent(parent, false);
            
            TextMeshProUGUI expText = expObj.AddComponent<TextMeshProUGUI>();
            expText.text = "⭐ 0";
            expText.fontSize = 24;
            expText.color = Color.cyan;
            expText.alignment = TextAlignmentOptions.Center;
            expText.fontStyle = FontStyles.Bold;
        }
        
        private GameObject CreateMemberContainer(Transform parent)
        {
            GameObject container = new GameObject("MemberContainer");
            container.transform.SetParent(parent, false);
            
            RectTransform rect = container.AddComponent<RectTransform>();
            rect.anchorMin = new Vector2(0, 0);
            rect.anchorMax = new Vector2(1, 1);
            rect.pivot = new Vector2(0.5f, 1);
            rect.anchoredPosition = new Vector2(0, -60);
            rect.sizeDelta = new Vector2(-20, -70);
            
            VerticalLayoutGroup layout = container.AddComponent<VerticalLayoutGroup>();
            layout.childAlignment = TextAnchor.UpperCenter;
            layout.spacing = 10;
            layout.childForceExpandWidth = true;
            layout.childForceExpandHeight = false;
            layout.childControlWidth = true;
            layout.childControlHeight = true;
            
            ContentSizeFitter fitter = container.AddComponent<ContentSizeFitter>();
            fitter.verticalFit = ContentSizeFitter.FitMode.PreferredSize;
            
            return container;
        }
        
        private void CreateMemberSlotPrefab()
        {
            #if UNITY_EDITOR
            // Check if already exists
            GameObject existingPrefab = UnityEditor.AssetDatabase.LoadAssetAtPath<GameObject>(SAFE_PREFAB_PATH);
            if (existingPrefab != null)
            {
                Debug.Log("[PartyUIBuilderSafe] WorldPartyMemberSlot prefab already exists");
                return;
            }
            
            // Create temporary slot
            GameObject slot = CreateMemberSlot();
            
            // Ensure folder exists
            if (!UnityEditor.AssetDatabase.IsValidFolder("Assets/Prefabs"))
                UnityEditor.AssetDatabase.CreateFolder("Assets", "Prefabs");
            
            if (!UnityEditor.AssetDatabase.IsValidFolder("Assets/Prefabs/UI"))
                UnityEditor.AssetDatabase.CreateFolder("Assets/Prefabs", "UI");
            
            // Save with SAFE name (not touching Battle prefabs!)
            UnityEditor.PrefabUtility.SaveAsPrefabAsset(slot, SAFE_PREFAB_PATH);
            Debug.Log("[PartyUIBuilderSafe] ✅ Created WorldPartyMemberSlot prefab (Battle prefabs safe!)");
            
            DestroyImmediate(slot);
            #endif
        }
        
        private GameObject CreateMemberSlot()
        {
            GameObject slot = new GameObject("WorldPartyMemberSlot");
            
            RectTransform rect = slot.AddComponent<RectTransform>();
            rect.sizeDelta = new Vector2(360, 90);
            
            Image bg = slot.AddComponent<Image>();
            bg.color = new Color(0.2f, 0.2f, 0.2f, 0.8f);
            
            CreateText(slot.transform, "NameText", new Vector2(10, -10), new Vector2(200, 30), 
                "Character Name", 20, Color.white, TextAlignmentOptions.Left, 
                new Vector2(0, 1), new Vector2(0, 1));
            
            CreateText(slot.transform, "LevelText", new Vector2(-10, -10), new Vector2(80, 30), 
                "Lv.5", 18, Color.yellow, TextAlignmentOptions.Right, 
                new Vector2(1, 1), new Vector2(1, 1));
            
            CreateText(slot.transform, "HPLabel", new Vector2(10, -35), new Vector2(40, 20), 
                "HP:", 16, Color.white, TextAlignmentOptions.Left, 
                new Vector2(0, 1), new Vector2(0, 1));
            
            CreateText(slot.transform, "HPText", new Vector2(50, -35), new Vector2(80, 20), 
                "150/150", 16, Color.green, TextAlignmentOptions.Left, 
                new Vector2(0, 1), new Vector2(0, 1));
            
            CreateBar(slot.transform, "HPBar", new Vector2(140, -35), new Vector2(200, 20), Color.green);
            
            CreateText(slot.transform, "MPLabel", new Vector2(10, -60), new Vector2(40, 20), 
                "MP:", 16, Color.white, TextAlignmentOptions.Left, 
                new Vector2(0, 1), new Vector2(0, 1));
            
            CreateText(slot.transform, "MPText", new Vector2(50, -60), new Vector2(80, 20), 
                "50/50", 16, Color.cyan, TextAlignmentOptions.Left, 
                new Vector2(0, 1), new Vector2(0, 1));
            
            CreateBar(slot.transform, "MPBar", new Vector2(140, -60), new Vector2(200, 20), Color.cyan);
            
            return slot;
        }
        
        private void CreateText(Transform parent, string name, Vector2 position, Vector2 size, 
            string text, int fontSize, Color color, TextAlignmentOptions alignment,
            Vector2 anchorMin, Vector2 anchorMax)
        {
            GameObject textObj = new GameObject(name);
            textObj.transform.SetParent(parent, false);
            
            RectTransform rect = textObj.AddComponent<RectTransform>();
            rect.anchorMin = anchorMin;
            rect.anchorMax = anchorMax;
            rect.pivot = anchorMin;
            rect.anchoredPosition = position;
            rect.sizeDelta = size;
            
            TextMeshProUGUI tmp = textObj.AddComponent<TextMeshProUGUI>();
            tmp.text = text;
            tmp.fontSize = fontSize;
            tmp.color = color;
            tmp.alignment = alignment;
        }
        
        private void CreateBar(Transform parent, string name, Vector2 position, Vector2 size, Color fillColor)
        {
            GameObject barContainer = new GameObject(name);
            barContainer.transform.SetParent(parent, false);
            
            RectTransform containerRect = barContainer.AddComponent<RectTransform>();
            containerRect.anchorMin = new Vector2(0, 1);
            containerRect.anchorMax = new Vector2(0, 1);
            containerRect.pivot = new Vector2(0, 1);
            containerRect.anchoredPosition = position;
            containerRect.sizeDelta = size;
            
            GameObject bg = new GameObject("Background");
            bg.transform.SetParent(barContainer.transform, false);
            
            RectTransform bgRect = bg.AddComponent<RectTransform>();
            bgRect.anchorMin = Vector2.zero;
            bgRect.anchorMax = Vector2.one;
            bgRect.sizeDelta = Vector2.zero;
            
            Image bgImage = bg.AddComponent<Image>();
            bgImage.color = new Color(0.3f, 0.3f, 0.3f, 1f);
            
            GameObject fill = new GameObject("Fill");
            fill.transform.SetParent(barContainer.transform, false);
            
            RectTransform fillRect = fill.AddComponent<RectTransform>();
            fillRect.anchorMin = Vector2.zero;
            fillRect.anchorMax = new Vector2(0, 1);
            fillRect.pivot = new Vector2(0, 0.5f);
            fillRect.sizeDelta = Vector2.zero;
            
            Image fillImage = fill.AddComponent<Image>();
            fillImage.color = fillColor;
            fillImage.type = Image.Type.Filled;
            fillImage.fillMethod = Image.FillMethod.Horizontal;
            fillImage.fillAmount = 1f;
        }
        
        private void AssignReferences(PartyStatusUI statusUI, GameObject partyPanel)
        {
            var type = typeof(PartyStatusUI);
            
            var partyPanelField = type.GetField("partyPanel", 
                System.Reflection.BindingFlags.NonPublic | System.Reflection.BindingFlags.Instance);
            if (partyPanelField != null)
                partyPanelField.SetValue(statusUI, partyPanel);
            
            Transform memberContainer = partyPanel.transform.Find("MemberContainer");
            var memberContainerField = type.GetField("memberContainer", 
                System.Reflection.BindingFlags.NonPublic | System.Reflection.BindingFlags.Instance);
            if (memberContainerField != null)
                memberContainerField.SetValue(statusUI, memberContainer);
            
            #if UNITY_EDITOR
            GameObject prefab = UnityEditor.AssetDatabase.LoadAssetAtPath<GameObject>(SAFE_PREFAB_PATH);
            var memberSlotPrefabField = type.GetField("memberSlotPrefab", 
                System.Reflection.BindingFlags.NonPublic | System.Reflection.BindingFlags.Instance);
            if (memberSlotPrefabField != null && prefab != null)
                memberSlotPrefabField.SetValue(statusUI, prefab);
            #endif
            
            Transform goldText = partyPanel.transform.Find("Header/GoldText");
            var goldTextField = type.GetField("goldText", 
                System.Reflection.BindingFlags.NonPublic | System.Reflection.BindingFlags.Instance);
            if (goldTextField != null && goldText != null)
                goldTextField.SetValue(statusUI, goldText.GetComponent<TextMeshProUGUI>());
            
            Transform expText = partyPanel.transform.Find("Header/ExpText");
            var expTextField = type.GetField("expText", 
                System.Reflection.BindingFlags.NonPublic | System.Reflection.BindingFlags.Instance);
            if (expTextField != null && expText != null)
                expTextField.SetValue(statusUI, expText.GetComponent<TextMeshProUGUI>());
            
            Debug.Log("[PartyUIBuilderSafe] ✅ References assigned");
        }
        
        private void Start()
        {
            if (buildOnStart)
            {
                BuildPartyUI();
                Destroy(this);
            }
        }
    }
}

```


#### PetManagementUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using System.Collections.Generic;
using RebirthWarrior.Core;
using RebirthWarrior.Character;
using System.Linq;

namespace RebirthWarrior.UI
{
    public class PetManagementUI : MonoBehaviour
    {
        [Header("Left Side (Active Pet)")]
        [SerializeField] private GameObject activePetInfoRoot;
        [SerializeField] private Image activePetPortrait;
        [SerializeField] private TextMeshProUGUI activePetNameText;
        [SerializeField] private TextMeshProUGUI activePetStatsText;
        [SerializeField] private Button restButton;

        [Header("Right Side (Storage)")]
        [SerializeField] private Transform gridContent;
        [SerializeField] private GameObject petSlotPrefab;
        [SerializeField] private Button summonButton;
        [SerializeField] private TextMeshProUGUI emptyText;

        [Header("Main Panel")]
        [SerializeField] private GameObject panelRoot;
        [SerializeField] private Button closeButton;

        private List<PetSlotUI> _spawnedSlots = new List<PetSlotUI>();
        private CharacterStats _selectedInactivePet;

        private void Awake()
        {
            if (closeButton) closeButton.onClick.AddListener(Hide);
            if (restButton) restButton.onClick.AddListener(OnRestClicked);
            if (summonButton) summonButton.onClick.AddListener(OnSummonClicked);

            // Đảm bảo tắt lúc đầu
            // if (panelRoot) panelRoot.SetActive(false); // Tạm comment để test thủ công
        }

        // === THÊM HÀM NÀY ĐỂ TEST TRONG INSPECTOR ===
        private void OnEnable()
        {
            // Khi bạn tích Active trong Inspector, hàm này sẽ chạy
            RefreshUI();
        }

        public void Show()
        {
            if (panelRoot) panelRoot.SetActive(true);
            RefreshUI();
        }

        public void Hide()
        {
            if (panelRoot) panelRoot.SetActive(false);
            if (InventoryUI.Instance) InventoryUI.Instance.ShowMainPanels();
        }

        private void RefreshUI()
        {
            Debug.Log("[PetUI] Bắt đầu Refresh UI..."); // LOG 1

            var gameState = GameStateManager.Instance;
            if (gameState == null)
            {
                Debug.LogError("[PetUI] Không tìm thấy GameStateManager!");
                return;
            }

            // --- 1. UPDATE ACTIVE PET ---
            CharacterStats activePet = gameState.GetActivePet();

            if (activePet != null)
            {
                Debug.Log($"[PetUI] Active Pet: {activePet.characterName}"); // LOG 2
                if (activePetInfoRoot) activePetInfoRoot.SetActive(true);

                if (activePet.characterData != null && activePetPortrait != null)
                    activePetPortrait.sprite = activePet.characterData.portraitSprite;

                if (activePetNameText != null)
                    activePetNameText.text = activePet.characterName;

                if (activePetStatsText != null)
                    activePetStatsText.text = $"Lv.{activePet.level}\nHP: {activePet.currentHP}/{activePet.maxHP}";
            }
            else
            {
                Debug.Log("[PetUI] Không có Active Pet."); // LOG 2
                if (activePetInfoRoot) activePetInfoRoot.SetActive(false);
            }

            // --- 2. UPDATE GRID ---
            if (gridContent == null || petSlotPrefab == null)
            {
                Debug.LogError("[PetUI] Thiếu Grid Content hoặc Prefab!");
                return;
            }

            // Xóa slot cũ
            foreach (Transform child in gridContent) Destroy(child.gameObject);
            _spawnedSlots.Clear();

            // Lấy danh sách từ Roster
            var roster = gameState.GetMasterRoster();
            if (roster == null)
            {
                Debug.Log("[PetUI] Roster bị Null!");
                return;
            }

            Debug.Log($"[PetUI] Tổng nhân vật trong Roster: {roster.Count}"); // LOG 3

            var inactivePets = new List<CharacterStats>();
            foreach (var character in roster)
            {
                // Kiểm tra điều kiện Pet
                if (character != null && character.characterData != null)
                {
                    // In ra để debug xem nó tìm thấy ai
                    // Debug.Log($"[PetUI] Kiểm tra: {character.characterName} - Type: {character.characterData.type}");

                    if (character.characterData.type == CharacterType.Pet && character != activePet)
                    {
                        inactivePets.Add(character);
                    }
                }
            }

            Debug.Log($"[PetUI] Tìm thấy {inactivePets.Count} pet trong kho."); // LOG 4

            if (emptyText != null)
                emptyText.gameObject.SetActive(inactivePets.Count == 0);

            foreach (var pet in inactivePets)
            {
                GameObject obj = Instantiate(petSlotPrefab, gridContent);
                PetSlotUI ui = obj.GetComponent<PetSlotUI>();
                if (ui != null)
                {
                    ui.Setup(pet, this);
                    _spawnedSlots.Add(ui);
                }
            }

            _selectedInactivePet = null;
            if (summonButton != null) summonButton.interactable = false;
        }

        // ... (Giữ nguyên các hàm sự kiện OnPetSlotSelected, OnSummonClicked...)
        public void OnPetSlotSelected(CharacterStats pet)
        {
            _selectedInactivePet = pet;
            if (summonButton) summonButton.interactable = true;
            foreach (var slot in _spawnedSlots) slot.SetSelected(false);
        }

        private void OnSummonClicked()
        {
            if (_selectedInactivePet != null)
            {
                GameStateManager.Instance.SetActivePet(_selectedInactivePet);
                RefreshUI();
            }
        }

        private void OnRestClicked()
        {
            GameStateManager.Instance.SetActivePet(null);
            RefreshUI();
        }
    }
}
```


#### PetSlotUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Character;

namespace RebirthWarrior.UI
{
    public class PetSlotUI : MonoBehaviour
    {
        [SerializeField] private Image icon;
        [SerializeField] private TextMeshProUGUI levelText;
        [SerializeField] private Button button;
        [SerializeField] private GameObject selectedHighlight;

        private CharacterStats petStats;
        private PetManagementUI manager;

        public void Setup(CharacterStats stats, PetManagementUI uiManager)
        {
            petStats = stats;
            manager = uiManager;

            if (stats != null && stats.characterData != null)
            {
                if (icon) icon.sprite = stats.characterData.portraitSprite; // Hoặc icon riêng nếu có
                if (levelText) levelText.text = $"Lv.{stats.level}";
            }

            button.onClick.RemoveAllListeners();
            button.onClick.AddListener(OnClicked);

            SetSelected(false);
        }

        private void OnClicked()
        {
            if (manager) manager.OnPetSlotSelected(petStats);
        }

        public void SetSelected(bool isSelected)
        {
            if (selectedHighlight) selectedHighlight.SetActive(isSelected);
        }
    }
}
```


#### QuestLogSlot.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Quests;
using System; // (Cần cho 'Action')

namespace RebirthWarrior.UI
{
    /// <summary>
    /// (File MỚI - Tương thích v12)
    /// Script cho Prefab trong danh sách Quest (cột trái).
    /// File này được viết để khớp với file QuestLogUI v1.5 của bạn.
    /// </summary>
    public class QuestLogSlot : MonoBehaviour
    {
        [SerializeField] private TextMeshProUGUI questTitleText;
        [SerializeField] private Button button;

        private Quest currentQuest;
        private Action onSelect; // (Dùng 'Action' để gọi lại QuestLogUI)

        private void Awake()
        {
            if (button == null) button = GetComponent<Button>();
            button.onClick.AddListener(OnSlotClicked);
        }

        public void Setup(Quest quest, Action onSelectCallback)
        {
            currentQuest = quest;
            onSelect = onSelectCallback;

            if (questTitleText != null)
            {
                questTitleText.text = quest.questName;
                // (Lưu ý: QuestLogUI v1.5 của bạn dùng quest.questName,
                // không phải key localization, chúng ta làm theo)
            }
        }

        private void OnSlotClicked()
        {
            onSelect?.Invoke(); // Gọi lại hàm SelectQuest(currentQuest)
        }
    }
}
```


#### QuestLogUI.cs
```csharp
using RebirthWarrior.Core;
using RebirthWarrior.Quests;
using RebirthWarrior.Items;
using System.Collections.Generic;
using TMPro;
using UnityEngine;
using UnityEngine.UI;

namespace RebirthWarrior.UI
{
    public class QuestLogUI : MonoBehaviour
    {
        public static QuestLogUI Instance { get; private set; }

        [Header("1. Panels")]
        [SerializeField] private GameObject mainPanel;
        [SerializeField] private Button closeButton;
        [SerializeField] private Button tabActiveButton;
        [SerializeField] private Button tabCompletedButton;

        [Header("2. List Area")]
        [SerializeField] private Transform questListContainer;
        [Tooltip("Prefab này PHẢI có script 'QuestLogSlot'")]
        [SerializeField] private GameObject questListSlotPrefab;

        [Header("3. Detail Area")]
        [SerializeField] private GameObject detailPanelRoot;
        [SerializeField] private TextMeshProUGUI questTitleText;
        [SerializeField] private TextMeshProUGUI questDescriptionText;

        [Header("4. Objectives & Rewards")]
        [SerializeField] private Transform objectivesContainer;
        [Tooltip("Prefab này PHẢI có script 'QuestObjectiveUI'")]
        [SerializeField] private GameObject objectivePrefab;

        [SerializeField] private Transform rewardsContainer;
        [Tooltip("Có thể dùng chung Prefab với Objective hoặc tạo riêng, cần có script 'QuestObjectiveUI'")]
        [SerializeField] private GameObject rewardPrefab;

        private QuestManager questManager;

        // Pooling
        private List<GameObject> questSlotPool = new List<GameObject>();
        private List<GameObject> objectivePool = new List<GameObject>();
        private List<GameObject> rewardPool = new List<GameObject>();

        private bool showingCompleted = false;

        private void Awake()
        {
            if (Instance == null) Instance = this;
            else Destroy(gameObject);

            if (mainPanel) mainPanel.SetActive(false);
            if (closeButton) closeButton.onClick.AddListener(ClosePanel);

            if (tabActiveButton) tabActiveButton.onClick.AddListener(() => SwitchTab(false));
            if (tabCompletedButton) tabCompletedButton.onClick.AddListener(() => SwitchTab(true));
        }

        private void Start()
        {
            questManager = QuestManager.Instance;
        }

        public void OpenPanel()
        {
            if (mainPanel) mainPanel.SetActive(true);
            ForceRefresh();
        }

        public void ClosePanel()
        {
            if (mainPanel) mainPanel.SetActive(false);
        }

        public void Toggle()
        {
            if (mainPanel.activeSelf) ClosePanel();
            else OpenPanel();
        }

        private void SwitchTab(bool completed)
        {
            showingCompleted = completed;
            ForceRefresh();
        }

        private void ForceRefresh()
        {
            if (questManager == null) questManager = QuestManager.Instance;
            if (questManager == null) return;

            PopulateQuestList();
            if (detailPanelRoot) detailPanelRoot.SetActive(false);
        }

        private void PopulateQuestList()
        {
            foreach (var slot in questSlotPool) slot.SetActive(false);

            List<Quest> quests = showingCompleted ? questManager.GetCompletedQuests() : questManager.GetActiveQuests();

            if (quests == null) return;

            for (int i = 0; i < quests.Count; i++)
            {
                if (quests[i] == null) continue;

                GameObject slotObj = GetPoolObject(questSlotPool, questListSlotPrefab, questListContainer);

                // === [FIX LỖI OUT OF RANGE] ===
                // Phải tạo biến cục bộ 'q' để lambda function bắt đúng giá trị
                Quest q = quests[i];

                var slotScript = slotObj.GetComponent<QuestLogSlot>();
                if (slotScript != null)
                {
                    // Truyền 'q' vào thay vì 'quests[i]'
                    slotScript.Setup(q, () => ShowDetail(q));
                }
                else
                {
                    Debug.LogError($"Prefab '{questListSlotPrefab.name}' đang thiếu script 'QuestLogSlot'!");
                }
            }
        }

        private void ShowDetail(Quest quest)
        {
            if (quest == null) return;
            if (detailPanelRoot) detailPanelRoot.SetActive(true);

            // 1. Info
            if (questTitleText) questTitleText.text = !string.IsNullOrEmpty(quest.questName) ? quest.questName : quest.name;
            if (questDescriptionText) questDescriptionText.text = quest.description;

            // Lấy status từ Manager
            QuestStatus status = questManager.GetQuestStatus(quest.questID);

            // 2. Objectives (Sử dụng QuestObjectiveUI)
            foreach (var obj in objectivePool) obj.SetActive(false);

            if (quest.objectives != null && objectivesContainer != null)
            {
                foreach (var obj in quest.objectives)
                {
                    if (obj == null) continue;

                    GameObject objGO = GetPoolObject(objectivePool, objectivePrefab, objectivesContainer);

                    var objUI = objGO.GetComponent<QuestObjectiveUI>();
                    if (objUI != null)
                    {
                        int current = 0;
                        if (status != null && status.objectiveProgress != null && status.objectiveProgress.ContainsKey(obj.targetID))
                            current = status.objectiveProgress[obj.targetID];

                        objUI.Setup(obj, current);
                    }
                }
            }

            // 3. Rewards (Sử dụng QuestObjectiveUI setup manual)
            foreach (var r in rewardPool) r.SetActive(false);

            if (rewardsContainer != null)
            {
                // Gold
                if (quest.rewardGold > 0)
                {
                    SpawnRewardUI("Vàng", quest.rewardGold);
                }
                // EXP
                if (quest.rewardExp > 0)
                {
                    SpawnRewardUI("Kinh nghiệm", quest.rewardExp);
                }
                // Items
                if (quest.rewardItems != null)
                {
                    foreach (var item in quest.rewardItems)
                    {
                        if (item != null) SpawnRewardUI(item.itemName, 1);
                    }
                }
            }

            // Fix Layout
            LayoutRebuilder.ForceRebuildLayoutImmediate(detailPanelRoot.GetComponent<RectTransform>());
        }

        private void SpawnRewardUI(string name, int amount)
        {
            GameObject rGO = GetPoolObject(rewardPool, rewardPrefab, rewardsContainer);
            var rUI = rGO.GetComponent<QuestObjectiveUI>();

            if (rUI != null)
            {
                rUI.SetupManual(name, amount);
            }
        }

        private GameObject GetPoolObject(List<GameObject> pool, GameObject prefab, Transform container)
        {
            foreach (var obj in pool)
            {
                if (!obj.activeSelf)
                {
                    obj.transform.SetParent(container, false);
                    obj.transform.localScale = Vector3.one;
                    obj.SetActive(true);
                    return obj;
                }
            }
            if (prefab == null) return new GameObject("Missing_Prefab");
            GameObject newObj = Instantiate(prefab, container);
            newObj.transform.localScale = Vector3.one;
            pool.Add(newObj);
            return newObj;
        }
    }
}
```



#### QuestObjectiveUI.cs
```csharp
using UnityEngine;
using TMPro;
using RebirthWarrior.Quests; // <-- THÊM DÒNG NÀY (Sửa lỗi CS0246)
using RebirthWarrior.Core;

namespace RebirthWarrior.UI
{
    /// <summary>
    /// Version 1.2 - Sửa lỗi Namespace (CS0101) và CS0246
    /// Đây là file GIAO DIỆN (MonoBehaviour)
    /// </summary>
    public class QuestObjectiveUI : MonoBehaviour
    {
        [SerializeField] private TextMeshProUGUI objectiveText;
        [SerializeField] private TextMeshProUGUI progressText;

        /// <summary>
        /// Gán data từ một QuestObjective (SO)
        /// </summary>
        public void Setup(QuestObjective objective, int currentProgress)
        {
            if (LocalizationManager.Instance != null && !string.IsNullOrEmpty(objective.objectiveNameKey))
            {
                objectiveText.text = LocalizationManager.Instance.GetLocalizedText(objective.objectiveNameKey);
            }
            else
            {
                objectiveText.text = objective.objectiveID;
            }

            progressText.text = $"{currentProgress} / {objective.requiredAmount}";

            if (currentProgress >= objective.requiredAmount)
            {
                objectiveText.fontStyle = FontStyles.Strikethrough;
                progressText.color = Color.green;
            }
            else
            {
                objectiveText.fontStyle = FontStyles.Normal;
                progressText.color = Color.white;
            }
        }

        /// <summary>
        /// Gán data thủ công (dùng để hiển thị Rewards)
        /// </summary>
        public void SetupManual(string text, int amount)
        {
            objectiveText.text = text;
            progressText.text = $"+{amount}";
            objectiveText.fontStyle = FontStyles.Normal;
            progressText.color = Color.yellow;
        }
    }
}
```


#### SaveLoadManager.cs
```csharp
using UnityEngine;
using System.Collections;
using System.Collections.Generic;
using TMPro;
using UnityEngine.SceneManagement;
using UnityEngine.UI;
using RebirthWarrior.SaveLoad;
using RebirthWarrior.Core;
using RebirthWarrior.Inventory;
using RebirthWarrior.Quests;
using RebirthWarrior.Character;

namespace RebirthWarrior.UI
{
    public enum SaveLoadMode { Save, Load }

    public class SaveLoadManager : MonoBehaviour
    {
        public static SaveLoadManager Instance;

        [Header("UI REFERENCES")]
        [SerializeField] private GameObject mainPanel;
        [SerializeField] private TextMeshProUGUI titleText;
        [SerializeField] private Button closeButton;

        [Header("SLOT CONFIGURATION")]
        [SerializeField] private Transform slotsContainer;
        [SerializeField] private GameObject saveSlotPrefab;
        [SerializeField] private int maxSlots = 4;

        private List<SaveSlotUI> instantiatedSlots = new List<SaveSlotUI>();
        private SaveLoadMode currentMode;

        private void Awake()
        {
            if (Instance == null) { Instance = this; DontDestroyOnLoad(gameObject); }
            else { Destroy(gameObject); return; }

            if (mainPanel) mainPanel.SetActive(false);
            if (closeButton) closeButton.onClick.AddListener(ClosePanel);
        }

        private void Start()
        {
            CreateSlots();
        }

        private void CreateSlots()
        {
            if (slotsContainer == null || saveSlotPrefab == null) return;

            foreach (Transform child in slotsContainer) Destroy(child.gameObject);
            instantiatedSlots.Clear();

            for (int i = 0; i < maxSlots; i++)
            {
                GameObject slotObj = Instantiate(saveSlotPrefab, slotsContainer);
                SaveSlotUI slotUI = slotObj.GetComponent<SaveSlotUI>();
                if (slotUI != null)
                {
                    slotUI.Setup(i, this);
                    instantiatedSlots.Add(slotUI);
                }
            }
        }

        public void OpenSavePanel()
        {
            if (mainPanel == null) return;
            currentMode = SaveLoadMode.Save;
            if (titleText) titleText.text = "LƯU GAME";
            mainPanel.SetActive(true);
            RefreshAllSlots();
            Time.timeScale = 0f;
        }

        public void OpenLoadPanel()
        {
            if (mainPanel == null) return;
            currentMode = SaveLoadMode.Load;
            if (titleText) titleText.text = "TẢI GAME";
            mainPanel.SetActive(true);
            RefreshAllSlots();
            if (SceneManager.GetActiveScene().name != "MainMenu") Time.timeScale = 0f;
        }

        public void ClosePanel()
        {
            if (mainPanel) mainPanel.SetActive(false);
            if (SceneManager.GetActiveScene().name != "MainMenu") Time.timeScale = 1f;
        }

        public void RefreshAllSlots()
        {
            foreach (var slot in instantiatedSlots) slot.RefreshUI();
        }

        public void OnSlotSelected(int index, bool hasData)
        {
            if (currentMode == SaveLoadMode.Save) StartCoroutine(CaptureAndSave(index));
            else if (currentMode == SaveLoadMode.Load && hasData) LoadGameProcess(index);
        }

        public void OnDeleteRequested(int index)
        {
            SaveSystem.DeleteSave(index);
            RefreshAllSlots();
        }

        private IEnumerator CaptureAndSave(int index)
        {
            float originalTime = Time.timeScale;
            Time.timeScale = 1f;
            if (mainPanel) mainPanel.SetActive(false);
            yield return new WaitForEndOfFrame();

            Texture2D screenShot = ScreenCapture.CaptureScreenshotAsTexture();
            if (mainPanel) mainPanel.SetActive(true);
            Time.timeScale = originalTime;

            GameSaveData data = CollectGameData();
            SaveSystem.SaveGame(data, index, screenShot);
            RefreshAllSlots();
        }

        private GameSaveData CollectGameData()
        {
            GameSaveData data = new GameSaveData();
            data.saveDate = System.DateTime.Now.ToString("dd/MM/yyyy HH:mm");

            string activeScene = SceneManager.GetActiveScene().name;
            data.currentScene = activeScene;
            data.locationName = GetLocationDisplayName(activeScene);

            if (GameStateManager.Instance)
            {
                var gs = GameStateManager.Instance;
                data.gold = gs.GetGold();
                data.hasBeenReborn = gs.hasBeenReborn;

                var main = gs.GetMainPlayer();
                data.playerName = main != null ? main.characterName : "Hero";
                data.playerLevel = main != null ? main.level : 1;

                foreach (var member in gs.GetMasterRoster())
                {
                    CharSaveData cData = new CharSaveData();
                    cData.charID = (member.characterData != null) ? member.characterData.characterID : member.characterID;
                    cData.customName = member.characterName;
                    cData.level = member.level;
                    cData.curHP = member.currentHP;

                    // Map Stamina/Toxic vào Save Data cũ
                    cData.curMP = member.currentStamina;
                    cData.baseMaxMP = member.baseMaxStamina;
                    cData.baseMag = member.baseToxicAttack;
                    cData.baseMDef = member.baseToxicResist;

                    cData.currentExp = member.currentExp;
                    cData.baseAtk = member.baseAttack;
                    cData.baseDef = member.baseDefense;
                    cData.baseSpd = member.baseSpeed;
                    cData.baseAgi = member.baseAgility;
                    cData.baseLuck = member.baseLuck;
                    cData.baseMaxHP = member.baseMaxHP;
                    cData.unspentPoints = member.unspentStatPoints;

                    cData.isCustom = member.isCustomCharacter;
                    cData.genderIdx = member.genderIndex;
                    cData.bodyIdx = member.bodyIndex;
                    cData.hairIdx = member.hairIndex;
                    cData.eyesIdx = member.eyesIndex;

                    foreach (var kvp in member.equippedItems)
                    {
                        if (kvp.Value != null)
                        {
                            cData.equippedItems.Add(new EquipSaveData { slotIndex = (int)kvp.Key, itemID = kvp.Value.itemID });
                        }
                    }

                    if (member.learnedSkills != null)
                    {
                        foreach (var skill in member.learnedSkills)
                            if (skill != null) cData.learnedSkillIDs.Add(skill.name);
                    }

                    data.partyMembers.Add(cData);
                }
            }

            var playerCtrl = FindObjectOfType<RebirthWarrior.World.PlayerController>();
            if (playerCtrl) { data.posX = playerCtrl.transform.position.x; data.posY = playerCtrl.transform.position.y; }

            if (activeScene == "WorldScene") { data.worldReturnX = data.posX; data.worldReturnY = data.posY; }
            else { data.worldReturnX = PlayerPrefs.GetFloat("WorldPositionX", 0f); data.worldReturnY = PlayerPrefs.GetFloat("WorldPositionY", 0f); }

            if (InventoryManager.Instance)
            {
                foreach (var slot in InventoryManager.Instance.GetAllItems())
                    if (slot?.item != null)
                        data.inventoryItems.Add(new ItemSaveData { itemID = slot.item.itemID, amount = slot.quantity });
            }

            // === [FIX LỖI SAVE QUEST] ===
            if (QuestManager.Instance)
            {
                foreach (var q in QuestManager.Instance.GetActiveQuests())
                {
                    QuestSaveData qData = new QuestSaveData { questID = q.questID };

                    // [FIX] Lấy status từ Manager thay vì từ Quest object
                    var status = QuestManager.Instance.GetQuestStatus(q.questID);
                    if (status != null)
                    {
                        foreach (var kvp in status.objectiveProgress)
                            qData.objectivesProgress.Add($"{kvp.Key}:{kvp.Value}");
                    }

                    data.activeQuests.Add(qData);
                }
                foreach (var q in QuestManager.Instance.GetCompletedQuests()) data.completedQuests.Add(q.questID);
            }
            // ============================

            return data;
        }

        private void LoadGameProcess(int index)
        {
            GameSaveData data = SaveSystem.LoadGameData(index);
            if (data == null) return;

            if (GameStateManager.Instance) GameStateManager.Instance.LoadFromData(data);
            if (InventoryManager.Instance) InventoryManager.Instance.LoadFromData(data);
            if (QuestManager.Instance) QuestManager.Instance.LoadFromData(data);

            PlayerPrefs.SetFloat("WorldPositionX", data.worldReturnX);
            PlayerPrefs.SetFloat("WorldPositionY", data.worldReturnY);
            PlayerPrefs.DeleteKey("ReturningFromBattle");
            PlayerPrefs.DeleteKey("ReturningFromTown");
            PlayerPrefs.SetInt("IsLoadingGame", 1);
            PlayerPrefs.SetFloat("LoadPosX", data.posX);
            PlayerPrefs.SetFloat("LoadPosY", data.posY);
            PlayerPrefs.Save();

            ClosePanel();
            SceneManager.LoadScene(data.currentScene);
        }

        private string GetLocationDisplayName(string sceneName)
        {
            switch (sceneName)
            {
                case "WorldScene": return "Thế Giới";
                case "TownScene": return "Thị Trấn";
                case "Battle": return "Chiến Trường";
                default: return sceneName;
            }
        }
    }
}
```


#### SaveSlotUI.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.SaveLoad;
using RebirthWarrior.Character;

namespace RebirthWarrior.UI
{
    public class SaveSlotUI : MonoBehaviour
    {
        [SerializeField] private int slotIndex;

        [Header("THÀNH PHẦN UI (Kéo từ Prefab SaveSlot)")]
        [SerializeField] private GameObject contentGroup; // Chứa info (Ẩn khi trống)
        [SerializeField] private TextMeshProUGUI emptyText; // Text "Trống"

        [Header("1. KHU VỰC ĐỘI HÌNH")]
        [SerializeField] private Transform partyContainer; // Object chứa Layout Group ngang
        [SerializeField] private GameObject partyMemberIconPrefab; // File Prefab Icon nhỏ

        [Header("2. KHU VỰC THÔNG TIN")]
        [SerializeField] private TextMeshProUGUI goldText;
        [SerializeField] private TextMeshProUGUI dateText;

        [Header("3. KHU VỰC BẢN ĐỒ")]
        [SerializeField] private TextMeshProUGUI locationText;
        [SerializeField] private Image mapImage;

        [Header("BUTTONS")]
        [SerializeField] private Button slotButton; // Nút to
        [SerializeField] private Button deleteButton; // Nút xóa

        private SaveLoadManager manager;
        private bool hasData;

        public void Setup(int index, SaveLoadManager managerRef)
        {
            slotIndex = index;
            manager = managerRef;

            slotButton.onClick.RemoveAllListeners();
            slotButton.onClick.AddListener(OnClick);

            if (deleteButton)
            {
                deleteButton.onClick.RemoveAllListeners();
                deleteButton.onClick.AddListener(OnDelete);
            }
            RefreshUI();
        }

        public void RefreshUI()
        {
            GameSaveData data = SaveSystem.LoadGameData(slotIndex);
            hasData = (data != null);

            if (hasData)
            {
                // Có dữ liệu -> Bật Content, Tắt EmptyText
                if (contentGroup) contentGroup.SetActive(true);
                if (emptyText) emptyText.gameObject.SetActive(false);
                if (deleteButton) deleteButton.gameObject.SetActive(true);

                // YÊU CẦU 2: HIỂN THỊ VÀNG
                if (goldText) goldText.text = $"{data.gold:N0} G";

                // HIỂN THỊ NGÀY
                if (dateText) dateText.text = data.saveDate;

                // YÊU CẦU 3: HIỂN THỊ TÊN BẢN ĐỒ
                if (locationText) locationText.text = string.IsNullOrEmpty(data.locationName) ? data.currentScene : data.locationName;

                // HIỂN THỊ ẢNH
                Sprite screen = SaveSystem.LoadScreenshot(slotIndex);
                if (screen != null && mapImage != null) mapImage.sprite = screen;

                // YÊU CẦU 1: HIỂN THỊ ICON ĐỘI HÌNH
                UpdatePartyDisplay(data);
            }
            else
            {
                // Slot trống
                if (contentGroup) contentGroup.SetActive(false);
                if (emptyText) emptyText.gameObject.SetActive(true);
                if (deleteButton) deleteButton.gameObject.SetActive(false);
            }
        }

        private void UpdatePartyDisplay(GameSaveData data)
        {
            if (!partyContainer || !partyMemberIconPrefab) return;

            // Xóa icon cũ
            foreach (Transform child in partyContainer) Destroy(child.gameObject);

            int count = 0;
            foreach (var charData in data.partyMembers)
            {
                if (count++ > 4) break; // Giới hạn 5 người

                GameObject iconObj = Instantiate(partyMemberIconPrefab, partyContainer);

                // --- 1. LOAD DATA ---
                // Code sẽ tìm trong Resources/Data/Characters/ID
                CharacterData asset = Resources.Load<CharacterData>($"Data/Characters/{charData.charID}");
                // Fallback: Tìm thẳng trong Resources/ID
                if (!asset) asset = Resources.Load<CharacterData>(charData.charID);

                // --- 2. GÁN AVATAR ---
                Image avatar = iconObj.transform.Find("Avatar")?.GetComponent<Image>();
                if (avatar)
                {
                    if (asset != null && asset.icon != null)
                    {
                        avatar.sprite = asset.icon; // Quan trọng: Phải gán 'Icon' trong CharacterData
                        avatar.enabled = true;
                    }
                    else
                    {
                        // Nếu không tìm thấy ảnh, tắt Image đi để đỡ hiện ô vuông trắng xấu xí
                        // avatar.enabled = false; 

                        // Hoặc gán ảnh mặc định nếu có
                        // avatar.sprite = defaultIcon;
                    }
                }

                // --- 3. GÁN LEVEL ---
                TextMeshProUGUI lvl = iconObj.transform.Find("Level")?.GetComponent<TextMeshProUGUI>();
                if (lvl) lvl.text = $"{charData.level}";

                // --- 4. GÁN TÊN (PHẦN BẠN BỊ THIẾU) ---
                // Tìm object con tên là "Name" (như trong Prefab bạn đã tạo)
                TextMeshProUGUI nameTxt = iconObj.transform.Find("Name")?.GetComponent<TextMeshProUGUI>();
                if (nameTxt)
                {
                    nameTxt.text = charData.customName; // Lấy tên đã lưu
                }
            }
        }

        private void OnClick() { if (manager) manager.OnSlotSelected(slotIndex, hasData); }
        private void OnDelete() { if (manager) manager.OnDeleteRequested(slotIndex); }
    }
}
```


#### UISetupHelper.cs
```csharp
using UnityEngine;
using UnityEngine.UI;

/// <summary>
/// Script tự động setup UI panels với đúng size và anchor
/// Attach vào Canvas và chạy 1 lần
/// </summary>
public class UISetupHelper : MonoBehaviour
{
    [Header("Assign These in Inspector")]
    public RectTransform partyPanel;
    public RectTransform enemyPanel;
    public RectTransform battleLogPanel;
    public RectTransform actionPanel;
    
    [Header("Container References")]
    public RectTransform partyMembersContainer;
    public RectTransform enemiesContainer;
    
    [Header("Settings")]
    public bool autoSetupOnStart = true;
    
    [ContextMenu("Setup UI Panels")]
    public void SetupPanels()
    {
        if (partyPanel != null)
        {
            SetupPartyPanel();
            Debug.Log("✅ PartyPanel setup complete!");
        }
        
        if (enemyPanel != null)
        {
            SetupEnemyPanel();
            Debug.Log("✅ EnemyPanel setup complete!");
        }
        
        if (battleLogPanel != null)
        {
            SetupBattleLogPanel();
            Debug.Log("✅ BattleLogPanel setup complete!");
        }
        
        if (actionPanel != null)
        {
            SetupActionPanel();
            Debug.Log("✅ ActionPanel setup complete!");
        }
        
        // Setup containers
        if (partyMembersContainer != null)
        {
            SetupPartyMembersContainer();
            Debug.Log("✅ PartyMembersContainer setup complete!");
        }
        
        if (enemiesContainer != null)
        {
            SetupEnemiesContainer();
            Debug.Log("✅ EnemiesContainer setup complete!");
        }
        
        Debug.Log("🎉 All UI panels setup successfully!");
    }
    
    private void Start()
    {
        if (autoSetupOnStart)
        {
            SetupPanels();
        }
    }

    /// <summary>
    /// Setup PartyPanel - Left side, stretch vertically
    /// </summary>
    private void SetupPartyPanel()
    {
        // Neo Panel cha vào 30% bên trái màn hình (để dành không gian cho EnemyPanel)
        partyPanel.anchorMin = new Vector2(0, 0);
        partyPanel.anchorMax = new Vector2(0.3f, 1); // <--- Tỷ lệ 30%

        partyPanel.pivot = new Vector2(0, 0.5f);
        partyPanel.anchoredPosition = Vector2.zero; // Bỏ vị trí cố định

        // Đặt margin (offset) để Panel căng ra giữa các điểm neo
        // 10px lề trái, 10px lề phải (từ 30% màn hình), 250px từ dưới, -100px từ trên
        partyPanel.offsetMin = new Vector2(10, 250);    // Left, Bottom
        partyPanel.offsetMax = new Vector2(-10, -100);  // Right, Top (Tính từ anchorMax)

        partyPanel.sizeDelta = Vector2.zero; // Đặt sizeDelta về 0 để sử dụng offset
    }

    /// <summary>
    /// Setup EnemyPanel - Right side, stretch vertically
    /// </summary>
    private void SetupEnemyPanel()
    {
        // Neo Panel cha vào 70% bên phải màn hình
        enemyPanel.anchorMin = new Vector2(0.3f, 0); // Bắt đầu từ 30% màn hình
        enemyPanel.anchorMax = new Vector2(1, 1);

        enemyPanel.pivot = new Vector2(1, 0.5f);
        enemyPanel.anchoredPosition = Vector2.zero; // Bỏ vị trí cố định

        // Đặt margin
        // 10px lề trái (từ 30% màn hình), 10px lề phải (từ 100% màn hình), 250px từ dưới, -100px từ trên
        enemyPanel.offsetMin = new Vector2(10, 250);   // Left, Bottom
        enemyPanel.offsetMax = new Vector2(-10, -100);  // Right, Top

        enemyPanel.sizeDelta = Vector2.zero; // Đặt sizeDelta về 0 để sử dụng offset
    }

    /// <summary>
    /// Setup BattleLogPanel - Bottom center
    /// </summary>
    private void SetupBattleLogPanel()
    {
        // Set anchor to bottom-stretch
        battleLogPanel.anchorMin = new Vector2(0, 0);
        battleLogPanel.anchorMax = new Vector2(1, 0);
        
        // Set pivot
        battleLogPanel.pivot = new Vector2(0.5f, 0);
        
        // Set size and position
        battleLogPanel.anchoredPosition = new Vector2(0, 160);
        battleLogPanel.sizeDelta = new Vector2(-200, 120); // Margin 100 left/right, height 120
        
        Debug.Log($"BattleLogPanel: Size: {battleLogPanel.rect.size}");
    }
    
    /// <summary>
    /// Setup ActionPanel - Bottom center
    /// </summary>
    private void SetupActionPanel()
    {
        // Set anchor to bottom-center
        actionPanel.anchorMin = new Vector2(0.5f, 0);
        actionPanel.anchorMax = new Vector2(0.5f, 0);
        
        // Set pivot
        actionPanel.pivot = new Vector2(0.5f, 0);
        
        // Set size and position
        actionPanel.anchoredPosition = new Vector2(0, 20);
        actionPanel.sizeDelta = new Vector2(1200, 140);
        
        Debug.Log($"ActionPanel: Size: {actionPanel.rect.size}");
    }
    
    /// <summary>
    /// Setup PartyMembersContainer with proper Layout Group
    /// </summary>
    private void SetupPartyMembersContainer()
    {
        // Ensure VerticalLayoutGroup exists
        VerticalLayoutGroup vlg = partyMembersContainer.GetComponent<VerticalLayoutGroup>();
        if (vlg == null)
        {
            vlg = partyMembersContainer.gameObject.AddComponent<VerticalLayoutGroup>();
        }
        
        // Configure Vertical Layout Group - CRITICAL SETTINGS
        vlg.childControlWidth = false;
        vlg.childControlHeight = false;  // MUST BE TRUE!
        vlg.childForceExpandWidth = false;
        vlg.childForceExpandHeight = false;
        vlg.childScaleWidth = false;
        vlg.childScaleHeight = false;
        vlg.childAlignment = TextAnchor.UpperCenter;
        vlg.spacing = 10;
        vlg.padding = new RectOffset(10, 10, 10, 10);

        // Thiết lập Container con STRETCH hoàn toàn trong Panel cha
        partyMembersContainer.anchorMin = Vector2.zero;
        partyMembersContainer.anchorMax = Vector2.one;
        partyMembersContainer.anchoredPosition = Vector2.zero;
        partyMembersContainer.sizeDelta = Vector2.zero;

        Debug.Log($"PartyMembersContainer: Layout Group configured (ControlHeight={vlg.childControlHeight})");
    }
    
    /// <summary>
    /// Setup EnemiesContainer with proper Layout Group
    /// </summary>
    private void SetupEnemiesContainer()
    {
        // Ensure HorizontalLayoutGroup exists
        HorizontalLayoutGroup hlg = enemiesContainer.GetComponent<HorizontalLayoutGroup>();
        if (hlg == null)
        {
            hlg = enemiesContainer.gameObject.AddComponent<HorizontalLayoutGroup>();
        }
        
        // Configure Horizontal Layout Group - CRITICAL SETTINGS
        hlg.childControlWidth = false;
        hlg.childControlHeight = false;  // MUST BE TRUE!
        hlg.childForceExpandWidth = false;
        hlg.childForceExpandHeight = false;
        hlg.childScaleWidth = false;
        hlg.childScaleHeight = false;
        hlg.childAlignment = TextAnchor.MiddleCenter;
        hlg.spacing = 20;
        hlg.padding = new RectOffset(20, 20, 20, 20);

        // Thiết lập Container con STRETCH hoàn toàn trong Panel cha
        enemiesContainer.anchorMin = Vector2.zero;
        enemiesContainer.anchorMax = Vector2.one;
        enemiesContainer.anchoredPosition = Vector2.zero;
        enemiesContainer.sizeDelta = Vector2.zero;

        Debug.Log($"EnemiesContainer: Layout Group configured (ControlHeight={hlg.childControlHeight})");
    }
    
    /// <summary>
    /// Reset về mặc định nếu cần
    /// </summary>
    [ContextMenu("Reset to Default")]
    public void ResetToDefault()
    {
        if (partyPanel != null)
        {
            partyPanel.anchorMin = Vector2.zero;
            partyPanel.anchorMax = Vector2.one;
            partyPanel.anchoredPosition = Vector2.zero;
            partyPanel.sizeDelta = Vector2.zero;
        }
        
        if (enemyPanel != null)
        {
            enemyPanel.anchorMin = Vector2.zero;
            enemyPanel.anchorMax = Vector2.one;
            enemyPanel.anchoredPosition = Vector2.zero;
            enemyPanel.sizeDelta = Vector2.zero;
        }
        
        Debug.Log("Reset to default complete");
    }
    
    /// <summary>
    /// Debug - In ra thông tin các panels
    /// </summary>
    [ContextMenu("Debug Panel Info")]
    public void DebugPanelInfo()
    {
        if (partyPanel != null)
        {
            Debug.Log($"PartyPanel:\n" +
                     $"  Anchor: Min={partyPanel.anchorMin}, Max={partyPanel.anchorMax}\n" +
                     $"  Position: {partyPanel.anchoredPosition}\n" +
                     $"  Size: {partyPanel.sizeDelta}\n" +
                     $"  Rect: {partyPanel.rect}");
        }
        
        if (enemyPanel != null)
        {
            Debug.Log($"EnemyPanel:\n" +
                     $"  Anchor: Min={enemyPanel.anchorMin}, Max={enemyPanel.anchorMax}\n" +
                     $"  Position: {enemyPanel.anchoredPosition}\n" +
                     $"  Size: {enemyPanel.sizeDelta}\n" +
                     $"  Rect: {enemyPanel.rect}");
        }
    }
}

```



#### WorldUIManager.cs
```csharp
using UnityEngine;
using RebirthWarrior.UI;
using UnityEngine.SceneManagement;
using System.Collections.Generic; // <-- SỬA LỖI CS0246 TẠI ĐÂY

namespace RebirthWarrior.UI
{
    /// <summary>
    /// Version 1.4 - Sửa lỗi CS0246 (Missing List<>)
    /// Đặt trên InventoryUI_Persistent (ở MainMenu)
    /// </summary>
    public class WorldUIManager : MonoBehaviour
    {
        public static WorldUIManager Instance { get; private set; }

        [Header("Scene-Aware UI")]
        [Tooltip("Kéo Panel/GameObject cha chứa các nút (Inventory, Quest) sẽ HIỂN THỊ trong World/Town vào đây")]
        [SerializeField] private GameObject worldButtonsContainer;
        // === CẬP NHẬT DANH SÁCH SCENE TẠI ĐÂY ===
        private readonly List<string> worldScenes = new List<string> {
            "WorldScene",
            "TownScene",
            "Map_HCMC_2025",
            "Map_HCMC_2100",
            "Map_HCMC_2060" // Thêm các map cốt truyện vào đây
        };
        // (Tên các scene mà UI này được phép hiển thị)
        // (Dòng 20 - Giờ đã hợp lệ)

        private void Awake()
        {
            if (Instance != null && Instance != this)
            {
                Destroy(gameObject);
            }
            else
            {
                Instance = this;
                // (Không cần DontDestroyOnLoad vì nó được gắn trên 
                // GameObject InventoryUI_Persistent đã có DontDestroyOnLoad)
            }
        }

        // ==========================================================
        // LOGIC MỚI ĐỂ QUẢN LÝ ẨN/HIỆN UI THEO SCENE (PHASE 11)
        // ==========================================================

        private void OnEnable()
        {
            // Đăng ký lắng nghe sự kiện khi một scene được tải
            SceneManager.sceneLoaded += OnSceneLoaded;
        }

        private void OnDisable()
        {
            // Hủy đăng ký
            SceneManager.sceneLoaded -= OnSceneLoaded;
        }

        /// <summary>
        /// Hàm này được gọi tự động mỗi khi một scene mới tải xong.
        /// </summary>
        private void OnSceneLoaded(Scene scene, LoadSceneMode mode)
        {
            if (worldButtonsContainer == null)
            {
                Debug.LogWarning("[WorldUIManager] 'World Buttons Container' chưa được gán!");
                return;
            }

            // Kiểm tra xem tên của scene vừa tải có nằm trong danh sách
            // các scene được phép hiển thị (WorldScene, TownScene) không.
            if (worldScenes.Contains(scene.name))
            {
                // Nếu ĐÚNG (là WorldScene/TownScene), BẬT UI
                worldButtonsContainer.SetActive(true);
            }
            else
            {
                // Nếu SAI (là MainMenu/BattleScene), TẮT UI
                worldButtonsContainer.SetActive(false);
            }
        }

        // ==========================================================
        // (CÁC HÀM TOGGLE KHÔNG ĐỔI)
        // =---------------------------------------------------------

        /// <summary>
        /// Được gọi bởi Nút "Button_Inventory" OnClick hoặc phím 'I'.
        /// </summary>
        public void ToggleInventoryPanel()
        {
            if (InventoryUI.Instance != null)
            {
                InventoryUI.Instance.ToggleInventory();
            }
            else
            {
                Debug.LogError("[WorldUIManager] Không tìm thấy InventoryUI.Instance!");
            }
        }

        /// <summary>
        /// Được gọi bởi phím 'L' (PlayerController) hoặc Nút "Quest" (InventoryUI)
        /// </summary>
        public void ToggleQuestLogPanel()
        {
            if (QuestLogUI.Instance != null)
            {
                QuestLogUI.Instance.Toggle();
            }
            else
            {
                Debug.LogError("[WorldUIManager] Không tìm thấy QuestLogUI.Instance! Panel_QuestLog đã được tạo (là con của InventoryUI_Persistent) chưa?");
            }
        }
    }
}
```



### C13. World Scripts

#### CameraController.cs
```csharp
using UnityEngine;

namespace RebirthWarrior.World
{
    public class CameraController : MonoBehaviour
    {
        [Header("Target")]
        [SerializeField] private Transform target;
        [SerializeField] private string playerTag = "Player";

        [Header("Settings")]
        [SerializeField] private float smoothSpeed = 5f;
        [SerializeField] private Vector2 minBounds = new Vector2(-20, -20);
        [SerializeField] private Vector2 maxBounds = new Vector2(20, 20);

        private void Awake()
        {
            if (target == null)
            {
                GameObject playerObj = GameObject.FindGameObjectWithTag(playerTag);
                if (playerObj != null) target = playerObj.transform;
            }
        }

        // Bằng dòng này (Dùng SmoothDamp sẽ mượt và ít bị trễ hơn Lerp):
        private Vector3 currentVelocity; // Biến phụ cho SmoothDamp
        [SerializeField] private float smoothTime = 0.15f; // Thời gian để camera đuổi kịp (0.1 - 0.2 là đẹp)

        private void LateUpdate()
        {
            if (target == null) return;

            // Dùng SmoothDamp thay vì Lerp
            Vector3 targetPosition = target.position;
            targetPosition.z = transform.position.z;

            Vector3 smoothedPosition = Vector3.SmoothDamp(transform.position, targetPosition, ref currentVelocity, smoothTime);

            // Clamp
            float clampedX = Mathf.Clamp(smoothedPosition.x, minBounds.x, maxBounds.x);
            float clampedY = Mathf.Clamp(smoothedPosition.y, minBounds.y, maxBounds.y);

            transform.position = new Vector3(clampedX, clampedY, transform.position.z);
        }
    }
}
```


#### CameraFollow.cs
```csharp
using UnityEngine;

namespace RebirthWarrior.World
{
    /// <summary>
    /// Camera follows player smoothly on world map
    /// </summary>
    public class CameraFollow : MonoBehaviour
    {
        [Header("Target")]
        [SerializeField] private Transform target;
        
        [Header("Follow Settings")]
        [SerializeField] private float smoothSpeed = 5f;
        [SerializeField] private Vector3 offset = new Vector3(0f, 0f, -10f);
        
        [Header("Boundaries (Optional)")]
        [SerializeField] private bool useBoundaries = false;
        [SerializeField] private Vector2 minBounds;
        [SerializeField] private Vector2 maxBounds;
        
        private void LateUpdate()
        {
            if (target == null)
            {
                // Try to find player if not assigned
                var player = GameObject.FindGameObjectWithTag("Player");
                if (player != null)
                {
                    target = player.transform;
                }
                return;
            }
            
            FollowTarget();
        }
        
        /// <summary>
        /// Follow target smoothly
        /// </summary>
        private void FollowTarget()
        {
            // Calculate desired position
            Vector3 desiredPosition = target.position + offset;
            
            // Apply boundaries if enabled
            if (useBoundaries)
            {
                desiredPosition.x = Mathf.Clamp(desiredPosition.x, minBounds.x, maxBounds.x);
                desiredPosition.y = Mathf.Clamp(desiredPosition.y, minBounds.y, maxBounds.y);
            }
            
            // Smoothly move camera
            Vector3 smoothedPosition = Vector3.Lerp(transform.position, desiredPosition, smoothSpeed * Time.deltaTime);
            
            // Keep Z position constant (important for 2D)
            smoothedPosition.z = offset.z;
            
            transform.position = smoothedPosition;
        }
        
        /// <summary>
        /// Set camera target
        /// </summary>
        public void SetTarget(Transform newTarget)
        {
            target = newTarget;
        }
        
        /// <summary>
        /// Set boundaries
        /// </summary>
        public void SetBoundaries(Vector2 min, Vector2 max)
        {
            useBoundaries = true;
            minBounds = min;
            maxBounds = max;
        }
        
        /// <summary>
        /// Instantly move to target (no smooth)
        /// </summary>
        public void SnapToTarget()
        {
            if (target == null) return;
            
            Vector3 snapPosition = target.position + offset;
            
            if (useBoundaries)
            {
                snapPosition.x = Mathf.Clamp(snapPosition.x, minBounds.x, maxBounds.x);
                snapPosition.y = Mathf.Clamp(snapPosition.y, minBounds.y, maxBounds.y);
            }
            
            snapPosition.z = offset.z;
            transform.position = snapPosition;
        }
    }
}

```


#### CraftingRecipe.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Items;
using RebirthWarrior.Skills;

namespace RebirthWarrior.Crafting
{
    [System.Serializable]
    public class Ingredient
    {
        public Item item;
        public int amount;
    }

    [CreateAssetMenu(menuName = "Rebirth Warrior/Crafting/Recipe")]
    public class CraftingRecipe : ScriptableObject
    {
        public string recipeName;
        public SurvivalSkillType requiredSkill;
        public int requiredLevel = 1;

        public List<Ingredient> inputs;
        public Item outputItem;
        public int outputAmount = 1;

        [Tooltip("Cần công cụ gì? (VD: Nồi, Búa)")]
        public Item requiredTool;
    }
}
```


#### EncounterManager.cs
```csharp
using UnityEngine;
using System.Collections;
using System.Collections.Generic;
using RebirthWarrior.Character;
using RebirthWarrior.Core;
using UnityEngine.SceneManagement;

namespace RebirthWarrior.World
{
    public class EncounterManager : MonoBehaviour
    {
        public static EncounterManager Instance { get; private set; }

        [Header("Encounter Settings")]
        [SerializeField] private int stepsPerEncounterCheck = 5;
        [SerializeField] private float baseEncounterChance = 0.3f;
        [SerializeField] private float encounterChanceIncrement = 0.1f;

        [Header("Global Fallback")]
        [SerializeField] private List<CharacterData> possibleEnemies;

        [Header("References")]
        [SerializeField] private PlayerController player; // Có thể null ban đầu

        private int stepCount = 0;
        private float currentEncounterChance;
        private bool isInEncounter = false;
        private Vector3 lastPosition;
        private float stepDistance = 0.5f;

        private EncounterZone currentZone;

        private void Awake()
        {
            if (Instance == null) { Instance = this; }
            else { Destroy(gameObject); return; }

            // Thử tìm ngay lúc đầu (có thể thất bại nếu Player chưa sinh ra)
            if (player == null) player = FindObjectOfType<PlayerController>();

            currentEncounterChance = baseEncounterChance;
            isInEncounter = false;
        }

        private void Update()
        {
            // Nếu đang trong trận đấu thì dừng mọi tính toán
            if (isInEncounter) return;

            // --- [FIX QUAN TRỌNG: AUTO-FIND PLAYER] ---
            // Nếu biến player bị mất (do chuyển cảnh hoặc chưa sinh ra), hãy tìm lại
            if (player == null)
            {
                player = FindObjectOfType<PlayerController>();

                // Nếu tìm thấy, cập nhật ngay vị trí hiện tại để tránh tính sai bước
                if (player != null)
                {
                    lastPosition = player.transform.position;
                    // Debug.Log("[EncounterManager] Đã tìm thấy Player!");
                }
                else
                {
                    // Vẫn chưa thấy Player đâu -> Chờ frame tiếp theo
                    return;
                }
            }

            // Chỉ tính bước khi có Player và đang ở trong vùng quái
            CheckMovement();
        }

        public void ResetEncounterState()
        {
            isInEncounter = false;
            stepCount = 0;
            currentEncounterChance = baseEncounterChance;

            // Tìm lại player nếu cần
            if (player == null) player = FindObjectOfType<PlayerController>();

            if (player != null)
            {
                player.SetControlEnabled(true);
                lastPosition = player.transform.position; // Reset mốc tính bước
            }
        }

        public void SetCurrentZone(EncounterZone zone)
        {
            currentZone = zone;
            // Debug.Log(zone != null ? $"-> Đã vào vùng quái: {zone.zoneName}" : "-> Đã ra khỏi vùng quái");
        }

        private void CheckMovement()
        {
            // Tính khoảng cách đã di chuyển so với vị trí lần cuối check
            float dist = Vector3.Distance(player.transform.position, lastPosition);

            if (dist >= stepDistance)
            {
                stepCount++;
                lastPosition = player.transform.position; // Cập nhật mốc mới

                // Đủ số bước thì gieo xúc xắc gặp quái
                if (stepCount >= stepsPerEncounterCheck)
                {
                    stepCount = 0;
                    TryTriggerEncounter();
                }
            }
        }

        private void TryTriggerEncounter()
        {
            if (currentZone == null) return; // Không ở trong vùng quái -> Bỏ qua

            float roll = Random.Range(0f, 1f);

            // Debug.Log($"🎲 Roll Encounter: {roll} / {currentEncounterChance * currentZone.encounterRate}");

            if (roll <= currentEncounterChance * currentZone.encounterRate)
            {
                TriggerEncounter();
            }
            else
            {
                // Nếu không gặp, tăng tỷ lệ lên một chút (Bad luck protection)
                currentEncounterChance += encounterChanceIncrement;
            }
        }

        public void TriggerEncounter()
        {
            if (isInEncounter) return;
            isInEncounter = true;
            Debug.Log(">>> GẶP QUÁI! Đang lưu vị trí...");

            if (player != null)
            {
                // 1. Lưu vị trí & Scene hiện tại
                PlayerPrefs.SetFloat("WorldPositionX", player.transform.position.x);
                PlayerPrefs.SetFloat("WorldPositionY", player.transform.position.y);
                PlayerPrefs.SetString("ReturnScene", SceneManager.GetActiveScene().name);
                PlayerPrefs.SetInt("ReturningFromBattle", 1);
                PlayerPrefs.Save();

                // 2. Dừng Player
                player.DisableMovement();
            }

            // 3. Chuẩn bị dữ liệu quái
            List<CharacterStats> enemies = new List<CharacterStats>();
            List<CharacterData> pool = (currentZone != null && currentZone.enemiesInZone.Count > 0)
                                       ? currentZone.enemiesInZone
                                       : possibleEnemies;

            if (pool != null && pool.Count > 0)
            {
                int count = Random.Range(1, 4); // 1 đến 3 quái
                for (int i = 0; i < count; i++)
                {
                    CharacterData randomData = pool[Random.Range(0, pool.Count)];
                    if (randomData == null) continue;

                    CharacterStats newEnemy = randomData.CreateStats(1); // Lv 1
                    newEnemy.currentHP = newEnemy.maxHP;
                    newEnemy.currentStamina = newEnemy.maxStamina;
                    enemies.Add(newEnemy);
                }
            }

            // 4. Gửi dữ liệu sang GameStateManager
            if (GameStateManager.Instance != null)
            {
                GameStateManager.Instance.nextEnemies = enemies;
                GameStateManager.Instance.battleStartingData = null;
            }

            // 5. Chuyển cảnh
            StartCoroutine(BattleTransition());
        }

        private IEnumerator BattleTransition()
        {
            yield return new WaitForSeconds(0.5f);
            SceneManager.LoadScene("Battle");
        }
    }
}
```


#### EncounterZone.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Character;

namespace RebirthWarrior.World
{
    public class EncounterZone : MonoBehaviour
    {
        [Header("Zone Settings")]
        public string zoneName = "Forest";
        public List<CharacterData> enemiesInZone;
        [Range(0f, 1f)] public float encounterRate = 0.2f; // Tỷ lệ gặp mỗi 5 bước

        private void OnTriggerEnter2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                EncounterManager.Instance.SetCurrentZone(this);
            }
        }

        private void OnTriggerExit2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                EncounterManager.Instance.SetCurrentZone(null);
            }
        }
    }
}
```


#### GameTimeManager.cs
```csharp
using UnityEngine;
using System;

namespace RebirthWarrior.Core
{
    public class GameTimeManager : MonoBehaviour
    {
        public static GameTimeManager Instance { get; private set; }

        [Header("Time Config")]
        [Tooltip("1 Giờ trong game = Bao nhiêu giây ngoài đời (Ở Local Map)")]
        public float realSecondsPerGameHour = 60f;

        [Tooltip("Đi 1 bước trên World Map tốn bao nhiêu phút game")]
        public int worldMapMinutesPerStep = 30;

        [Header("Current Time")]
        public int day = 1;
        public int hour = 8; // Bắt đầu lúc 8h sáng
        public int minute = 0;

        public event Action<int, int> OnTimeChanged; // hour, minute
        public event Action OnNewDay;

        private float timer;
        private bool isWorldMapMode = false;

        private void Awake()
        {
            if (Instance == null) { Instance = this; DontDestroyOnLoad(gameObject); }
            else Destroy(gameObject);
        }

        private void Update()
        {
            if (!isWorldMapMode)
            {
                // Local Map: Trôi theo thời gian thực
                timer += Time.deltaTime;
                float secondsPerMinute = realSecondsPerGameHour / 60f;

                if (timer >= secondsPerMinute)
                {
                    timer = 0;
                    AdvanceTime(1);
                }
            }
        }

        public void SetWorldMapMode(bool isWorldMap)
        {
            isWorldMapMode = isWorldMap;
        }

        // Gọi hàm này khi Player di chuyển trên WorldMap
        public void AdvanceTimeByStep()
        {
            AdvanceTime(worldMapMinutesPerStep);
        }

        public void AdvanceTime(int minutesToAdd)
        {
            minute += minutesToAdd;
            while (minute >= 60)
            {
                minute -= 60;
                hour++;
                // Check đổi giờ để trừ Stamina
                RebirthWarrior.Character.CharacterStats.OnHourPassed();
            }

            while (hour >= 24)
            {
                hour -= 24;
                day++;
                OnNewDay?.Invoke();
            }

            OnTimeChanged?.Invoke(hour, minute);
        }

        public string GetTimeDisplay()
        {
            return $"Day {day} - {hour:00}:{minute:00}";
        }
    }
}
```



#### InnManager.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Core;
using RebirthWarrior.UI; // Cần namespace này để gọi SaveLoadManager

namespace RebirthWarrior.World
{
    public class InnManager : MonoBehaviour
    {
        [Header("Inn Settings")]
        [SerializeField] private int restCost = 50;

        [Header("UI References")]
        [SerializeField] private GameObject innPanel;
        [SerializeField] private TextMeshProUGUI infoText;
        [SerializeField] private Button restButton;
        [SerializeField] private Button saveButton; // <-- Nút này cần được gán trong Inspector
        [SerializeField] private Button closeButton;

        [Header("Prompt UI")]
        [SerializeField] private GameObject promptUI;
        [SerializeField] private TextMeshProUGUI promptText;

        private bool playerInRange = false;
        private PlayerController player;

        private void Awake()
        {
            if (innPanel) innPanel.SetActive(false);
            if (promptUI) promptUI.SetActive(false);

            if (restButton) restButton.onClick.AddListener(OnRestClicked);
            if (saveButton) saveButton.onClick.AddListener(OnSaveClicked);
            if (closeButton) closeButton.onClick.AddListener(CloseInn);
        }

        private void Update()
        {
            if (playerInRange && Input.GetKeyDown(KeyCode.E)) OpenInn();
        }

        private void OpenInn()
        {
            if (promptUI) promptUI.SetActive(false);
            if (innPanel) innPanel.SetActive(true);
            UpdateUI();

            // Khóa di chuyển Player khi mở Menu
            if (player) player.DisableMovement();
        }

        private void CloseInn()
        {
            if (innPanel) innPanel.SetActive(false);
            if (playerInRange && promptUI) promptUI.SetActive(true);

            // Mở khóa di chuyển
            if (player) player.EnableMovement();
        }

        private void UpdateUI()
        {
            var gameState = GameStateManager.Instance;
            if (gameState == null) return;

            if (infoText)
            {
                infoText.text = $"Nghỉ ngơi: <color=red>{restCost} G</color>\n" +
                                $"Hiện có: <color=yellow>{gameState.GetGold()} G</color>";
            }
            if (restButton) restButton.interactable = gameState.HasEnoughGold(restCost);
        }

        private void OnRestClicked()
        {
            var gameState = GameStateManager.Instance;
            if (gameState && gameState.HasEnoughGold(restCost))
            {
                gameState.RemoveGold(restCost);
                gameState.HealPartyFull();
                Debug.Log($"[InnManager] Đã nghỉ ngơi và hồi phục.");
                UpdateUI();
            }
        }

        // --- [QUAN TRỌNG] HÀM KÍCH HOẠT SAVE ---
        private void OnSaveClicked()
        {
            Debug.Log("[InnManager] Chuyển sang Menu Save...");

            if (SaveLoadManager.Instance != null)
            {
                // 1. Tắt bảng Inn đi (để đỡ vướng)
                innPanel.SetActive(false);

                // 2. Mở bảng Save (Chế độ Save)
                SaveLoadManager.Instance.OpenSavePanel();
            }
            else
            {
                Debug.LogError("Không tìm thấy SaveLoadManager! Hãy kiểm tra Prefab UI.");
            }
        }

        private void OnTriggerEnter2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                playerInRange = true;
                player = other.GetComponent<PlayerController>();
                if (promptUI) { promptUI.SetActive(true); if (promptText) promptText.text = "Bấm E để vào Trọ"; }
            }
        }

        private void OnTriggerExit2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                playerInRange = false;
                player = null;
                if (promptUI) promptUI.SetActive(false);
                CloseInn();
            }
        }
    }
}
```



#### LootSystem.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Items;
using RebirthWarrior.Core;

namespace RebirthWarrior.World
{
    // --- DATA ---
    [CreateAssetMenu(menuName = "Rebirth Warrior/Loot Table")]
    public class LootTable : ScriptableObject
    {
        [System.Serializable]
        public class DropEntry
        {
            public Item item;
            [Range(0, 100)] public float chance;
            public int minAmount = 1;
            public int maxAmount = 1;
        }
        public List<DropEntry> drops;
        public int minItems = 1;
        public int maxItems = 3;

        public List<Item> GenerateLoot()
        {
            List<Item> result = new List<Item>();
            int count = Random.Range(minItems, maxItems + 1);

            for (int i = 0; i < count; i++)
            {
                foreach (var entry in drops)
                {
                    if (Random.Range(0f, 100f) <= entry.chance)
                    {
                        // Logic đơn giản: Clone item để set số lượng (hoặc trả về List struct)
                        // Ở đây ta trả về Item gốc, Inventory sẽ handle số lượng sau
                        result.Add(entry.item);
                        break; // Mỗi slot chỉ lấy 1 món rồi next
                    }
                }
            }
            return result;
        }
    }

    // --- COMPONENT GẮN VÀO NPC/CHEST ---
    public class LootContainer : MonoBehaviour
    {
        public LootTable lootTable;
        public float restockHours = 24f; // 24 giờ game sẽ reset đồ

        // Túi đồ thực tế hiện tại
        public List<Item> currentContents = new List<Item>();

        private float lastRestockTotalHours = -999;

        public void CheckRestock()
        {
            if (lootTable == null) return;

            // Tính tổng giờ hiện tại
            float currentTotalHours = (GameTimeManager.Instance.day * 24) + GameTimeManager.Instance.hour;

            if (currentTotalHours - lastRestockTotalHours >= restockHours)
            {
                Refill();
                lastRestockTotalHours = currentTotalHours;
            }
        }

        public void Refill()
        {
            currentContents.Clear();
            currentContents = lootTable.GenerateLoot();
            // Debug.Log($"[LootContainer] Đã làm đầy túi của {name}");
        }

        // Hàm gọi khi Player lấy đồ
        public void RemoveItem(Item item)
        {
            if (currentContents.Contains(item)) currentContents.Remove(item);
        }
    }
}
```





#### MapBossController.cs
```csharp
using UnityEngine;
using UnityEngine.SceneManagement;
using RebirthWarrior.Core;
using RebirthWarrior.Character;
using RebirthWarrior.Dialogue;
using RebirthWarrior.Battle;
using System.Collections.Generic;
using TMPro; // Cần cho UI Prompt

namespace RebirthWarrior.World
{
    [RequireComponent(typeof(BoxCollider2D))]
    public class MapBossController : MonoBehaviour
    {
        [Header("Boss Info")]
        [SerializeField] private CharacterData bossData;
        [SerializeField] private int bossLevel = 10;

        [Header("Interaction")]
        [SerializeField] private DialogueData preBattleDialogue;
        [SerializeField] private float interactRadius = 2.0f;

        [Header("UI Prompt (MỚI)")]
        [Tooltip("Kéo GameObject InteractionPrompt trong Canvas vào đây (giống NPC)")]
        [SerializeField] private GameObject promptUI;
        [SerializeField] private TextMeshProUGUI promptText;

        [Header("Battle Rules")]
        [SerializeField] private ScriptedBattleContext battleRules;

        private bool isPlayerInRange = false;
        private Transform playerTransform;

        private void Start()
        {
            var playerObj = GameObject.FindGameObjectWithTag("Player");
            if (playerObj) playerTransform = playerObj.transform;
            GetComponent<Collider2D>().isTrigger = true;

            if (promptUI) promptUI.SetActive(false);
        }

        private void Update()
        {
            CheckDistance();

            if (isPlayerInRange && Input.GetKeyDown(KeyCode.E))
            {
                StartBossEncounter();
            }
        }

        private void OnMouseDown()
        {
            if (isPlayerInRange) StartBossEncounter();
        }

        private void CheckDistance()
        {
            if (playerTransform == null) return;
            float dist = Vector2.Distance(transform.position, playerTransform.position);
            bool wasInRange = isPlayerInRange;
            isPlayerInRange = (dist <= interactRadius);

            // Xử lý UI Prompt
            if (isPlayerInRange != wasInRange)
            {
                if (promptUI)
                {
                    promptUI.SetActive(isPlayerInRange);
                    if (isPlayerInRange && promptText)
                        promptText.text = $"Chiến đấu với {bossData.characterNameKey} (E)";
                }
            }
        }

        public void StartBossEncounter()
        {
            if (GameStateManager.Instance == null) return;

            // Tắt Prompt
            if (promptUI) promptUI.SetActive(false);

            // 1. Lưu Scene hiện tại để quay về đúng chỗ (FIX LỖI RETURN)
            string currentScene = SceneManager.GetActiveScene().name;
            PlayerPrefs.SetString("PreviousScene", currentScene);
            PlayerPrefs.SetFloat("WorldPositionX", playerTransform.position.x);
            PlayerPrefs.SetFloat("WorldPositionY", playerTransform.position.y);
            PlayerPrefs.SetInt("ReturningFromBattle", 1);
            PlayerPrefs.Save();

            // 2. Chạy Dialogue (nếu có)
            if (preBattleDialogue != null && DialogueManager.Instance != null)
            {
                // Truyền Action callback vào (đã fix ở DialogueManager)
                DialogueManager.Instance.StartDialogue(preBattleDialogue, OnDialogueFinished);
            }
            else
            {
                OnDialogueFinished();
            }
        }

        private void OnDialogueFinished()
        {
            var gameState = GameStateManager.Instance;

            CharacterStats bossStats = bossData.CreateStats(bossLevel);
            bossStats.currentHP = bossStats.maxHP;
            gameState.nextEnemies = new List<CharacterStats> { bossStats };
            gameState.currentBattleContext = battleRules;

            SceneManager.LoadScene("Battle");
        }
    }
}
```




#### MapLocation.cs
```csharp
using UnityEngine;
using UnityEngine.SceneManagement;
using RebirthWarrior.Core;

namespace RebirthWarrior.WorldMap
{
    [RequireComponent(typeof(CircleCollider2D))]
    public class MapLocation : MonoBehaviour
    {
        [Header("Location Identity")]
        [Tooltip("ID dùng để định vị. Phải trùng với Target Portal ID ở TownExit.")]
        public string locationID; // Ví dụ: "Loc_Base_2060"

        [Header("Visual Info")]
        public string locationName = "New City";

        [Header("Destination")]
        [Tooltip("Tên Scene sẽ load khi vào đây")]
        public string sceneToLoad;
        [Tooltip("ID spawn point bên trong Town")]
        public string targetSpawnID;

        private bool isPlayerClose = false;

        private void Awake()
        {
            GetComponent<CircleCollider2D>().isTrigger = true;
        }

        private void Update()
        {
            if (isPlayerClose && (Input.GetKeyDown(KeyCode.Return) || Input.GetKeyDown(KeyCode.E)))
            {
                EnterLocation();
            }
        }

        public void EnterLocation()
        {
            if (string.IsNullOrEmpty(sceneToLoad)) return;

            if (GameStateManager.Instance)
            {
                GameStateManager.Instance.nextSpawnPointID = targetSpawnID;
            }

            // Lưu vị trí token hiện tại trước khi vào Map
            if (WorldMapManager.Instance != null)
            {
                // Gọi hàm save position (nếu chưa có thì tự implement tay ở đây cũng được)
                PlayerPrefs.SetFloat("WorldPositionX", transform.position.x);
                PlayerPrefs.SetFloat("WorldPositionY", transform.position.y);
                PlayerPrefs.SetInt("ReturningFromTown", 1);
                PlayerPrefs.Save();
            }

            SceneManager.LoadScene(sceneToLoad);
        }

        private void OnTriggerEnter2D(Collider2D other)
        {
            if (other.GetComponent<WorldMapPlayer>()) isPlayerClose = true;
        }

        private void OnTriggerExit2D(Collider2D other)
        {
            if (other.GetComponent<WorldMapPlayer>()) isPlayerClose = false;
        }
    }
}
```





#### NPC.cs
```csharp
using RebirthWarrior.Core;
using RebirthWarrior.Dialogue;
using RebirthWarrior.Quests;
using System.Collections.Generic;
using TMPro;
using UnityEngine;
using RebirthWarrior.UI;

namespace RebirthWarrior.World
{
    [RequireComponent(typeof(Collider2D))]
    [RequireComponent(typeof(LootContainer))]
    public class NPC : MonoBehaviour
    {
        [Header("Data")]
        [SerializeField] private DialogueData dialogueData;
        [SerializeField] private List<string> relatedQuestIDs;

        [Header("Dialogue State Config")]
        public string startQuestState = "QuestGive";
        public string processingQuestState = "QuestWait";
        public string completeQuestState = "QuestEnd";
        public string defaultState = "Default";

        [Header("UI Interaction")]
        [SerializeField] private GameObject promptUI;
        [SerializeField] private TextMeshProUGUI promptText;

        [Header("Quest Indicators")]
        [SerializeField] private GameObject readyToCompleteIcon;
        [SerializeField] private GameObject availableQuestIcon;
        [SerializeField] private float iconHeight = 2.0f;

        [Header("Pickpocket (Mới)")]
        public LootContainer lootContainer;
        public int pickpocketFailCount = 0;
        [SerializeField] private RebirthWarrior.UI.ChatBubbleUI chatBubble;

        private bool playerInRange = false;
        private RebirthWarrior.NPCSystem.NPCMovement npcMovement;

        private void Awake()
        {
            if (promptUI) promptUI.SetActive(false);
            if (readyToCompleteIcon) readyToCompleteIcon.SetActive(false);
            if (availableQuestIcon) availableQuestIcon.SetActive(false);
        }

        private void Start()
        {
            npcMovement = GetComponent<RebirthWarrior.NPCSystem.NPCMovement>();
            lootContainer = GetComponent<LootContainer>();

            if (lootContainer) lootContainer.CheckRestock();

            if (QuestManager.Instance != null)
            {
                QuestManager.Instance.OnQuestStarted += (q) => UpdateQuestStatus();
                QuestManager.Instance.OnQuestCompleted += (q) => UpdateQuestStatus();
                QuestManager.Instance.OnObjectiveProgress += (q, o, p) => UpdateQuestStatus();
                UpdateQuestStatus();
            }
        }

        private void Update()
        {
            if (playerInRange && Input.GetKeyDown(KeyCode.E)) Interact();
            AnimateIcons();
        }

        private void Interact()
        {
            if (DialogueManager.Instance == null || DialogueManager.Instance.IsDialogueActive()) return;
            if (promptUI) promptUI.SetActive(false);

            if (npcMovement != null)
            {
                var player = FindObjectOfType<PlayerController>();
                npcMovement.PauseMovement(player ? player.transform : null);
            }

            string stateToPlay = defaultState;
            bool foundPriority = false;

            if (QuestManager.Instance != null && relatedQuestIDs != null)
            {
                // [FIX ERROR 2] Gọi trực tiếp GetQuestByID từ QuestManager
                foreach (string qID in relatedQuestIDs)
                {
                    var quest = QuestManager.Instance.GetQuestByID(qID);
                    if (quest != null && QuestManager.Instance.GetQuestState(quest) == QuestState.ReadyToComplete)
                    {
                        stateToPlay = completeQuestState; foundPriority = true; break;
                    }
                }
                if (!foundPriority)
                {
                    foreach (string qID in relatedQuestIDs)
                    {
                        var quest = QuestManager.Instance.GetQuestByID(qID);
                        if (quest != null && QuestManager.Instance.GetQuestState(quest) == QuestState.Active)
                        {
                            stateToPlay = processingQuestState; foundPriority = true; break;
                        }
                    }
                }
                if (!foundPriority)
                {
                    foreach (string qID in relatedQuestIDs)
                    {
                        var quest = QuestManager.Instance.GetQuestByID(qID);
                        if (quest != null && QuestManager.Instance.GetQuestState(quest) == QuestState.NotStarted && QuestManager.Instance.CanOfferQuest(quest))
                        {
                            stateToPlay = startQuestState; foundPriority = true; break;
                        }
                    }
                }
            }

            DialogueManager.Instance.StartDialogue(dialogueData, stateToPlay, OnDialogueEnd);
        }

        public void UpdateQuestStatus()
        {
            if (QuestManager.Instance == null || relatedQuestIDs == null) return;
            bool showReady = false;
            bool showAvailable = false;

            foreach (string qID in relatedQuestIDs)
            {
                // [FIX ERROR 3] Gọi trực tiếp GetQuestByID
                var quest = QuestManager.Instance.GetQuestByID(qID);
                if (quest == null) continue;
                QuestState state = QuestManager.Instance.GetQuestState(quest);

                if (state == QuestState.ReadyToComplete) { showReady = true; break; }
                if (state == QuestState.NotStarted && QuestManager.Instance.CanOfferQuest(quest)) showAvailable = true;
            }

            if (readyToCompleteIcon) readyToCompleteIcon.SetActive(showReady);
            if (availableQuestIcon) availableQuestIcon.SetActive(!showReady && showAvailable);
        }

        private void AnimateIcons()
        {
            float yOffset = Mathf.Sin(Time.time * 3f) * 0.1f;
            Vector3 finalPos = new Vector3(0, iconHeight + yOffset, 0);
            if (readyToCompleteIcon && readyToCompleteIcon.activeSelf) readyToCompleteIcon.transform.localPosition = finalPos;
            if (availableQuestIcon && availableQuestIcon.activeSelf) availableQuestIcon.transform.localPosition = finalPos;
        }

        private void OnTriggerEnter2D(Collider2D other) { if (other.CompareTag("Player")) { playerInRange = true; if (promptUI) promptUI.SetActive(true); } }
        private void OnTriggerExit2D(Collider2D other) { if (other.CompareTag("Player")) { playerInRange = false; if (promptUI) promptUI.SetActive(false); } }

        public void OnDialogueEnd()
        {
            if (playerInRange && promptUI) promptUI.SetActive(true);
            UpdateQuestStatus();
            if (npcMovement != null) npcMovement.ResumeMovement();
        }

        public bool TryPickpocket(int playerSkillLevel)
        {
            int chance = (playerSkillLevel * 10) - (pickpocketFailCount * 15);
            chance = Mathf.Clamp(chance, 5, 95);

            int roll = Random.Range(0, 100);
            if (roll <= chance)
            {
                Debug.Log("Móc túi thành công!");
                return true;
            }
            else
            {
                Debug.Log("Móc túi thất bại!");
                pickpocketFailCount++;
                if (chatBubble) chatBubble.ShowText("Đồ ăn cắp! Cút ngay!", 2f);
                return false;
            }
        }
    }
}
```




#### PlayerController.cs

Chức năng: Điều khiển nhân vật di chuyển 8 hướng trong không gian Isometric.

Logic:

Sử dụng use8Direction (true) và useIsometricMovement (true).

Hàm HandleInput() sử dụng input.Normalize() để chuẩn hóa tốc độ 8 hướng.

Hàm ToIso() xoay vector (x, y) thành vector Isometric (x-y, (x+y)*0.5).

Tích hợp Animation: Gửi rawInput (Vector 2D thô) sang PlayerAnimation.SetDirection() để tính góc quay animation.

Fix: Đã thêm lại các hàm DisableMovement(), EnableMovement() để các script cũ có thể khóa di chuyển.

```csharp
using UnityEngine;
using RebirthWarrior.Character; // Cần namespace này để gọi PlayerAnimation

namespace RebirthWarrior.World
{
    [RequireComponent(typeof(Rigidbody2D))]
    public class PlayerController : MonoBehaviour
    {
        [Header("Movement Settings")]
        [SerializeField] private float moveSpeed = 5f;

        [Header("Isometric Settings")]
        [SerializeField] private bool useIsometricMovement = true;
        [SerializeField] private bool use8Direction = true;

        [Header("Components")]
        [SerializeField] private Rigidbody2D rb;
        // KHÔNG dùng Animator trực tiếp ở đây nữa, dùng qua PlayerAnimation
        [SerializeField] private PlayerAnimation playerAnimation;

        private Vector2 rawInput;   // Input bàn phím (W,A,S,D)
        private Vector2 moveInput;  // Vector lực đẩy (đã xoay Isometric)
        private bool isMoving;
        private bool canMove = true;

        private void Awake()
        {
            if (rb == null) rb = GetComponent<Rigidbody2D>();
            // Tự tìm component PlayerAnimation nếu chưa gán
            if (playerAnimation == null) playerAnimation = GetComponent<PlayerAnimation>();

            // Setup Rigidbody
            rb.gravityScale = 0f;
            rb.constraints = RigidbodyConstraints2D.FreezeRotation;
            rb.collisionDetectionMode = CollisionDetectionMode2D.Continuous;
            Application.targetFrameRate = 60; // Hoặc 120 tùy màn hình
        }

        private void Update()
        {
            if (!canMove)
            {
                rawInput = Vector2.zero;
                moveInput = Vector2.zero;
                return;
            }

            HandleInput();

            // GỬI INPUT SANG SCRIPT ANIMATION
            // Lưu ý: Gửi rawInput (hướng bàn phím) để tính góc animation chuẩn xác hơn
            // Nếu bạn muốn animation xoay theo hướng vật lý thực tế thì gửi moveInput
            if (playerAnimation != null)
            {
                playerAnimation.SetDirection(rawInput);
            }
        }

        private void FixedUpdate()
        {
            if (rb != null)
                rb.velocity = moveInput * moveSpeed;
        }

        private void HandleInput()
        {
            float x = Input.GetAxisRaw("Horizontal");
            float y = Input.GetAxisRaw("Vertical");

            rawInput = new Vector2(x, y);

            // Xử lý 8 hướng (Normalize để đi chéo không bị nhanh)
            if (use8Direction && rawInput.sqrMagnitude > 1)
                rawInput.Normalize();
            else if (!use8Direction)
            {
                if (Mathf.Abs(x) > Mathf.Abs(y)) rawInput.y = 0; else rawInput.x = 0;
            }

            // Biến đổi sang Isometric cho vật lý
            if (useIsometricMovement)
                moveInput = ToIso(rawInput);
            else
                moveInput = rawInput;

            isMoving = rawInput.sqrMagnitude > 0.01f;
        }

        private Vector2 ToIso(Vector2 input)
        {
            float isoX = input.x - input.y;
            float isoY = (input.x + input.y) * 0.5f;
            return new Vector2(isoX, isoY);
        }

        public void DisableMovement()
        {
            canMove = false;

            // Reset input để nhân vật dừng hẳn animation và vật lý
            rawInput = Vector2.zero;
            moveInput = Vector2.zero;
            isMoving = false;

            if (rb != null) rb.velocity = Vector2.zero;
        }

        public void EnableMovement()
        {
            canMove = true;
        }

        // Hàm này giữ lại để tương thích nếu có script nào dùng
        public void SetControlEnabled(bool enabled)
        {
            if (enabled) EnableMovement();
            else DisableMovement();
        }
    }
}
```




#### ShopManager.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using System.Collections.Generic;

namespace RebirthWarrior.World
{
    /// <summary>
    /// Shop system with inventory integration + ICON SUPPORT
    /// Version 3.1 - Fixed item icons in shop
    /// </summary>
    public class ShopManager : MonoBehaviour
    {
        [Header("Shop Settings")]
        [SerializeField] private string shopName = "General Store";
        [SerializeField] private List<Items.Item> shopInventory;

        [Header("UI References")]
        [SerializeField] private GameObject shopPanel;
        [SerializeField] private TextMeshProUGUI shopNameText;
        [SerializeField] private TextMeshProUGUI goldText;
        [SerializeField] private Transform itemListContainer;
        [SerializeField] private GameObject itemButtonPrefab;
        [SerializeField] private Button closeButton;

        [Header("Prompt UI")]
        [SerializeField] private GameObject promptUI;
        [SerializeField] private TextMeshProUGUI promptText;

        [Header("Feedback")]
        [SerializeField] private GameObject feedbackPanel;
        [SerializeField] private TextMeshProUGUI feedbackText;

        private bool playerInRange = false;
        private PlayerController player;

        private void Awake()
        {
            if (shopPanel != null)
                shopPanel.SetActive(false);

            if (promptUI != null)
                promptUI.SetActive(false);

            if (feedbackPanel != null)
                feedbackPanel.SetActive(false);

            if (closeButton != null)
                closeButton.onClick.AddListener(CloseShop);
        }

        private void Update()
        {
            if (playerInRange && Input.GetKeyDown(KeyCode.E))
            {
                OpenShop();
            }
        }

        private void OnTriggerEnter2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                playerInRange = true;
                player = other.GetComponent<PlayerController>();
                ShowPrompt();
            }
        }

        private void OnTriggerExit2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                playerInRange = false;
                player = null;
                HidePrompt();
            }
        }

        private void ShowPrompt()
        {
            if (promptUI != null)
                promptUI.SetActive(true);

            if (promptText != null)
                promptText.text = $"Press E to open {shopName}";
        }

        private void HidePrompt()
        {
            if (promptUI != null)
                promptUI.SetActive(false);
        }

        private void OpenShop()
        {
            Debug.Log($"[ShopManager] Opening {shopName}");

            HidePrompt();

            if (shopPanel != null)
                shopPanel.SetActive(true);

            if (shopNameText != null)
                shopNameText.text = shopName;

            UpdateGoldDisplay();
            PopulateShop();

            if (player != null)
                player.SetControlEnabled(false);
        }

        private void CloseShop()
        {
            Debug.Log("[ShopManager] Closing shop");

            if (shopPanel != null)
                shopPanel.SetActive(false);

            if (playerInRange)
                ShowPrompt();

            if (player != null)
                player.SetControlEnabled(true);
        }

        /// <summary>
        /// Populate shop with items - WITH ICON SUPPORT
        /// </summary>
        private void PopulateShop()
        {
            if (itemListContainer == null || itemButtonPrefab == null)
            {
                Debug.LogError("[ShopManager] Missing references!");
                return;
            }

            // Clear existing items
            foreach (Transform child in itemListContainer)
            {
                Destroy(child.gameObject);
            }

            // Create item buttons
            foreach (var item in shopInventory)
            {
                if (item == null) continue;

                GameObject itemButton = Instantiate(itemButtonPrefab, itemListContainer);

                // ✅ SET ICON (NEW!)
                var iconImage = itemButton.transform.Find("Icon")?.GetComponent<Image>();
                if (iconImage == null)
                    iconImage = itemButton.transform.Find("ItemIcon")?.GetComponent<Image>();

                if (iconImage != null)
                {
                    if (item.icon != null)
                    {
                        iconImage.sprite = item.icon;
                        iconImage.color = Color.white; // Ensure white!
                        iconImage.enabled = true;
                        Debug.Log($"[ShopManager] ✓ Set icon for {item.itemName}");
                    }
                    else
                    {
                        iconImage.enabled = false;
                        Debug.LogWarning($"[ShopManager] Item {item.itemName} has no icon!");
                    }
                }
                else
                {
                    Debug.LogWarning($"[ShopManager] Icon not found in ItemButton prefab!");
                }

                // Set item name
                var itemNameText = itemButton.transform.Find("ItemName")?.GetComponent<TextMeshProUGUI>();
                if (itemNameText != null)
                    itemNameText.text = item.itemName;

                // Set price
                var priceText = itemButton.transform.Find("Price")?.GetComponent<TextMeshProUGUI>();
                if (priceText != null)
                    priceText.text = $"{item.buyPrice}g";

                // Add buy button listener
                var buyButton = itemButton.GetComponent<Button>();
                if (buyButton != null)
                {
                    buyButton.onClick.AddListener(() => BuyItem(item));
                }
            }

            Debug.Log($"[ShopManager] Populated shop with {shopInventory.Count} items");
        }

        /// <summary>
        /// Buy item - deducts gold and adds to inventory
        /// </summary>
        private void BuyItem(Items.Item item)
        {
            var gameState = Core.GameStateManager.Instance;
            var inventory = Inventory.InventoryManager.Instance;

            if (gameState == null)
            {
                Debug.LogError("[ShopManager] GameStateManager not found!");
                ShowFeedback("System error!", Color.red);
                return;
            }

            if (inventory == null)
            {
                Debug.LogError("[ShopManager] InventoryManager not found!");
                ShowFeedback("System error!", Color.red);
                return;
            }

            // Check if inventory is full
            if (inventory.IsInventoryFull() && !inventory.HasItem(item))
            {
                Debug.Log("[ShopManager] Inventory is full!");
                ShowFeedback("Inventory is full!", Color.red);
                return;
            }

            // Check if has enough gold
            if (gameState.HasEnoughGold(item.buyPrice))
            {
                // Remove gold
                gameState.RemoveGold(item.buyPrice);

                // Add item to inventory
                bool added = inventory.AddItem(item, 1);

                if (added)
                {
                    Debug.Log($"[ShopManager] ✅ Bought {item.itemName} for {item.buyPrice}g");
                    ShowFeedback($"Bought {item.itemName}!", Color.green);

                    // Update UI
                    UpdateGoldDisplay();
                }
                else
                {
                    // Refund if couldn't add to inventory
                    gameState.AddGold(item.buyPrice);
                    ShowFeedback("Couldn't add item!", Color.red);
                }
            }
            else
            {
                Debug.Log($"[ShopManager] ❌ Not enough gold! Need {item.buyPrice}g, have {gameState.GetGold()}g");
                ShowFeedback("Not enough gold!", Color.red);
            }
        }

        private void UpdateGoldDisplay()
        {
            var gameState = Core.GameStateManager.Instance;

            if (gameState != null && goldText != null)
            {
                goldText.text = $"Gold: {gameState.GetGold()}";
            }
        }

        /// <summary>
        /// Show feedback message
        /// </summary>
        private void ShowFeedback(string message, Color color)
        {
            if (feedbackPanel != null && feedbackText != null)
            {
                feedbackText.text = message;
                feedbackText.color = color;
                feedbackPanel.SetActive(true);

                // Auto-hide after 2 seconds
                CancelInvoke(nameof(HideFeedback));
                Invoke(nameof(HideFeedback), 2f);
            }
        }

        private void HideFeedback()
        {
            if (feedbackPanel != null)
                feedbackPanel.SetActive(false);
        }
    }
}
```




#### TownEntrance.cs
```csharp
using UnityEngine;
using UnityEngine.UI;
using TMPro;
using RebirthWarrior.Core; // Cần để gọi GameStateManager

namespace RebirthWarrior.World
{
    public class TownEntrance : MonoBehaviour
    {
        [Header("Town Settings")]
        [SerializeField] private string townName = "Village";
        [SerializeField] private string townSceneName = "TownScene";

        [Header("Portal ID System (MỚI)")]
        [Tooltip("ID của chính cổng này (Để WorldManager tìm ra khi từ Town trở về)")]
        public string portalID; // Vd: "Gate_Village_Main"

        [Tooltip("ID điểm đến bên trong Town")]
        public string targetSpawnID; // Vd: "Spawn_Village_Entrance"

        [Header("UI")]
        [SerializeField] private GameObject promptUI;
        [SerializeField] private TextMeshProUGUI promptText;

        private bool playerInRange = false;
        private PlayerController player;

        private void Awake() { if (promptUI != null) promptUI.SetActive(false); }

        private void Update() { if (playerInRange && Input.GetKeyDown(KeyCode.E)) EnterTown(); }

        private void OnTriggerEnter2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                playerInRange = true;
                player = other.GetComponent<PlayerController>();
                if (promptUI) { promptUI.SetActive(true); if (promptText) promptText.text = $"Vào {townName} (E)"; }
            }
        }

        private void OnTriggerExit2D(Collider2D other)
        {
            if (other.CompareTag("Player")) { playerInRange = false; player = null; if (promptUI) promptUI.SetActive(false); }
        }

        private void EnterTown()
        {
            Debug.Log($"[TownEntrance] Entering {townName}...");
            if (player != null) player.SetControlEnabled(false);

            // --- LOGIC MỚI: Gửi ID điểm đến ---
            if (GameStateManager.Instance != null)
                GameStateManager.Instance.nextSpawnPointID = targetSpawnID;

            // Lưu backup cho Save Game
            PlayerPrefs.SetFloat("WorldPositionX", player.transform.position.x);
            PlayerPrefs.SetFloat("WorldPositionY", player.transform.position.y);
            PlayerPrefs.SetString("CurrentTown", townSceneName);
            PlayerPrefs.Save();

            UnityEngine.SceneManagement.SceneManager.LoadScene(townSceneName);
        }
    }
}
```





#### TownExit.cs
```csharp
using UnityEngine;
using TMPro;
using RebirthWarrior.Core;

namespace RebirthWarrior.World
{
    public class TownExit : MonoBehaviour
    {
        [Header("Portal Settings (MỚI)")]
        [SerializeField] private string worldSceneName = "WorldScene";
        [Tooltip("ID của cổng TownEntrance ngoài World muốn ra")]
        public string targetPortalID; // Vd: "Gate_Village_Main"

        [Header("UI")]
        [SerializeField] private GameObject promptUI;
        [SerializeField] private TextMeshProUGUI promptText;

        private bool playerInRange = false;

        private void Awake() { if (promptUI != null) promptUI.SetActive(false); }
        private void Update() { if (playerInRange && Input.GetKeyDown(KeyCode.E)) ExitTown(); }

        private void OnTriggerEnter2D(Collider2D other) { if (other.CompareTag("Player")) { playerInRange = true; if (promptUI) promptUI.SetActive(true); } }
        private void OnTriggerExit2D(Collider2D other) { if (other.CompareTag("Player")) { playerInRange = false; if (promptUI) promptUI.SetActive(false); } }

        private void ExitTown()
        {
            Debug.Log("[TownExit] Exiting town...");
            if (promptUI) promptUI.SetActive(false);

            // --- LOGIC MỚI: Gửi ID ra World ---
            if (GameStateManager.Instance != null)
                GameStateManager.Instance.nextSpawnPointID = targetPortalID;

            TownManager.ExitTown(worldSceneName);
        }
    }
}
```





#### TownManager.cs
```csharp
using UnityEngine;
using UnityEngine.SceneManagement;
using System.Collections;
using RebirthWarrior.Core;

namespace RebirthWarrior.World
{
    public class TownManager : MonoBehaviour
    {
        [Header("References")]
        [SerializeField] private Transform defaultSpawnPoint;

        // --- FIX: Đổi từ private thành public để Tutorial có thể truy cập ---
        [SerializeField] public PlayerController player;

        [Header("Combat")]
        [SerializeField] private EncounterManager encounterManager;

        private static TownManager instance;
        public static TownManager Instance => instance;

        private void Awake()
        {
            if (instance != null && instance != this) { Destroy(gameObject); return; }
            instance = this;

            if (encounterManager == null) encounterManager = FindObjectOfType<EncounterManager>();
        }

        private void Start()
        {
            if (player != null)
            {
                OnPlayerReady(player);
            }
        }

        public void OnPlayerReady(PlayerController pController)
        {
            this.player = pController;
            Debug.Log("[TownManager] 📞 Đã nhận Player! Bắt đầu xử lý vị trí...");

            StartCoroutine(ProcessPosition());
        }

        private IEnumerator ProcessPosition()
        {
            yield return null;

            if (PlayerPrefs.GetInt("ReturningFromBattle", 0) == 1)
            {
                HandleBattleReturn();
            }
            else
            {
                HandleSpawnPointLogic();
            }

            ClearFlags();
        }

        private void HandleBattleReturn()
        {
            if (player == null) return;

            if (PlayerPrefs.HasKey("WorldPositionX") && PlayerPrefs.HasKey("WorldPositionY"))
            {
                float x = PlayerPrefs.GetFloat("WorldPositionX");
                float y = PlayerPrefs.GetFloat("WorldPositionY");
                Vector3 targetPos = new Vector3(x, y, 0f);

                var rb = player.GetComponent<Rigidbody2D>();
                if (rb != null)
                {
                    rb.velocity = Vector2.zero;
                    rb.position = targetPos;
                    rb.Sleep();
                }
                player.transform.position = targetPos;
                Debug.Log($"✅ [TownManager] Player restored at: {targetPos}");
            }
        }

        private void HandleSpawnPointLogic()
        {
            if (player == null) return;

            string targetID = "";
            if (GameStateManager.Instance != null)
            {
                targetID = GameStateManager.Instance.nextSpawnPointID;
                GameStateManager.Instance.nextSpawnPointID = "";
            }

            Transform targetTransform = defaultSpawnPoint;

            if (!string.IsNullOrEmpty(targetID))
            {
                GameObject spawnObj = GameObject.Find(targetID);
                if (spawnObj != null) targetTransform = spawnObj.transform;
            }

            if (targetTransform != null)
            {
                player.transform.position = targetTransform.position;

                var rb = player.GetComponent<Rigidbody2D>();
                if (rb != null) rb.position = targetTransform.position;
            }
        }

        private void ClearFlags()
        {
            PlayerPrefs.DeleteKey("ReturningFromBattle");
            PlayerPrefs.DeleteKey("ReturningFromTown");
        }

        public static void ExitTown(string sceneName)
        {
            SceneManager.LoadScene(sceneName);
        }
    }
}
```






#### WorldMapManager.cs
```csharp
using UnityEngine;
using RebirthWarrior.Core;
using RebirthWarrior.Character;
using System.Collections.Generic;
using System.Collections;
using System.Linq;
using UnityEngine.SceneManagement;

namespace RebirthWarrior.WorldMap
{
    public class WorldMapManager : MonoBehaviour
    {
        public static WorldMapManager Instance { get; private set; }

        [Header("References")]
        // FIX: Bỏ SerializeField bắt buộc, để code tự tìm
        [SerializeField] private WorldMapPlayer worldMapPlayer;

        [Header("Map Configuration")]
        [Tooltip("Kéo TOÀN BỘ các MapLocation (Node) trên bản đồ vào đây")]
        [SerializeField] private List<MapLocation> allLocations;

        [Header("Encounter Settings")]
        [SerializeField] private float distanceForEncounterCheck = 2f;
        [SerializeField] private float encounterChance = 0.3f;
        [SerializeField] private List<CharacterData> defaultFallbackEnemies;

        // Runtime Variables
        private WorldMapZone currentActiveZone;
        private float distanceAccumulated = 0f;

        private void Awake()
        {
            if (Instance == null) Instance = this;
            else Destroy(gameObject);
        }

        private IEnumerator Start()
        {
            if (defaultFallbackEnemies == null) defaultFallbackEnemies = new List<CharacterData>();

            // --- AUTO FIX: Tự tìm Player nếu quên gán trong Inspector ---
            if (worldMapPlayer == null)
            {
                worldMapPlayer = FindObjectOfType<WorldMapPlayer>();
                if (worldMapPlayer != null)
                {
                    Debug.Log("[WorldMapManager] ⚠️ Quên gán WorldMapPlayer trong Inspector. Đã tự động tìm thấy!");
                }
                else
                {
                    Debug.LogError("[WorldMapManager] ❌ LỖI NGHIÊM TRỌNG: Không tìm thấy GameObject nào có script 'WorldMapPlayer' trong Scene này!");
                }
            }
            // ------------------------------------------------------------

            yield return null;
            InitializePlayerPosition();
        }

        private void InitializePlayerPosition()
        {
            if (worldMapPlayer == null)
            {
                // Nếu vẫn null thì return ngay để tránh Crash
                return;
            }

            // TRƯỜNG HỢP 1: Quay về từ Battle
            if (PlayerPrefs.GetInt("ReturningFromBattle", 0) == 1)
            {
                float x = PlayerPrefs.GetFloat("WorldPositionX", 0);
                float y = PlayerPrefs.GetFloat("WorldPositionY", 0);
                worldMapPlayer.transform.position = new Vector3(x, y, 0);

                PlayerPrefs.DeleteKey("ReturningFromBattle");
                Debug.Log($"[WorldMap] Restored position from Battle: {worldMapPlayer.transform.position}");
            }
            // TRƯỜNG HỢP 2: Quay về từ Town (TownExit)
            else if (GameStateManager.Instance != null && !string.IsNullOrEmpty(GameStateManager.Instance.nextSpawnPointID))
            {
                string portalID = GameStateManager.Instance.nextSpawnPointID;
                Debug.Log($"[WorldMap] Nhận yêu cầu spawn tại ID: '{portalID}'");

                MapLocation targetLoc = allLocations.Find(loc => loc.locationID == portalID);

                if (targetLoc != null)
                {
                    worldMapPlayer.transform.position = targetLoc.transform.position;
                    worldMapPlayer.SetTarget(targetLoc.transform.position);
                    Debug.Log($"[WorldMap] ✅ Đã tìm thấy Node '{targetLoc.locationName}'. Di chuyển Token tới: {targetLoc.transform.position}");
                }
                else
                {
                    Debug.LogError($"[WorldMap] ❌ KHÔNG TÌM THẤY Node nào có ID '{portalID}' trong list allLocations! Hãy kiểm tra lại Inspector.");
                }

                GameStateManager.Instance.nextSpawnPointID = "";
            }
            else
            {
                Debug.Log("[WorldMap] Không có dữ liệu spawn đặc biệt. Sử dụng vị trí mặc định.");
            }
        }

        public static void ReturnToWorld()
        {
            PlayerPrefs.SetInt("ReturningFromBattle", 1);
            string sceneToLoad = PlayerPrefs.GetString("ReturnScene", "Map_HCMC_2060");
            SceneManager.LoadScene(sceneToLoad);
        }

        public void OnPlayerMoved(float distance)
        {
            distanceAccumulated += distance;
            if (distanceAccumulated >= distanceForEncounterCheck)
            {
                distanceAccumulated = 0f;
                CheckForEncounter();
            }
        }

        public void SetCurrentZone(WorldMapZone zone) => currentActiveZone = zone;
        public void ClearCurrentZone(WorldMapZone zone) { if (currentActiveZone == zone) currentActiveZone = null; }

        private void CheckForEncounter()
        {
            bool hasZoneEnemies = currentActiveZone != null && currentActiveZone.zoneEnemies != null && currentActiveZone.zoneEnemies.Count > 0;
            bool hasDefaultEnemies = defaultFallbackEnemies != null && defaultFallbackEnemies.Count > 0;

            if (!hasZoneEnemies && !hasDefaultEnemies) return;

            if (Random.value <= encounterChance) TriggerEncounter();
        }

        private void TriggerEncounter()
        {
            List<CharacterData> poolToUse = (currentActiveZone != null && currentActiveZone.zoneEnemies != null && currentActiveZone.zoneEnemies.Count > 0)
                ? currentActiveZone.zoneEnemies
                : defaultFallbackEnemies;

            if (poolToUse == null || poolToUse.Count == 0) return;

            var randomEnemyData = poolToUse[Random.Range(0, poolToUse.Count)];

            int playerLvl = 1;
            if (GameStateManager.Instance != null && GameStateManager.Instance.GetMainPlayer() != null)
            {
                playerLvl = GameStateManager.Instance.GetMainPlayer().level;
            }

            var enemyStats = randomEnemyData.CreateStats(playerLvl);
            if (GameStateManager.Instance != null)
            {
                GameStateManager.Instance.nextEnemies = new List<CharacterStats> { enemyStats };
            }

            // --- FIX CRASH: Chỉ lưu vị trí nếu tìm thấy Player ---
            if (worldMapPlayer != null)
            {
                PlayerPrefs.SetFloat("WorldPositionX", worldMapPlayer.transform.position.x);
                PlayerPrefs.SetFloat("WorldPositionY", worldMapPlayer.transform.position.y);
            }

            PlayerPrefs.SetInt("ReturningFromBattle", 1);
            PlayerPrefs.SetString("ReturnScene", SceneManager.GetActiveScene().name);
            PlayerPrefs.Save();

            SceneManager.LoadScene("Battle");
        }
    }
}
```



#### WorldMapPlayer.cs
```csharp
using UnityEngine;
using UnityEngine.EventSystems;

namespace RebirthWarrior.WorldMap
{
    public class WorldMapPlayer : MonoBehaviour
    {
        [Header("Settings")]
        [SerializeField] private float moveSpeed = 3.0f;

        private Vector2 targetPosition;
        private bool isMoving = false;
        private Animator animator;

        private void Awake()
        {
            targetPosition = transform.position;
            animator = GetComponent<Animator>();
        }

        private void Update()
        {
            // Trong WorldMap, chúng ta dùng chuột để click
            if (Input.GetMouseButtonDown(0))
            {
                // Check không click vào UI
                if (EventSystem.current != null && EventSystem.current.IsPointerOverGameObject()) return;

                Vector3 mousePos = Camera.main.ScreenToWorldPoint(Input.mousePosition);
                SetTarget(new Vector2(mousePos.x, mousePos.y));
            }

            Move();
        }

        public void SetTarget(Vector2 target)
        {
            targetPosition = target;
            isMoving = true;
            if (animator) animator.SetBool("IsMoving", true);

            // Flip X logic
            if (targetPosition.x < transform.position.x) transform.localScale = new Vector3(-1, 1, 1);
            else transform.localScale = new Vector3(1, 1, 1);
        }

        private void Move()
        {
            if (!isMoving) return;

            float step = moveSpeed * Time.deltaTime;
            Vector3 previousPos = transform.position;

            transform.position = Vector2.MoveTowards(transform.position, targetPosition, step);

            // Tính distance để báo cho Manager (Random Encounter)
            float dist = Vector3.Distance(previousPos, transform.position);
            if (dist > 0 && WorldMapManager.Instance != null)
            {
                WorldMapManager.Instance.OnPlayerMoved(dist);
            }

            if (Vector2.Distance(transform.position, targetPosition) < 0.01f)
            {
                isMoving = false;
                if (animator) animator.SetBool("IsMoving", false);
            }
        }
    }
}
```



#### WorldMapZone.cs
```csharp
using UnityEngine;
using System.Collections.Generic;
using RebirthWarrior.Character;

namespace RebirthWarrior.WorldMap
{
    [RequireComponent(typeof(PolygonCollider2D))] // Dùng Polygon để vẽ hình dáng méo mó tùy ý
    public class WorldMapZone : MonoBehaviour
    {
        [Header("Zone Info")]
        public string zoneName = "Vùng An Toàn";
        [Tooltip("Cấp độ trung bình của quái vùng này (Để tham khảo)")]
        public string levelRange = "Lv 1 - 10";

        [Header("Enemies In This Zone")]
        public List<CharacterData> zoneEnemies; // Danh sách quái riêng

        private void Awake()
        {
            // Tự động set trigger để Player đi xuyên qua được
            GetComponent<Collider2D>().isTrigger = true;
        }

        private void OnTriggerEnter2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                // Báo cho Manager biết Player đã vào vùng này
                WorldMapManager.Instance.SetCurrentZone(this);
            }
        }

        private void OnTriggerExit2D(Collider2D other)
        {
            if (other.CompareTag("Player"))
            {
                // Báo cho Manager biết Player đã ra khỏi vùng (Về mặc định)
                WorldMapManager.Instance.ClearCurrentZone(this);
            }
        }
    }
}
```




## PHẦN D: PREFABS

### D1. UI Prefabs

#### BattleItemSlot.prefab
```
├── Canvas (Environment)
│   ├── BattleItemSlot
│   │   ├── icon
│   │   ├── name
│   │   └── Quantity
```

#### BattleItemSlot 1.prefab
```
├── Canvas (Environment)
│   ├── BattleItemSlot
│   │   ├── ItemText
│   │   ├── icon
│   │   └── qty
```

#### BattleStation_Prefab.prefab
```
BattleStation_Prefab (Panel)
├── SpawnPoint
├── HUD_Canvas
│   ├── selectindi
│   ├── Name
│   ├── Level
│   ├── HP Bar
│   │   ├── Background
│   │   └── Fill Area
│   │       └── HPFill (Image - Green)
│   └── mana
│       ├── Background
│       └── Fill Area
│           └── HPFill (Image - blue)
```

#### CharacterSlot.prefab
```
CharacterSlot (Panel)
├── khung-portrait (Image)
├── Portrait (Image)
├── CharacterName (TMPro)
├── HPBar (Slider)
│   ├── Background
│   ├──  Fill Area
│   │   └── HPFill (Image - Green)
├── HPText (TMPro)
└── MPBar (Slider)
│   ├── Background
│   ├──  Fill Area
│   │   └── HPFill (Image - Green)
├── MPText (TMPro)
```

#### ChoiceButton_Prefab.prefab
```
├── Canvas (Environment)
│   ├── ChoiceButton_Prefab
│   │   └── Text
```

#### Dialog_Panel_NPC.prefab
```
├── Canvas (Environment)
│   ├── Dialog_Panel_NPC
│   │   ├── khungdialouge
│   │   ├── NPCNameText
│   │   ├── Avatar_right
│   │   └── DialogueText
```

#### Dialog_Panel_Player.prefab
```
├── Canvas (Environment)
│   ├── Dialog_Panel_Player
│   │   ├── khungdialouge
│   │   ├── NPCNameText
│   │   ├── Avatar_right
│   │   └── DialogueText
```

#### dmagepopup.prefab
```
├── Canvas (Environment)
│   ├── dmagepopup
│   │   └── dmgtxt
```

#### DropSlotUI.prefab
```
├── Canvas (Environment)
│   ├── DropSlotUI
│   │   ├── Icon
│   │   ├── Name
│   │   └── Quantity
```


#### EquipSlotUI.prefab
```
EquipSlotUI (Button)
├── Icon (Image)
└── SlotNameText (TMPro)

```



#### ItemButton.prefab
```
ItemButton (Button)
├── ItemName (TMPro)
├── Icon (Image)
└── Price (TMPro)

```

#### ItemSlot.prefab
```
ItemSlot (Button)
├── Icon (Image)
└── Quantity  (TMPro)

```

#### Panel_SaveLoad.prefab
```
Canvas (Environment)
├── Panel_SaveLoad
│   ├── title panel
│   ├── closeButton
│   └── containerslot

```

#### PartyMemberIcon.prefab
```
Canvas (Environment)
PartyMemberUI (Panel)
├── Avatar (Image)
├── Name (TMPro)
├── Level (TMPro)
└── Lvltext (TMPro)
```


#### PartySlotButton.prefab
```
Canvas (Environment)
PartySlotButton 
├── InUseVisuals (Image)
│   ├── Image
│   ├── Portrait
│   ├── Text (TMP)
│   ├── NameText
│   ├── LevelText
│   ├── HighlightBorder
│   └── removeButton
│       └── Text (TMP)
└── EmptySlotVisuals
    └── EmptyText
```

#### PetSlot.prefab
```
Canvas (Environment)
PartyMemberUI (Panel)
├── Icon (Image)
├── LevelText (TMPro)
└── SelectionBorder
```

#### QuestListSlot_Prefab.prefab
```
Canvas (Environment)
QuestListSlot_Prefab
└── QuestButton
    └── questTitleText
```

#### QuestObjectiveUI_Prefab.prefab
```
Canvas (Environment)
QuestObjectiveUI_Prefab
├── ObjectiveText
└── ProgressText
```

#### saveslot.prefab
```
Canvas (Environment)
saveslot
├── Empty Text
├── Content
│   ├── DoiHinh
│   ├── Map
│   ├── Left_PartyArea
│   │   └── PartyContainer
│   ├── Middle_InfoArea
│   │   ├── GoldText
│   │   ├── TimeText
│   │   └── DateText
│   └── Right_MapArea
│       ├── MapName
│       └── ScreenshotMask
│           └── MapImage
└── deletebutton
```

#### SkillButton_Prefab.prefab
```
Canvas (Environment)
SkillButton_Prefab
├── Icon
├── SkillNameText
└── MPCostText
```


#### VictorySlot.prefab
```
Canvas (Environment)
VictorySlot
├── Portrait (Image)
├── Name
├── Level
├── EXP Bar (Slider)
│   ├── Background
│   └── Fill Area
│       └── Fill (Image - Green)
├── EXP Gain
└── Level Up!
```

### D2. icon
#### QuestPointer_Prefab.prefab
```
Canvas (Environment)
└── QuestPointer_Prefab
```

### D3. icon
Chúng ta sẽ có 2 prefab làm base, sau đó sẽ tạo Prefab Variant để nhân bản:
1- Cho toàn bộ Followers, Pet với Skeletal để rigging attack animation theo hướng NE
2- Cho toàn bộ Enemy với Skeletal để rigging attack animation theo hướng SW

Prefab riêng Cho Main Player với Skeletal để rigging toàn bộ animation di chuyển theo 8 hướng, và attack animation theo hướng NE


### D4. PrefabsParty

#### PartyMemberSlot.prefab
```
PartyMemberSlot (Panel)
├── NameText (TMPro)
├── LevelText (TMPro)
├── HPLabel (TMPro)
├── HPText (TMPro)
├── HPBar (Slider)
│   ├── Background
│   └── Fill (Image - Green)
├── MPLabel (TMPro)
├── MPText (TMPro)
└── MPBar (Slider)
│   ├── Background
│   └── Fill (Image - Green)
```

#### WorldPartyMemberSlot.prefab
```
WorldPartyMemberSlot (Panel)
├── NameText (TMPro)
├── LevelText (TMPro)
├── HPLabel (TMPro)
├── HPText (TMPro)
├── HPBar (Slider)
│   ├── Background
│   └── Fill (Image - Green)
├── MPLabel (TMPro)
├── MPText (TMPro)
└── MPBar (Slider)
│   ├── Background
│   └── Fill (Image - Green)
```


## PHẦN E: SCENES

### E1. MainMenu.unity  
- Main Menu Canvas
  - Title
  - New Game Button
  - Load Game Button
  - Setting Button
  - Credits Button
- Background Image
- BGM Audio Source

├── Main Camera
├── Canvas (Component MainMenu.cs , DialogueUIInitializer.cs )
│    ├── BackgroundImage
│    ├── BackgroundOverlay
│    ├── VideoRawImage
│    ├── Menu_Panel
│    │   └── ButtonLayout
│    │       ├── NewGame_Button
│    │       ├── LoadGame_Button
│    │       └── Options_Button
│    └── Version (TMPro)
├── EventSystem
├── _GameSystems (Component InventoryManager.cs , LocalizationManager.cs, DialogueManager.cs, MenuIntroController.cs, GameManager.cs )
│    └── RebirthManager
└── InventoryUI_Persistent (Component InventoryUI.cs, SaveLoadManager.cs , QuestNavigator.cs, WorldUIManager.cs, CanvasResetter.cs  )
     ├── PartyManagementPanel  (Component PartyManagementUI.cs)
     │   ├── Title (TMPro)
     │   ├── ClosePartyPanel_Button (Button)
     │   ├── BattleTeam_Label (TMPro)
     │   ├── BattleTeamContainer     
     │   ├── Reserve_Label  (TMPro)    
     │   └── ReserveScrollView (Scrollview)
     │       ├── Viewport
     │       │   └── ReserveTeamContainer
     │       ├── Scrollbar Horizontal
     │       └── Scrollbar Vertical
     ├── StatsPanel (Component CharacterStatsUI.cs)
     │   ├── Stats Info (TMPro)
     │   ├── CharacterName_Text_v2 (TMPro)
     │   ├── StatsList_Text_Left (TMPro)
     │   ├── StatsList_Text_Right (TMPro)
     │   ├── Stats_CharacterPortrait   
     │   │    ├── Portrait_Outfit
     │   │    ├── Portrait_Eyes
     │   │    └── Portrait_Hair
     │   ├── Stats_PrevChar_Button  (Button)    
     │   ├── Stats_NextChar_Button  (Button)    
     │   ├── SkillScrollView_StatsPanel    
     │   │    ├── SkillList_Container
     │   │    │   └── Content
     │   │    ├── Scrollbar Horizontal
     │   │    └── Scrollbar Vertical
     │   └── Close_StatsPanel_Button  (Button)
     ├── InventoryPanel
     │   ├── Image  (background inventory panel)
     │   ├── Header
     │   │    ├── Title
     │   │    ├── GoldText
     │   │    └── CloseButton
     │   ├── ItemScrollView
     │   │    ├── Viewport
     │   │    │   └── ItemGridContainer
     │   │    ├── Scrollbar Horizontal
     │   │    └── Scrollbar Vertical
     │   ├── ItemDetailsPanel
     │   │    ├── khung-icon 
     │   │    ├── ItemIcon     
     │   │    ├── ItemName
     │   │    ├── ItemType
     │   │    ├── ItemDescription
     │   │    ├── ItemStats
     │   │    ├── ActionButton
     │   │    └── DropButton
     │   ├── EquipmentPanel_v2
     │   │    ├── ItemDetailsPanel (sử dụng EquipSlotUI.prefab copy)
     │   │    │    ├── HeadSlot.prefab
     │   │    │    │    ├── Icon
     │   │    │    │    └── SlotNameText       
     │   │    │    ├── ArmorSlot.prefab
     │   │    │    │    ├── Icon
     │   │    │    │    └── SlotNameText                
     │   │    │    ├── WeaponSlot
     │   │    │    │    ├── Icon
     │   │    │    │    └── SlotNameText            
     │   │    │    ├── ShieldSlot.prefab
     │   │    │    │    ├── Icon
     │   │    │    │    └── SlotNameText                
     │   │    │    ├── HandsSlot.prefab
     │   │    │    │    ├── Icon
     │   │    │    │    └── SlotNameText              
     │   │    │    ├── RingSlot.prefab
     │   │    │    │    ├── Icon
     │   │    │    │    └── SlotNameText          
     │   │    │    └── FeetSlot.prefab         
     │   │    │         ├── Icon
     │   │    │         └── SlotNameText          
     │   │    ├── CharacterNameText
     │   │    ├── CharacterPortrait
     │   │    │    ├── Portrait_Outfit
     │   │    │    ├── Portrait_Eyes
     │   │    │    └── Portrait_Hair        
     │   │    ├── CharacterStatsText
     │   │    ├── Button_PrevChar   
     │   │    ├── Button_NextChar
     │   │    ├── petMgmtButton   
     │   │    └── Button        
     │   │         ├── Stats_button   
     │   │         ├── PartyMgmt_Button   
     │   │         └── Button_QuestLog                  
     │   ├── CharacterSelectionPanel
     │   │    ├── Title
     │   │    ├── Scroll View
     │   │    │    ├── Viewport
     │   │    │    │    └── CharacterGrid
     │   │    │    ├── Scrollbar Horizontal
     │   │    │    └── Scrollbar Vertical
     │   │    └── CancelButton
     │   ├── DragIcon     
     │   └── FeedbackPanel
     │       └── FeedbackText
     ├── Panel_QuestLog (Component QuestLogUI.cs)
     │   ├── Title_Quest_Panel (TMPro)
     │   ├── CloseButton    
     │   ├── LeftPanel    
     │   │    ├── Tab_Container
     │   │    │   ├── ActiveQuests_Button 
     │   │    │   └── CompletedQuests_Button
     │   │    └── QuestList_ScrollView
     │   │        ├── Viewport
     │   │        │    └── QuestList_Content         
     │   │        ├── Scrollbar Horizontal           
     │   │        └── Scrollbar Vertical   
     │   └── RightPanel
     │        ├── QuestTitle_Text   
     │        ├── QuestDescription_ScrollView
     │        │   ├── Viewport
     │        │   │    └── Content   
     │        │   │        └── QuestDescription_Text      
     │        │   ├── Scrollbar Horizontal           
     │        │   └── Scrollbar Vertical 
     │        ├── Objectives_Header
     │        ├── Objectives_Container
     │        ├── Rewards_Header
     │        ├── Rewards_Container                   
     │        └── TrackQuest_Button
     ├── World_Buttons_Container
     │   ├── Button_Inventory_Persistent
     │   └── Button_QuestLog_Persistent
     ├── PetManagementPanel     (Component PetManagementUI.cs)
     │   ├── Background    
     │   ├── Title
     │   ├── LeftSide_Active        
     │   │    ├── Portraitr
     │   │    ├── NameText
     │   │    ├── StatsText              
     │   │    └── ButtonRest
     │   ├── RightSide_Storage        
     │   │    ├── Label
     │   │    ├── Scroll View
     │   │    │   ├── Viewport
     │   │    │   │    └── PetGridContainer  
     │   │    │   ├── Scrollbar Horizontal           
     │   │    │   └── Scrollbar Vertical 
     │   │    ├── SummonButton              
     │   │    └── EmptyText              
     │   └── CloseButton     
     ├── Panel_SaveLoad (prefab)
     │   ├── title panel
     │   ├── closeButton    
     │   └── containerslot
     ├── DIALOGUE_SYSTEM_WRAPPER (Component DialogueUIInitializer.cs)
     │   ├── Dialog_Panel_NPC (prefab)
     │   ├── Dialog_Panel_Player (prefab)    
     │   ├── ChoiceButton_Prefab (prefab)  
     │   └── ContinueButton
     ├── videoplayer
     ├── _QuestManager (Component QuestManager.cs)
     ├── nhacnen_quanlyloop
     └── audiosource-quanlynoloop
         
### E2. WorldScene.unity
- World Map (10 Regions)
- Player Avatar
- Location Markers (Towns/Dungeons)
- Random Encounter System
- Minimap UI
- Party Status UI

WorldScene
├── Main Camera
├── Grid
│    ├── Ground
│    ├── Obstacles
│    └── Decoration
├── PlayerToken
├── EncounterManager
├── WorldManager (Component WorldManager.cs)
├── Canvas
│    ├── InteractionPrompt
│    │   └── PromptText
│    └── PartyStatusPanel (Component PartyStatusUI.cs)
│        ├── GoldText
│        ├── ExpText
│        └── MemberContainer
├── PartyUIBuilder
├── REGION_1_SEA
│    ├── Loc_NeoSaigon (Component Maplocation.cs)
│    │   └── 9-Sliced
│    └── Zone_Spawn_SEA
├── REGION_2_CHINA_RUSSIA
├── REGION_3_Japan_Korea
├── REGION_4_EU
├── REGION_5_USA
├── Audio Source
└── _WorldMapSystem (Component worldmapmanager.cs)

### E3. Battle.unity
- Battle Background (Dynamic based on location)
- Party Positions (4 slots + 1 pet)
- Enemy Positions (6 slots)
- Battle UI Canvas
- Battle Manager
- Turn Manager
- Camera Controller

BattleUI
├── Main Camera
├── Grid
│    ├── Ground
│    ├── Obstacles
│    └── Decoration
├── BattlePositions
│    ├── Player_Side
│    │   ├── P_Station_1
│    │   ├── P_Station_2
│    │   ├── P_Station_3
│    │   ├── P_Station_4
│    │   ├── P_Station_5
│    │   ├── P_Station_6
│    │   └── P_Station_0
│    └── Enemy_Side
│        ├── E_Station_0
│        ├── E_Station_1
│        ├── E_Station_2
│        ├── E_Station_3
│        ├── E_Station_4
│        ├── E_Station_5
│        └── E_Station_6
├── Canvas
│    ├── Character Detail Panel
│    │   ├── Detail Avatar
│    │   ├── Name
│    │   ├── Level
│    │   ├── detail Stats
│    │   └── Close
│    ├── BattleLogPanel
│    │   ├── BattleLogScrollView
│    │   └── LogText (TMPro)
│    ├── ActionPanel
│    │   ├── AttackButton
│    │   ├── SkillButton
│    │   ├── DefendButton
│    │   ├── BattleItemSlot 1 (prefab)
│    │   └── EscapeButton
│    ├── BattleUI
│    ├── SkillPanel
│    │   ├── Scroll View
│    │   │   ├── SkillGridContainer
│    │   │   │   └── Content 
│    │   │   ├── Scrollbar Horizontal
│    │   │   └── Scrollbar Vertical
│    │   └── SkillPanel_CloseButton
│    ├── ItemPanel
│    ├── TargetSelectionPanel
│    ├── EnemyTurnPanel
│    │   └── EnemyTurnText (TMPro)
│    ├── VictoryPanel
│    │   ├── Background (Image)
│    │   ├── VictoryText (TMPro)
│    │   ├── GoldText
│    │   ├── ContinueButton
│    │   ├── CharacterListContainer (Image - Horizontal layout group)
│    │   └── LootGrid (Image - Grid layout group)
│    ├── DefeatPanel
│    │   ├── Background (Image)
│    │   ├── DefeatText (TMPro)
│    │   ├── MessageText (TMPro)
│    │   ├── ReturnButton
│    │   └── PenaltyText
│    ├── DialoguePanel
│    │   ├── NameText
│    │   ├── Avatar_Left
│    │   ├── DialogueText
│    │   ├── Choices_Container
│    │   ├── PlayerNameText_Display
│    │   ├── Avatar_Right
│    │   └── Continuebutton
│    └── itempanel
│        ├── Scroll View
│        │   ├── Viewport
│        │   │   └── itemcontainer 
│        │   ├── Scrollbar Horizontal
│        │   └── Scrollbar Vertical
│        └── itemPanel_CloseButton
├── BattleManager
├── TargetSelector
├── SelectionManager
├── BattleLoader
├── Canvas-dmgpopup
└── EventSystem


### E4. Map_HCMC_2025.unity
- Town Layout (Buildings, NPCs)
- Shop Areas
- Quest Givers
- Save Point
- Inn (Heal & Rest)
- Dialogue System

TownScene
├── Main Camera
├── Grid
│    ├── Ground
│    ├── Obstacles
│    └── Decoration
├── Boss_Prologue (prefab) (Component MapBossController.cs)
├── NPC_guard (prefab) (Component NPC.cs, NPCMovement.cs)
│    ├── canvasbubble
│    │   └── bubblecontainer
│    ├── Icon_Available
│    └── Icon_Ready
├── TownExit
├── TownManager (Component TownManager.cs)
├── Spawn_cong_lang
├── Canvas
│    ├── InteractionPrompt
│    │   └── PromptText
│    ├── ShopPanel
│    │   ├── Header
│    │   │   ├── ShopNameText 
│    │   │   ├── GoldText
│    │   │   └── CloseButton
│    │   ├── ItemScrollView
│    │   │   ├── Viewport
│    │   │   │   └── ItemListContainer
│    │   │   └── Scrollbar Vertical
│    │   └── FeedbackPanel
│    │           └── FeedbackText
│    └── InnPanel
│        ├── CostText 
│        ├── GoldText
│        ├── RestButton
│        └── CancelButton
├── DialogueManager (Component DialogueManager.cs)
├── Shop
│    └── canvasbubble
│        └── bubblecontainer
├── Inn
├── Loi di NPC
│    ├── Path_guard
│    │   ├── Point A
│    │   ├── Point B
│    │   ├── Point C
│    │   └── Point D
│    └── Path_shop
│        ├── Point A
│        └── Point B
└── EncounterManager  (Component EncounterManager.cs)

### E4. Map_HCMC_2100.unity
- Town Layout (Buildings, NPCs)
- Shop Areas
- Quest Givers
- Save Point
- Inn (Heal & Rest)
- Dialogue System

TownScene
├── Main Camera
├── Grid
│    ├── Ground
│    ├── Obstacles
│    └── Decoration
├── Boss_Prologue (prefab) (Component MapBossController.cs)
├── NPC_guard (prefab) (Component NPC.cs, NPCMovement.cs)
│    ├── canvasbubble
│    │   └── bubblecontainer
│    ├── Icon_Available
│    └── Icon_Ready
├── TownExit
├── TownManager (Component TownManager.cs)
├── Spawn_cong_lang
├── Canvas
│    ├── InteractionPrompt
│    │   └── PromptText
│    ├── ShopPanel
│    │   ├── Header
│    │   │   ├── ShopNameText 
│    │   │   ├── GoldText
│    │   │   └── CloseButton
│    │   ├── ItemScrollView
│    │   │   ├── Viewport
│    │   │   │   └── ItemListContainer
│    │   │   └── Scrollbar Vertical
│    │   └── FeedbackPanel
│    │           └── FeedbackText
│    └── InnPanel
│        ├── CostText 
│        ├── GoldText
│        ├── RestButton
│        └── CancelButton
├── DialogueManager (Component DialogueManager.cs)
├── Shop
│    └── canvasbubble
│        └── bubblecontainer
├── Inn
├── Loi di NPC
│    ├── Path_guard
│    │   ├── Point A
│    │   ├── Point B
│    │   ├── Point C
│    │   └── Point D
│    └── Path_shop
│        ├── Point A
│        └── Point B
└── EncounterManager  (Component EncounterManager.cs)

### E4. Map_HCMC_2060.unity
- Town Layout (Buildings, NPCs)
- Shop Areas
- Quest Givers
- Save Point
- Inn (Heal & Rest)
- Dialogue System

TownScene
├── Main Camera
├── Grid
│    ├── Ground
│    ├── Obstacles
│    └── Decoration
├── Boss_Prologue (prefab) (Component MapBossController.cs)
├── NPC_guard (prefab) (Component NPC.cs, NPCMovement.cs)
│    ├── canvasbubble
│    │   └── bubblecontainer
│    ├── Icon_Available
│    └── Icon_Ready
├── TownExit
├── TownManager (Component TownManager.cs)
├── Spawn_cong_lang
├── Canvas
│    ├── InteractionPrompt
│    │   └── PromptText
│    ├── ShopPanel
│    │   ├── Header
│    │   │   ├── ShopNameText 
│    │   │   ├── GoldText
│    │   │   └── CloseButton
│    │   ├── ItemScrollView
│    │   │   ├── Viewport
│    │   │   │   └── ItemListContainer
│    │   │   └── Scrollbar Vertical
│    │   └── FeedbackPanel
│    │           └── FeedbackText
│    └── InnPanel
│        ├── CostText 
│        ├── GoldText
│        ├── RestButton
│        └── CancelButton
├── DialogueManager (Component DialogueManager.cs)
├── Shop
│    └── canvasbubble
│        └── bubblecontainer
├── Inn
├── Loi di NPC
│    ├── Path_guard
│    │   ├── Point A
│    │   ├── Point B
│    │   ├── Point C
│    │   └── Point D
│    └── Path_shop
│        ├── Point A
│        └── Point B
└── EncounterManager  (Component EncounterManager.cs)

## PHẦN F: DATA FILES

### F1. Localization Files

#### vi.json
```json
{
  "items": [
    {
      "key": "GAME_TITLE",
      "value": "Chiến Hồn: Huyền Thoại Trọng Sinh"
    },
    {
      "key": "MENU_START",
      "value": "Bắt Đầu"
    },
    {
      "key": "MENU_CONTINUE",
      "value": "Tiếp Tục"
    },
    {
      "key": "MENU_SETTINGS",
      "value": "Cài Đặt"
    },
    {
      "key": "MENU_QUIT",
      "value": "Thoát"
    },
    {
      "key": "BATTLE_ATTACK",
      "value": "Tấn Công"
    },
    {
      "key": "BATTLE_SKILL",
      "value": "Kỹ Năng"
    },
    {
      "key": "BATTLE_DEFEND",
      "value": "Phòng Thủ"
    },
    {
      "key": "BATTLE_ITEM",
      "value": "Vật Phẩm"
    },
    {
      "key": "BATTLE_ESCAPE",
      "value": "Chạy Trốn"
    },
    {
      "key": "STATS_HP",
      "value": "Sinh Lực"
    },
    {
      "key": "STATS_MP",
      "value": "Ma Lực"
    },
    {
      "key": "STATS_LEVEL",
      "value": "Cấp Độ"
    },
    {
      "key": "STATS_EXP",
      "value": "Kinh Nghiệm"
    },
    {
      "key": "STATS_ATK",
      "value": "Tấn Công"
    },
    {
      "key": "STATS_DEF",
      "value": "Phòng Thủ"
    },
    {
      "key": "STATS_MAG",
      "value": "Ma Thuật"
    },
    {
      "key": "STATS_SPD",
      "value": "Tốc Độ"
    },
    {
      "key": "UI_PARTY",
      "value": "Đội Hình"
    },
    {
      "key": "UI_INVENTORY",
      "value": "Hành Trang"
    },
    {
      "key": "UI_QUESTS",
      "value": "Nhiệm Vụ"
    },
    {
      "key": "UI_MAP",
      "value": "Bản Đồ"
    },
    {
      "key": "UI_SAVE",
      "value": "Lưu Game"
    },
    {
      "key": "UI_LOAD",
      "value": "Tải Game"
    },
    {
      "key": "BATTLE_VICTORY",
      "value": "Chiến Thắng!"
    },
    {
      "key": "BATTLE_DEFEAT",
      "value": "Thất Bại..."
    },
    {
      "key": "BATTLE_EXP_GAINED",
      "value": "Nhận được {0} kinh nghiệm"
    },
    {
      "key": "BATTLE_GOLD_GAINED",
      "value": "Nhận được {0} vàng"
    },
    {
      "key": "CHARACTER_LEVEL_UP",
      "value": "{0} đã lên cấp {1}!"
    },
    {
      "key": "ITEM_OBTAINED",
      "value": "Nhận được {0}"
    },
    {
      "key": "QUEST_COMPLETED",
      "value": "Hoàn thành nhiệm vụ: {0}"
    },
    {
      "key": "DIALOG_CONFIRM",
      "value": "Xác Nhận"
    },
    {
      "key": "DIALOG_CANCEL",
      "value": "Hủy Bỏ"
    },
    {
      "key": "ERROR_SAVE_FAILED",
      "value": "Lưu game thất bại!"
    },
    {
      "key": "ERROR_LOAD_FAILED",
      "value": "Tải game thất bại!"
    },
    {
      "key": "STORY_PROLOGUE_TITLE",
      "value": "Chương Mở Đầu: Trọng Sinh"
    },
    {
      "key": "STORY_PROLOGUE_TEXT",
      "value": "Thế kỷ 21, một game thủ cuồng nhiệt qua đời vì quá say mê game. Linh hồn anh được đưa về Việt Nam thời xưa, khi quân Nguyên đang xâm lược. Với tri thức từ tương lai, liệu anh có thể thay đổi lịch sử?"
    }
  ]
}

```

#### en.json
```json
{
  "items": [
    {
      "key": "GAME_TITLE",
      "value": "Rebirth Warrior: Legends of Vietnam"
    },
    {
      "key": "MENU_START",
      "value": "Start Game"
    },
    {
      "key": "MENU_CONTINUE",
      "value": "Continue"
    },
    {
      "key": "MENU_SETTINGS",
      "value": "Settings"
    },
    {
      "key": "MENU_QUIT",
      "value": "Quit"
    },
    {
      "key": "BATTLE_ATTACK",
      "value": "Attack"
    },
    {
      "key": "BATTLE_SKILL",
      "value": "Skill"
    },
    {
      "key": "BATTLE_DEFEND",
      "value": "Defend"
    },
    {
      "key": "BATTLE_ITEM",
      "value": "Item"
    },
    {
      "key": "BATTLE_ESCAPE",
      "value": "Escape"
    },
    {
      "key": "STATS_HP",
      "value": "Health"
    },
    {
      "key": "STATS_MP",
      "value": "Mana"
    },
    {
      "key": "STATS_LEVEL",
      "value": "Level"
    },
    {
      "key": "STATS_EXP",
      "value": "Experience"
    },
    {
      "key": "STATS_ATK",
      "value": "Attack"
    },
    {
      "key": "STATS_DEF",
      "value": "Defense"
    },
    {
      "key": "STATS_MAG",
      "value": "Magic"
    },
    {
      "key": "STATS_SPD",
      "value": "Speed"
    },
    {
      "key": "UI_PARTY",
      "value": "Party"
    },
    {
      "key": "UI_INVENTORY",
      "value": "Inventory"
    },
    {
      "key": "UI_QUESTS",
      "value": "Quests"
    },
    {
      "key": "UI_MAP",
      "value": "Map"
    },
    {
      "key": "UI_SAVE",
      "value": "Save Game"
    },
    {
      "key": "UI_LOAD",
      "value": "Load Game"
    },
    {
      "key": "BATTLE_VICTORY",
      "value": "Victory!"
    },
    {
      "key": "BATTLE_DEFEAT",
      "value": "Defeat..."
    },
    {
      "key": "BATTLE_EXP_GAINED",
      "value": "Gained {0} experience"
    },
    {
      "key": "BATTLE_GOLD_GAINED",
      "value": "Gained {0} gold"
    },
    {
      "key": "CHARACTER_LEVEL_UP",
      "value": "{0} reached level {1}!"
    },
    {
      "key": "ITEM_OBTAINED",
      "value": "Obtained {0}"
    },
    {
      "key": "QUEST_COMPLETED",
      "value": "Quest completed: {0}"
    },
    {
      "key": "DIALOG_CONFIRM",
      "value": "Confirm"
    },
    {
      "key": "DIALOG_CANCEL",
      "value": "Cancel"
    },
    {
      "key": "ERROR_SAVE_FAILED",
      "value": "Failed to save game!"
    },
    {
      "key": "ERROR_LOAD_FAILED",
      "value": "Failed to load game!"
    },
    {
      "key": "STORY_PROLOGUE_TITLE",
      "value": "Prologue: Rebirth"
    },
    {
      "key": "STORY_PROLOGUE_TEXT",
      "value": "21st century. A hardcore gamer died from gaming addiction. His soul was reborn in ancient Vietnam during the Mongol invasion. With knowledge from the future, can he change history?"
    }
  ]
}

```

## PHẦN G: GAME BALANCE & FORMULAS


### G2. Experience Formula
```
EXP to Next Level = 100 * (1.5 ^ CurrentLevel)
Level 1→2: 150 EXP
Level 10→11: 5,767 EXP
Level 99→100: 1,079,100 EXP
```

### G3. Turn Order
```
Priority = Speed + Random(0, Agility)
Higher priority acts first
```

## PHẦN H: DEVELOPMENT PHASES

### Phase 1: Foundation ✅ (Complete)
- Core systems setup
- Basic character system
- Save/Load system
- Game State Manager

### Phase 2: Battle System ✅ (Complete)
- Turn-based combat
- Enemy AI
- Victory/Defeat conditions
- Rewards system

### Phase 3: World System ✅ (Complete)
- World map navigation
- Town exploration
- NPC dialogue
- Area transitions

### Phase 4: Inventory & Shop ✅ (Complete)
- Inventory management
- Item usage
- Shop system
- Equipment (pending)

### Phase 5: Skills System  ✅ (Complete)
- Skill creation
- Skill UI
- Battle integration
- Skill books (not yet complete)

## Phase 6 : Hệ thống Quản lý Đội hình (Party Management). ✅ (Complete)


### Phase 7: Rebirth System ✅ (Complete)
- Class change mechanic
- Stat retention
- Bonus system
- UI implementation

### Phase 8: Quest System ✅ (Complete)
- Quest Creation
- Quest UI

### Phase 9: Pet System ✅ (Complete)
- Pet Egg Logic (Inventory integration)
- Pet Slot 5 Implementation (Battle & World)
- Pet UI (Master-Detail View: Active/Inactive)
- Fix: Pet Equipment & Party conflict (Fix lỗi NullRefException trong CharacterStats)

### Phase 10: Isometric & 8-Direction Movement  ✅ (Complete)
- Movement Vector Transformation (Isometric logic).
- 8-Direction Input & Normalization.
- Animation Logic: Chuyển sang PlayerAnimation.cs (Angle-based Indexing).
- Physics/Interaction: Điều chỉnh Collider về Bottom Center để tương thích 2.5D.

### Phase 11: Data-Driven Visuals & Customization ✅ (Complete)
- Data: Mở rộng CharacterData và Item.cs để chứa thông tin Visual/Audio/VFX.
- Battle Visuals: Chuyển Battle từ UI sang World Space Prefab (BattleVisualController).
- Customization Core: Áp dụng hệ thống 2D Skeletal Animation (Xương), Sprite Library (đổi giáp), và Animator Override Controller (đổi Animation vũ khí).
- Battle Orientation: Cố định hướng nhìn: Player NE, Enemy SW.

### Phase 12: Hệ Thống Hội Thoại & Tương Tác NPC (Dialogue & Interaction) ✅ (Complete)
#### A. Cấu Trúc Hệ Thống Hội Thoại (Dialogue System)

Hệ thống hội thoại được thiết kế theo mô hình Node-based Data, tách biệt hoàn toàn Logic và UI.

* 1 - Core Manager: DialogueManager (Singleton). Quản lý luồng hội thoại, xử lý lựa chọn và kích hoạt sự kiện.

* 2 - Data Structure: Sử dụng ScriptableObject (DialogueData) để lưu trữ nội dung.

    - DialogueLine: Chứa text, ID người nói (NPC/Player), Sprite cảm xúc (Portrait), và Audio clip.

    - DialogueChoice: Các lựa chọn rẽ nhánh. Mỗi lựa chọn trỏ đến một DialogueData tiếp theo (NextDialogueID).

    - DialogueAction: Sự kiện được kích hoạt khi kết thúc hoặc chọn nhánh (Ví dụ: StartQuest, CompleteQuest, HealParty, GiveItem).

* 3 - Logic Flow:

    - Player tương tác với NPC -> NPCInteractable gọi DialogueManager.StartDialogue(data).

    - UI hiển thị dựa trên người nói (NPC Panel bên trái, Player Panel bên phải).

    - Khi gặp ngã rẽ (Choice), hệ thống sinh ra các Button lựa chọn.

    - Khi kết thúc, hệ thống kiểm tra DialogueAction để cập nhật Quest/Inventory thông qua QuestManager và GameStateManager.

#### B. Hệ Thống Bong Bóng Chat (Bubble Chat System)

Hệ thống hội thoại thời gian thực (Ambient Dialogue) hiển thị trên đầu nhân vật mà không làm gián đoạn gameplay.

* 1 - Implementation: Sử dụng World Space Canvas gắn trực tiếp vào Prefab NPC/Enemy.

* 2 - Logic:

    - Trigger: Kích hoạt khi Player đi vào vùng TriggerZone, hoặc theo chu kỳ ngẫu nhiên (Random Timer), hoặc khi vào trận (BattleCry).

    - Behavior: Text xuất hiện kèm hiệu ứng Fade In/Out và tự động hủy sau $X$ giây.

    - Pooling: (Optimization) Sử dụng Object Pooling cho Bubble để tránh Instantiate quá nhiều trong các khu vực đông đúc (Town).

#### C. NPC AI & Movement (Hệ Thống Di Chuyển NPC)

NPC trong Town/Map tuân thủ quy tắc vật lý và render 2.5D Isometric.

* 1 - Movement States:

    - Idle: Đứng yên, có thể play animation thở/nhìn quanh.

    - Patrol: Di chuyển theo danh sách điểm Waypoints đặt sẵn trong Editor.

    - Wander: Di chuyển ngẫu nhiên trong bán kính WanderRadius quanh điểm xuất phát.

* 2 - Interaction Logic:

    - Khi Player nhấn nút tương tác: NPC chuyển sang trạng thái Interact.

    - Face Player: NPC dừng di chuyển và xoay mặt về hướng Player (dùng Animator blend tree để chọn sprite hướng phù hợp).

    - Sau khi hội thoại kết thúc: NPC quay lại trạng thái cũ (Patrol/Wander).

* 3 - Sorting Order: Sử dụng Transparency Sort Axis (Y-Axis) để xử lý việc NPC đứng trước/sau Player và các vật thể môi trường.

#### D. Tích Hợp Hệ Thống (Integration)

* 1 - Quest Integration: Dialogue System gọi trực tiếp QuestManager.Instance.AcceptQuest(string questID) và CompleteQuest(string questID).

* 2 - ocalization: Toàn bộ Text trong DialogueData hỗ trợ đa ngôn ngữ thông qua LocalizationManager. Key được map theo định dạng DLG_{NPCID}_{SequenceID}.

### Phase 13: NEW FEATURE PLAN: FALLOUT-STYLE MAP (Chưa làm hoàn chỉnh - Lưu cho AI sau)

* 1 - Concept: Thay vì điều khiển nhân vật chạy bộ trên WorldScene rộng lớn, chuyển sang cơ chế Abstract Map (Bản đồ chiến thuật).

* 2 - Mechanics:

    - World Map Scene: Camera nhìn từ trên cao (Top-down/Paper Map). Player là một Token/Pawn di chuyển bằng click chuột.

    - Locations (Địa điểm):

        - Fixed Locations: Thành phố, Hầm ngục cố định theo cốt truyện (luôn hiển thị hoặc unlock).

        - Random Encounters: Khi di chuyển, có tỉ lệ gặp quái -> Chuyển cảnh sang Battle Scene.

        - Random Locations: Hệ thống sinh ngẫu nhiên các địa điểm (Thị trấn hoang, Ốc đảo, Trại buôn) tại tọa độ ngẫu nhiên khi New Game.

* 3 -Discovery: Các địa điểm Random ban đầu bị ẩn (Hidden). Khi Token đi ngang qua phạm vi nhất định -> Hiện lên (Discovered) -> Cho phép bấm "Enter" để vào Scene chi tiết (2.5D Gameplay).

* 4 -Persistency: Lưu lại tọa độ các Random Location đã tìm thấy vào Save File để lần sau load game chúng vẫn ở đó.

### Phase 14: Cập nhật lại stats, damage, thêm 5 survival skills.  (Chưa làm hoàn chỉnh - Lưu cho AI sau)
#### A. Hệ thống chỉ số mới (Stats Refactor)
* 1 - Toxic Attack (Thay Magic):

    - Đây là chỉ số tấn công đặc biệt (Elemental Damage).

    - Logic Damage: Khi tính sát thương, nó sẽ tách làm 2 phần:

    - Physical Dmg = Attacker.Attack - Defender.Defense (Nếu < 0 thì bằng 0).

    - Toxic Dmg = Attacker.Toxic - Defender.ToxicResist (Nếu < 0 thì bằng 0).

    - Tổng Dmg = Physical Dmg + Toxic Dmg.

* 2 - Ý nghĩa: Vũ khí tẩm độc hoặc Zombie phun độc sẽ xuyên qua giáp vật lý (Defense), chỉ có mặc đồ kháng độc (Toxic Resist) mới đỡ được.

* 3 - Sinh Lực - Stamina (Thay Mana):

    - Dùng cho: Chạy (Sprint), Kỹ năng đặc biệt, và tiêu hao theo thời gian.

    - Nếu Stamina <= 0: Nhân vật dính trạng thái "Suy kiệt" -> Trừ HP theo thời gian (VD: -1% HP mỗi giây thực).

#### B. Hệ thống Thời gian (Game Time System)
* 1 - Cấu trúc: Một GameTimeManager quản lý giờ/phút/ngày.

* 2 - Cấu hình (Inspector):

    - RealSecondsPerGameMinute: Bao nhiêu giây ngoài đời = 1 phút trong game (cho Map thường).

    - WorldMapMinutesPerStep: Mỗi bước đi trên WorldMap tốn bao nhiêu phút game.

* 3 - Cơ chế:

    - Update liên tục biến CurrentTotalMinutes.

    - Từ đó quy đổi ra: Day, Hour, Minute.

    - Gửi sự kiện OnHourChanged (để tính đói/khát).

#### C. CƠ CHẾ MỞ KHÓA (LOCKPICKING) & THƯỞNG

* 1 - Logic: Chúng ta không gán cứng item vào từng cái rương (vì làm map rất mệt). Thay vào đó, chúng ta dùng ScriptableObject gọi là LootTable.

    - Ví dụ: Sếp tạo 1 bảng Loot_YTe_Cap1. Trong đó quy định: 50% ra Băng gạc, 10% ra Thuốc kháng sinh, 40% ra Cồn.

    - Khi Map load: Cái rương vẫn trống rỗng (để nhẹ game).

    - Khi Mở Khóa Thành Công: Lúc này code mới chạy hàm GenerateLoot(). Nó dựa vào % trong bảng trên để sinh ra item thật.

    - Vàng/Tiền: Vàng cũng được coi là 1 Item (ID: "Gold"), có số lượng ngẫu nhiên (ví dụ 50-100).

* 2 - Hiển thị: Sau khi mở khóa xong, game sẽ bật panel Loot UI (giống như mở hòm đồ), hiển thị danh sách các món vừa quay ra được. Player bấm "Take All" để vơ vét.


#### D. CƠ CHẾ MÓC TÚI (PICKPOCKETING) & NPC INVENTORY
Sếp đề xuất hiển thị Panel túi đồ NPC là rất chuẩn (giống Skyrim/Fallout). Dưới đây là cách xử lý kỹ thuật để đảm bảo hiệu năng và logic reset.

* 1 - Định nghĩa "Túi NPC"
    - NPC không cần một hệ thống Inventory phức tạp như Player (không cần slot trang bị, không cần sắp xếp đẹp).

    - Cấu trúc: Mỗi NPC sẽ có một component LootContainer.

    - Dữ liệu: Component này chứa 2 thứ:

    - LootTable (Dữ liệu gốc): Quy định NPC này thường mang theo cái gì (VD: Lính gác thì mang đạn, dân thường mang thức ăn).

    - CurrentItems (List<Item>): Danh sách thực tế đang có trong túi lúc này.

* 2 - Logic Móc Túi & Hiển thị
    - Trigger: Player đứng gần -> Bấm "Móc túi" -> Check tỷ lệ thành công.

    - Nếu Thành Công:

        - Mở Loot UI (Chính là cái UI dùng cho mở Rương ở trên).

        - Bên trái là Túi Player, Bên phải là Túi NPC (List CurrentItems).

        - Player kéo đồ từ phải sang trái để lấy.

    - Hệ quả:

        - Item bị lấy sẽ xóa khỏi list CurrentItems của NPC.

        - Nếu lấy sạch -> CurrentItems rỗng.

        - NPC vẫn hoạt động bình thường (trừ khi Sếp muốn NPC phản ứng nếu mất vũ khí - nhưng cái đó phức tạp, tạm thời cứ để logic là mất item trong túi ảo thôi).

* 3 - Cơ chế Reset (Làm mới túi đồ)
Để thế giới sống động, túi NPC cần được làm đầy lại sau một thời gian (để Player còn có cái mà farm tiếp).

    - Config: Trong Inspector của NPC (hoặc Global Config), có biến RestockHours = 24 (game time).

    - Logic:

        - Mỗi NPC lưu một biến lastRestockTime.

        - Khi Player tương tác (Móc túi): Code kiểm tra CurrentGameTime - lastRestockTime.

        - Nếu thời gian trôi qua > RestockHours:

        - Xóa sạch CurrentItems cũ (nếu còn rác).

        - Chạy lại GenerateLoot() từ LootTable để sinh đồ mới.

        - Cập nhật lastRestockTime mới.

        - Lợi ích: Dù Player rời map hay ở lại map, chỉ cần đủ thời gian trôi qua là túi tự đầy lại. Không cần load lại Scene.


#### E. Kỹ năng Nấu ăn & Chế thuốc (Crafting System)
Hai kỹ năng này có logic giống nhau, chỉ khác Data.

* 1 - Điều kiện Unlock: Player phải dùng Item SkillBook (Sách dạy nấu ăn/Sách y học) để học skill lần đầu.

* 2 - Điều kiện Chế tạo:

    - Phải có Item công cụ trong người (Nồi nấu ăn / Bộ dụng cụ hóa học). Không cần đứng cạnh lửa.

* 3 - Logic Panel:

    - Hiện danh sách công thức (Recipes).

    - Mỗi Recipe có RequiredLevel. Nếu SkillLevel < RequiredLevel -> Ẩn hoặc hiện khóa (Locked).

    - Khi bấm "Chế tạo" -> Kiểm tra nguyên liệu trong Inventory -> Trừ nguyên liệu -> Thêm thành phẩm -> Tăng XP Kỹ năng.

* 4 - Tiến trình:

    - Level 0-4: Chỉ thấy công thức Cấp 1.

    - Level 5: Unlock công thức Cấp 2.

    - Level 10: Unlock công thức Cấp 3...

#### F. Kỹ năng Chế tạo & Sửa chữa Vũ Khí / Giáp
* 1 - Chế tạo: Tương tự Nấu ăn (cần Tool, Recipe).

* 2 - Sửa chữa:

    - Item trang bị (Vũ khí/Giáp) sẽ có chỉ số CurrentDurability / MaxDurability.

    - Khi sửa: Tốn nguyên liệu (Scrap) -> Hồi phục Durability dựa trên Skill Level.


#### G. CÁC FILE liên quan:
DANH SÁCH FILE SCRIPTS CẦN CUNG CẤP & CHỈNH SỬA
Dựa trên phân tích trên, để triển khai hệ thống Kỹ Năng Sinh Tồn (Crafting, Lockpick, Pickpocket) và Thời Gian, tôi cần Sếp chuẩn bị các file sau.

    - GameTimeManager.cs: Quản lý ngày/giờ, tốc độ trôi thời gian.

    - SkillManager.cs: Quản lý Level, XP của 5 kỹ năng (Mở khóa, Móc túi, Nấu ăn, Y tế, Chế tạo).

    - LootSystem.cs: Quản lý rương đồ, túi NPC và cơ chế Reset.

    - CraftingRecipe.cs: ScriptableObject định nghĩa công thức nấu ăn/chế tạo.

    - LootUI.cs (chưa viết): Panel hiển thị đồ trong Rương/Túi NPC để Player nhặt.

    - CraftingUI.cs (chưa viết): Panel hiển thị danh sách công thức và nút chế tạo.



### Phase 15: Content Creation ❌ (Not Started)
- 15 playable characters
- 50+ enemies
- 100+ items
- 30+ skills
- 10+ towns
- Quest content

### Phase 16: Polish & Testing ❌ (Not Started)
- Balance testing
- Bug fixes
- Performance optimization
- Audio implementation
- Visual effects

## PHẦN I: KNOWN ISSUES & BUGS

### Resolved Issues ✅

### Current Issues ⚠️
- 1. Lỗi Desync trong Battle (Nghiêm trọng) 🔴
Vị trí: BattleManager.cs và BattleVisualController.cs.

Vấn đề: Trong BattleManager, các coroutine như ExecuteActionRoutine sử dụng WaitForSeconds(1f) hoặc 0.5f (hardcoded) để chờ animation kết thúc.

Rủi ro: Nếu animation đánh của nhân vật dài hơn 1 giây (hoặc máy lag), logic game sẽ chạy tiếp sang lượt sau trong khi nhân vật vẫn đang múa kiếm. Điều này gây ra lỗi chồng chéo lượt, UI hiện sai hoặc crash game.
- 2. Lỗi Race Condition trong Singleton (Trung bình) 🟡
Vị trí: GameInitializer.cs, GameStateManager.cs, InventoryManager.cs.

Vấn đề: Tất cả đều khởi tạo trong Awake(). Nếu GameInitializer chạy trước GameStateManager trong Awake, nó sẽ báo lỗi NullReferenceException.

Rủi ro: Game lúc chạy được lúc không tùy thuộc vào thứ tự load scene của Unity.
- 3. Lỗi Logic "Ghost Slot" trong Inventory (Tiềm ẩn) 🟡
Vị trí: InventoryManager.cs.

Vấn đề: Hệ thống hỗ trợ item chiếm nhiều ô (Multi-slot item) nhưng logic TryMoveItem rất phức tạp và dễ toang khi di chuyển một item to đè lên một item to khác.

### New System Constraints (BẮT BUỘC TUÂN THỦ) ⚠️
1. **Art Asset Standard (2D Skeletal):** Mọi nhân vật/trang bị mới phải được Rigging (tạo xương) bằng **Unity 2D Animation Package**. Sprite phải có Pivot ở **Bottom Center**.
2. **Sprite Library:** Giáp/quần áo mới phải được thêm vào **Sprite Library Asset** và được tham chiếu bằng **Label** trong `Item.cs` để `BattleVisualController` đổi skin.
3. **Animation Override:** Khi thêm một WeaponType mới (khác kiếm/súng), BẮT BUỘC phải tạo một **Animator Override Controller** mới và gán vào `BattleVisualController`.
4. **Isometric Setup:** World Environment phải sử dụng **Transparency Sort Axis Y=1**.
5. **Singleton EventSystem:** Sử dụng SceneEventSystemDestroyer trong các Scene con (Town, Battle) để tự hủy EventSystem thừa, tránh xung đột với DontDestroyOnLoad từ MainMenu.
6. **Scene Management:** Luôn kiểm tra GameStateManager.Instance và InventoryUI_Persistent trước khi gọi logic UI/Data.
7. **Quest IDs:** Đảm bảo tính nhất quán tuyệt đối giữa QuestID, ObjectiveID, ItemID và NPCID trong Database (String Matching).


## PHẦN J: OPTIMIZATION NOTES

### Mobile Optimization
- Touch input support required
- UI scaling for different screens
- Battery optimization needed
- Memory management for low-end devices
- Texture atlasing for sprites

### Performance Tips
- Object pooling for battle effects
- Async scene loading
- LOD system for world map
- Culling for off-screen objects
- Batch sprite rendering

## PHẦN K: TESTING


---

**END OF SUPER PROMPT**
**Last Updated:** December 2025
**Version:** 3.0
**Total Progress:** ~70% Complete
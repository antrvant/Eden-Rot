# Scenes - CH003

Metadata:

- chapterID: CH003
- sourceFilename: chapter_003_loi_nhan_tren_tu_lanh.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH003_EMPTY_APARTMENT | A Home That Is No Longer Home | LOC_CH003_TRUNG_APARTMENT_1208 | Slow the pace and turn family objects into investigation evidence. | Trung stands in the empty apartment after Chapter 002. | Player finds emotional items and prepares to follow Mai's note. | char_trung;char_mai;char_binh | none | ITM_CH003_FRIDGE_NOTE;ITM_CH003_BROKEN_BINH_TOY;ITM_CH003_BINH_DRAWING;ITM_CH003_FOLDED_FAMILY_PHOTO;ITM_CH003_UNEATEN_LUNCH_BOX | Scene 1 - Nha khong con la nha. |
| SCN_CH003_CHALK_TRAIL | Chalk on the Stairs | LOC_CH003_STAIRWELL | Introduce tracking marker system and Binh's handprint motif. | Player exits apartment looking for the first chalk mark. | Player identifies direction through stairwell and can confront lying neighbor. | char_trung;npc_lying_neighbor | ENM_CH003_TRAPPED_STAIRWELL_INFECTED | ITM_CH003_CHALK_ARROW;ITM_CH003_BINH_HANDPRINT | Scene 2 - Dau phan tren cau thang. |
| SCN_CH003_NEIGHBOR_TRADE | Neighbor Trade | LOC_CH003_FLOOR_09_NEIGHBOR | Show kindness, bargaining, and social fracture inside the apartment building. | Player follows trail to Floor 9 or neighbor apartment. | Player receives testimony, Ba Bay request, or social consequence. | char_trung;npc_neighbor;npc_ba_bay;npc_lying_neighbor | none | ITM_CH003_WET_TOWEL;ITM_CH003_CAMERA_ACCESS | Scene 3 - Hang xom doi do. |
| SCN_CH003_MINIMART_BLOATER | Mini Mart Below the Building | LOC_CH003_GROUND_MINIMART | Provide stealth loot and first Bloater mutation foreshadow. | Chalk trail leads to ground floor mini mart. | Player recovers supplies/medicine and avoids or triggers Bloater hazard. | char_trung;npc_ba_bay | ENM_CH003_BLOATER_FORESHADOW;ENM_CH003_MINIMART_INFECTED | ITM_CH003_MILK_POWDER;ITM_CH003_MEDICINE_BAG;ITM_CH003_ANTISEPTIC;ITM_CH003_POWER_CELL;ITM_CH003_MINIMART_SHELF_MARK;ITM_CH003_BLOATED_CORPSE | Scene 4 - Sieu thi duoi chan chung cu. |
| SCN_CH003_LOCKED_APARTMENT | The Locked Apartment | LOC_CH003_LOCKED_APARTMENT | Force a choice between risk, rescue, and clue gathering. | Player hears knocking or learns someone was locked inside. | Player rescues, skips, or marks the trapped child and may receive Mai/Binh clue. | char_trung;npc_locked_child;npc_locked_child_family;npc_selfish_family | ENM_CH003_LOCKED_APARTMENT_INFECTED | ITM_CH003_LOCKED_APARTMENT_KEYS;ITM_CH003_CHILD_CHALK_FRAGMENT | Scene 5 - Can ho bi khoa. |
| SCN_CH003_NORTH_ARROW | The Arrow Out of Home | LOC_CH003_NORTH_BACK_ALLEY | Convert apartment investigation into the Chapter 004 route. | Player reaches the north/back exit of the building. | Player finds checkpoint arrow, tracks, Binh cloth scrap, and receives Hoang call. | char_trung;comp_hoang;char_mai;char_binh;npc_teacher_group | none | ITM_CH003_NORTH_CHALK_MARK;ITM_CH003_BINH_SHIRT_SCRAP;ITM_CH003_TRUCK_TRACKS;ITM_CH003_MAI_WHITE_CHALK | Scene 6 - Mui ten ra khoi nha. |

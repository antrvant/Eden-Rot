# Dialogue - CH003

Metadata:

- chapterID: CH003
- sourceFilename: chapter_003_loi_nhan_tren_tu_lanh.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH003_NOTE_001 | char_mai | STATE_FRIDGE_NOTE | If you come home and do not find us, do not panic. I could not take Binh to my mother's place. Someone was bitten on the stairs. I went north with the teacher from the building. Find me by the white chalk marks. | Player internal A: "She knew I would come."; Player internal B: "I came home too late."; Player internal C: "I will find you." | open_choice | inspect:ITM_CH003_FRIDGE_NOTE | DT_007 and Chapter 002 ending note. |
| DLG_CH003_NOTE_002A | char_trung | STATE_NOTE_INTERNAL_A | She knew I would come. | none | set_flag:FLAG_CH003_FAMILY_TRUST_PLUS;set_flag:FLAG_CH003_TRACKING_CLUES_UNLOCKED | choice:DLG_CH003_NOTE_001:A | DT_007 internal A. |
| DLG_CH003_NOTE_002B | char_trung | STATE_NOTE_INTERNAL_B | I came home too late. | none | set_flag:FLAG_CH003_GUILT_PLUS | choice:DLG_CH003_NOTE_001:B | DT_007 internal B. |
| DLG_CH003_NOTE_002C | char_trung | STATE_NOTE_INTERNAL_C | I will find you. | none | set_flag:FLAG_CH003_FAMILY_DRIVE_PLUS | choice:DLG_CH003_NOTE_001:C | DT_007 internal C. |
| DLG_CH003_BINH_MEMORY_001 | char_binh | STATE_VOICE_MEMORY | Dad, come home before I sleep, okay? | none | set_flag:FLAG_CH003_BINH_MEMORY_PLAYED | phone_available | Scene 1 replays Binh's old voice message. |
| DLG_CH003_TRUNG_001 | char_trung | STATE_APARTMENT_SEARCH | Mai left a trail for me. | none | none | first_chalk_found | Implementation Notes bark. |
| DLG_CH003_LYING_NEIGHBOR_001 | npc_lying_neighbor | STATE_DENIAL | I did not see anyone. My family has our own problems. | Choice A: "There is white chalk on your hand."; Choice B: "I have water. Trade information."; Choice C: "Tell the truth, or I open your door to what is outside." | open_choice | hallway_confrontation | DT_009. |
| DLG_CH003_LYING_NEIGHBOR_002A | npc_lying_neighbor | STATE_EXPOSED | She asked me to open the back exit. I could not. | none | set_flag:FLAG_CH003_INSIGHT_PLUS;set_flag:FLAG_CH003_NEIGHBOR_LIE_EXPOSED | choice:DLG_CH003_LYING_NEIGHBOR_001:A | DT_009 Choice A and Scene 2. |
| DLG_CH003_LYING_NEIGHBOR_002B | npc_lying_neighbor | STATE_TRADE | Give me the water. I saw them go down the stairs. North side, I think. | none | set_flag:FLAG_CH003_TRADE_PLUS;set_flag:FLAG_CH003_NEIGHBOR_TESTIMONY_RECEIVED | choice:DLG_CH003_LYING_NEIGHBOR_001:B | DT_009 Choice B. |
| DLG_CH003_LYING_NEIGHBOR_002C | npc_lying_neighbor | STATE_THREATENED | Fine! She went down. The north exit. Keep that thing away from my door. | none | set_flag:FLAG_CH003_INTIMIDATION_PLUS;set_flag:FLAG_CH003_NEIGHBOR_RESENTMENT | choice:DLG_CH003_LYING_NEIGHBOR_001:C | DT_009 Choice C. |
| DLG_CH003_NEIGHBOR_001 | npc_neighbor | STATE_MAI_SEEN | Mai went down the stairs with Binh. He was crying, but she covered his eyes and told him to count the steps. | Choice A: "Was she hurt?"; Choice B: "Why did you not keep them here?"; Choice C: "Which direction?" | open_choice | neighbor_talk | DT_008. |
| DLG_CH003_NEIGHBOR_002A | npc_neighbor | STATE_MAI_NOT_HURT | It was not her blood. At least, not when I saw her. | none | set_flag:FLAG_CH003_HOPE_PLUS | choice:DLG_CH003_NEIGHBOR_001:A | DT_008 Choice A. |
| DLG_CH003_NEIGHBOR_002B | npc_neighbor | STATE_DOORS_LOCKED | I opened my door. The next family locked the stair access. Everyone feared their own death first. | none | set_flag:FLAG_CH003_ANGER_PLUS | choice:DLG_CH003_NEIGHBOR_001:B | DT_008 Choice B. |
| DLG_CH003_NEIGHBOR_002C | npc_neighbor | STATE_NORTH_ROUTE | North. She marked the wall with chalk. Your wife is very smart. | none | set_flag:FLAG_CH003_CLUE_PROGRESS_PLUS;set_flag:FLAG_CH003_NEIGHBOR_TESTIMONY_RECEIVED | choice:DLG_CH003_NEIGHBOR_001:C | DT_008 Choice C. |
| DLG_CH003_BA_BAY_001 | npc_ba_bay | STATE_BA_BAY_GREETING | Trung? Your wife came through here. Binh cried, but he listened. She told him to count the stairs. | none | set_flag:FLAG_CH003_BA_BAY_MET | scene:SCN_CH003_NEIGHBOR_TRADE | Scene 3. |
| DLG_CH003_BA_BAY_002 | npc_ba_bay | STATE_BA_BAY_CARE | If you have time to run, you have time to stop the bleeding. Your wife will worry more if she sees you like this. | none | none | injured_hand | Scene 3 and implementation bark. |
| DLG_CH003_BA_BAY_003 | npc_ba_bay | STATE_MEDICINE_REQUEST | If you reach the ground floor, bring me antiseptic from the medicine cabinet. There are still old people here. | none | set_flag:FLAG_CH003_BA_BAY_MEDICINE_REQUESTED | ba_bay_met | SQ_Apt_03. |
| DLG_CH003_BLOATER_001 | npc_ba_bay | STATE_BLOATER_WARNING | Do not go near it. It does not die like the others. | none | set_flag:FLAG_CH003_BLOATER_FORESHADOW_SEEN | minimart_cold_storage | Scene 4. |
| DLG_CH003_LOCKED_CHILD_001 | npc_locked_child | STATE_LOCKED_CHILD_FOUND | Are you with the soldiers? | none | set_flag:FLAG_CH003_LOCKED_CHILD_FOUND | locked_apartment_opened | Scene 5. |
| DLG_CH003_LOCKED_CHILD_002 | npc_locked_child | STATE_MAI_CLUE | Teacher Mai said if I met a good adult, I should follow them. If I met an adult who said they were good, I should hide. | none | none | locked_child_found | Scene 5. |
| DLG_CH003_LOCKED_CHILD_003 | npc_locked_child | STATE_BINH_CLUE | She went north. A little boy held onto her shirt. She said his name was Binh. | none | set_flag:FLAG_CH003_LOCKED_CHILD_CLUE_RECEIVED | locked_child_rescued | Scene 5. |
| DLG_CH003_HOANG_001 | comp_hoang | STATE_CHECKPOINT_CALL | I found chatter about a military checkpoint still open to the north. But listen: you need to reach it before dark. After dark, they close the gate. | none | set_flag:FLAG_CH003_NORTH_CHECKPOINT_CLUE_UNLOCKED | north_alley_reached | Scene 6. |
| DLG_CH003_HOANG_002 | comp_hoang | STATE_HOANG_TEASE | Your wife is smarter than you. | none | none | north_alley_reached | Scene 6. |
| DLG_CH003_HOANG_003 | comp_hoang | STATE_HOANG_WARNING | Good. Then do not be late this time. | none | none | north_alley_reached | Scene 6. |
| DLG_CH003_TRUNG_002 | char_trung | STATE_NORTH_EXIT | Mai is still fighting. Binh is still alive. | none | set_flag:FLAG_CH003_FAMILY_DRIVE_PLUS | final_chalk_mark_found | Scene 6 ending intent. |

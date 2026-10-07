# Flags - CH003

Metadata:

- chapterID: CH003
- sourceFilename: chapter_003_loi_nhan_tren_tu_lanh.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH003_FRIDGE_NOTE_REREAD | progression | false | Player rereads Mai's fridge note. | MQ_003 start and internal choice. | Scene 1 and DT_007. |
| FLAG_CH003_FAMILY_TRUST_PLUS | moral | 0 | Player interprets Mai's note as trust and steadies Trung. | Family emotional profile. | DT_007 internal A. |
| FLAG_CH003_GUILT_PLUS | moral | 0 | Player focuses on arriving too late or abandons optional rescue. | Guilt profile. | DT_007 internal B and SQ_Apt_04. |
| FLAG_CH003_FAMILY_DRIVE_PLUS | moral | 0 | Player commits to finding Mai/Binh. | Family drive and Chapter 004 route. | DT_007 internal C and Scene 6. |
| FLAG_CH003_BINH_MEMORY_PLAYED | emotional | false | Player plays or hears Binh's old voice message. | Family memory references. | Scene 1. |
| FLAG_CH003_TRACKING_CLUES_UNLOCKED | system | false | Player understands Mai's chalk trail. | Tracking marker system. | Rewards and SQ_Apt_01. |
| FLAG_CH003_FIRST_CHALK_MARK_FOUND | progression | false | Player finds the first chalk arrow outside the apartment. | MQ_003 objective 3. | Scene 2. |
| FLAG_CH003_BINH_HANDPRINT_FOUND | emotional | false | Player finds Binh's small chalk handprint. | Family proof and tracking emotional layer. | Scene 2. |
| FLAG_CH003_CHALK_MARKS_FOUND_COUNT | counter | 0 | Increment for each white chalk mark found. | SQ_003_01 completion. | SQ_Apt_01. |
| FLAG_CH003_NEIGHBOR_LIE_EXPOSED | social | false | Player notices chalk on lying neighbor's hand. | Social check consequence. | DT_009 Choice A. |
| FLAG_CH003_INSIGHT_PLUS | personality | 0 | Player exposes the lie through observation. | Personality profile. | DT_009 Choice A. |
| FLAG_CH003_TRADE_PLUS | personality | 0 | Player trades water/medicine/food for information. | Apartment resident reputation. | DT_009 Choice B. |
| FLAG_CH003_INTIMIDATION_PLUS | personality | 0 | Player threatens a neighbor for information. | Apartment resident resentment. | DT_009 Choice C. |
| FLAG_CH003_NEIGHBOR_RESENTMENT | social | false | Player intimidates or humiliates a neighbor. | Possible Chapter 05 apartment NPC reaction. | SQ_Apt_02. |
| FLAG_CH003_NEIGHBOR_TESTIMONY_RECEIVED | progression | false | Neighbor confirms Mai and Binh went down the stairs/north. | MQ_003 objective 4. | DT_008 and Scene 3. |
| FLAG_CH003_HOPE_PLUS | emotional | 0 | Player learns blood was not Mai's when neighbor saw her. | Emotional state. | DT_008 Choice A. |
| FLAG_CH003_ANGER_PLUS | emotional | 0 | Player learns other residents locked routes out of fear. | Emotional state. | DT_008 Choice B. |
| FLAG_CH003_CLUE_PROGRESS_PLUS | progression | 0 | Player asks directly for direction and receives north clue. | MQ_003 route progress. | DT_008 Choice C. |
| FLAG_CH003_BA_BAY_MET | social | false | Player meets Ba Bay. | SQ_003_03 and possible future NPC continuity. | Scene 3. |
| FLAG_CH003_BA_BAY_MEDICINE_REQUESTED | sidequest | false | Ba Bay asks Trung to recover medicine/antiseptic. | SQ_003_03. | Scene 3. |
| FLAG_CH003_MEDICINE_RECOVERED | sidequest | false | Player recovers Ba Bay's medicine bag or antiseptic. | Ba Bay support and medkit reward. | SQ_Apt_03. |
| FLAG_CH003_BA_BAY_SUPPORT_SEED | continuity | false | Player helps Ba Bay enough to seed future support. | Later base/recruit possibility. | SQ_Apt_03 reward. |
| FLAG_CH003_MINIMART_ENTERED | progression | false | Player enters the ground floor mini mart. | MQ_003 objective 5-6. | Scene 4. |
| FLAG_CH003_BLOATER_FORESHADOW_SEEN | world_state | false | Player sees bloated corpse in cold storage. | Mutation tutorial and later Bloater boss. | Lore Reveal and Scene 4. |
| FLAG_CH003_BLOATER_NOISE_TRIGGERED | hazard | false | Player makes loud noise near the bloated corpse. | Optional Bloater hazard activation. | Continuity Notes. |
| FLAG_CH003_MILK_POWDER_OBTAINED | resource | false | Player takes milk powder from mini mart. | Resource/barter. | Scene 4. |
| FLAG_CH003_LOCKED_APARTMENT_FOUND | sidequest | false | Player hears knocking or identifies locked apartment. | SQ_003_04. | Scene 5. |
| FLAG_CH003_LOCKED_CHILD_FOUND | sidequest | false | Player opens the locked room and finds the child alive. | SQ_003_04. | Scene 5. |
| FLAG_CH003_LOCKED_CHILD_RESCUED | choice | false | Player rescues the locked-apartment child. | Compassion and clue path. | SQ_Apt_04. |
| FLAG_CH003_LOCKED_CHILD_SKIPPED | choice | false | Player avoids the rescue to follow the trail faster. | Pragmatism/Guilt. | SQ_Apt_04. |
| FLAG_CH003_LOCKED_APARTMENT_MARKED | choice | false | Player marks the locked apartment for later. | Deferred rescue state. | Scene 5. |
| FLAG_CH003_LOCKED_CHILD_CLUE_RECEIVED | progression | false | Locked child says Mai, Binh, and the teacher group went north. | Alternate clue source. | Scene 5. |
| FLAG_CH003_COMPASSION_PLUS | moral | 0 | Player rescues the locked child or helps residents. | Moral profile. | Rewards. |
| FLAG_CH003_PRAGMATISM_PLUS | moral | 0 | Player skips optional rescues to follow Mai quickly. | Moral profile. | Rewards. |
| FLAG_CH003_NORTH_ARROW_FOUND | progression | false | Player finds the large north checkpoint chalk mark. | MQ_003 completion route. | Scene 6. |
| FLAG_CH003_BINH_SHIRT_SCRAP_FOUND | emotional | false | Player finds Binh's shirt scrap on the fence. | Emotional inventory and proof trail. | Scene 6. |
| FLAG_CH003_TRUCK_TRACKS_FOUND | world_state | false | Player sees truck tracks and many footprints. | Ending hook: possible forced group movement. | Ending Hook. |
| FLAG_CH003_NORTH_CHECKPOINT_CLUE_UNLOCKED | progression | false | Player identifies checkpoint direction from chalk/tracks/Hoang call. | Chapter 004 start. | Scene 6. |
| FLAG_CH003_EMOTIONAL_ITEMS_OBTAINED | item_state | false | Player carries photo, chalk, and/or shirt scrap. | Later emotional inventory. | Continuity Notes. |
| FLAG_CH003_MQ_COMPLETE | progression | false | MQ_003 completes after north checkpoint clue is confirmed. | Chapter completion. | Main Quest completion condition. |

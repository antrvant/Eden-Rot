# Chapter Manifest - CH003

## Source Chapter

- sourceChapterID: CH003
- sourceFilename: chapter_003_loi_nhan_tren_tu_lanh.md
- sourcePath: ../chapters/chapter_003_loi_nhan_tren_tu_lanh.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: The Fridge Note
- originalTitle: Loi Nhan Tren Tu Lanh
- act: Act 1 - Sai Gon Burns
- gameplayHours: 4h
- primaryPOV: Trung
- mainQuestID: MQ_003
- mainQuestName: Find First Clue

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH003_TRUNG_APARTMENT_1208 | Trung's Apartment 1208 | Emotional investigation, fridge note, family evidence |
| LOC_CH003_APARTMENT_HALLWAY | Apartment Hallway | First chalk mark and lying neighbor encounter |
| LOC_CH003_STAIRWELL | Apartment Stairwell | Tracking tutorial, blood trace, trapped infected |
| LOC_CH003_FLOOR_09_NEIGHBOR | Floor 9 Neighbor Apartment | Neighbor testimony and barter/social pressure |
| LOC_CH003_GROUND_MINIMART | Ground Floor Mini Mart | Stealth loot and Bloater foreshadow |
| LOC_CH003_LOCKED_APARTMENT | Locked Apartment | Optional rescue and clue about Mai's group |
| LOC_CH003_NORTH_BACK_ALLEY | North Back Alley | Final arrow, truck tracks, route to checkpoint |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH002_EMPTY_HOME_FOUND | Chapter 003 begins after Trung finds the apartment empty. |
| FLAG_CH002_CHALK_TRAIL_UNLOCKED | Mai's fridge note tells Trung to follow white chalk marks. |
| FLAG_CH002_FRIDGE_NOTE_READ | Required for the internal choice around Mai's message. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH003_FRIDGE_NOTE_REREAD | Trung rereads Mai's fridge note and steadies himself. |
| FLAG_CH003_TRACKING_CLUES_UNLOCKED | Tracking/chalk clue system unlocks. |
| FLAG_CH003_FIRST_CHALK_MARK_FOUND | First chalk arrow outside the apartment is found. |
| FLAG_CH003_BINH_HANDPRINT_FOUND | Binh's small chalk handprint is found beside Mai's mark. |
| FLAG_CH003_NEIGHBOR_TESTIMONY_RECEIVED | Neighbor confirms Mai and Binh went down the stairs. |
| FLAG_CH003_BA_BAY_MET | Trung meets Ba Bay, retired nurse and potential future caretaker NPC. |
| FLAG_CH003_MEDICINE_RECOVERED | Player recovers medicine/antiseptic for Ba Bay. |
| FLAG_CH003_BLOATER_FORESHADOW_SEEN | Player sees the bloated corpse mutation in the mini mart. |
| FLAG_CH003_LOCKED_CHILD_RESCUED | Player rescues the child in the locked apartment. |
| FLAG_CH003_NORTH_CHECKPOINT_CLUE_UNLOCKED | Player identifies the route toward the northern military checkpoint. |
| FLAG_CH003_EMOTIONAL_ITEMS_OBTAINED | Player obtains family photo, Mai's chalk, and/or Binh cloth scrap. |

## Generated Files

Load in this exact order:

1. chapter_manifest.md
2. characters.md
3. quests.md
4. dialogue.md
5. items.md
6. scenes.md
7. enemies.md
8. factions.md
9. flags.md
10. validation.md

## Canon Summary

Chapter 003 slows the pace after two chapters of flight and turns Trung's home into the first investigation space. Mai's fridge note, white chalk arrows, and Binh's small handprints prove that Mai did not wait helplessly; she created a trail for Trung while protecting Binh and other children. Trung questions neighbors, bargains or intimidates for information, helps Ba Bay recover medicine, sees the first Bloater mutation foreshadow in the mini mart, and may rescue a child locked away by frightened neighbors. The chapter ends with a larger chalk arrow pointing north toward a military checkpoint, truck tracks, many footprints, and a scrap of Binh's shirt caught on a fence.

## Continuity Resolution - Nhi

| issue | decision |
|---|---|
| Chapter 002 has a named child `Nhi` tied to the lost mother side quest. | Keep `npc_nhi` as the recurring Nhi because she is referenced again in later canon chapters as the lost mother/Nhi thread. |
| Chapter 003 prose also names the locked-apartment child "Nhi." | Treat this as a naming conflict, not the same person. Generate the Chapter 003 locked-apartment child as `npc_locked_child` with displayName `TODO_DERIVE_OR_APPROVE`. |
| Tooling impact | Do not create a second `npc_nhi` in CH003. Use validation TODO to request a canon rename for the locked-apartment child. |

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH003_001 | What should the locked-apartment child's canonical name be, since "Nhi" conflicts with the recurring Chapter 002 Nhi? | Use `npc_locked_child` and `TODO_DERIVE_OR_APPROVE`. |
| OQ_CH003_002 | Does the Bloater become active combat in Chapter 003 or remain foreshadow only? | Mark as optional hazard, not mandatory boss. |
| OQ_CH003_003 | Does Ba Bay become a recruit/base NPC later if medicine is recovered? | Track flag; later chapter must confirm. |
| OQ_CH003_004 | What is the exact route and checkpoint name for Chapter 004? | Use northern military checkpoint clue only. |

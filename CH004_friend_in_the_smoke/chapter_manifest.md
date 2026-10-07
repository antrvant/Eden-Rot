# Chapter Manifest - CH004

## Source Chapter

- sourceChapterID: CH004
- sourceFilename: chapter_004_ban_than_trong_khoi_lua.md
- sourcePath: ../chapters/chapter_004_ban_than_trong_khoi_lua.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: Friend in the Smoke
- originalTitle: Ban Than Trong Khoi Lua
- act: Act 1 - Sai Gon Burns
- gameplayHours: 4h
- primaryPOV: Trung
- mainQuestID: MQ_004
- mainQuestName: Reunite Hoang

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH004_NORTH_BACK_ALLEY | North Back Alley Behind Apartment | Continuation of chalk trail after Chapter 003 |
| LOC_CH004_CANAL_BRIDGE | Canal Bridge | Fake guide encounter and route suspicion |
| LOC_CH004_BURNING_RESIDENTIAL_BLOCK | Burning Residential Block | Human deception, looter/infected mix |
| LOC_CH004_BURNING_NARROW_ALLEY | Burning Narrow Alley | Runner zombie chase and Hoang rescue |
| LOC_CH004_TRAFFIC_CAMERA_STATION | Old Traffic Camera Station | Camera route confirmation and hacking puzzle |
| LOC_CH004_IT_WAREHOUSE | Small IT Warehouse | Camera terminal and trapped survivor moral choice |
| LOC_CH004_NORTH_OVERPASS | Overpass Toward Northern Checkpoint | Two-person bike escape and inner circle dialogue |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH003_NORTH_CHECKPOINT_CLUE_UNLOCKED | Chapter 004 follows Mai's chalk route north. |
| FLAG_CH003_EMOTIONAL_ITEMS_OBTAINED | Trung carries family photo, Mai's chalk, and/or Binh's shirt scrap into the chapter. |
| FLAG_CH002_HOANG_CONTACT_UNLOCKED | Hoang must already be established as a phone contact. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH004_DEGRADED_CHALK_TRACKING | Player learns to track chalk marks damaged by smoke and dust. |
| FLAG_CH004_FAKE_GUIDES_EXPOSED | Fake safe-route guides are exposed as looters. |
| FLAG_CH004_FIRST_RUNNER_SEEN | First Runner zombie variant is introduced. |
| FLAG_CH004_HOANG_REUNITED | Trung and Hoang reunite in person. |
| FLAG_CH004_HOANG_JOINED | Hoang joins as companion. |
| FLAG_CH004_TRUST_HOANG_PLUS | Trust with Hoang increases through rescue or route support. |
| FLAG_CH004_CAMERA_ROUTE_HINT_UNLOCKED | Camera route hint mechanic unlocks. |
| FLAG_CH004_MAI_BINH_CAMERA_CONFIRMED | Traffic camera confirms Mai and Binh reached the checkpoint route. |
| FLAG_CH004_YELLOW_TRUCK_SEEN | Camera shows a yellow rescue truck near Mai/Binh's group. |
| FLAG_CH004_SURVIVORS_RESCUED | Player rescues the trapped survivor group. |
| FLAG_CH004_SURVIVORS_ABANDONED | Player leaves the trapped survivor group. |
| FLAG_CH004_SURVIVORS_AIDED | Player leaves tools/instructions without full rescue. |
| FLAG_CH004_HOANG_SECRET_REVEALED | Trung discovers Hoang promised to return for the trapped group. |
| FLAG_CH004_INNER_CIRCLE_DEFINED | Hoang defines the "inner circle" survival philosophy. |
| FLAG_CH004_NORTH_CHECKPOINT_DESTINATION_UNLOCKED | Next destination is the northern checkpoint/fake safe zone. |

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

Trung follows Mai's chalk trail through smoke north of the apartment, carrying family keepsakes from Chapter 003. The chalk marks are damaged by smoke and dust, forcing him to interpret Mai's logic instead of blindly following arrows. A fake guide group tries to lure survivors into a looting route, and a new fast Runner infected almost kills Trung in a burning alley. Hoang arrives on a motorbike and saves him, becoming a real companion. Together they access an old traffic camera station and confirm that Mai, Binh, and a teacher group reached the northern checkpoint route, but a yellow rescue truck approaches them before the feed cuts. The chapter also reveals Hoang's moral fracture: he had promised to return for trapped survivors but chose to find Trung first.

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH004_001 | What are the exact identities of the trapped survivor group? | Use generic group IDs until later canon confirms names. |
| OQ_CH004_002 | Which faction owns or operates the yellow rescue truck? | Track as clue only; do not assign named faction yet. |
| OQ_CH004_003 | Do the fake guides return later? | Track exposure/avoidance flags only. |
| OQ_CH004_004 | What is the exact technical ID/name for the northern checkpoint in Chapter 005? | Use `LOC_CH004_NORTH_CHECKPOINT_ROUTE` as destination clue; Chapter 005 should define checkpoint location. |

# Chapter Manifest - CH005

## Source Chapter

- sourceChapterID: CH005
- sourceFilename: chapter_005_khu_an_toan_gia.md
- sourcePath: ../chapters/chapter_005_khu_an_toan_gia.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: False Safe Zone
- originalTitle: Khu An Toan Gia
- act: Act 1 - Sai Gon Burns
- gameplayHours: 4h
- primaryPOV: Trung
- mainQuestID: MQ_005
- mainQuestName: Reach Safe Zone

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH005_FALSE_CHECKPOINT_ROAD | Road to the Northern Checkpoint | Arrival, crowd queue, false hope |
| LOC_CH005_FALSE_SAFE_GATE | False Safe Zone Gate | Inward barbed wire, child-priority separation, erased chalk |
| LOC_CH005_REGISTRY_TABLE | Registry Table | Fake administration, fees, entry list clue |
| LOC_CH005_ENTRY_QUEUE | Entry Queue | Price of safety, wedding ring exchange, crowd navigation |
| LOC_CH005_QUARANTINE_TENT | Quarantine Tent | Lurker introduction and medical lie |
| LOC_CH005_ADMIN_BACK_ROOM | Admin Back Room | Fake stamp, transfer records, Mai/Binh clue |
| LOC_CH005_SERVICE_GATE | Service Gate | Collapse escape route |
| LOC_CH005_DRAINAGE_RETREAT | Drainage Retreat Path | After-fence trust wound and real outpost clue |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH004_HOANG_JOINED | Hoang is now Trung's companion. |
| FLAG_CH004_NORTH_CHECKPOINT_DESTINATION_UNLOCKED | Chapter 005 begins at the checkpoint route unlocked in Chapter 004. |
| FLAG_CH004_MAI_BINH_CAMERA_CONFIRMED | The checkpoint is pursued because camera footage confirmed Mai/Binh moved that way. |
| FLAG_CH004_YELLOW_TRUCK_SEEN | Yellow rescue truck clue connects to child-priority transfer suspicion. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH005_FALSE_SAFE_ZONE_REACHED | Trung and Hoang arrive at the northern checkpoint. |
| FLAG_CH005_INWARD_BARBED_WIRE_NOTICED | Hoang identifies the fence is built to keep people in. |
| FLAG_CH005_ERASED_CHALK_MARK_FOUND | Trung finds Mai's partly erased chalk mark near the gate. |
| FLAG_CH005_CHILD_PRIORITY_SCAM_SEEN | Player sees children separated under the phrase "children first." |
| FLAG_CH005_REGISTRY_ACCESSED | Player gains access to the registry list. |
| FLAG_CH005_MAI_BINH_TRANSFER_LIST_FOUND | Player finds Mai and Binh on the transfer records. |
| FLAG_CH005_LURKER_KNOWLEDGE_UNLOCKED | First Lurker encounter teaches darkness behavior. |
| FLAG_CH005_FAKE_SAFE_ZONE_EXPOSED | Player obtains enough evidence that the safe zone is fake. |
| FLAG_CH005_FAKE_STAMP_OBTAINED | Player can carry the fake military stamp as evidence. |
| FLAG_CH005_RIPPED_TRANSFER_LIST_OBTAINED | Player carries the torn transfer list for Chapter 006. |
| FLAG_CH005_EDEN_MARK_SEEN | The unexplained `E` mark appears beside Binh's entry. |
| FLAG_CH005_REAL_ARMY_OUTPOST_UNLOCKED | Next destination becomes the real army outpost. |

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

Trung and Hoang reach the northern checkpoint believing Mai and Binh may be inside. The place looks official: loudspeakers, uniforms, stamps, a registry table, medical tents, and a promise that children will be prioritized. Hoang notices the barbed wire faces inward and suspects a trap. Trung finds Mai's partly erased chalk mark, then fights through bureaucracy, bribes, threats, and forged authority to reach the entry lists. The safe zone is revealed as a fake system that collects valuables, separates children, locks suspected infected with healthy people, and transfers useful adults and monitored children elsewhere. A Lurker attacks inside the dark quarantine tent. Trung finds records marking Mai as a useful teacher and Binh as a boy to monitor under an unexplained `E` code. The fake safe zone collapses from inside, and Trung and Hoang escape with evidence pointing toward a real army outpost.

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH005_001 | What is the fake safe zone manager's proper name? | Use `npc_false_safe_manager` until canon names him. |
| OQ_CH005_002 | Is the separated mother a recurring named NPC later? | Track as `npc_separated_mother`; later chapters can bind exact identity. |
| OQ_CH005_003 | What does the `E` mark mean? | Store only as an unexplained seed; do not explain in CH005. |
| OQ_CH005_004 | What exact location ID should the real army outpost use in Chapter 006? | Use `LOC_CH005_REAL_ARMY_OUTPOST_LEAD` as destination clue only. |

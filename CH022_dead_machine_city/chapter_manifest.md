# Chapter Manifest - CH022

## Source Chapter

- sourceChapterID: CH022
- sourceFilename: chapter_022_thanh_pho_nguoi_may_chet.md
- sourcePath: ../chapters/chapter_022_thanh_pho_nguoi_may_chet.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: Dead Machine City
- originalTitle: Thanh Pho Nguoi May Chet
- act: Act 4 - East Asia & The Naval Key
- gameplayHours: 5h
- primaryPOV: Trung
- mainQuestID: MQ_022
- mainQuestName: Decode Architect Signal

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH022_APPROACH | Nha Di Approaching Tech Port | Establish dead automated city; cranes still moving |
| LOC_CH022_DOCK_GATE | Dock Security Gate | Binh targeted by biometric scan |
| LOC_CH022_CONTAINER_YARD | Container Yard | Environmental horror; forklifts and cranes as hazards |
| LOC_CH022_ENGINEER_HOUSING | Engineer Housing and Maintenance Office | Chen Wei keycard, voice logs, daycare discovery |
| LOC_CH022_SERVER_HALL | Flooded Server Hall | Architect signal decoding and data extraction |
| LOC_CH022_EXOSUIT_BAY | Maintenance Exosuit Bay | First cybernetic infected encounter |
| LOC_CH022_DEPARTURE | Nha Di Leaving Port | Tokyo signal reception and Chapter 23 hook |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH021_PORT_ARRAY_SIGNAL_RECEIVED | Chapter 22 follows the port array signal from Chapter 21. |
| FLAG_CH021_VESSEL_REPAIRED | Nha Di must be operational to reach the tech port. |
| FLAG_CH021_HOANG_TECHNICAL_SERVICE | Hoang is technically useful but socially untrusted for hacking tasks. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH022_PORT_ARRAY_DECODED | Port array data has been decoded from server hall. |
| FLAG_CH022_ARCHITECT_SIGNAL_DECODED | Architect signal chain has been decoded. |
| FLAG_CH022_EDENROT_PORT_ARRAY_CLASSIFIED | Port classified as EDENROT CLASS: PORT ARRAY. |
| FLAG_CH022_ASTER_NAMED | Architect Commander Aster has been identified in signal authority. |
| FLAG_CH022_TOKYO_RELAY_SIGNAL_RECEIVED | Tokyo relay signal requesting naval codes has been received. |
| FLAG_CH022_CYBERNETIC_INFECTED_INTRODUCED | First cybernetic infected has been encountered. |
| FLAG_CH022_BINH_DATA_FLAGGED | Binh has been flagged as biometric anomaly by port AI. |
| FLAG_CH022_EDENROT_CHILD_PROFILE_FLAGGED | Binh flagged as EDENROT CHILD PROFILE CANDIDATE. |
| FLAG_CH022_BINH_DATA_OUTBOUND_BLOCKED | Outbound transmission of Binh data has been blocked. |
| FLAG_CH022_BINH_DATA_PRIOR_SYNC_UNKNOWN | Whether Binh data synced before block is unknown. |
| FLAG_CH022_EDENROT_PORT_ARRAY_HANDOFF_COMPLETE | Port array handoff to Tokyo relay is complete. |
| FLAG_CH022_HOANG_HACK_TRANSPARENCY | Hoang narrated hack steps transparently. |
| FLAG_CH022_NHA_DI_NAVIGATION_UPGRADED | Nha Di navigation module has been upgraded. |
| FLAG_CH022_ENGINEER_FAMILY_LOG_FOUND | Chen Wei engineer log and daycare have been discovered. |

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

Nha Di follows the port array signal to an automated South China tech port that is still operating after human collapse. The group must enter the port to recover navigation parts and decode the Architect signal. Automated systems identify Binh as a biometric anomaly and attempt to classify him as an EDENROT child profile candidate. Hoang must hack under distrust, narrating every step to maintain transparency. The team encounters the first cybernetic infected, a former port worker trapped in an industrial exosuit whose machine keeps trying to return it to duty. They recover data pointing to Tokyo and Architect Commander Aster, whose name appears for the first time as signal authority. Mai reminds the group that it is not only humans who turn children into data. The chapter ends with a fragmented Tokyo relay signal warning: "If anyone is human, do not come in the black rain."

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH022_001 | Did Binh's data sync to Architects before the block? | Track as unknown risk; FLAG_CH022_BINH_DATA_PRIOR_SYNC_UNKNOWN. |
| OQ_CH022_002 | What is Aster's full role in the relay chain? | Named as signal authority; direct appearance in Chapter 23. |
| OQ_CH022_003 | Can cybernetic infected be freed from exosuits? | Not resolved; combat only disables joints. |
| OQ_CH022_004 | Who was Chen Wei's daughter Lili? | Lore only; daycare empty except names board. |

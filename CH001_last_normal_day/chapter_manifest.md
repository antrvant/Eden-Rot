# Chapter Manifest - CH001

## Source Chapter

- sourceChapterID: CH001
- sourceFilename: chapter_001_ngay_binh_thuong_cuoi_cung.md
- sourcePath: ../chapters/chapter_001_ngay_binh_thuong_cuoi_cung.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: The Last Normal Day
- originalTitle: Ngay Binh Thuong Cuoi Cung
- act: Act 1 - Sai Gon Burns
- gameplayHours: 3h
- primaryPOV: Trung
- mainQuestID: MQ_001
- mainQuestName: Escape Office

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH001_TRUNG_APARTMENT | Trung's Apartment | Family introduction and promise scene |
| LOC_CH001_OFFICE_FLOOR_18 | Office Floor 1 | Main workplace, departments, meeting room, rumor tension, and outbreak reveal. Legacy ID retained for compatibility. |
| LOC_CH001_GLASS_MEETING_ROOM | Glass Meeting Room | Phone surrender, missed call, and locked-door betrayal |
| LOC_CH001_ELEVATOR_HALLWAY | Elevator Hallway | First bite and outbreak reveal |
| LOC_CH001_EMERGENCY_STAIRS | Emergency Stairs | One-level descent from Floor 1 to Base and boss chase transition |
| LOC_CH001_BASEMENT_PARKING | Base Outdoor Parking | Walled ground-level parking, tutorial climax, escape car, and final phone call. Legacy ID retained for compatibility. |

## Required Previous Flags

| flagID | reason |
|---|---|
| NONE | Chapter 001 is the opening chapter and requires no previous continuity flag. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH001_TRUNG_PROMISED_HOME | Trung promised Binh he would come home early. |
| FLAG_CH001_MAI_CALL_MISSED | Trung missed or delayed Mai's call during the meeting. |
| FLAG_CH001_PHONE_RECOVERED | Player recovered Trung's phone before escape. |
| FLAG_CH001_MAI_LOCATION_KNOWN | Player knows Mai planned to take Binh to her mother's home. |
| FLAG_CH001_COWORKER_01_RESCUED | Player rescued npc_coworker_01. |
| FLAG_CH001_COWORKER_01_ABANDONED | Player left npc_coworker_01 behind. |
| FLAG_CH001_COWORKER_01_AIDED | Player gave aid without fully rescuing npc_coworker_01. |
| FLAG_CH001_COMPASSION_PLUS | Player chose a costly compassionate action. |
| FLAG_CH001_PRAGMATISM_PLUS | Player chose the faster survival route. |
| FLAG_CH001_GUILT_PLUS | Player hesitated or abandoned someone at emotional cost. |
| FLAG_CH001_BOSS_INFECTED | npc_boss was bitten and became infected. |
| FLAG_CH001_OFFICE_ESCAPED | Trung escaped the office building into the burning city. |
| FLAG_CH001_FAMILY_OBJECTIVE_UNLOCKED | Family objective "Go Home to Find Mai and Binh" is unlocked. |
| FLAG_CH001_PHONE_LOG_UNLOCKED | Phone log system is unlocked if the phone was recovered. |

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

Trung begins a normal workday in Sai Gon after promising Mai and Binh he will return home early for Binh's small class performance. The company's main workplace and glass meeting room are on Floor 1; the Boss is already waiting there, so Chapter 001 does not require a visit to his optional sixth-floor office. A hidden outbreak is treated as rumor and business risk while management pressures workers to keep working. Trung misses Mai's call, recovers his phone during the chaos, witnesses the first infected attack, confronts the Boss's locked-door betrayal, and descends one level through the emergency stairs to the Base. The climax occurs in the walled outdoor parking area at ground level, where Mai's call breaks up and Trung escapes through the parking gate toward the burning city.

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH001_001 | Should npc_boss die in Chapter 001 or survive as a later recurring infected? | Marked as unresolved in enemies.md and validation.md. |
| OQ_CH001_002 | What is Mai's mother's exact location or location ID? | Use TODO_DERIVE_OR_APPROVE until a later chapter confirms it. |
| OQ_CH001_003 | Which coworker returns in Chapter 05 if rescued? | Track npc_coworker_01 survival flag; do not invent later role yet. |

# Chapter Manifest - CH002

## Source Chapter

- sourceChapterID: CH002
- sourceFilename: chapter_002_thanh_pho_khong_con_den_do.md
- sourcePath: ../chapters/chapter_002_thanh_pho_khong_con_den_do.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: The City With No Red Lights
- originalTitle: Thanh Pho Khong Con Den Do
- act: Act 1 - Sai Gon Burns
- gameplayHours: 4h
- primaryPOV: Trung
- mainQuestID: MQ_002
- mainQuestName: Reach Home

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH002_COMPANY_BASEMENT | Company Basement Parking | Transition from Chapter 001 and vehicle/key crisis |
| LOC_CH002_SAIGON_INTERSECTION | Sai Gon Central Intersection | Social collapse and no-red-light motif |
| LOC_CH002_CONVENIENCE_STORE | Convenience Store | Resource tutorial and moral economy choice |
| LOC_CH002_BACK_ALLEY | Back Alley Near Power Lines | Hoang phone call and route guidance |
| LOC_CH002_OVERPASS_SCHOOL_BUS | Overpass Near Kindergarten Bus | Lost child timed moral rescue |
| LOC_CH002_TRUNG_APARTMENT_BUILDING | Trung's Apartment Building | Final climb, silent home, and trail discovery |
| LOC_CH002_TRUNG_APARTMENT_1208 | Trung's Apartment 1208 | Empty home, broken toy, blood trace, fridge note |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH001_OFFICE_ESCAPED | Chapter 002 begins after Trung escapes the office basement. |
| FLAG_CH001_PHONE_RECOVERED | Optional continuity: if true, Trung receives calls/messages directly; if false, alternate clue route is required. |
| FLAG_CH001_COWORKER_01_RESCUED | Optional continuity: controls whether npc_coworker_01 appears in the basement opening. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH002_BASEMENT_ESCAPED | Trung escapes the company basement into the city. |
| FLAG_CH002_CAR_LOST | Trung cannot use his own car because the key/car is missing or stolen. |
| FLAG_CH002_MAI_WARNING_RECEIVED | Trung receives Mai's warning not to take dangerous main roads. |
| FLAG_CH002_BASIC_SCAVENGING_UNLOCKED | Convenience store/resource tutorial is completed. |
| FLAG_CH002_HOANG_CONTACT_UNLOCKED | Hoang becomes an active phone contact. |
| FLAG_CH002_TRUST_HOANG_PLUS | Player trusts Hoang's route guidance. |
| FLAG_CH002_HOANG_PRAGMATISM_SEED | Hoang's survival-first advice is established. |
| FLAG_CH002_NHI_RESCUED | Player rescues Nhi from the overturned school bus. |
| FLAG_CH002_NHI_ABANDONED | Player leaves the mother and child event unresolved. |
| FLAG_CH002_CHILD_RIBBON_OBTAINED | Player receives or records Nhi's ribbon as a rescue token. |
| FLAG_CH002_EMPTY_HOME_FOUND | Trung reaches home and finds Mai and Binh gone. |
| FLAG_CH002_CHALK_TRAIL_UNLOCKED | Mai's chalk-mark trail becomes the Chapter 003 investigation lead. |
| FLAG_CH002_FAMILY_DRIVE_PLUS | Trung's family drive intensifies after finding the empty apartment. |

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

After escaping the office, Trung enters a Sai Gon that is still crowded but no longer governed by shared rules. Traffic lights continue changing while nobody stops, public broadcasts insist the situation is controlled, fake rescuers rob the injured, and basic water becomes a weapon of price gouging. Trung must cross the city toward his apartment while Mai leaves broken warnings and Hoang calls with useful but ruthless route advice. Along the way, Trung faces repeated choices between helping strangers and reaching Mai and Binh faster. The chapter ends at home, but there is no reunion: the apartment is empty, Binh's toy is broken, blood marks the floor, and Mai's fridge note points Trung toward a chalk trail for Chapter 003.

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH002_001 | If Trung did not recover his phone in Chapter 001, what alternate device or clue delivers Mai/Hoang information? | Marked as TODO_DERIVE_OR_APPROVE in validation. |
| OQ_CH002_002 | Does npc_coworker_01 survive all of Chapter 002 if present? | Track conditional appearance and possible separation; do not force future status. |
| OQ_CH002_003 | What exact northern route does Mai take after leaving the apartment? | Use chalk trail clue only; Chapter 003 should define the route. |
| OQ_CH002_004 | Are the mother and Nhi a recurring thread? | Confirmed by later canon references; keep `npc_nhi` as the recurring Nhi and track rescue/abandon flags. |

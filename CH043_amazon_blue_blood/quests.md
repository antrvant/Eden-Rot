# Quests - CH043

Metadata:

- chapterID: CH043
- sourceFilename: chapter_043_amazon_ngap_mau_xanh.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_043 | Navigate Flooded Jungle | main | npc_iara | Rebirth reaches Amazon basin edge after CH042 | One group reaches outer citadel approach; party split resolved; Chapter 44 breach unlocked | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ043_01 | MQ_043 | 1 | Transfer convoy to river boats. | GoTo | LOC_CH043_FLOODED_HIGHWAY | 1 | Main Quest objective 1. |
| OBJ_MQ043_02 | MQ_043 | 2 | Recruit Iara as guide. | TalkTo | npc_iara | 1 | Main Quest objective 2. |
| OBJ_MQ043_03 | MQ_043 | 3 | Identify EDENROT Predatory Memory Basin. | Investigate | LOC_CH043_FLOODED_HIGHWAY | 1 | Main Quest objective 3. |
| OBJ_MQ043_04 | MQ_043 | 4 | Navigate moving canopy route. | Navigate | LOC_CH043_NARROW_CHANNEL | 1 | Main Quest objective 4. |
| OBJ_MQ043_05 | MQ_043 | 5 | Cross green water memory zone. | Navigate | LOC_CH043_GLOWING_ALGAE_RIVER | 1 | Main Quest objective 5. |
| OBJ_MQ043_06 | MQ_043 | 6 | Disable hanging radio trap. | Interact | LOC_CH043_RIVER_OUTPOST | 1 | Main Quest objective 6. |
| OBJ_MQ043_07 | MQ_043 | 7 | Identify familiar memory bait. | Investigate | LOC_CH043_RIVER_OUTPOST | 1 | Main Quest objective 7. |
| OBJ_MQ043_08 | MQ_043 | 8 | Identify first Stalker. | Observe | LOC_CH043_RIVER_CHANNEL | 1 | Main Quest objective 8. |
| OBJ_MQ043_09 | MQ_043 | 9 | Establish floating church camp. | GoTo | LOC_CH043_FLOATING_CHURCH | 1 | Main Quest objective 9. |
| OBJ_MQ043_10 | MQ_043 | 10 | Investigate Orison schoolroom. | Investigate | LOC_CH043_ORISON_SCHOOLROOM | 1 | Main Quest objective 10. |
| OBJ_MQ043_11 | MQ_043 | 11 | Survive Stalker Pack ambush. | Combat | LOC_CH043_OPEN_WATER | 1 | Main Quest objective 11. |
| OBJ_MQ043_12 | MQ_043 | 12 | Confirm predatory memory basin. | Investigate | LOC_CH043_OPEN_WATER | 1 | Main Quest objective 12. |
| OBJ_MQ043_13 | MQ_043 | 13 | Protect child archive names. | Choice | LOC_CH043_OPEN_WATER | 1 | Main Quest objective 13. |
| OBJ_MQ043_14 | MQ_043 | 14 | Escape reverse current. | Navigate | LOC_CH043_RIVER_JUNCTION | 1 | Main Quest objective 14. |
| OBJ_MQ043_15 | MQ_043 | 15 | Manage party split. | Event | LOC_CH043_RIVER_JUNCTION | 1 | Main Quest objective 15. |
| OBJ_MQ043_16 | MQ_043 | 16 | Use family code against voice lures. | Interact | LOC_CH043_RIVER_CHANNEL | 1 | Main Quest objective 16. |
| OBJ_MQ043_17 | MQ_043 | 17 | Reach outer citadel approach. | GoTo | LOC_CH043_CITADEL_CLEARING | 1 | Main Quest objective 17. |
| OBJ_MQ043_18 | MQ_043 | 18 | Unlock breach citadel chapter. | UnlockQuest | MQ_044 | 1 | Main Quest objective 18. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ043_A_001 | SQ_043_A | Carefully separate wet paper, read faded names, archive them. | OrisonChildNamesRecovered = high; Chapter 46 rescue UI has real names. | SQ_043_A. |
| OBJ_SQ043_B_001 | SQ_043_B | Stop near Iara's old home to retrieve hand-crank map drum. | IaraTrust = high; better navigation during reverse current. | SQ_043_B. |
| OBJ_SQ043_C_001 | SQ_043_C | Let Yusuf walk/row for one shift instead of being treated as cargo. | YusufAgency = true; Mai dialogue about being saved does not remove personhood. | SQ_043_C. |
| OBJ_SQ043_D_001 | SQ_043_D | Hoang tells Trung about infection answering jungle pulses. | HoangSignalHonesty = true. | SQ_043_D. |
| OBJ_SQ043_E_001 | SQ_043_E | Shut down radio trap playing Binh's childhood lullaby. | FamilyCodeEstablished = true. | SQ_043_E. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ043_BOATS_LOST | MQ_043 | Boats lost before outpost. | Cannot continue navigation; mission failure. | Failure Conditions. |
| FAIL_MQ043_BINH_RESONANCE_STRAIN | MQ_043 | Binh resonance strain exceeds safe threshold. | Chapter 44 begins with fever and lower trust. | Failure Conditions. |
| FAIL_MQ043_STALKER_LEARNS_TOO_MUCH | MQ_043 | Stalker Pack learns too many player patterns. | Future encounters become much harder. | Failure Conditions. |
| FAIL_MQ043_ARCHIVE_DESTROYED | MQ_043 | Orison archive destroyed. | Fewer children identifiable in Chapter 46. | Failure Conditions. |
| FAIL_MQ043_VOICE_LURE_INJURY | MQ_043 | Fake voice lure causes character injury. | Character injury carried forward. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ043_ACT7_OPENED | MQ_043 | progression | Act 7 opened | Completion Rewards. |
| REW_MQ043_EDENROT_CLASSIFIED | MQ_043 | system_unlock | EDENROT Predatory Memory Basin classified | Completion Rewards. |
| REW_MQ043_STALKER_AI | MQ_043 | system_unlock | Stalker Pack adaptive AI introduced | Completion Rewards. |
| REW_MQ043_FAMILY_CODE | MQ_043 | system_unlock | Family code mechanic unlocked | Completion Rewards. |
| REW_MQ043_ORISON_DATA | MQ_043 | data_unlock | Orison child archive data for Chapters 44-46 | Completion Rewards. |
| REW_MQ043_PARTY_SPLIT | MQ_043 | system_unlock | Party split structure for multi-group chapters | Completion Rewards. |
| REW_MQ043_CITADEL_REACHED | MQ_043 | progression | Outer citadel approach reached | Completion Rewards. |
| REW_MQ043_CH44_UNLOCKED | MQ_043 | quest_unlock | Chapter 44 breach unlocked | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH043_AMAZON_NAVIGATION | MQ_043 | Amazon navigation mechanics | Transfer to river boats complete. |
| UNLOCK_CH043_STALKER_AI | MQ_043 | Stalker adaptive AI | First Stalker identified. |
| UNLOCK_CH043_FAMILY_CODE | MQ_043 | Family code mechanic | Family code established at floating church. |
| UNLOCK_CH043_EDENROT_FIELD | MQ_043 | EDENROT Predatory Memory Basin logic | Basin confirmed after Stalker Pack ambush. |
| UNLOCK_CH043_PARTY_SPLIT | MQ_043 | Multi-group chapter structure | Reverse current forces three-way split. |
| UNLOCK_CH043_ORISON_ARCHIVE | MQ_043 | Orison child archive data | Child name sheets recovered from schoolroom. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH043_ACT7_STARTED | MQ_043 | Rebirth enters Amazon basin. |
| FLAG_CH043_EDENROT_IDENTIFIED | MQ_043 | Thu classifies basin as EDENROT CLASS. |
| FLAG_CH043_FAMILY_CODE_ESTABLISHED | MQ_043 | Family code set at floating church camp. |
| FLAG_CH043_STALKER_PACK_ACTIVE | MQ_043 | First Stalker observed. |
| FLAG_CH043_ORISON_NAMES_RECOVERED | MQ_043 | Child archive names saved over fuel. |
| FLAG_CH043_PARTY_SPLIT_ACTIVE | MQ_043 | Reverse current forces three-way split. |
| FLAG_CH043_CH44_BREACH_UNLOCKED | MQ_043 | Outer citadel approach reached. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_043_A | Names in the Wet Paper | environmental | Recover water-damaged student name sheets from Orison schoolroom. | Chapter 46 rescue UI has real names instead of unknown IDs. | SQ_043_A. |
| SQ_043_B | Iara's Flooded Home | npc_iara | Stop near Iara's old home to retrieve hand-crank map drum. | IaraTrust = high; better navigation during reverse current. | SQ_043_B. |
| SQ_043_C | Yusuf Walks | comp_yusuf | Let Yusuf walk/row for one shift instead of being treated as cargo. | YusufAgency = true; Mai dialogue about being saved does not remove personhood. | SQ_043_C. |
| SQ_043_D | Hoang's Echo | comp_hoang | Hoang hears infection answering jungle pulses; tell Trung or hide it. | HoangSignalHonesty = true if told. | SQ_043_D. |
| SQ_043_E | The False Lullaby | environmental | Radio trap plays lullaby from Binh's childhood; shut it down or record it. | FamilyCodeEstablished = true if shut down. | SQ_043_E. |

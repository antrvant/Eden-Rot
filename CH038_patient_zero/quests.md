# Quests - CH038

Metadata:

- chapterID: CH038
- sourceFilename: chapter_038_patient_zero.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_038 | Retrieve Patient Zero Data | main | automatic | Group enters Alpine Lab 7 | Patient Zero data recovered; Plague Doctor disabled; Africa route unlocked | Metadata: MQ_038 - Retrieve Patient Zero Data. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ038_001 | MQ_038 | 1 | Secure Alpine Lab vestibule. | GoTo | LOC_CH038_LAB_VESTIBULE | 1 | Main Quest objective 1. |
| OBJ_MQ038_002 | MQ_038 | 2 | Air-gap Rebirth systems. | Interact | LOC_CH038_LAB_VESTIBULE | 1 | Main Quest objective 2. |
| OBJ_MQ038_003 | MQ_038 | 3 | Classify Alpine Lab as EDENROT salvation-cost engine. | Observe | LOC_CH038_LAB_VESTIBULE | 1 | Main Quest objective 3. |
| OBJ_MQ038_004 | MQ_038 | 4 | Search ethics archive. | GoTo | LOC_CH038_ETHICS_ARCHIVE | 1 | Main Quest objective 4. |
| OBJ_MQ038_005 | MQ_038 | 5 | Recover original therapeutic project files. | Fetch | ITM_CH038_THERAPEUTIC_FILES | 1 | Main Quest objective 5. |
| OBJ_MQ038_006 | MQ_038 | 6 | Restore Patient Zero identity records. | Interact | LOC_CH038_PATIENT_HISTORY | 1 | Main Quest objective 6. |
| OBJ_MQ038_007 | MQ_038 | 7 | Access Plague Doctor control suite. | GoTo | LOC_CH038_PLAGUE_DOCTOR_SUITE | 1 | Main Quest objective 7. |
| OBJ_MQ038_008 | MQ_038 | 8 | Survive lab defense activation. | Combat | LOC_CH038_PLAGUE_DOCTOR_SUITE | 1 | Main Quest objective 8. |
| OBJ_MQ038_009 | MQ_038 | 9 | Review cure simulation. | Interact | LOC_CH038_SIMULATION_THEATER | 1 | Main Quest objective 9. |
| OBJ_MQ038_010 | MQ_038 | 10 | Reject immediate Binh biomarker validation. | Choice | LOC_CH038_SIMULATION_THEATER | 1 | Main Quest objective 10. |
| OBJ_MQ038_011 | MQ_038 | 11 | Traverse cryo ward. | StealthOrCombat | LOC_CH038_CRYO_WARD | 1 | Main Quest objective 11. |
| OBJ_MQ038_012 | MQ_038 | 12 | Stabilize Patient Zero chamber. | Interact | LOC_CH038_PATIENT_CHAMBER | 1 | Main Quest objective 12. |
| OBJ_MQ038_013 | MQ_038 | 13 | Retrieve mutation path data. | Fetch | ITM_CH038_MUTATION_PATH_DATA | 1 | Main Quest objective 13. |
| OBJ_MQ038_014 | MQ_038 | 14 | Disable forced cost acceptance. | CombatOrPuzzle | LOC_CH038_CONTROL_ROOM | 1 | Main Quest objective 14. |
| OBJ_MQ038_015 | MQ_038 | 15 | Defeat/disable Plague Doctor validation protocol. | Boss | npc_plague_doctor | 1 | Main Quest objective 15. |
| OBJ_MQ038_016 | MQ_038 | 16 | Extract Patient Zero dataset. | Fetch | ITM_CH038_PATIENT_ZERO_DATASET | 1 | Main Quest objective 16. |
| OBJ_MQ038_017 | MQ_038 | 17 | Decode missing Africa bio-enzyme requirement. | Observe | LOC_CH038_EMERGENCY_TRAM | 1 | Main Quest objective 17. |
| OBJ_MQ038_018 | MQ_038 | 18 | Unlock Chapter 39 bio-jungle route. | Progression | LOC_CH038_EMERGENCY_TRAM | 1 | Main Quest objective 18. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ038_BIOMARKER_UPLOADED | MQ_038 | Lab uploads Binh biomarker data to Architect network. | Major protocol violation. | Failure Conditions. |
| FAIL_MQ038_PLAGUE_DOCTOR_ACTIVATES | MQ_038 | Plague Doctor validation protocol fully activates. | Forced validation threat. | Failure Conditions. |
| FAIL_MQ038_DATA_CORRUPTED | MQ_038 | Patient Zero data corrupted. | Cure path damaged. | Failure Conditions. |
| FAIL_MQ038_CRYO_COLLAPSE | MQ_038 | Cryo ward containment collapse reaches team. | Combat/escape failure. | Failure Conditions. |
| FAIL_MQ038_DOCTOR_VIOLATES | MQ_038 | Doctor violates consent protocol. | Trust damage; ethics failure. | Failure Conditions. |
| FAIL_MQ038_ENZYME_CLUE_MISSED | MQ_038 | Africa enzyme clue missed. | Chapter 39 route not unlocked. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ038_PZ_DATA | MQ_038 | data_item | PatientZeroDataRecovered | Completion Rewards. |
| REW_MQ038_FORMULA | MQ_038 | data_item | CureFormulaPartial | Completion Rewards. |
| REW_MQ038_AFRICA_ROUTE | MQ_038 | route_unlock | Africa bio-jungle route | Completion Rewards. |
| REW_MQ038_PLAGUE_DOCTOR | MQ_038 | lore | Plague Doctor lore | Completion Rewards. |
| REW_MQ038_CONSENT | MQ_038 | data_item | Consent records | Completion Rewards. |
| REW_MQ038_ORIGIN | MQ_038 | lore | Therapeutic origin reveal | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH038_PZ_DATASET | MQ_038 | Patient Zero dataset | Retrieve mutation path and origin files. |
| UNLOCK_CH038_FORMULA_PARTIAL | MQ_038 | Cure formula partial | Decode enzyme requirement. |
| UNLOCK_CH038_PLAGUE_DOCTOR_SEALED | MQ_038 | Plague Doctor protocol sealed | Disable forced cost acceptance. |
| UNLOCK_CH038_AFRICA_ROUTE | MQ_038 | Africa bio-jungle route | Decode enzyme reference. |
| UNLOCK_CH038_CONSENT_RECORDS | MQ_038 | Consent records | Recover ethics archive. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_PZ_01 | The Salvation Contract | automatic | Compare original vs emergency consent; recover dissent notes; decide whether to publish. | ConsentRecordsRecovered. | SQ_PZ_01. |
| SQ_PZ_02 | The Plague Doctor | automatic | Collect Vorn logs; identify self-justification; seal dangerous protocols. | PlagueDoctorDataSealed. | SQ_PZ_02. |
| SQ_PZ_03 | The First One Not Asked | automatic | Find Elise's letter; restore name in lab index; play final consent log. | PatientZeroNameRestored. | SQ_PZ_03. |
| SQ_PZ_04 | Formula Missing Enzyme | automatic | Decode enzyme references; cross-link signals; mark Congo/Nigeria route. | AfricaBioJungleRouteUnlocked. | SQ_PZ_04. |
| SQ_PZ_05 | Blood Is Not the Answer to Everything | automatic | Review risk; refuse invasive validation; store model in vault. | BinhValidationRefused; trust increase. | SQ_PZ_05. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|

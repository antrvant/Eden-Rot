# Quests - CH021

Metadata:

- chapterID: CH021
- sourceFilename: chapter_021_dao_khong_ten.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_021 | Repair Vessel | main | automatic | Bio-storm forces group onto unnamed island after CH020 | Vessel repaired, named, escaped island, port array signal received | Main Quest section. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ021_001 | MQ_021 | 1 | Assess vessel damage after bio-storm | Inspect | LOC_CH021_VESSEL_STRANDED | 1 | MQ_021_01. |
| OBJ_MQ021_002 | MQ_021 | 2 | Establish temporary camp and boat safety rules | Setup | LOC_CH021_VESSEL_DECK | 1 | MQ_021_02. |
| OBJ_MQ021_003 | MQ_021 | 3 | Scout unnamed island | Explore | LOC_CH021_FISHING_VILLAGE | 1 | MQ_021_03. |
| OBJ_MQ021_004 | MQ_021 | 4 | Salvage repair parts from fishing village | Scavenge | ITM_CH021_SEALANT_KIT | 1 | MQ_021_04. |
| OBJ_MQ021_005 | MQ_021 | 5 | Investigate missing island map | Investigation | LOC_CH021_FISHING_VILLAGE | 1 | MQ_021_05. |
| OBJ_MQ021_006 | MQ_021 | 6 | Reach lighthouse relay | GoTo | LOC_CH021_LIGHTHOUSE_RELAY | 1 | MQ_021_06. |
| OBJ_MQ021_007 | MQ_021 | 7 | Retrieve battery, filter, and generator parts | Scavenge | ITM_CH021_LIGHTHOUSE_BATTERY | 1 | MQ_021_07. |
| OBJ_MQ021_008 | MQ_021 | 8 | Copy maritime relay logs | DataExtract | ITM_CH021_LIGHTHOUSE_RELAY_LOG | 1 | MQ_021_08. |
| OBJ_MQ021_009 | MQ_021 | 9 | Survive tide-borne drowned infected | Combat | ENM_CH021_DROWNED_INFECTED | 1 | MQ_021_09. |
| OBJ_MQ021_010 | MQ_021 | 10 | Repair vessel | Repair | LOC_CH021_VESSEL_STRANDED | 1 | MQ_021_10. |
| OBJ_MQ021_011 | MQ_021 | 11 | Name the vessel | Interact | LOC_CH021_VESSEL_DECK | 1 | MQ_021_11. |
| OBJ_MQ021_012 | MQ_021 | 12 | Escape island before swimmers board | Escape | LOC_CH021_VESSEL_DEPARTURE | 1 | MQ_021_12. |
| OBJ_MQ021_013 | MQ_021 | 13 | Receive port array signal | UnlockQuest | MQ_022 | 1 | MQ_021_13. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ021_01_001 | SQ_021_01 | Ask passengers for boat name suggestions | Boat morale boost | SQ_Island_01. |
| OBJ_SQ021_02_001 | SQ_021_02 | Restore local power at lighthouse and read logs | Signal to Chapter 22 | SQ_Island_02. |
| OBJ_SQ021_03_001 | SQ_021_03 | Discover barnacle armor weak points on drowned infected | Maritime enemy tutorial | SQ_Island_03. |
| OBJ_SQ021_04_001 | SQ_021_04 | Tune radio near lighthouse for Me Linh signal | Future side quest seed | SQ_Island_04. |
| OBJ_SQ021_05_001 | SQ_021_05 | Create no-running-on-deck rule and storm drill | Child morale and mobile classroom | SQ_Island_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ021_DELAY_REPAIRS | MQ_021 | Player delays vessel repairs | Tide rises, more drowned attack | Fail States section. |
| FAIL_MQ021_UNSECURED_BOAT | MQ_021 | Boat interior not secured before attack | Child/survivor injury during attack | Fail States section. |
| FAIL_MQ021_REFUSE_HOANG | MQ_021 | Player refuses Hoang technical help | Repair slower, more risk | Fail States section. |
| FAIL_MQ021_TRUST_HOANG_UNSUPERVISED | MQ_021 | Player trusts Hoang unsupervised | Tension and sabotage suspicion | Fail States section. |
| FAIL_MQ021_IGNORE_RELAY_LOGS | MQ_021 | Player ignores relay logs | Miss Chapter 22 signal clue | Fail States section. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ021_VESSEL_REPAIRED | MQ_021 | system_unlock | Vessel repaired and operational | Rewards section. |
| REW_MQ021_VESSEL_NAMED | MQ_021 | narrative | Vessel named "Nha Di" | Rewards section. |
| REW_MQ021_MARITIME_RELAY_CLUE | MQ_021 | lore | Maritime relay clue for Chapter 22 | Rewards section. |
| REW_MQ021_EDENROT_ISLAND_CLASS | MQ_021 | lore | EDENROT CLASS: ISLAND RELAY classification | Rewards section. |
| REW_MQ021_DROWNED_CODEX | MQ_021 | system_unlock | Drowned infected codex | Rewards section. |
| REW_MQ021_MOBILE_BASE | MQ_021 | system_unlock | Mobile base systems unlocked | Rewards section. |
| REW_MQ021_RELAY_LOG | MQ_021 | item | ITM_CH021_LIGHTHOUSE_RELAY_LOG | Rewards section. |
| REW_MQ021_CHALK_MARK | MQ_021 | item | ITM_CH021_NHA_DI_CHALK_MARK | Rewards section. |
| REW_MQ021_SWIMMER_FORESHADOW | MQ_021 | lore | SwimmerVariantForeshadowed threat flag | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH021_MOBILE_BASE | MQ_021 | Mobile base systems | Vessel repaired. |
| UNLOCK_CH021_MARITIME_REPAIR | MQ_021 | Maritime repair loop | First island salvage complete. |
| UNLOCK_CH021_SEA_HAZARDS | MQ_021 | Sea hazard rules | Drowned infected encountered. |
| UNLOCK_CH021_BOAT_NAMING | MQ_021 | Boat naming and morale system | Vessel named. |
| UNLOCK_CH021_MQ022_TECH_PORT | MQ_021 | Chapter 22 tech port mission | Port array signal received. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH021_VESSEL_REPAIRED | MQ_021 | Vessel repair complete. |
| FLAG_CH021_VESSEL_NAMED | MQ_021 | Binh writes "Nha Di" in chalk. |
| FLAG_CH021_MOBILE_BASE_UNLOCKED | MQ_021 | Vessel operational as mobile home. |
| FLAG_CH021_MARITIME_RELAY_03_DISCOVERED | MQ_021 | Lighthouse relay logs copied. |
| FLAG_CH021_EDENROT_ISLAND_RELAY_CLASSIFIED | MQ_021 | Relay logs confirm EDENROT classification. |
| FLAG_CH021_PORT_ARRAY_SIGNAL_RECEIVED | MQ_021 | Radio captures coordinates to tech port. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_021_01 | Name For The Vessel | environmental | Ask passengers for names, let Binh write chosen name | Boat morale boost; mobile base identity | SQ_Island_01. |
| SQ_021_02 | Dead Lighthouse | environmental | Reach lighthouse, restore power, read logs, retrieve parts | Signal to Chapter 22 | SQ_Island_02. |
| SQ_021_03 | Bodies Below The Waterline | environmental | Mark tide line, discover barnacle weak points, escape swimmer | Maritime enemy tutorial | SQ_Island_03. |
| SQ_021_04 | Me Linh Promise | comp_lam | Tune radio, search call logs, find partial registry | Future side quest seed | SQ_Island_04. |
| SQ_021_05 | Classroom On Deck | comp_mai | Assign sleeping corners, create rules, write names board, set storm drill | Child morale and mobile classroom | SQ_Island_05. |

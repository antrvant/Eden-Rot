# Quests - CH034

Metadata:

- chapterID: CH034
- sourceFilename: chapter_034_ban_do_cua_ngay_tan_the.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_034 | Choose Next Front | main | npc_thu | CH033 global signal map and terraforming fragment available | Europe first front selected and Act 6 unlocked | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ034_001 | MQ_034 | 1 | Review global signal map. | Interact | LOC_CH034_MAP_ROOM | 1 | Main Quest objective 1. |
| OBJ_MQ034_002 | MQ_034 | 2 | Classify major fronts. | Interact | LOC_CH034_MAP_ROOM | 1 | Main Quest objective 2. |
| OBJ_MQ034_003 | MQ_034 | 3 | Classify EDENROT strategic promise map. | Interact | LOC_CH034_MAP_ROOM | 1 | Main Quest objective 3. |
| OBJ_MQ034_004 | MQ_034 | 4 | Hold strategy council. | TalkTo | LOC_CH034_PLANNING_CHAMBER | 1 | Main Quest objective 4. |
| OBJ_MQ034_005 | MQ_034 | 5 | Analyze terraforming fragment. | Interact | LOC_CH034_MEDICAL_ROOM | 1 | Main Quest objective 5. |
| OBJ_MQ034_006 | MQ_034 | 6 | Decode Patient Zero route hint. | Interact | LOC_CH034_MEDICAL_ROOM | 1 | Main Quest objective 6. |
| OBJ_MQ034_007 | MQ_034 | 7 | Establish Cure Ethics Addendum. | Interact | LOC_CH034_MEDICAL_ROOM | 1 | Main Quest objective 7. |
| OBJ_MQ034_008 | MQ_034 | 8 | Lock Binh biomarker data. | Interact | LOC_CH034_SIDE_ROOM | 1 | Main Quest objective 8. |
| OBJ_MQ034_009 | MQ_034 | 9 | Investigate Hoang weak ping. | Interact | LOC_CH034_LISTEN_DECK | 1 | Main Quest objective 9. |
| OBJ_MQ034_010 | MQ_034 | 10 | Create North America shared node. | Interact | LOC_CH034_CONVY_CAMP | 1 | Main Quest objective 10. |
| OBJ_MQ034_011 | MQ_034 | 11 | Assign allies to nodes. | Interact | LOC_CH034_CONVY_CAMP | 1 | Main Quest objective 11. |
| OBJ_MQ034_012 | MQ_034 | 12 | Confirm Paris archive route. | TalkTo | LOC_CH034_MAP_VOTE | 1 | Main Quest objective 12. |
| OBJ_MQ034_013 | MQ_034 | 13 | Negotiate delayed ally promises. | TalkTo | LOC_CH034_MAP_VOTE | 1 | Main Quest objective 13. |
| OBJ_MQ034_014 | MQ_034 | 14 | Require arrow cost ledger. | Interact | LOC_CH034_MAP_VOTE | 1 | Main Quest objective 14. |
| OBJ_MQ034_015 | MQ_034 | 15 | Choose Europe first front. | Interact | LOC_CH034_MAP_VOTE | 1 | Main Quest objective 15. |
| OBJ_MQ034_016 | MQ_034 | 16 | Prepare Atlantic crossing. | Interact | LOC_CH034_DEPARTURE | 1 | Main Quest objective 16. |
| OBJ_MQ034_017 | MQ_034 | 17 | Unlock Act 6 Europe route. | UnlockQuest | MQ_035 | 1 | Main Quest objective 17. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ034_01_001 | SQ_034_01 | List who benefits and waits for each route. | PromiseDebtLedger. | SQ_Map_01. |
| OBJ_SQ034_02_001 | SQ_034_02 | Compare Doctor's models and choose linked sequence. | EuropeAfricaLinkedPlan. | SQ_Map_02. |
| OBJ_SQ034_03_001 | SQ_034_03 | Lock biomarker data and update consent protocol. | CureEthicsAddendum and BinhDataVault. | SQ_Map_03. |
| OBJ_SQ034_04_001 | SQ_034_04 | Verify Paris signal and exchange child-safety code. | ParisArchiveInvitation. | SQ_Map_04. |
| OBJ_SQ034_05_001 | SQ_034_05 | Trace Hoang ping partially and store for later. | HoangAliveProbable and HoangSearchDeferred. | SQ_Map_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ034_BINH_DATA_LEAK | MQ_034 | Binh biomarker data leaks into global network. | Severe child danger. | Failure Conditions. |
| FAIL_MQ034_FACTION_SPLIT | MQ_034 | Factions split over route decision. | Group fractures. | Failure Conditions. |
| FAIL_MQ034_NA_NO_GOVERNANCE | MQ_034 | NORAD left without governance. | Falls into conflict. | Failure Conditions. |
| FAIL_MQ034_PATIENT_ZERO_LOST | MQ_034 | Patient Zero clue lost due to delay. | Cure context lost. | Failure Conditions. |
| FAIL_MQ034_FALSE_ROUTE | MQ_034 | Architect listener injects false route. | Wrong destination. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ034_EUROPE_ROUTE | MQ_034 | region_unlock | Europe route unlocked | Completion Rewards. |
| REW_MQ034_ACT6 | MQ_034 | quest_unlock | Act 6 unlocked | Completion Rewards. |
| REW_MQ034_CURE_ETHICS | MQ_034 | system_unlock | Cure ethics addendum | Completion Rewards. |
| REW_MQ034_NA_NODE | MQ_034 | system_unlock | North America shared node | Completion Rewards. |
| REW_MQ034_ALLY_QUEUE | MQ_034 | network_unlock | Global ally task queue | Completion Rewards. |
| REW_MQ034_PATIENT_ZERO | MQ_034 | lore_unlock | Patient Zero trail | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH034_EUROPE | MQ_034 | Europe route | Europe selected as first front. |
| UNLOCK_CH034_ACT6 | MQ_034 | Act 6 | Europe route confirmed. |
| UNLOCK_CH034_NA_NODE | MQ_034 | North America shared node | Shared governance established. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH034_EUROPE_ROUTE_UNLOCKED | MQ_034 | Europe selected as first front. |
| FLAG_CH034_ACT6_UNLOCKED | MQ_034 | Act 6 accessible. |
| FLAG_CH034_NA_SHARED_NODE | MQ_034 | NORAD delegated to shared governance. |
| FLAG_CH034_PATIENT_ZERO_PATH_ACTIVE | MQ_034 | Europe cure trail activated. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_034_01 | Price of an Arrow | npc_eli | List who benefits/waits for each route, record reasons. | PromiseDebtLedger. | SQ_Map_01. |
| SQ_034_02 | Europe or Africa | npc_doctor | Compare models, ask allies, choose linked sequence. | EuropeAfricaLinkedPlan. | SQ_Map_02. |
| SQ_034_03 | Binh's Blood Is Not Data | comp_mai | Lock biomarker data, update consent protocol. | CureEthicsAddendum and BinhDataVault. | SQ_Map_03. |
| SQ_034_04 | Invitation from Paris | npc_amelie | Verify Paris signal, exchange child-safety code. | ParisArchiveInvitation. | SQ_Map_04. |
| SQ_034_05 | Hoang's Signal | npc_thu | Trace ping, determine if spoofed, store for later. | HoangAliveProbable and HoangSearchDeferred. | SQ_Map_05. |

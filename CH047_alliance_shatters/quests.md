# Quests - CH047

Metadata:

- chapterID: CH047
- sourceFilename: chapter_047_lien_minh_tan_vo.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_047 | Survive Citadel Collapse | main | automatic | Chapter begins with evacuation | Guardian Circle signed; children evacuated; Hunter repelled; Chapter 48 unlocked | Metadata: MQ_047 - Survive Citadel Collapse. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ047_001 | MQ_047 | 1 | Evacuate children by buddy line. | Escort | LOC_CH047_COLLAPSE_CORRIDOR | 1 | MQ_047_01. |
| OBJ_MQ047_002 | MQ_047 | 2 | Maintain Hoang stasis pod. | Escort | LOC_CH047_COLLAPSE_CORRIDOR | 1 | MQ_047_02. |
| OBJ_MQ047_003 | MQ_047 | 3 | Exit root column. | GoTo | LOC_CH047_ROOT_COLUMN_EXIT | 1 | MQ_047_03. |
| OBJ_MQ047_004 | MQ_047 | 4 | Identify PROTECTION OWNERSHIP FRACTURE. | Observe | LOC_CH047_ROOT_COLUMN_EXIT | 1 | MQ_047_04. |
| OBJ_MQ047_005 | MQ_047 | 5 | De-escalate first custody claim. | Dialogue | LOC_CH047_ROOT_COLUMN_EXIT | 1 | MQ_047_05. |
| OBJ_MQ047_006 | MQ_047 | 6 | Identify Hunter first shot. | Observe | LOC_CH047_BATTLEFIELD_AMAZON | 1 | MQ_047_06. |
| OBJ_MQ047_007 | MQ_047 | 7 | Escape collapsing citadel route. | GoTo | LOC_CH047_FLOODED_TUNNEL | 1 | MQ_047_07. |
| OBJ_MQ047_008 | MQ_047 | 8 | Convene faction council under fire. | Dialogue | LOC_CH047_COMMAND_RAFT | 1 | MQ_047_08. |
| OBJ_MQ047_009 | MQ_047 | 9 | Remove Hunter tracker from Binh. | Interact | LOC_CH047_COMMAND_RAFT | 1 | MQ_047_09. |
| OBJ_MQ047_010 | MQ_047 | 10 | Rescue trapped faction squad. | Combat | LOC_CH047_BATTLEFIELD_AMAZON | 1 | MQ_047_10. |
| OBJ_MQ047_011 | MQ_047 | 11 | Defeat or repel Hunter. | Boss | LOC_CH047_CANOPY_RUINS | 1 | MQ_047_11. |
| OBJ_MQ047_012 | MQ_047 | 12 | Save Hoang pod during power failure. | Choice | LOC_CH047_HOANG_POD_SITE | 1 | MQ_047_12. |
| OBJ_MQ047_013 | MQ_047 | 13 | Receive Antarctica countdown broadcast. | Observe | LOC_CH047_ALLIANCE_BROADCAST | 1 | MQ_047_13. |
| OBJ_MQ047_014 | MQ_047 | 14 | Share countdown; protect child data. | Choice | LOC_CH047_ALLIANCE_BROADCAST | 1 | MQ_047_14. |
| OBJ_MQ047_015 | MQ_047 | 15 | Establish Guardian Circle Charter. | Dialogue | LOC_CH047_GUARDIAN_CIRCLE_SITE | 1 | MQ_047_15. |
| OBJ_MQ047_016 | MQ_047 | 16 | Contain protection ownership fracture. | Dialogue | LOC_CH047_GUARDIAN_CIRCLE_SITE | 1 | MQ_047_16. |
| OBJ_MQ047_017 | MQ_047 | 17 | Launch Southern Ocean route. | Progression | LOC_CH047_FLEET_DEPARTURE | 1 | MQ_047_17. |
| OBJ_MQ047_018 | MQ_047 | 18 | Unlock Chapter 48 Antarctica. | Progression | LOC_CH047_FLEET_DEPARTURE | 1 | MQ_047_18. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ047_FRIENDLY_FIRE | MQ_047 | Friendly fire between factions. | Alliance split. | Failure Conditions. |
| FAIL_MQ047_CHILDREN_SCATTER | MQ_047 | Children panic and scatter. | Lost children. | Failure Conditions. |
| FAIL_MQ047_HUNTER_CAPTURES_CHILD | MQ_047 | Hunter captures/tags a child. | Child compromised. | Failure Conditions. |
| FAIL_MQ047_HOANG_LOST | MQ_047 | Hoang pod lost. | Hoang branch damage. | Failure Conditions. |
| FAIL_MQ047_RECORDS_SEIZED | MQ_047 | Child records seized by one faction. | Data ownership violation. | Failure Conditions. |
| FAIL_MQ047_COUNTDOWN_HIDDEN | MQ_047 | Countdown not shared; alliance split. | Alliance collapse. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ047_CHILDREN | MQ_047 | ally_group | MajorityChildrenEvacuated | Completion. |
| REW_MQ047_CHARTER | MQ_047 | governance | GuardianCircleCharter | Completion. |
| REW_MQ047_ANTARCTICA | MQ_047 | knowledge | AntarcticaCountdownPublic | Completion. |
| REW_MQ047_ALLIANCE | MQ_047 | faction_status | AllianceFracturedButIntact | Completion. |
| REW_MQ047_ROUTE | MQ_047 | route_unlock | SouthernOceanRoute | Completion. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH047_GUARDIAN_CIRCLE | MQ_047 | Guardian Circle governance | Charter signed. |
| UNLOCK_CH047_HUNTER_REPELLED | MQ_047 | Hunter threat cleared | Hunter repelled. |
| UNLOCK_CH047_ANTARCTICA_PUBLIC | MQ_047 | Antarctica countdown public | Countdown shared. |
| UNLOCK_CH047_CH48_ANTARCTICA | MQ_047 | Chapter 48 Antarctica | Southern Ocean route opened. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_047_A | Voluntary Name Cards | char_mai | Replace faction wrist tags with name cards children can keep/remove. | ChildrenCustodyPanicReduced. | SQ_047_A. |
| SQ_047_B | False Muzzle Flash | char_iara | Prove Hunter framed Heartland before NORAD retaliates. | FriendlyFirePrevented. | SQ_047_B. |
| SQ_047_C | Debt Of The Almost-Betrayers | char_trung | Rescue faction squad that attempted to seize child data. | AllianceMercyDebt. | SQ_047_C. |
| SQ_047_D | Rafi's Rope Loop | char_rafi | Help Rafi evacuate without hand contact using rope loop. | RafiTrustMaintained. | SQ_047_D. |
| SQ_047_E | Hoang Power Relay | char_trung | Keep Hoang pod stable without draining medical supply for Nina. | HoangStasisMaintained_Act7End; NinaVitalsStable. | SQ_047_E. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|

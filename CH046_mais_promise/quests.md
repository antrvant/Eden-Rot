# Quests - CH046

Metadata:

- chapterID: CH046
- sourceFilename: chapter_046_loi_hua_cua_mai.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_046 | Free the Children | main | automatic | Group enters prison/lab wing | Children rescued; Glutton defeated; Antarctica transfer discovered; Chapter 47 unlocked | Metadata: MQ_046 - Free the Children. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ046_001 | MQ_046 | 1 | Enter Orison prison/lab wing. | GoTo | LOC_CH046_PRISON_LAB_WING | 1 | MQ_046_01. |
| OBJ_MQ046_002 | MQ_046 | 2 | Identify EDENROT FUTURE MATERIAL WARD classification. | Observe | LOC_CH046_PRISON_LAB_WING | 1 | MQ_046_02. |
| OBJ_MQ046_003 | MQ_046 | 3 | Establish Mai rescue protocol. | Dialogue | LOC_CH046_PRISON_LAB_WING | 1 | MQ_046_03. |
| OBJ_MQ046_004 | MQ_046 | 4 | Meet Ana and child ward. | Dialogue | LOC_CH046_CHILD_WARD | 1 | MQ_046_04. |
| OBJ_MQ046_005 | MQ_046 | 5 | Prove names from archive. | Dialogue | LOC_CH046_CHILD_WARD | 1 | MQ_046_05. |
| OBJ_MQ046_006 | MQ_046 | 6 | Confront Orison in classroom. | Dialogue | LOC_CH046_CLASSROOM | 1 | MQ_046_06. |
| OBJ_MQ046_007 | MQ_046 | 7 | Create name circle. | Interact | LOC_CH046_NAME_CIRCLE | 1 | MQ_046_07. |
| OBJ_MQ046_008 | MQ_046 | 8 | Rescue transfer pod children. | Timed | LOC_CH046_TRANSFER_POD_BAY | 1 | MQ_046_08. |
| OBJ_MQ046_009 | MQ_046 | 9 | Stop recycler pod drop. | Combat | LOC_CH046_RECYCLER_CHAMBER | 1 | MQ_046_09. |
| OBJ_MQ046_010 | MQ_046 | 10 | Reject Orison trade for Binh. | Choice | LOC_CH046_CLASSROOM | 1 | MQ_046_10. |
| OBJ_MQ046_011 | MQ_046 | 11 | Establish No Child As Currency. | Dialogue | LOC_CH046_CLASSROOM | 1 | MQ_046_11. |
| OBJ_MQ046_012 | MQ_046 | 12 | Break ward lockdown. | Combat | LOC_CH046_WARD_CRAWLSPACE | 1 | MQ_046_12. |
| OBJ_MQ046_013 | MQ_046 | 13 | Escort children to evacuation bridge. | Escort | LOC_CH046_EVAC_BRIDGE | 1 | MQ_046_13. |
| OBJ_MQ046_014 | MQ_046 | 14 | Defeat Glutton recycler. | Boss | LOC_CH046_EVAC_BRIDGE | 1 | MQ_046_14. |
| OBJ_MQ046_015 | MQ_046 | 15 | Recover child records. | Interact | LOC_CH046_TERRAFORM_RELAY | 1 | MQ_046_15. |
| OBJ_MQ046_016 | MQ_046 | 16 | Discover Antarctica terraforming transfer. | Observe | LOC_CH046_TERRAFORM_RELAY | 1 | MQ_046_16. |
| OBJ_MQ046_017 | MQ_046 | 17 | Count children by name. | Dialogue | LOC_CH046_EVAC_ALCOVE | 1 | MQ_046_17. |
| OBJ_MQ046_018 | MQ_046 | 18 | Unlock Chapter 47 citadel collapse. | Progression | LOC_CH046_EVAC_ALCOVE | 1 | MQ_046_18. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ046_CHILD_PANIC | MQ_046 | Child panic causes scattering. | Lost children; weakened ending. | Failure Conditions. |
| FAIL_MQ046_TRADE_ACCEPTED | MQ_046 | Orison trade accepted. | Major moral damage; bad ending branch. | Failure Conditions. |
| FAIL_MQ046_GLUTTON_CONSUMES_PODS | MQ_046 | Glutton consumes key pods. | Lost children. | Failure Conditions. |
| FAIL_MQ046_RECORDS_DESTROYED | MQ_046 | Child records destroyed. | Worse CH047 alliance dispute. | Failure Conditions. |
| FAIL_MQ046_HOANG_STASIS_FAILS | MQ_046 | Hoang stasis fails from power neglect. | Hoang lost. | Failure Conditions. |
| FAIL_MQ046_TERRAFORM_MISSED | MQ_046 | Terraforming transfer entirely missed. | Antarctica route unknown. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ046_CHILDREN | MQ_046 | ally_group | ImmuneChildrenSaved | Completion. |
| REW_MQ046_RECORDS | MQ_046 | data_item | ChildRecordsRecovered | Completion. |
| REW_MQ046_ANTARCTICA | MQ_046 | knowledge | AntarcticaSourceLocated | Completion. |
| REW_MQ046_COUNTDOWN | MQ_046 | progression | 30DayCountdown | Completion. |
| REW_MQ046_TRUST | MQ_046 | reputation | ChildTrust increase | Completion. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH046_CHILD_ALLIES | MQ_046 | Immune children allies | Children rescued. |
| UNLOCK_CH046_GLUTTON_CLEARED | MQ_046 | Glutton recycler cleared | Glutton defeated. |
| UNLOCK_CH046_ANTARCTICA_ROUTE | MQ_046 | Antarctica route fragment | Transfer discovered. |
| UNLOCK_CH046_CH47_COLLAPSE | MQ_046 | Chapter 47 citadel collapse | Collapse protocol activated. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_046_A | Mateo's Tap Code | char_mateo | Learn Mateo's tap rhythm for silent lockdown communication. | MateoTrust; lower child panic during Glutton. | SQ_046_A. |
| SQ_046_B | Rafi's Distance | char_rafi | Rescue Rafi by creating safe path without grabbing him. | RafiRescuedWithoutForce; Mai trust high. | SQ_046_B. |
| SQ_046_C | Luz's Lie | char_luz | Protect Luz's cover until breakout or expose her early. | LuzInsiderRoute. | SQ_046_C. |
| SQ_046_D | Nina's Pod | char_nina | Save Nina with Samir medical care and Binh calming; no resonance forcing. | NinaRescued; future cure dialogue. | SQ_046_D. |
| SQ_046_E | Hoang Stasis Power | char_trung | Reroute power to Hoang pod without sacrificing child pod safety. | HoangStasisMaintained. | SQ_046_E. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|

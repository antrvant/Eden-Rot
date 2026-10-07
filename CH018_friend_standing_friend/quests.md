# Quests - CH018

Metadata:

- chapterID: CH018
- sourceFilename: chapter_018_ban_than_ban_dung.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_018 | Hoang Betrayal | main | automatic | Chapter start after supply theft discovery | Mai captured, bandit fort lead recovered, Hoang status unresolved | Metadata lists Main Quest: MQ_018 - Hoang Betrayal. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ018_001 | MQ_018 | 1 | Investigate the supply theft in storage. | GoTo | LOC_CH018_SUPPLY_STORAGE | 1 | Main Quest objective 1. |
| OBJ_MQ018_002 | MQ_018 | 2 | Compare mud and cloth markers from storage floor. | Interact | ITM_CH018_MUD_SAMPLE | 1 | Main Quest objective 2 and Scene 1. |
| OBJ_MQ018_003 | MQ_018 | 3 | Identify the security gap only the guard team knows. | Investigate | LOC_CH018_FENCE_GAP | 1 | Main Quest objective 3 and Scene 1. |
| OBJ_MQ018_004 | MQ_018 | 4 | Notice Hoang's unexplained absence overnight. | Investigate | char_hoang | 1 | Main Quest objective 4 and Scene 1. |
| OBJ_MQ018_005 | MQ_018 | 5 | Follow or reconstruct Hoang's route to the checkpoint. | GoTo | LOC_CH018_OLD_TOLL_STATION | 1 | Main Quest objective 5 and Scene 4. |
| OBJ_MQ018_006 | MQ_018 | 6 | Discover the bandit checkpoint trade. | Investigate | npc_bandit_trader | 1 | Main Quest objective 6 and Scene 3. |
| OBJ_MQ018_007 | MQ_018 | 7 | Identify the EDEN broker hint at checkpoint. | Investigate | npc_eden_broker | 1 | Main Quest objective 7 and Scene 3. |
| OBJ_MQ018_008 | MQ_018 | 8 | Confront Hoang about the fuel source. | Dialogue | char_hoang | 1 | Main Quest objective 8 and Scene 4. |
| OBJ_MQ018_009 | MQ_018 | 9 | Determine what information was sold. | Dialogue | char_hoang | 1 | Main Quest objective 9 and Scene 5. |
| OBJ_MQ018_010 | MQ_018 | 10 | Respond to bandit raid at school. | CombatOrEscape | ENM_CH018_BANDIT_RAIDERS | 1 | Main Quest objective 10 and Scene 6. |
| OBJ_MQ018_011 | MQ_018 | 11 | Evacuate Class 3B children. | Protect | LOC_CH018_CLASS_3B | 1 | Main Quest objective 11 and Scene 6. |
| OBJ_MQ018_012 | MQ_018 | 12 | Protect Binh and children during raid. | Protect | char_binh | 1 | Main Quest objective 12 and Scene 6. |
| OBJ_MQ018_013 | MQ_018 | 13 | Discover Mai has been captured. | Investigate | char_mai | 1 | Main Quest objective 13 and Scene 7. |
| OBJ_MQ018_014 | MQ_018 | 14 | Recover bandit fort lead from dead bandit map. | Fetch | ITM_CH018_BANDIT_FORT_MAP | 1 | Main Quest objective 14 and Scene 7. |
| OBJ_MQ018_015 | MQ_018 | 15 | Decide Hoang's immediate status. | Choice | char_hoang | 1 | Main Quest objective 15 and Scene 7. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ018_01_001 | SQ_Betrayal_01 | Compare mud from gate, refugee area, and security path. | Identifies true origin of theft trail. | SQ_Betrayal_01. |
| OBJ_SQ018_01_002 | SQ_Betrayal_01 | Identify cloth marker as bandit route sign. | Confirms external involvement, protects refugees from false blame. | SQ_Betrayal_01. |
| OBJ_SQ018_02_001 | SQ_Betrayal_02 | Observe trade from cover or arrive after. | Reveals bandit network and fuel economy. | SQ_Betrayal_02. |
| OBJ_SQ018_02_002 | SQ_Betrayal_02 | Recover map mark from checkpoint. | Unlocks fort direction clue. | SQ_Betrayal_02. |
| OBJ_SQ018_03_001 | SQ_Betrayal_03 | Ask exactly what Hoang said to trader. | Identifies omissions in Hoang's account. | SQ_Betrayal_03. |
| OBJ_SQ018_03_002 | SQ_Betrayal_03 | Present route, guard, and classroom clues to Hoang. | Forces Hoang to confront what he enabled. | SQ_Betrayal_03. |
| OBJ_SQ018_04_001 | SQ_Betrayal_04 | Use Mai's safe-room rules during evacuation. | Improves child survival rate. | SQ_Betrayal_04. |
| OBJ_SQ018_04_002 | SQ_Betrayal_04 | Find Mai's chalk mark on desk edge. | Confirms Mai's direction and agency. | SQ_Betrayal_04. |
| OBJ_SQ018_05_001 | SQ_Betrayal_05 | Search Hoang's gear for copied checkpoint map. | Reveals bandit fort location. | SQ_Betrayal_05. |
| OBJ_SQ018_05_002 | SQ_Betrayal_05 | Decode checkpoint symbols on map. | Identifies likely bandit fort position. | SQ_Betrayal_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ018_ACCUSE_REFUGEES | MQ_018 | Player accuses refugees publicly without evidence. | Base splits; raid casualties increase. | Fail States section. |
| FAIL_MQ018_IGNORE_HOANG_CLUES | MQ_018 | Player ignores clues about Hoang's absence. | Raid hits harder; more children injured. | Fail States section. |
| FAIL_MQ018_ATTACK_HOANG_EARLY | MQ_018 | Player attacks Hoang before raid. | Security chaos; bandits exploit gap. | Fail States section. |
| FAIL_MQ018_CLASSROOM_UNPROTECTED | MQ_018 | Player fails to evacuate class during raid. | Child casualty or capture. | Fail States section. |
| FAIL_MQ018_SHOOT_LIEUTENANT | MQ_018 | Player shoots bandit lieutenant recklessly. | Mai wounded or taken farther. | Fail States section. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ018_BANDIT_FORT_UNLOCK | MQ_018 | location_unlock | Bandit Fort | Rewards section. |
| REW_MQ018_MAI_CAPTURED_FLAG | MQ_018 | world_state | MaiCaptured | Rewards section. |
| REW_MQ018_HOANG_BETRAYAL_FLAG | MQ_018 | world_state | HoangBetrayalStarted | Rewards section. |
| REW_MQ018_BANDIT_NETWORK_FLAG | MQ_018 | intel | BanditTradeNetwork | Rewards section. |
| REW_MQ018_CHECKPOINT_MAP | MQ_018 | item | Bandit checkpoint map | Rewards section. |
| REW_MQ018_MAI_CHALK_MARK | MQ_018 | item | Mai chalk mark | Rewards section. |
| REW_MQ018_EDEN_BROKER_INTEL | MQ_018 | intel | EDEN broker asks for Eden Node proof | Rewards section. |
| REW_MQ018_BINH_TRUST_FLAG | MQ_018 | emotional_flag | BinhTrustShaken | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH018_BANDIT_FORT_LOCATION | MQ_018 | Bandit fort map location | Recover map from dead bandit or Hoang's gear. |
| UNLOCK_CH018_RESCUE_MISSION | MQ_018 | Chapter 19 rescue mission | Mai captured and fort location confirmed. |
| UNLOCK_CH018_MORAL_COMPLEXITY | MQ_018 | Hoang not pure evil flag | Hoang fights during raid proving unintended consequence. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH018_HOANG_BETRAYAL_STARTED | MQ_018 | Hoang completes checkpoint trade. |
| FLAG_CH018_HOANG_SOLD_COORDINATES | MQ_018 | Trung discovers checkpoint fuel evidence. |
| FLAG_CH018_MAI_CAPTURED | MQ_018 | Bandit lieutenant takes Mai during raid. |
| FLAG_CH018_BANDIT_FORT_UNLOCKED | MQ_018 | Map fragment recovered from dead bandit. |
| FLAG_CH018_BINH_TRUST_SHAKEN | MQ_018 | Binh asks "Did Hoang sell Mom?" |
| FLAG_CH018_MAI_CHALK_TRAIL | MQ_018 | Player finds Mai's chalk mark on desk. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Betrayal_01 | Mud Tracks in Storage | automatic | Inspect mud and cloth traces to identify theft origin without false accusation. | Determines how fractured base becomes before raid. | SQ_Betrayal_01. |
| SQ_Betrayal_02 | Fuel Checkpoint Trade | automatic | Reach old toll station, observe trade, identify trader, recover map mark. | Reveals bandit network and fuel economy. | SQ_Betrayal_02. |
| SQ_Betrayal_03 | Friend's Lie | automatic | Ask Hoang exactly what he said, identify omissions, decide custody level. | Affects Hoang trust and Chapter 19 companion availability. | SQ_Betrayal_03. |
| SQ_Betrayal_04 | Classroom Violated | automatic | Trigger child evacuation, use safe-room rules, find Mai chalk mark. | Child morale and Mai trail for rescue. | SQ_Betrayal_04. |
| SQ_Betrayal_05 | Secret Map | automatic | Search Hoang's gear, decode checkpoint symbols, find bandit fort. | Unlocks Chapter 19 rescue route. | SQ_Betrayal_05. |

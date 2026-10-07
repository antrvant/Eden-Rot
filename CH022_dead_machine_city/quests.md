# Quests - CH022

Metadata:

- chapterID: CH022
- sourceFilename: chapter_022_thanh_pho_nguoi_may_chet.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_022 | Decode Architect Signal | main | automatic | Nha Di follows port array signal to tech port after CH021 | Architect signal decoded; Binh data blocked; cybernetic infected defeated; Tokyo relay signal received | Main Quest section. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ022_001 | MQ_022 | 1 | Approach automated tech port | GoTo | LOC_CH022_APPROACH | 1 | MQ_022_01. |
| OBJ_MQ022_002 | MQ_022 | 2 | Dock safely between cranes | Navigate | LOC_CH022_CONTAINER_YARD | 1 | MQ_022_02. |
| OBJ_MQ022_003 | MQ_022 | 3 | Bypass biometric security gate | Hack | LOC_CH022_DOCK_GATE | 1 | MQ_022_03. |
| OBJ_MQ022_004 | MQ_022 | 4 | Spoof Binh camera flag | Hack | LOC_CH022_DOCK_GATE | 1 | MQ_022_04. |
| OBJ_MQ022_005 | MQ_022 | 5 | Cross container yard hazards | Navigate | LOC_CH022_CONTAINER_YARD | 1 | MQ_022_05. |
| OBJ_MQ022_006 | MQ_022 | 6 | Retrieve engineer keycard | Scavenge | ITM_CH022_ENGINEER_KEYCARD | 1 | MQ_022_06. |
| OBJ_MQ022_007 | MQ_022 | 7 | Salvage navigation and boat parts | Scavenge | ITM_CH022_NAVIGATION_MODULE | 1 | MQ_022_07. |
| OBJ_MQ022_008 | MQ_022 | 8 | Enter server hall | GoTo | LOC_CH022_SERVER_HALL | 1 | MQ_022_08. |
| OBJ_MQ022_009 | MQ_022 | 9 | Decode Architect signal | DataExtract | ITM_CH022_PORT_ARRAY_DATA | 1 | MQ_022_09. |
| OBJ_MQ022_010 | MQ_022 | 10 | Block immune child outbound data | Hack | LOC_CH022_SERVER_HALL | 1 | MQ_022_10. |
| OBJ_MQ022_011 | MQ_022 | 11 | Defeat cybernetic infected | Combat | ENM_CH022_CYBERNETIC_INFECTED | 1 | MQ_022_11. |
| OBJ_MQ022_012 | MQ_022 | 12 | Escape port | Escape | LOC_CH022_DEPARTURE | 1 | MQ_022_12. |
| OBJ_MQ022_013 | MQ_022 | 13 | Receive Tokyo relay signal | UnlockQuest | MQ_023 | 1 | MQ_022_13. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ022_01_001 | SQ_022_01 | Observe crane pattern and disable one lane | Safer yard crossing | SQ_TechPort_01. |
| OBJ_SQ022_02_001 | SQ_022_02 | Break camera line of sight and spoof biometric profile | Affects Architect tracking | SQ_TechPort_02. |
| OBJ_SQ022_03_001 | SQ_022_03 | Find manual override and stop corpse conveyor | More parts or more safety | SQ_TechPort_03. |
| OBJ_SQ022_04_001 | SQ_022_04 | Tune antenna and translate partial Japanese/English signal | Chapter 23 setup | SQ_TechPort_04. |
| OBJ_SQ022_05_001 | SQ_022_05 | Find engineer body, listen to log, check daycare | Mai/Binh morale; port humanization | SQ_TechPort_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ022_EARLY_ALARM | MQ_022 | Trigger port alarm early | Drones and cranes become more aggressive | Fail States section. |
| FAIL_MQ022_CONFIRM_BINH_ASSET | MQ_022 | Confirm Binh as asset | Cure Ethics and Family Trust damage; data may broadcast | Fail States section. |
| FAIL_MQ022_SKIP_SERVER | MQ_022 | Skip server hall | No Aster clue; weaker Chapter 23 hook | Fail States section. |
| FAIL_MQ022_FAIL_DATA_BLOCK | MQ_022 | Fail to block Binh outbound data | Architects get stronger lock on Binh | Fail States section. |
| FAIL_MQ022_EXCESSIVE_GUNS | MQ_022 | Use guns too much | Container horde released | Fail States section. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ022_NAV_MODULE | MQ_022 | item | ITM_CH022_NAVIGATION_MODULE | Rewards section. |
| REW_MQ022_PORT_DATA | MQ_022 | item | ITM_CH022_PORT_ARRAY_DATA | Rewards section. |
| REW_MQ022_EDENROT_PORT_CLASS | MQ_022 | lore | EDENROT CLASS: PORT ARRAY classification | Rewards section. |
| REW_MQ022_ARCHITECT_SIGNAL | MQ_022 | lore | Architect signal decoded | Rewards section. |
| REW_MQ022_ASTER_FORESHADOW | MQ_022 | lore | Architect Commander Aster named | Rewards section. |
| REW_MQ022_CYBERNETIC_CODEX | MQ_022 | system_unlock | Cybernetic infected codex | Rewards section. |
| REW_MQ022_TOKYO_ROUTE | MQ_022 | quest_unlock | Tokyo relay route | Rewards section. |
| REW_MQ022_VESSEL_UPGRADE | MQ_022 | item | Nha Di upgrade parts | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH022_CYBERNETIC_COMBAT | MQ_022 | Cybernetic infected combat | First exosuit infected defeated. |
| UNLOCK_CH022_HACKING_SYSTEMS | MQ_022 | Hacking and data objectives | Server hall decoded. |
| UNLOCK_CH022_BIOMETRIC_PRIVACY | MQ_022 | Biometric security mechanics | Binh data flagging encountered. |
| UNLOCK_CH022_MQ023_TOKYO | MQ_022 | Chapter 23 Tokyo mission | Tokyo relay signal received. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH022_PORT_ARRAY_DECODED | MQ_022 | Server hall data extracted. |
| FLAG_CH022_ARCHITECT_SIGNAL_DECODED | MQ_022 | Architect signal chain decoded. |
| FLAG_CH022_ASTER_NAMED | MQ_022 | Aster reference found in signal authority. |
| FLAG_CH022_BINH_DATA_FLAGGED | MQ_022 | Port AI flags Binh as biometric anomaly. |
| FLAG_CH022_BINH_DATA_OUTBOUND_BLOCKED | MQ_022 | Hoang blocks outbound transmission. |
| FLAG_CH022_TOKYO_RELAY_SIGNAL_RECEIVED | MQ_022 | Tokyo relay signal received on departure. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_022_01 | Port Still Running | environmental | Observe crane pattern, disable lane, avoid forklift, retrieve manifest | Safer yard crossing | SQ_TechPort_01. |
| SQ_022_02 | Camera Eyes Watching Binh | environmental | Break line of sight, spoof profile, refuse asset confirmation, purge cache | Affects Architect tracking | SQ_TechPort_02. |
| SQ_022_03 | Robots Don't Know The Dead | environmental | Find manual override, stop corpse conveyor, free trapped body/log | More parts or more safety | SQ_TechPort_03. |
| SQ_022_04 | Japanese Signal | environmental | Tune antenna, translate signal, identify naval code request, decide response | Chapter 23 setup | SQ_TechPort_04. |
| SQ_022_05 | Engineer's Oath | environmental | Find engineer body, listen to log, check daycare, leave memorial | Mai/Binh morale; port humanization | SQ_TechPort_05. |

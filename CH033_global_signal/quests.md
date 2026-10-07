# Quests - CH033

Metadata:

- chapterID: CH033
- sourceFilename: chapter_033_tin_hieu_toan_cau.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_033 | Broadcast Rebirth | main | npc_thu | NORAD satellite window opens after CH032 bunker assault | Rebirth signal transmitted and global responses archived | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ033_001 | MQ_033 | 1 | Stabilize global signal window. | Interact | LOC_CH033_SATELLITE_RELAY | 1 | Main Quest objective 1. |
| OBJ_MQ033_002 | MQ_033 | 2 | Convene broadcast council. | TalkTo | LOC_CH033_INTAKE_TUNNEL | 1 | Main Quest objective 2. |
| OBJ_MQ033_003 | MQ_033 | 3 | Classify EDENROT global coordination signal. | Interact | LOC_CH033_NORAD_CONTROL | 1 | Main Quest objective 3. |
| OBJ_MQ033_004 | MQ_033 | 4 | Build message priority list. | Interact | LOC_CH033_PUBLIC_LEDGER | 1 | Main Quest objective 4. |
| OBJ_MQ033_005 | MQ_033 | 5 | Draft Rebirth promise. | Interact | LOC_CH033_QUIET_ROOM | 1 | Main Quest objective 5. |
| OBJ_MQ033_006 | MQ_033 | 6 | Translate broadcast packet. | Interact | LOC_CH033_TRANSLATION_CORNER | 1 | Main Quest objective 6. |
| OBJ_MQ033_007 | MQ_033 | 7 | Remove immune child sensitive data. | Interact | LOC_CH033_TRANSLATION_CORNER | 1 | Main Quest objective 7. |
| OBJ_MQ033_008 | MQ_033 | 8 | Classify weak incoming signals. | Interact | LOC_CH033_LISTEN_DECK | 1 | Main Quest objective 8. |
| OBJ_MQ033_009 | MQ_033 | 9 | Strip location metadata. | Interact | LOC_CH033_SATELLITE_RELAY | 1 | Main Quest objective 9. |
| OBJ_MQ033_010 | MQ_033 | 10 | Block Architect listener injection. | Interact | LOC_CH033_SATELLITE_RELAY | 1 | Main Quest objective 10. |
| OBJ_MQ033_011 | MQ_033 | 11 | Set promise signal non-command. | Interact | LOC_CH033_NORAD_CONTROL | 1 | Main Quest objective 11. |
| OBJ_MQ033_012 | MQ_033 | 12 | Record final broadcast. | Interact | LOC_CH033_BROADCAST_ROOM | 1 | Main Quest objective 12. |
| OBJ_MQ033_013 | MQ_033 | 13 | Transmit Rebirth signal. | Interact | LOC_CH033_BROADCAST_ROOM | 1 | Main Quest objective 13. |
| OBJ_MQ033_014 | MQ_033 | 14 | Archive global responses. | Interact | LOC_CH033_NORAD_CONTROL | 1 | Main Quest objective 14. |
| OBJ_MQ033_015 | MQ_033 | 15 | Detect Hoang weak ping. | Interact | LOC_CH033_LISTEN_DECK | 1 | Main Quest objective 15. |
| OBJ_MQ033_016 | MQ_033 | 16 | Capture terraforming map fragment. | Interact | LOC_CH033_NORAD_CONTROL | 1 | Main Quest objective 16. |
| OBJ_MQ033_017 | MQ_033 | 17 | Unlock next front decision. | UnlockQuest | MQ_034 | 1 | Main Quest objective 17. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ033_01_001 | SQ_033_01 | Hear all faction proposals and remove claims of ownership. | BroadcastCouncilLegitimacy. | SQ_Broadcast_01. |
| OBJ_SQ033_02_001 | SQ_033_02 | Gather multilingual survivors and record short variants. | MultilingualBroadcastPacket. | SQ_Broadcast_02. |
| OBJ_SQ033_03_001 | SQ_033_03 | Compare signal history and identify false lures. | SignalMapReliable. | SQ_Broadcast_03. |
| OBJ_SQ033_04_001 | SQ_033_04 | Capture terraforming map frames and decode zone names. | TerraformingMapFragment. | SQ_Broadcast_04. |
| OBJ_SQ033_05_001 | SQ_033_05 | Strip metadata and block injection phrase from Architect listener. | ArchitectListenerConfirmed. | SQ_Broadcast_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ033_VALE_METADATA | MQ_033 | VALE gains targeting metadata. | Broadcast becomes tracking payload. | Failure Conditions. |
| FAIL_MQ033_BINH_EXPOSED | MQ_033 | Broadcast exposes Binh/immune children. | Severe child danger. | Failure Conditions. |
| FAIL_MQ033_PROPAGANDA | MQ_033 | Message becomes faction propaganda. | Global trust drops. | Failure Conditions. |
| FAIL_MQ033_FALSE_SIGNAL | MQ_033 | False signal corrupts map. | Unreliable signal map. | Failure Conditions. |
| FAIL_MQ033_SATELLITE_COLLAPSE | MQ_033 | Satellite safe mode collapses before transmission. | Broadcast fails. | Failure Conditions. |
| FAIL_MQ033_ARCHITECT_INJECTION | MQ_033 | Architect injection replaces Rebirth message. | Message corrupted. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ033_GLOBAL_ALLIES | MQ_033 | network_unlock | Global ally network | Completion Rewards. |
| REW_MQ033_SIGNAL_MAP | MQ_033 | item | World signal map | Completion Rewards. |
| REW_MQ033_TERRAFORM_MAP | MQ_033 | item | Architect terraforming map fragment | Completion Rewards. |
| REW_MQ033_CH34_FRONT | MQ_033 | quest_unlock | Chapter 34 front selection | Completion Rewards. |
| REW_MQ033_BROADCAST_REP | MQ_033 | reputation | Broadcast reputation | Completion Rewards. |
| REW_MQ033_MULTILINGUAL | MQ_033 | item | Multilingual warning packet | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH033_GLOBAL_NETWORK | MQ_033 | Global ally network | Broadcast transmitted. |
| UNLOCK_CH033_SIGNAL_MAP | MQ_033 | World signal map | Responses archived. |
| UNLOCK_CH033_CH34_FRONT | MQ_033 | Next front decision | Terraforming map captured. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH033_REBIRTH_SIGNAL_TRANSMITTED | MQ_033 | Broadcast transmitted successfully. |
| FLAG_CH033_GLOBAL_ALLIES_SEED | MQ_033 | World responses received. |
| FLAG_CH033_TERRAFORMING_MAP_FRAGMENT | MQ_033 | Architect map captured. |
| FLAG_CH033_CH34_FRONT_DECISION_UNLOCKED | MQ_033 | Next front selection available. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_033_01 | Who Speaks | npc_mai | Hear faction proposals, remove ownership claims. | BroadcastCouncilLegitimacy. | SQ_Broadcast_01. |
| SQ_033_02 | Translate the Promise | npc_mai | Gather multilingual survivors, record variants. | MultilingualBroadcastPacket. | SQ_Broadcast_02. |
| SQ_033_03 | Weak Signals | npc_thu | Classify incoming signals, identify false lures. | SignalMapReliable. | SQ_Broadcast_03. |
| SQ_033_04 | Terraforming Map | npc_doctor | Capture map frames, decode zone names, find Patient Zero clue. | TerraformingMapFragment. | SQ_Broadcast_04. |
| SQ_033_05 | The Listener | npc_thu | Strip metadata, air-gap VALE core, block injection. | ArchitectListenerConfirmed. | SQ_Broadcast_05. |

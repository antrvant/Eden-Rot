# Quests - CH048

Metadata:

- chapterID: CH048
- sourceFilename: chapter_048_bien_bang_cuoi_cung.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_048 | Reach Antarctica | main | char_trung | Act 8 begins after CH047 alliance assembly | Fleet reaches Antarctica ice shelf, long-range comms lost, proceed under ice message received | Metadata and Main Quest. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ048_01 | MQ_048 | 1 | Draft the voluntary alliance call as a request, not a command. | Choice | LOC_CH048_COMMAND_RAFT | 1 | Scene 1. |
| OBJ_MQ048_02 | MQ_048 | 2 | Broadcast the countdown without exposing child data. | Broadcast | LOC_CH048_COMMAND_RAFT | 1 | Scene 1. |
| OBJ_MQ048_03 | MQ_048 | 3 | Restate NoChildAsCurrency before fleet roles are assigned. | Dialogue | char_mai | 1 | Scene 1. |
| OBJ_MQ048_04 | MQ_048 | 4 | Receive allied frequency responses. | WaitEvent | LOC_CH048_FLEET_BRIDGE | 1 | Scene 2. |
| OBJ_MQ048_05 | MQ_048 | 5 | Assign fleet roles based on trust. | Management | LOC_CH048_FLEET_BRIDGE | 1 | Scene 2. |
| OBJ_MQ048_06 | MQ_048 | 6 | Configure Guardian Circle ship pods for children. | Choice | LOC_CH048_GUARDIAN_DECK | 1 | Scene 3. |
| OBJ_MQ048_07 | MQ_048 | 7 | Stabilize Hoang cold hold pod. | Check | LOC_CH048_COLD_HOLD | 1 | Scene 4. |
| OBJ_MQ048_08 | MQ_048 | 8 | Navigate the first ice field. | Navigation | LOC_CH048_SOUTHERN_OCEAN | 1 | Scene 5. |
| OBJ_MQ048_09 | MQ_048 | 9 | Resolve repair resource dispute for child food ship. | Choice | LOC_CH048_MERCHANT_SHIP_4 | 1 | Scene 5. |
| OBJ_MQ048_10 | MQ_048 | 10 | Debrief Source dreams with consent only. | Dialogue | LOC_CH048_SOURCE_DREAM_CHAMBER | 1 | Scene 6. |
| OBJ_MQ048_11 | MQ_048 | 11 | Classify Source dream data as consent-bound testimony. | System | char_mai | 1 | Scene 6. |
| OBJ_MQ048_12 | MQ_048 | 12 | Investigate the fleet leak without collective child search. | Investigation | LOC_CH048_OPEN_CHANNEL | 1 | Scene 7. |
| OBJ_MQ048_13 | MQ_048 | 13 | Rescue the ice-trapped ally vessel Saint Lark. | Action | LOC_CH048_ICE_RESCUE_SITE | 1 | Scene 8. |
| OBJ_MQ048_14 | MQ_048 | 14 | Stabilize the aurora static event. | Survival | LOC_CH048_AURORA_ZONE | 1 | Scene 9. |
| OBJ_MQ048_15 | MQ_048 | 15 | Survive whiteout navigation using distributed trust. | Navigation | LOC_CH048_WHITEOUT_ZONE | 1 | Scene 10. |
| OBJ_MQ048_16 | MQ_048 | 16 | Reach Antarctica ice shelf. | Arrival | LOC_CH048_ICE_SHELF_APPROACH | 1 | Scene 11. |
| OBJ_MQ048_17 | MQ_048 | 17 | Lose long-range communications. | Event | LOC_CH048_LOCAL_COMM_AREA | 1 | Scene 12. |
| OBJ_MQ048_18 | MQ_048 | 18 | Receive proceed under ice message and unlock Chapter 49. | Unlock | LOC_CH048_LOCAL_COMM_AREA | 1 | Scene 12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ048_A_001 | SQ_048_A | Spend bandwidth trying to reach the silent ally frequency. | Signal returns late with damaged vessel or remains silent. | SQ_048_A. |
| OBJ_SQ048_B_001 | SQ_048_B | Build a rope-loop evacuation route Rafi can use without touch. | RafiWhiteoutSafe = true. | SQ_048_B. |
| OBJ_SQ048_C_001 | SQ_048_C | Help Luz identify trader slang in the fleet leak. | FleetLeakContained = true. | SQ_048_C. |
| OBJ_SQ048_D_001 | SQ_048_D | Give Hoang one honest update when he wakes. | HoangStillIncluded = true. | SQ_048_D. |
| OBJ_SQ048_E_001 | SQ_048_E | Adapt Mateo tap code into ship hull communication system. | DistributedTrustProtocol = high. | SQ_048_E. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ048_BROADCAST_EXPOSES_CHILDREN | MQ_048 | Broadcast includes child data. | Alliance trust reduced; child safety compromised. | Scene 1. |
| FAIL_MQ048_CHILDREN_IN_CARGO_DECK | MQ_048 | Children placed in secure cargo deck. | Guardian Circle fails at sea; child trust damaged. | Scene 3. |
| FAIL_MQ048_FORCED_DREAM_SCAN | MQ_048 | Source dreams scanned without consent. | Child trust damaged; consent-bound data corrupted. | Scene 6. |
| FAIL_MQ048_COLLECTIVE_CHILD_SEARCH | MQ_048 | All children searched due to leak. | Guardian Circle damaged; Rafi trust broken. | Scene 7. |
| FAIL_MQ048_ICE_VESSEL_ABANDONED | MQ_048 | Saint Lark abandoned to save fuel. | Final alliance trust lowered. | Scene 8. |
| FAIL_MQ048_WHITEOUT_SCATTER | MQ_048 | Fleet scattered beyond recovery in whiteout. | Reduced reinforcements for Act 8. | Scene 10. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ048_FINAL_ALLIANCE_FLEET | MQ_048 | system_unlock | Combined faction fleet support | Scene 2. |
| REW_MQ048_GUARDIAN_CIRCLE_AT_SEA | MQ_048 | system_unlock | Child rights under travel stress | Scene 3. |
| REW_MQ048_SOURCE_DREAMS | MQ_048 | system_unlock | Pre-Source resonance warning | Scene 6. |
| REW_MQ048_DISTRIBUTED_TRUST_PROTOCOL | MQ_048 | system_unlock | Whiteout fallback command | Scene 10. |
| REW_MQ048_ANTARCTICA_SOURCE_APPROACH | MQ_048 | system_unlock | Chapter 49 entry | Scene 12. |
| REW_MQ048_MATEO_HULL_CODE | MQ_048 | item | ITM_CH048_MATEO_HULL_CODE_SYSTEM | SQ_048_E. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH048_ACT8 | MQ_048 | Act 8 begins | Chapter starts. |
| UNLOCK_CH048_FLEET_SYSTEM | MQ_048 | Final Alliance Fleet system | Frequencies answer. |
| UNLOCK_CH048_GUARDIAN_SEA | MQ_048 | Guardian Circle at sea | Pods configured. |
| UNLOCK_CH048_SOURCE_DREAMS | MQ_048 | Source dream system | Dreams occur at 03:12. |
| UNLOCK_CH048_DISTRIBUTED_TRUST | MQ_048 | Distributed trust protocol | Whiteout survival. |
| UNLOCK_CH048_CH049 | MQ_048 | Chapter 49 Terraforming Source | Proceed under ice message. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH048_ACT8_STARTED | MQ_048 | Chapter opens. |
| FLAG_CH048_VOLUNTARY_ALLIANCE_CALL_SENT | MQ_048 | Broadcast sent as request. |
| FLAG_CH048_GUARDIAN_CIRCLE_AT_SEA_ACTIVE | MQ_048 | Mixed pods configured. |
| FLAG_CH048_SOURCE_DREAM_DATA_CONSENT_BOUND | MQ_048 | Dreams debriefed with consent. |
| FLAG_CH048_COVENANT_FLEET_STRESS_TEST_PASSED_PARTIAL | MQ_048 | Whiteout survived with distributed trust. |
| FLAG_CH048_ANTARCTICA_ICE_SHELF_REACHED | MQ_048 | Fleet arrives at ice shelf. |
| FLAG_CH048_CH49_TERRAFORMING_SOURCE_UNLOCKED | MQ_048 | Proceed under ice message received. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_048_A | The Frequency That Does Not Answer | npc_radio_operator | Spend bandwidth trying silent ally frequency. | Late vessel arrival or emotional cost. | SQ_048_A. |
| SQ_048_B | Rafi's Drill | npc_rafi | Build rope-loop route Rafi can use without touch. | RafiWhiteoutSafe flag. | SQ_048_B. |
| SQ_048_C | Luz Finds The Leak | npc_luz | Help Luz identify trader slang in leak. | FleetLeakContained flag. | SQ_048_C. |
| SQ_048_D | Hoang's Cold Minute | comp_hoang | Give Hoang one honest update. | HoangStillIncluded flag. | SQ_048_D. |
| SQ_048_E | Mateo Hull Code | npc_mateo | Adapt tap code for hull communication. | DistributedTrustProtocol high. | SQ_048_E. |

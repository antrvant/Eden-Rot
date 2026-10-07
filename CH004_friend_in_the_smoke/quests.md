# Quests - CH004

Metadata:

- chapterID: CH004
- sourceFilename: chapter_004_ban_than_trong_khoi_lua.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_004 | Reunite Hoang | main | automatic | Starts after MQ_003 when Trung leaves the apartment through the north/back alley | Hoang joins as companion and both leave by motorbike toward the northern checkpoint | Metadata lists MQ_004 - Reunite Hoang; Main Quest section gives premise and objectives. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ004_001 | MQ_004 | 1 | Leave the apartment complex through the back exit. | GoTo | LOC_CH004_NORTH_BACK_ALLEY | 1 | Main Quest objective 1. |
| OBJ_MQ004_002 | MQ_004 | 2 | Follow Mai's chalk trail through the northern alley. | Track | ITM_CH004_DEGRADED_CHALK_MARK | 1 | Main Quest objective 2 and Scene 1. |
| OBJ_MQ004_003 | MQ_004 | 3 | Confront the fake guide group. | SocialCheck | npc_fake_guide_leader | 1 | Main Quest objective 3. |
| OBJ_MQ004_004 | MQ_004 | 4 | Survive the Runner in the burning alley. | Survive | ENM_CH004_FIRST_RUNNER | 1 | Main Quest objective 4. |
| OBJ_MQ004_005 | MQ_004 | 5 | Reunite with Hoang. | CompanionIntro | comp_hoang | 1 | Main Quest objective 5. |
| OBJ_MQ004_006 | MQ_004 | 6 | Reach the traffic camera station. | GoTo | LOC_CH004_TRAFFIC_CAMERA_STATION | 1 | Main Quest objective 6. |
| OBJ_MQ004_007 | MQ_004 | 7 | Restart the camera terminal and search for Mai and Binh. | HackPuzzle | ITM_CH004_TRAFFIC_CAMERA_TERMINAL | 1 | Main Quest objective 7. |
| OBJ_MQ004_008 | MQ_004 | 8 | Choose how to handle the trapped survivor group. | MoralChoice | npc_trapped_survivor_leader | 1 | Main Quest objective 8. |
| OBJ_MQ004_009 | MQ_004 | 9 | Escape the burning district on Hoang's motorbike. | Escape | ITM_CH004_HOANG_MOTORBIKE | 1 | Main Quest objective 9. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ004_01_001 | SQ_004_01 | Read old messages between Trung and Hoang. | Unlocks a warm friend dialogue line and adds depth to Hoang. | SQ_Hoang_01. |
| OBJ_SQ004_02_001 | SQ_004_02 | Retrieve the traffic server drive or UPS from the station. | Unlocks later shortcut or safe-zone-fraud information. | SQ_Hoang_02. |
| OBJ_SQ004_02_002 | SQ_004_02 | Clear or avoid infected trapped near the server room. | Allows safer terminal access. | SQ_Hoang_02 risk. |
| OBJ_SQ004_03_001 | SQ_004_03 | Return upstairs and open the room holding trapped survivors. | Compassion +1 and HoangSecret reveal if discovered. | SQ_Hoang_03. |
| OBJ_SQ004_03_002 | SQ_004_03 | Leave directions or supplies for the trapped group. | Balanced +1; deferred outcome. | DT_011 Choice C. |
| OBJ_SQ004_04_001 | SQ_004_04 | Expose the fake guide route scam. | Can recover stolen supplies for victims. | SQ_Hoang_04. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ004_HEALTH_ZERO | MQ_004 | Trung dies to Runner, infected, fire, or looters. | Reload checkpoint. | Gameplay beats include combat/chase. |
| FAIL_MQ004_RUNNER_CATCH | MQ_004 | Player fails Runner dodge/sprint sequence before Hoang rescue trigger. | Reload chase checkpoint or trigger injury state. | Scene 3. |
| FAIL_MQ004_CAMERA_POWER | MQ_004 | Player cannot restore power to camera terminal. | Main quest blocked until UPS/cable puzzle is solved. | Scene 5. |
| FAIL_SQ004_03_SURVIVORS_LOST | SQ_004_03 | Player leaves or delays too long while trapped group is threatened. | Sets abandonment/guilt/Hoang secret state. | Scene 6. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ004_HOANG_COMPANION | MQ_004 | companion_join | comp_hoang | Rewards section. |
| REW_MQ004_CAMERA_ROUTE_HINT | MQ_004 | system_unlock | Camera Route Hint | Rewards section. |
| REW_MQ004_TRUST_HOANG | MQ_004 | relationship_unlock | TrustHoang | Rewards section. |
| REW_MQ004_NORTH_CHECKPOINT | MQ_004 | destination_unlock | Northern checkpoint | Rewards section. |
| REW_MQ004_COMPASSION | MQ_004 | moral_flag | Compassion +1 if trapped survivors are rescued | Rewards section. |
| REW_MQ004_PRAGMATISM | MQ_004 | moral_flag | Pragmatism +1 if player leaves immediately | Rewards section. |
| REW_MQ004_BALANCED | MQ_004 | moral_flag | Balanced +1 if player leaves directions/supplies | Rewards section. |
| REW_MQ004_HOANG_SECRET | MQ_004 | relationship_flag | HoangSecret +1 if his broken promise is discovered | Rewards section and Scene 6. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH004_DEGRADED_TRACKING | MQ_004 | Tracking with degraded clues | Follow smoke-damaged chalk. |
| UNLOCK_CH004_SOCIAL_SUSPICION | MQ_004 | Social suspicion/dialogue check | Confront fake guides. |
| UNLOCK_CH004_MIXED_COMBAT | MQ_004 | Human + infected combat | Fight fake guides/looters while infected close in. |
| UNLOCK_CH004_RUNNER_CHASE | MQ_004 | Runner chase upgrade | First Runner encounter. |
| UNLOCK_CH004_COMPANION_HOANG | MQ_004 | Companion intro | Hoang rescues Trung. |
| UNLOCK_CH004_CAMERA_TERMINAL | MQ_004 | Camera terminal puzzle | Restore traffic camera access. |
| UNLOCK_CH004_TWO_PERSON_BIKE | MQ_004 | Two-person bike escape | Leave on Hoang's motorbike. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH004_HOANG_JOINED | MQ_004 | Hoang joins at the end of the chapter. |
| FLAG_CH004_MAI_BINH_CAMERA_CONFIRMED | MQ_004 | Traffic camera shows Mai/Binh near checkpoint route. |
| FLAG_CH004_YELLOW_TRUCK_SEEN | MQ_004 | Camera shows a yellow rescue truck near Mai/Binh's group. |
| FLAG_CH004_HOANG_SECRET_REVEALED | MQ_004 | Player discovers Hoang previously promised to return for trapped survivors. |
| FLAG_CH004_INNER_CIRCLE_DEFINED | MQ_004 | Hoang states his inner-circle philosophy. |
| FLAG_CH004_NORTH_CHECKPOINT_DESTINATION_UNLOCKED | MQ_004 | Chapter ends with checkpoint as next destination. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_004_01 | Old Messages | automatic | Read old messages between Trung and Hoang while phone is charged or checked. | Adds warmth to friendship and unlocks familiar banter. | SQ_Hoang_01. |
| SQ_004_02 | Traffic Server | comp_hoang | Retrieve server drive/UPS from traffic camera station. | May unlock Chapter 05 shortcut or safe-zone-fraud info. | SQ_Hoang_02. |
| SQ_004_03 | The Group Left Behind | trapped survivor voices | Rescue, abandon, or aid the survivor group Hoang promised to return for. | May create later witnesses for or against Hoang. | SQ_Hoang_03. |
| SQ_004_04 | Fake Guides | fake guide group | Discover and expose the fake safe-route scam. | Recover stolen goods and reinforce fake safety motif for Chapter 05. | SQ_Hoang_04. |

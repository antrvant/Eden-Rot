# Quests - CH050

Metadata:

- chapterID: CH050
- sourceFilename: chapter_050_rebirth_warrior.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_050 | Final Choice | main | char_trung | CH049 completed, final battlefield triggered | Final choice selected, ending executed, EDENROT completed | Metadata and Main Quest. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ050_01 | MQ_050 | 1 | Stabilize the final battlefield around Binh. | Survival | LOC_CH050_FINAL_BATTLEFIELD | 1 | Scene 1. |
| OBJ_MQ050_02 | MQ_050 | 2 | Prevent Prime from using Binh's connection. | Block | npc_prime | 1 | Scene 1. |
| OBJ_MQ050_03 | MQ_050 | 3 | Reject bridge data taken during violation. | Choice | LOC_CH050_CHOICE_CONSOLE | 1 | Scene 1. |
| OBJ_MQ050_04 | MQ_050 | 4 | Survive Apex Predator birth. | Combat | npc_apex | 1 | Scene 2. |
| OBJ_MQ050_05 | MQ_050 | 5 | Reconnect local alliance voices. | Event | LOC_CH050_ICE_TUNNEL_BATTLEFIELD | 1 | Scene 3. |
| OBJ_MQ050_06 | MQ_050 | 6 | Counter Apex phase one patterns. | Combat | npc_apex | 1 | Scene 4. |
| OBJ_MQ050_07 | MQ_050 | 7 | Reject Prime's final argument. | Dialogue | npc_prime | 1 | Scene 5. |
| OBJ_MQ050_08 | MQ_050 | 8 | Resolve Hoang's final intervention. | Choice | comp_hoang | 1 | Scene 6. |
| OBJ_MQ050_09 | MQ_050 | 9 | Protect the final choice console. | Combat | npc_apex | 1 | Scene 7. |
| OBJ_MQ050_10 | MQ_050 | 10 | Evaluate the ending matrix. | System | LOC_CH050_CHOICE_CONSOLE | 1 | Scene 8. |
| OBJ_MQ050_11 | MQ_050 | 11 | Verify humane rewrite prerequisites. | System | LOC_CH050_CHOICE_CONSOLE | 1 | Scene 8. |
| OBJ_MQ050_12 | MQ_050 | 12 | Select destroy, reset, rewrite, or hybrid. | Choice | LOC_CH050_CHOICE_CONSOLE | 1 | Scene 8. |
| OBJ_MQ050_13 | MQ_050 | 13 | Execute the chosen ending. | Event | LOC_CH050_CORE_CATHEDRAL | 1 | Scene 9. |
| OBJ_MQ050_14 | MQ_050 | 14 | Free or lose Binh according to flags. | Event | char_binh | 1 | Scene 10. |
| OBJ_MQ050_15 | MQ_050 | 15 | Resolve Source and Eden Strain. | Event | LOC_CH050_CORE_CATHEDRAL | 1 | Scene 10. |
| OBJ_MQ050_16 | MQ_050 | 16 | Establish Edenrot warning doctrine. | Lore | char_mai | 1 | Scene 9. |
| OBJ_MQ050_17 | MQ_050 | 17 | Play faction and companion epilogues. | Epilogue | LOC_CH050_EPILOGUE_SETTLEMENT | 1 | Scene 11. |
| OBJ_MQ050_18 | MQ_050 | 18 | Close the family arc. | Epilogue | LOC_CH050_EPILOGUE_MEAL_HALL | 1 | Scene 12. |
| OBJ_MQ050_19 | MQ_050 | 19 | Complete EDENROT. | Event | LOC_CH050_EPILOGUE_MEAL_HALL | 1 | Scene 12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ050_A_001 | SQ_050_A | Use family code and green reflection against Apex memory patterns. | Apex phase one countered faster. | Scene 4. |
| OBJ_SQ050_B_001 | SQ_050_B | Allow Hoang to jam Apex sync under restraint protocol. | HoangFinalIntervention resolved; Apex shield disabled. | Scene 6. |
| OBJ_SQ050_C_001 | SQ_050_C | Detect and delete assumed consent clause from rewrite contract. | Rewrite contract cleaned; humane path secured. | Scene 7. |
| OBJ_SQ050_D_001 | SQ_050_D | Pass Mentor's line to Binh. | MentorLinePassedOn flag. | Scene 12. |
| OBJ_SQ050_E_001 | SQ_050_E | Place soup bowl for Hoang at final meal. | Hoang integration in epilogue. | Scene 12. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ050_BINH_PERMANENT_AMPLIFIER | MQ_050 | Player uses Binh as permanent amplifier. | Bad ending branch. | Scene 8. |
| FAIL_MQ050_CHILDREN_SACRIFICED | MQ_050 | Player sacrifices children anchors. | Guardian Circle fails; bad ending. | Scene 7. |
| FAIL_MQ050_PRIME_AUTO_RESET | MQ_050 | Player lets Prime auto-select reset. | Architect Control ending. | Scene 8. |
| FAIL_MQ050_SOURCE_DESTROYED_WITH_BINH | MQ_050 | Source destroyed before Binh disconnected (unless Family First route). | Binh lost. | Scene 10. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ050_FINAL_CHOICE_MATRIX | MQ_050 | system_unlock | Destroy/Reset/Rewrite/Hybrid conditions | Scene 8. |
| REW_MQ050_EDENROT_HUMAN_COVENANT_REWRITE | MQ_050 | system_unlock | Final consent-based Source rewrite doctrine | Scene 9. |
| REW_MQ050_EDENROT_WARNING_DOCTRINE | MQ_050 | system_unlock | Survivor warning label for repair becoming ownership | Scene 9. |
| REW_MQ050_SOURCE_CORE | MQ_050 | system_unlock | Final battlefield environment | Scene 1. |
| REW_MQ050_BINH_TRUST_CHECK | MQ_050 | system_unlock | Ending condition | Scene 10. |
| REW_MQ050_APEX_PREDATOR | MQ_050 | system_unlock | Final adaptive guardian encounter | Scene 2. |
| REW_MQ050_POST_EDENROT_EPILOGUE | MQ_050 | system_unlock | Cure clinics, Guardian Circle, ordinary-life closure | Scene 11, 12. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH050_FINAL_BATTLEFIELD | MQ_050 | Final battlefield | Chapter begins. |
| UNLOCK_CH050_APEX_FIGHT | MQ_050 | Apex Predator encounter | Apex born. |
| UNLOCK_CH050_CHOICE_MATRIX | MQ_050 | Final choice system | Console stabilized. |
| UNLOCK_CH050_ENDINGS | MQ_050 | Ending branches | Choice selected. |
| UNLOCK_CH050_EPILOGUE | MQ_050 | Epilogue montage | Ending executed. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH050_FINAL_CHOICE_SELECTED | MQ_050 | Player selects ending. |
| FLAG_CH050_ENDING_REBIRTH_HYBRID | MQ_050 | Hybrid Rebirth Rewrite selected with all conditions met. |
| FLAG_CH050_ENDING_FAMILY_FIRST | MQ_050 | Family First ending selected. |
| FLAG_CH050_ENDING_IRON_REBIRTH | MQ_050 | Iron Rebirth ending selected. |
| FLAG_CH050_ENDING_BROKEN_CURE | MQ_050 | Broken Cure ending selected. |
| FLAG_CH050_ENDING_ARCHITECT_CONTROL | MQ_050 | Architect Control ending selected. |
| FLAG_CH050_ENDING_ASH | MQ_050 | Ash ending selected. |
| FLAG_CH050_EDENROT_WARNING_DOCTRINE_ESTABLISHED | MQ_050 | Edenrot becomes in-world warning term. |
| FLAG_CH050_EDENROT_COMPLETED | MQ_050 | Story completed. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_050_A | Survival Memory | gameplay | Use learned counter-patterns against Apex. | Faster phase one victory. | Scene 4. |
| SQ_050_B | Hoang's Last Refusal | comp_hoang | Allow Hoang to jam Apex sync under protocol. | Hoang redemption act; Apex shield down. | Scene 6. |
| SQ_050_C | Line Seven Is A Cage | npc_luz | Detect and delete assumed consent clause. | Rewrite contract cleaned. | Scene 7. |
| SQ_050_D | Mentor's Line | char_trung | Pass Mentor's running line to Binh. | MentorLinePassedOn flag. | Scene 12. |
| SQ_050_E | The Bowl At The Door | char_binh | Place soup bowl for Hoang at final meal. | Hoang integration without forced forgiveness. | Scene 12. |

# Quests - CH002

Metadata:

- chapterID: CH002
- sourceFilename: chapter_002_thanh_pho_khong_con_den_do.md
- language: English

## Main Quest

| questID | questName | questType | giver | description | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_002 | Reach Home | main | automatic | Cross a collapsing Saigon and reach apartment 1208 before the last phone signal disappears. Every stranger on the route tests whether Trung chooses family, compassion, or survival. | Starts after MQ_001 when Trung escapes the office building | Trung reaches apartment 1208 and finds Mai's fridge note and chalk trail clue | Metadata lists Main Quest: MQ_002 - Reach Home; Main Quest section gives premise and objectives. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ002_001 | MQ_002 | 1 | Escape the basement parking level. | Escape | LOC_CH002_COMPANY_BASEMENT | 1 | Main Quest objective 1. |
| OBJ_MQ002_002 | MQ_002 | 2 | Find a vehicle or a route home on foot. | RouteChoice | LOC_CH002_COMPANY_BASEMENT | 1 | Main Quest objective 2 and SQ_Street_03. |
| OBJ_MQ002_003 | MQ_002 | 3 | Cross the blocked city intersection. | Traverse | LOC_CH002_SAIGON_INTERSECTION | 1 | Main Quest objective 3. |
| OBJ_MQ002_004 | MQ_002 | 4 | Gather water, bandages, and a power bank. | Scavenge | LOC_CH002_CONVENIENCE_STORE | 3 | Main Quest objective 4. |
| OBJ_MQ002_005 | MQ_002 | 5 | Answer Hoang's call and choose a route. | DialogueChoice | comp_hoang | 1 | Main Quest objective 5 and SQ_Street_04. |
| OBJ_MQ002_006 | MQ_002 | 6 | Decide whether to help the mother searching for her child. | MoralChoice | npc_lost_mother | 1 | Main Quest objective 6 and SQ_Street_01. |
| OBJ_MQ002_007 | MQ_002 | 7 | Reach Trung's apartment building. | GoTo | LOC_CH002_TRUNG_APARTMENT_BUILDING | 1 | Main Quest objective 7. |
| OBJ_MQ002_008 | MQ_002 | 8 | Search the family apartment. | Investigate | LOC_CH002_TRUNG_APARTMENT_1208 | 1 | Main Quest objective 8. |
| OBJ_MQ002_009 | MQ_002 | 9 | Read Mai's note and identify the chalk trail lead. | Inspect | ITM_CH002_FRIDGE_NOTE | 1 | Chapter ending and Continuity Notes. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ002_01_001 | SQ_002_01 | Search the overturned school bus for Nhi. | Unlocks rescue route and Compassion +1. | SQ_Street_01. |
| OBJ_SQ002_01_002 | SQ_002_01 | Return Nhi to her mother. | May allow mother/Nhi to reappear at a safe zone later. | SQ_Street_01 reward. |
| OBJ_SQ002_02_001 | SQ_002_02 | Trade water, jewelry, or valuables for gasoline. | May obtain gasoline but risk being cheated. | SQ_Street_02. |
| OBJ_SQ002_02_002 | SQ_002_02 | Check whether the gasoline is diluted. | Avoids vehicle failure in the street. | SQ_Street_02 twist. |
| OBJ_SQ002_03_001 | SQ_002_03 | Search for Trung's car key or identify who took it. | Determines whether vehicle route remains viable. | SQ_Street_03. |
| OBJ_SQ002_03_002 | SQ_002_03 | Choose force, trade, or abandonment for the locked car problem. | Sets personality/moral flags. | SQ_Street_03 choice. |
| OBJ_SQ002_04_001 | SQ_002_04 | Listen to Hoang's route advice. | Unlocks route hint and Hoang contact. | SQ_Street_04. |
| OBJ_SQ002_04_002 | SQ_002_04 | Choose alley shortcut or main road. | Sets TrustHoang or cautious route flags. | SQ_Street_04 choice. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ002_HEALTH_ZERO | MQ_002 | Trung dies during street traversal, infected attack, or human hazard. | Reload checkpoint. | Gameplay beats include chase, traversal, and moral events. |
| FAIL_MQ002_PHONE_DEAD | MQ_002 | Phone battery reaches zero before route calls/clues are received. | Hoang/Mai phone content requires alternate delivery. | Scene 3 and 4 stress battery/power bank. |
| FAIL_SQ002_01_NHI_LOST | SQ_002_01 | Player leaves or timer expires before rescuing Nhi. | Sets Guilt +1 and Nhi unresolved/abandoned. | SQ_Street_01 failure/skip. |
| FAIL_SQ002_02_DILUTED_GAS | SQ_002_02 | Player uses untested diluted gasoline. | Vehicle stalls in the street. | SQ_Street_02 twist. |
| FAIL_SQ002_03_CAR_ROUTE_LOST | SQ_002_03 | Player fails to recover key or loses the vehicle. | Must continue on foot. | Scene 1 and SQ_Street_03. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ002_STREET_NAVIGATION | MQ_002 | system_unlock | Street navigation | Rewards section. |
| REW_MQ002_SCAVENGING | MQ_002 | system_unlock | Basic scavenging | Rewards section. |
| REW_MQ002_HOANG_CONTACT | MQ_002 | phone_contact | Hoang | Rewards section and SQ_Street_04. |
| REW_MQ002_FAMILY_TRACE_OBJECTIVE | MQ_002 | quest_unlock | Find Mai and Binh's trail | Rewards section and Chapter 03 continuity. |
| REW_MQ002_COMPASSION | MQ_002 | moral_flag | Compassion +1 if the child or trapped civilians are rescued | Rewards section. |
| REW_MQ002_PRAGMATISM | MQ_002 | moral_flag | Pragmatism +1 if Trung goes straight home | Rewards section. |
| REW_MQ002_FAMILY_DRIVE | MQ_002 | moral_flag | FamilyDrive +1 after finding the empty apartment | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH002_STREET_NAVIGATION | MQ_002 | Street navigation | Leave basement and enter city route. |
| UNLOCK_CH002_OBSTACLE_TRAVERSAL | MQ_002 | Obstacle traversal | Cross blocked intersection and vehicle wrecks. |
| UNLOCK_CH002_BASIC_SCAVENGING | MQ_002 | Basic scavenging | Gather water, bandage, power bank. |
| UNLOCK_CH002_BARTER_THREAT_CHOICE | MQ_002 | Barter/threat choice | Convenience store interaction. |
| UNLOCK_CH002_PHONE_ROUTE_HINT | MQ_002 | Phone route hint | Hoang call completed. |
| UNLOCK_CH002_TIMED_RESCUE | MQ_002 | Timed moral event | Lost child event starts. |
| UNLOCK_CH002_TENSION_EXPLORATION | MQ_002 | Tension exploration | Enter silent apartment building. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH002_BASEMENT_ESCAPED | MQ_002 | Player exits the company basement. |
| FLAG_CH002_HOANG_CONTACT_UNLOCKED | MQ_002 | Player answers or receives Hoang's call. |
| FLAG_CH002_TRUST_HOANG_PLUS | MQ_002 | Player follows Hoang's route guidance. |
| FLAG_CH002_HOANG_PRAGMATISM_SEED | MQ_002 | Player hears Hoang's survival-first warning. |
| FLAG_CH002_NHI_RESCUED | MQ_002 | Player rescues Nhi. |
| FLAG_CH002_NHI_ABANDONED | MQ_002 | Player leaves Nhi/lost mother event unresolved. |
| FLAG_CH002_EMPTY_HOME_FOUND | MQ_002 | Player enters apartment 1208 and finds no family. |
| FLAG_CH002_CHALK_TRAIL_UNLOCKED | MQ_002 | Player reads Mai's fridge note. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_002_01 | The Mother Who Lost Her Child | npc_lost_mother | Find Nhi in the overturned kindergarten bus and choose whether to spend time rescuing her. | Compassion +1 and possible future safe-zone reappearance; skip adds guilt. | SQ_Street_01. |
| SQ_002_02 | Gasoline at a Cutthroat Price | roadside_gas_seller | Trade scarce resources or valuables for gasoline and check if it is diluted. | Bad gasoline can kill a vehicle route; reinforces barter scams. | SQ_Street_02. |
| SQ_002_03 | The Locked Car | automatic | Find the car key, break into a vehicle, or abandon the vehicle route. | Sets force/trade/abandonment route consequences. | SQ_Street_03 and Scene 1. |
| SQ_002_04 | Hoang's Call | comp_hoang | Hear Hoang's camera-guided route and decide whether to trust the alley shortcut. | Establishes Hoang as useful but survival-optimized. | SQ_Street_04 and DT_004. |

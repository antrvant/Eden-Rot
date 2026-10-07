# Quests - CH031

Metadata:

- chapterID: CH031
- sourceFilename: chapter_031_heartland_convoy.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_031 | Protect Convoy | main | comp_mai | CH030 completed; Heartland route unlocked | Convoy survives grain elevator ambush; NORAD coordinates recovered; Hoang redemption seed opened | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ031_01 | MQ_031 | 1 | Process Hoang's departure. | Dialogue | LOC_CH031_MORNING_CONVVOY_CAMP | 1 | Main Quest objective 1. |
| OBJ_MQ031_02 | MQ_031 | 2 | Recover packet log and note. | Investigation | LOC_CH031_MORNING_CONVVOY_CAMP | 1 | Main Quest objective 2. |
| OBJ_MQ031_03 | MQ_031 | 3 | Register rescued children. | Social | LOC_CH031_MORNING_CONVVOY_CAMP | 1 | Main Quest objective 3. |
| OBJ_MQ031_04 | MQ_031 | 4 | Assign convoy vehicle roles. | Management | LOC_CH031_ROLLING_HIGHWAY | 1 | Main Quest objective 4. |
| OBJ_MQ031_05 | MQ_031 | 5 | Classify EDENROT Migrant Nation Trace. | Investigation | LOC_CH031_ROLLING_HIGHWAY | 1 | Main Quest objective 5. |
| OBJ_MQ031_06 | MQ_031 | 6 | Leave Red Canyon before pursuit. | GoTo | LOC_CH031_ROLLING_HIGHWAY | 1 | Main Quest objective 6. |
| OBJ_MQ031_07 | MQ_031 | 7 | Investigate truck stop relief signs. | Investigation | LOC_CH031_TRUCK_STOP | 1 | Main Quest objective 7. |
| OBJ_MQ031_08 | MQ_031 | 8 | Expose fake checkpoint. | Social | LOC_CH031_TRUCK_STOP | 1 | Main Quest objective 8. |
| OBJ_MQ031_09 | MQ_031 | 9 | Salvage truck stop supplies. | Scavenge | LOC_CH031_TRUCK_STOP | 1 | Main Quest objective 9. |
| OBJ_MQ031_10 | MQ_031 | 10 | Evade drone hunter in corn fields. | Stealth | LOC_CH031_CORN_FIELDS | 1 | Main Quest objective 10. |
| OBJ_MQ031_11 | MQ_031 | 11 | Build signal decoys. | Crafting | LOC_CH031_CORN_FIELDS | 1 | Main Quest objective 11. |
| OBJ_MQ031_12 | MQ_031 | 12 | Hold child name circle. | Social | LOC_CH031_NIGHT_CAMP_OVERPASS | 1 | Main Quest objective 12. |
| OBJ_MQ031_13 | MQ_031 | 13 | Humanize trace by roll call. | Social | LOC_CH031_NIGHT_CAMP_OVERPASS | 1 | Main Quest objective 13. |
| OBJ_MQ031_14 | MQ_031 | 14 | Decode Hoang's warning ping. | Investigation | LOC_CH031_RADIO_TRUCK | 1 | Main Quest objective 14. |
| OBJ_MQ031_15 | MQ_031 | 15 | Reroute to grain elevator town. | GoTo | LOC_CH031_GRAIN_ELEVATOR_TOWN | 1 | Main Quest objective 15. |
| OBJ_MQ031_16 | MQ_031 | 16 | Defend convoy ambush. | Combat | LOC_CH031_GRAIN_ELEVATOR_TOWN | 1 | Main Quest objective 16. |
| OBJ_MQ031_17 | MQ_031 | 17 | Rescue Binh and Noah. | Protect | comp_binh | 1 | Main Quest objective 17. |
| OBJ_MQ031_18 | MQ_031 | 18 | Witness Hoang saving Binh. | Cutscene | LOC_CH031_GRAIN_ELEVATOR_TOWN | 1 | Main Quest objective 18. |
| OBJ_MQ031_19 | MQ_031 | 19 | Choose convoy over Hoang chase. | Choice | LOC_CH031_RAIL_LINE | 1 | Main Quest objective 19. |
| OBJ_MQ031_20 | MQ_031 | 20 | Recover NORAD broadcast node. | Scavenge | LOC_CH031_GRAIN_ELEVATOR_TOWN | 1 | Main Quest objective 20. |
| OBJ_MQ031_21 | MQ_031 | 21 | Unlock NORAD mountain route. | Unlock | MQ_032 | 1 | Main Quest objective 21. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ031_01_001 | SQ_031_01 | Assign vehicle roles and create convoy rules. | Mobile base morale modifiers. | SQ_Heart_01. |
| OBJ_SQ031_02_001 | SQ_031_02 | Decide what to do with Hoang's belongings. | HoangMemoryStatus = unresolved. | SQ_Heart_02. |
| OBJ_SQ031_03_001 | SQ_031_03 | Detect fake relief signs and free trapped travelers. | Truck stop supply cache. | SQ_Heart_03. |
| OBJ_SQ031_04_001 | SQ_031_04 | Find name tokens and hold name circle. | Child morale and panic resistance. | SQ_Heart_04. |
| OBJ_SQ031_05_001 | SQ_031_05 | Analyze drone pattern and build decoy emitters. | DroneHunterCountermeasure. | SQ_Heart_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ031_CHILDREN_UNREGISTERED | MQ_031 | Rescued children unregistered or left behind during departure. | Children lost. | Metadata. |
| FAIL_MQ031_TRUCK_STOP_AMBUSH | MQ_031 | Truck stop ambush captures child bus. | Children captured. | Metadata. |
| FAIL_MQ031_DRONE_TAGS_BINH | MQ_031 | Drone hunter successfully tags Binh. | Binh tracked by VALE. | Metadata. |
| FAIL_MQ031_HORDE_REACHES_CLINIC | MQ_031 | Grain elevator horde reaches clinic truck. | Medical resources lost. | Metadata. |
| FAIL_MQ031_CHASE_HOANG | MQ_031 | Player chases Hoang and loses too many convoy vehicles. | Convoy losses. | Metadata. |
| FAIL_MQ031_NODE_DESTROYED | MQ_031 | NORAD broadcast node destroyed before coordinates recovered. | Route lost. | Metadata. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ031_MOBILE_BASE | MQ_031 | system_unlock | Mobile base system | Rewards section. |
| REW_MQ031_CONVVOY_MORALE | MQ_031 | morale_flag | Convoy morale/trust | Rewards section. |
| REW_MQ031_HOANG_REDEMPTION | MQ_031 | story_flag | CQ_HOANG_04 RedemptionPossible | Rewards section. |
| REW_MQ031_NORAD_COORDINATES | MQ_031 | route_item | NORAD coordinates | Rewards section. |
| REW_MQ031_BROADCAST_PARTS | MQ_031 | resource_item | Emergency broadcast parts | Rewards section. |
| REW_MQ031_CHILD_INTEGRATION | MQ_031 | community_flag | Child community integration | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH031_MOBILE_BASE | MQ_031 | Mobile base system | Convoy formed with rules and roles. |
| UNLOCK_CH031_NORAD_ROUTE | MQ_031 | NORAD mountain route | Broadcast node recovered. |
| UNLOCK_CH031_MQ032 | MQ_031 | MQ_032 Assault NORAD | NORAD coordinates obtained. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH031_HEARTLAND_CONVVOY_FORMED | MQ_031 | Convoy established with rules. |
| FLAG_CH031_MOBILE_BASE_UNLOCKED | MQ_031 | Vehicle roles assigned. |
| FLAG_CH031_CONVOY_CHOSEN_OVER_HOANG | MQ_031 | Trung chooses convoy at rail line. |
| FLAG_CH031_BINH_SAVED_BY_HOANG | MQ_031 | Hoang saves Binh from drone. |
| FLAG_CH031_NORAD_BROADCAST_RECOVERED | MQ_031 | Emergency broadcast node found. |
| FLAG_CH031_NORAD_ROUTE_UNLOCKED | MQ_031 | Mountain bunker route opened. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_031_01 | Mobile Nation | comp_mai | Assign vehicle roles, create convoy rules. | Mobile base morale modifiers. | SQ_Heart_01. |
| SQ_031_02 | Hoang's Empty Seat | comp_binh | Decide on Hoang's belongings; let Binh ask questions. | HoangMemoryStatus = unresolved. | SQ_Heart_02. |
| SQ_031_03 | Truck Stop Without Coffee | npc_mara | Detect fake checkpoint, free travelers, salvage supplies. | Supply cache obtained. | SQ_Heart_03. |
| SQ_031_04 | Children Who Need Names | npc_june | Find name tokens, hold name circle, pair with guardians. | Child morale and panic resistance. | SQ_Heart_04. |
| SQ_031_05 | Drone Over Cornfields | npc_thu | Analyze drone pattern, build decoy emitters. | DroneHunterCountermeasure. | SQ_Heart_05. |

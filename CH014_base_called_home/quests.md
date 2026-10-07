# Quests - CH014

Metadata:

- chapterID: CH014
- sourceFilename: chapter_014_can_cu_mang_ten_nha.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_014 | Build First Base | main | char_trung | Group reaches abandoned school after leaving factory area | First base founded; fence built; admission rules drafted; EDEN offer received and rejected; base named "Nha" | Metadata and Main Quest. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ014_001 | MQ_014 | 1 | Lead the group to the abandoned elementary school. | GoTo | LOC_CH014_SCHOOL_GROUNDS | 1 | Scene 1. |
| OBJ_MQ014_002 | MQ_014 | 2 | Clear infected from the school grounds and parking area. | Combat | ENM_CH014_SCHOOL_INFECTED | 2 | Scene 2. |
| OBJ_MQ014_003 | MQ_014 | 3 | Choose a classroom as a safe room for children. | Interact | LOC_CH014_CLASSROOM_3B | 1 | Scene 2. |
| OBJ_MQ014_004 | MQ_014 | 4 | Inspect the well and confirm water is not safe to drink. | Investigate | LOC_CH014_SCHOOL_WELL | 1 | Scene 4. |
| OBJ_MQ014_005 | MQ_014 | 5 | Assign survivor roles: fence, kitchen, medical, children, water. | Decision | FAC_CH014_SURVIVOR_COMMUNITY | 1 | Scene 3. |
| OBJ_MQ014_006 | MQ_014 | 6 | Resolve Ong Tu Nieu's kitchen conflict. | Decision | npc_ong_tu_nieu | 1 | Scene 5. |
| OBJ_MQ014_007 | MQ_014 | 7 | Establish classroom rules with Mai. | Interact | char_mai | 1 | Scene 6. |
| OBJ_MQ014_008 | MQ_014 | 8 | Retrieve pump repair parts from the brick yard. | Scavenge | ITM_CH014_PUMP_BELT | 1 | Scene 4 and SQ_Base_01. |
| OBJ_MQ014_009 | MQ_014 | 9 | Build a temporary perimeter fence. | Construct | LOC_CH014_PERIMETER | 1 | Scene 8. |
| OBJ_MQ014_10 | MQ_014 | 10 | Hold the first base council and draft admission rules. | Decision | LOC_CH014_TEACHERS_ROOM | 1 | Scene 7. |
| OBJ_MQ014_11 | MQ_014 | 11 | Investigate the package left at the gate. | Investigate | ITM_CH014_EDEN_TRADE_PACKAGE | 1 | Scene 9. |
| OBJ_MQ014_12 | MQ_014 | 12 | Pin the EDENROT notice as evidence instead of burning it. | Decision | ITM_CH014_EDENROT_NOTICE | 1 | Scene 9. |
| OBJ_MQ014_13 | MQ_014 | 13 | Name the base. Canon: "Nha" (Home). | Decision | LOC_CH014_SCHOOL_GROUNDS | 1 | Scene 9. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ014_01_001 | SQ_Base_01 | Find the dead animal source near the water tank. | Faster water purification path. | SQ_Base_01. |
| OBJ_SQ014_01_002 | SQ_Base_01 | Boil the first batch of water with Ong Tu Nieu. | Ong Tu Nieu trust seed. | SQ_Base_01. |
| OBJ_SQ014_02_001 | SQ_Base_02 | Let Binh choose a corner without forcing him. | Binh comfort increases. | SQ_Base_02. |
| OBJ_SQ014_02_002 | SQ_Base_02 | Find chalk, cloth, or blankets for the classroom. | Child morale improves. | SQ_Base_02. |
| OBJ_SQ014_03_001 | SQ_Base_03 | Build a quarantine corner with a caregiver. | Humane quarantine established. | SQ_Base_03. |
| OBJ_SQ014_04_001 | SQ_Base_04 | Use Binh's drawing to spot the blind corner behind the bathroom. | Fence gap fixed; security improves. | SQ_Base_04. |
| OBJ_SQ014_05_001 | SQ_Base_05 | Decide whether to announce Binh's condition internally. | Affects base trust and future faction tension. | SQ_Base_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ014_PARKING_NOT_CLEARED | MQ_014 | Player does not clear parking area infected. | Night attack; one survivor wounded. | Fail States. |
| FAIL_MQ014_WATER_NOT_HANDLED | MQ_014 | Player does not purify water. | Children fall sick; morale drops; Doctor mandatory quest. | Fail States. |
| FAIL_MQ014_KITCHEN_CONFLICT | MQ_014 | Player does not resolve Ong Tu Nieu dispute. | Kitchen divided; food lost. | Fail States. |
| FAIL_MQ014_NO_ADMISSION_RULES | MQ_014 | Player does not draft admission rules. | Survivors argue; some leave or conflict erupts. | Fail States. |
| FAIL_MQ014_NO_FENCE | MQ_014 | Player does not build perimeter fence. | Yellow jacket scout gets closer to classroom in ending. | Fail States. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ014_FIRST_BASE | MQ_014 | system_unlock | First base system unlocked | Rewards. |
| REW_MQ014_SURVIVOR_ROLES | MQ_014 | system_unlock | Survivor role assignment unlocked | Rewards. |
| REW_MQ014_RESOURCE_METERS | MQ_014 | system_unlock | Water/food/security/child morale meters | Rewards. |
| REW_MQ014_MAI_SAFE_ROOM | MQ_014 | character_unlock | Mai - Child Safe Room | Rewards. |
| REW_MQ014_ONG_TU_NIEU_KITCHEN | MQ_014 | character_unlock | Ong Tu Nieu - Communal Kitchen (conditional) | Rewards. |
| REW_MQ014_HOANG_PERIMETER | MQ_014 | character_unlock | Hoang - Perimeter Captain | Rewards. |
| REW_MQ014_BINH_DRAWINGS | MQ_014 | character_unlock | Binh - Child Clue Drawings | Rewards. |
| REW_MQ014_EDEN_LETTER | MQ_014 | item | ITM_CH014_EDENROT_NOTICE | Rewards. |
| REW_MQ014_BASE_FLAG | MQ_014 | flag | FLAG_CH014_FIRST_BASE_FOUNDED | Rewards. |
| REW_MQ014_THREAT_FLAG | MQ_014 | flag | FLAG_CH014_EDEN_KNOWS_LOCATION | Rewards. |
| REW_MQ014_MORAL_FLAG | MQ_014 | flag | FLAG_CH014_EDEN_NODE_TRADE_REJECTED | Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH014_BASE_CONSTRUCTION | MQ_014 | Base construction system | First base founded. |
| UNLOCK_CH014_RESOURCE_ALLOCATION | MQ_014 | Resource allocation | Roles assigned. |
| UNLOCK_CH014_SURVIVOR_ROLES | MQ_014 | Survivor role assignment | Base council held. |
| UNLOCK_CH014_CHILD_MORALE | MQ_014 | Child morale system | Classroom rules established. |
| UNLOCK_CH014_WATER_SYSTEM | MQ_014 | Water purification | Well inspected; parts obtained. |
| UNLOCK_CH014_ADMISSION_SYSTEM | MQ_014 | Admission/governance | Rules drafted. |
| UNLOCK_CH014_DEFENSE_PERIMETER | MQ_014 | Defense perimeter | Fence built. |
| UNLOCK_CH014_EDENROT_EVIDENCE_BOARD | MQ_014 | EDENROT evidence board | Notice preserved. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH014_FIRST_BASE_FOUNDED | MQ_014 | School claimed as base. |
| FLAG_CH014_BASE_NAME_NHA | MQ_014 | Base named "Nha." |
| FLAG_CH014_MAI_CHILD_SAFE_ROOM | MQ_014 | Classroom 3B established. |
| FLAG_CH014_BINH_CAN_DRAW_CLUES | MQ_014 | Binh draws fence gap and well clue. |
| FLAG_CH014_HOANG_PERIMETER_CAPTAIN | MQ_014 | Hoang assigned perimeter. |
| FLAG_CH014_ONG_TU_NIEU_KITCHEN | MQ_014 | Ong Tu Nieu allowed to cook. |
| FLAG_CH014_WATER_SYSTEM_DAMAGED | MQ_014 | Well water contaminated. |
| FLAG_CH014_FENCE_LEVEL_1 | MQ_014 | Temporary fence built. |
| FLAG_CH014_ADMISSION_RULES_DRAFTED | MQ_014 | Entry rules posted. |
| FLAG_CH014_EDEN_KNOWS_LOCATION | MQ_014 | Package delivered at gate. |
| FLAG_CH014_TRADE_BINH_OFFER_RECEIVED | MQ_014 | EDEN trade letter received. |
| FLAG_CH014_BASE_KNOWS_BINH_THREAT | MQ_014 | Core adults informed of B-07 threat. |
| FLAG_CH014_EDEN_NODE_TRADE_REJECTED | MQ_014 | Trung/Mai reject trade. |
| FLAG_CH014_EDENROT_EVIDENCE_BOARD | MQ_014 | Letter pinned as evidence. |
| FLAG_CH014_BINH_WROTE_NAME | MQ_014 | Binh writes name on blackboard. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Base_01 | Muddy Well | npc_worker_lead | Inspect well, find dead animal, retrieve pump belt, boil first batch, assign water duty. | Water meter unlocked; disease event in CH015 if mishandled. | SQ_Base_01. |
| SQ_Base_02 | Classroom Without Blackboard | char_mai | Clear classroom, choose layout, create rules, find supplies, let Binh choose corner. | Child morale and trauma recovery milestones unlocked. | SQ_Base_02. |
| SQ_Base_03 | Wounded Who Need Keeping | npc_doctor | Examine wound, build quarantine, decide guard policy, give water/medicine, reassure survivors. | Humane quarantine rules established. | SQ_Base_03. |
| SQ_Base_04 | First Fence | comp_hoang | Inspect perimeter, retrieve scrap, build gate brace, assign watch, use Binh's drawing. | Security meter and Hoang leadership role unlocked. | SQ_Base_04. |
| SQ_Base_05 | Admission List | char_trung | Hold council, draft rules, decide child priority, decide quarantine, decide Binh disclosure. | Governance system and future faction tensions unlocked. | SQ_Base_05. |

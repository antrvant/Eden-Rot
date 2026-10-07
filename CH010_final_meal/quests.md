# Quests - CH010

Metadata:

- chapterID: CH010
- sourceFilename: chapter_010_bua_toi_cuoi_cung.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_010 | Final Meal | main | npc_old_cook | FLAG_CH009_RETREAT_WITH_RECORDING is set | Dinner served, letters read, sabotage discovered, side gate infiltration detected | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ010_001 | MQ_010 | 1 | Meet Old Cook at the kitchen. | TalkTo | npc_old_cook | 1 | Main Quest objective 1. |
| OBJ_MQ010_002 | MQ_010 | 2 | Gather rice, water, salt, canned meat. | Gather | ITM_CH010_FOOD_SUPPLIES | 1 | Main Quest objective 2. |
| OBJ_MQ010_003 | MQ_010 | 3 | Investigate broken seal at auxiliary storage. | Investigate | LOC_CH010_AUXILIARY_STORAGE | 1 | Main Quest objective 3. |
| OBJ_MQ010_004 | MQ_010 | 4 | Bring food back to kitchen. | Fetch | LOC_CH010_OUTPOST_KITCHEN | 1 | Main Quest objective 4. |
| OBJ_MQ010_005 | MQ_010 | 5 | Help serve dinner portions. | Interact | LOC_CH010_OUTPOST_YARD | 1 | Main Quest objective 5. |
| OBJ_MQ010_006 | MQ_010 | 6 | Listen to/read unsent letters. | Interact | ITM_CH009_UNSENT_LETTERS | 1 | Main Quest objective 6. |
| OBJ_MQ010_007 | MQ_010 | 7 | Talk with Mentor about Mai/Binh plan. | TalkTo | npc_mentor | 1 | Main Quest objective 7. |
| OBJ_MQ010_008 | MQ_010 | 8 | Check sabotage traces near auxiliary storage. | Investigate | LOC_CH010_AUXILIARY_STORAGE | 1 | Main Quest objective 8. |
| OBJ_MQ010_009 | MQ_010 | 9 | Collect clue: Edenrot rumor. | Observe | LOC_CH010_OUTPOST_YARD | 1 | Main Quest objective 9. |
| OBJ_MQ010_010 | MQ_010 | 10 | End night with side gate infiltration signs. | Inspect | LOC_CH010_SIDE_GATE | 1 | Main Quest objective 10. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ010_01_001 | SQ_010_01 | Report sabotage to Mentor. | Mentor trust +1. | SQ_010_01. |
| OBJ_SQ010_02_001 | SQ_010_02 | Investigate side gate with Hoang. | Early warning for CH011. | SQ_010_02. |
| OBJ_SQ010_03_001 | SQ_010_03 | Convince child to eat. | Refugee trust +1. | SQ_010_03. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ010_SABOTAGE_IGNORED | MQ_010 | Player ignores sabotage evidence. | Outpost unprepared for CH011 collapse. | Scene 4. |
| FAIL_MQ010_SIDE_GATE_SKIPPED | MQ_010 | Player does not investigate side gate. | Heavier surprise attack in CH011. | Scene 6. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| RWD_MQ010_MORALE | MQ_010 | faction_flag | Outpost morale buff for Chapter 11 | Dinner scene. |
| RWD_MQ010_COOK_RELATIONSHIP | MQ_010 | relationship_flag | Old Cook relationship established | Scene 1. |
| RWD_MQ010_WOODEN_SPOON | MQ_010 | item | Old Cook's wooden spoon (memory item) | Scene 1. |
| RWD_MQ010_FOOTPRINTS | MQ_010 | evidence | Strange footprints near auxiliary storage | Scene 4. |
| RWD_MQ010_SUPPLY_SCHEDULE | MQ_010 | evidence | Copied supply distribution schedule | Scene 4. |
| RWD_MQ010_EDENROT_RUMOR | MQ_010 | lore | Edenrot rumor | Scene 5. |
| RWD_MQ010_MENTOR_TRUST | MQ_010 | relationship_flag | Mentor trust +1 (if sabotage reported) | Scene 3. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH010_COLLAPSE | MQ_010 | Chapter 11 outpost collapse | Dinner night complete. |
| UNLOCK_CH010_ATTACK_TRIGGER | MQ_010 | Side gate infiltration leads to attack | Side gate infiltration detected. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH009_MAI_SIGNAL_RECEIVED | MQ_010 | Recording available for playback. |
| FLAG_CH009_UNSENT_LETTERS_COLLECTED | MQ_010 | Letters available for reading. |
| FLAG_CH010_SABOTAGE_DISCOVERED | MQ_010 | Sabotage traces found at auxiliary storage. |
| FLAG_CH010_SIDE_GATE_INFILTRATION | MQ_010 | Infiltration signs detected at side gate. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_010_01 | Last Rice Package | npc_old_cook | Retrieve last rice from auxiliary storage. | Morale buff, sabotage clue. | Scene 1. |
| SQ_010_02 | Mentor's Letter | environmental | See Mentor writing/keeping an unsent letter. | Mentor backstory hint; do not read full letter. | Scene 3. |
| SQ_010_03 | Child Who Won't Eat | npc_old_cook / npc_nam | Convince child to eat after losing family. | Refugee trust +1. | Scene 5. |
| SQ_010_04 | Footprints Near Storage | comp_hoang | Follow strange footprints from storage to side gate. | If completed, CH011 has early warning. | Scene 4. |
| SQ_010_05 | Unsent Letters | environmental | Choose to read/keep/assign recipients for 3 letters. | Morale, lore, emotional texture. | Scene 5. |

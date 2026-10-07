# Quests - CH011

Metadata:

- chapterID: CH011
- sourceFilename: chapter_011_su_sup_do_cua_can_cu.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_011 | Base Collapse | main | Automatic (crisis event) | FLAG_CH010_SIDE_GATE_INFILTRATION is set | Survivors assembled and group escapes through drainage tunnel | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ011_001 | MQ_011 | 1 | Investigate side gate opening. | Investigate | LOC_CH011_SIDE_GATE | 1 | Main Quest objective 1. |
| OBJ_MQ011_002 | MQ_011 | 2 | Sound alarm / alert Mentor. | TalkTo | npc_mentor | 1 | Main Quest objective 2. |
| OBJ_MQ011_003 | MQ_011 | 3 | Identify false loudspeaker orders. | Investigate | LOC_CH011_OUTPOST_YARD | 1 | Main Quest objective 3. |
| OBJ_MQ011_004 | MQ_011 | 4 | Rescue Edenrot risk map from radio tent. | Scavenge | LOC_CH011_RADIO_TENT | 1 | Main Quest objective 4. |
| OBJ_MQ011_005 | MQ_011 | 5 | Choose rescue priority: radio, doctor, refugees, ammo. | Choice | Multiple | 1 | Main Quest objective 5. |
| OBJ_MQ011_006 | MQ_011 | 6 | Confront bandit saboteur. | TalkTo | npc_saboteur | 1 | Main Quest objective 6. |
| OBJ_MQ011_007 | MQ_011 | 7 | Support Mentor at West Gate. | GoTo | LOC_CH011_WEST_GATE | 1 | Main Quest objective 7. |
| OBJ_MQ011_008 | MQ_011 | 8 | Receive dog tag / map / retreat order. | Interact | npc_mentor | 1 | Main Quest objective 8. |
| OBJ_MQ011_009 | MQ_011 | 9 | Issue assembly command to survivors. | TalkTo | LOC_CH011_MEDICAL_YARD | 1 | Main Quest objective 9. |
| OBJ_MQ011_010 | MQ_011 | 10 | Lead group through drainage tunnel. | GoTo | LOC_CH011_DRAINAGE_TUNNEL | 1 | Main Quest objective 10. |
| OBJ_MQ011_011 | MQ_011 | 11 | Escape outpost. | Escape | LOC_CH011_DRAINAGE_TUNNEL | 1 | Main Quest objective 11. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ011_01_001 | SQ_011_01 | Rescue radio operator and frequency list. | Radio capability preserved. | SQ_011_01. |
| OBJ_SQ011_02_001 | SQ_011_02 | Rescue doctor and medical supplies. | Medical capability preserved. | SQ_011_02. |
| OBJ_SQ011_03_001 | SQ_011_03 | Delay ammo storage explosion. | Reduced casualties. | SQ_011_03. |
| OBJ_SQ011_04_001 | SQ_011_04 | Rescue refugee tent civilians. | More survivors. | SQ_011_04. |
| OBJ_SQ011_05_001 | SQ_011_05 | Capture/kill saboteur. | Bandit intel. | SQ_011_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ011_SAVE_EVERYONE | MQ_011 | Player tries to save everyone. | Time runs out; heavier casualties. | Scene 3. |
| FAIL_MQ011_RETURN_TO_MENTOR | MQ_011 | Player returns to Mentor. | Hoang stops; emotional damage. | Scene 5. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| RWD_MQ011_DOG_TAG | MQ_011 | item | Mentor's dog tag | Scene 5. |
| RWD_MQ011_RETREAT_MAP | MQ_011 | item | Mentor's retreat map | Scene 5. |
| RWD_MQ011_EDENROT_MAP | MQ_011 | evidence | Edenrot risk map (optional) | Scene 2. |
| RWD_MQ011_LEADERSHIP | MQ_011 | system_unlock | Leadership burden unlocked | Scene 6. |
| RWD_MQ011_BANDIT_THREAT | MQ_011 | enemy_knowledge | Bandit threat +1 | Scene 4. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH011_JOURNEY | MQ_011 | Chapter 12 survivor journey | Escape complete. |
| UNLOCK_CH011_INVESTIGATION | MQ_011 | Church / industrial zone investigation | Escape complete. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH010_SABOTAGE_DISCOVERED | MQ_011 | Confirms sabotage from CH010. |
| FLAG_CH011_MENTOR_DEAD | MQ_011 | Mentor removed from party at West Gate. |
| FLAG_CH011_MENTOR_DOG_TAG_OBTAINED | MQ_011 | Mentor's dog tag retrieved. |
| FLAG_CH011_SURVIVOR_LIST | MQ_011 | Tracks who survived the collapse. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_011_01 | Mentor's Dog Tag | npc_mentor | Retrieve dog tag during retreat. | Mentor legacy item; unlock future Army trust dialogue. | Scene 5. |
| SQ_011_02 | Rescue Radio Operator | npc_radio_operator | Bring radio operator and frequency list out. | Radio capability preserved. | Scene 2. |
| SQ_011_03 | Delayed Ammo Explosion | npc_engineer | Close safety valve / push ammo crates from fire. | Reduced casualties; some ammo. | Scene 3. |
| SQ_011_04 | Trapped Refugees | npc_nam | Open path from refugee tent to drainage. | Refugee trust +1, more survivors. | Scene 3. |
| SQ_011_05 | Kitchen Informant | npc_old_cook | Confront saboteur in outpost. | Bandit network intel. | Scene 4. |

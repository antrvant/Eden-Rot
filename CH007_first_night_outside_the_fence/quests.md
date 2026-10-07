# Quests - CH007

Metadata:

- chapterID: CH007
- sourceFilename: chapter_007_dem_dau_ngoai_tuong_rao.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_007 | First Night Defense | main | npc_mentor | Starts after CH006 when Mentor assigns Trung West Gate duty | Outpost survives until dawn and Trung reports to Mentor | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ007_001 | MQ_007 | 1 | Receive night guard assignment from Mentor. | TalkTo | npc_mentor | 1 | Main Quest objective 1. |
| OBJ_MQ007_002 | MQ_007 | 2 | Check the refugee tent and speak with refugees. | Visit | LOC_CH007_REFUGEE_TENT | 1 | Main Quest objective 2. |
| OBJ_MQ007_003 | MQ_007 | 3 | Gather reinforcement materials for the fence. | Gather | LOC_CH007_MATERIAL_DEPOT | 1 | Main Quest objective 3. |
| OBJ_MQ007_004 | MQ_007 | 4 | Allocate defenses between gate, tent, and ammo shed. | DefenseChoice | LOC_CH007_WEST_GATE | 1 | Main Quest objective 4. |
| OBJ_MQ007_005 | MQ_007 | 5 | Investigate the scream outside the fence. | Investigate | LOC_CH007_WATCH_TOWER | 1 | Main Quest objective 5. |
| OBJ_MQ007_006 | MQ_007 | 6 | Keep the crowd from opening the gate. | SocialControl | npc_lost_mother | 1 | Main Quest objective 6. |
| OBJ_MQ007_007 | MQ_007 | 7 | Defend against three zombie waves. | DefenseCombat | LOC_CH007_WEST_GATE | 3 | Main Quest objective 7. |
| OBJ_MQ007_008 | MQ_007 | 8 | Stop the Screamer. | KillOrMark | ENM_CH007_FIRST_SCREAMER | 1 | Main Quest objective 8. |
| OBJ_MQ007_009 | MQ_007 | 9 | Survive until dawn and report to Mentor. | Report | npc_mentor | 1 | Main Quest objective 9. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ007_01_001 | SQ_007_01 | Gather wood, wire, sandbags, nails, and sheet metal. | Improves selected defense points. | SQ_Defense_01. |
| OBJ_SQ007_01_002 | SQ_007_01 | Choose where reinforcement materials go. | Determines which point risks breach. | SQ_Defense_01. |
| OBJ_SQ007_02_001 | SQ_007_02 | Find a lost child or their guardian inside the refugee tent. | Refugee morale +1. | SQ_Defense_02. |
| OBJ_SQ007_03_001 | SQ_007_03 | Inventory ammo and investigate a missing ammo box. | Seeds sabotage or accounting issue for Chapters 10-11. | SQ_Defense_03. |
| OBJ_SQ007_04_001 | SQ_007_04 | Persuade or restrain the lost mother before she opens the gate. | Affects casualties and refugee trust. | SQ_Defense_04. |
| OBJ_SQ007_05_001 | SQ_007_05 | Record or analyze Screamer audio after the battle. | Unlocks Screamer codex. | SQ_Defense_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ007_GATE_BREACHED | MQ_007 | Gate opens or collapses during wave. | Major casualties or reload depending implementation. | Scene 5-6. |
| FAIL_MQ007_TENT_OVERRUN | MQ_007 | Refugee tent is not protected from climber/horde. | Refugee casualties and trust loss. | Scene 5. |
| FAIL_MQ007_AMMO_SHED_LOST | MQ_007 | Ammo shed is not defended and is overrun/damaged. | Reduced ammo for future defense. | Scene 5 and SQ_Defense_03. |
| FAIL_SQ007_04_MOTHER_OPENS_GATE | SQ_007_04 | Mother opens gate under Screamer influence. | High breach risk and casualties. | Scene 6. |
| FAIL_MQ007_TRUNG_DOWNED | MQ_007 | Trung is downed during defense. | Reload checkpoint or rescue state. | Gameplay Beats. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ007_BASE_DEFENSE | MQ_007 | system_unlock | Base defense basics | Rewards section. |
| REW_MQ007_SCREAMER_KNOWLEDGE | MQ_007 | enemy_knowledge | Screamer | Rewards section. |
| REW_MQ007_CROWD_PANIC | MQ_007 | system_unlock | Crowd panic mechanic | Rewards section. |
| REW_MQ007_MENTOR_RESPECT | MQ_007 | relationship_flag | MentorRespect +1 if gate holds | Rewards section. |
| REW_MQ007_REFUGEE_TRUST | MQ_007 | faction_flag | RefugeeTrust +1 if tent is protected | Rewards section. |
| REW_MQ007_HOANG_PRAGMATISM | MQ_007 | relationship_flag | HoangPragmatism +1 if ammo shed prioritized | Rewards section. |
| REW_MQ007_CHILD_EAR_CLOTH | MQ_007 | item | ITM_CH007_CHILD_EAR_CLOTH | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH007_GUARD_DUTY | MQ_007 | Guard duty tutorial | Accept night assignment. |
| UNLOCK_CH007_DEFENSE_PREP | MQ_007 | Defense preparation | Gather and allocate materials. |
| UNLOCK_CH007_RESOURCE_ALLOCATION | MQ_007 | Base defense resource allocation | Choose gate/tent/ammo priorities. |
| UNLOCK_CH007_SCREAMER_AUDIO | MQ_007 | Sound-based threat | First scream heard. |
| UNLOCK_CH007_CROWD_PANIC | MQ_007 | Crowd panic | Refugees try to open gate. |
| UNLOCK_CH007_MULTI_POINT_DEFENSE | MQ_007 | Multi-point defense | Three wave defense begins. |
| UNLOCK_CH007_DAWN_REVIEW | MQ_007 | Consequence review | Survive until dawn. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH007_SCREAMER_KNOWLEDGE_UNLOCKED | MQ_007 | Player identifies Screamer as horde-calling threat. |
| FLAG_CH007_COMMANDER_SEED | MQ_007 | Trung gives orders that refugees follow. |
| FLAG_CH007_NHI_NAME_REMEMBERED | MQ_007 | Trung repeats Nhi's name to the lost mother. |
| FLAG_CH007_MAI_FRAGMENT_BLOCKED | MQ_007 | New Mai fragment is lost under Screamer noise. |
| FLAG_CH007_TRAINING_DAY_UNLOCKED | MQ_007 | Mentor sets Chapter 008 training day. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_007_01 | Reinforce the Fence | npc_engineer | Gather and allocate limited defense materials. | Determines weak point in night wave. | SQ_Defense_01. |
| SQ_007_02 | Lost Child in the Tent | refugee child | Find the child's parent/guardian before the wave. | Refugee morale +1. | SQ_Defense_02. |
| SQ_007_03 | Missing Ammo | comp_hoang or npc_phuc | Inventory ammo and investigate missing ammo box. | Seeds sabotage or accounting issue. | SQ_Defense_03. |
| SQ_007_04 | Mother at the Gate | npc_lost_mother | Stop her from opening the gate when Screamer mimics a child. | Affects casualties and continuing Nhi thread. | SQ_Defense_04. |
| SQ_007_05 | Scream in the Night | npc_radio_operator | Record/analyze Screamer audio after battle. | Unlocks Screamer codex and radio-interference lore. | SQ_Defense_05. |

# Quests - CH008

Metadata:

- chapterID: CH008
- sourceFilename: chapter_008_bai_hoc_cua_dai_uy.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_008 | Survival Training | main | npc_mentor | Starts the morning after CH007 outpost defense | Trung retreats from the Tank/armory threat and earns permission for MQ_009 Restore Radio | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ008_001 | MQ_008 | 1 | Check the radio tent and learn which parts are needed. | TalkTo | npc_radio_operator | 1 | Main Quest objective 1. |
| OBJ_MQ008_002 | MQ_008 | 2 | Meet Mentor at the training yard. | GoTo | LOC_CH008_TRAINING_YARD | 1 | Main Quest objective 2. |
| OBJ_MQ008_003 | MQ_008 | 3 | Complete the breathing and firearm drill. | Training | ITM_CH008_TRAINING_RIFLE | 1 | Main Quest objective 3. |
| OBJ_MQ008_004 | MQ_008 | 4 | Complete the stealth run with the scout. | Stealth | LOC_CH008_ABANDONED_HOUSES | 1 | Main Quest objective 4. |
| OBJ_MQ008_005 | MQ_008 | 5 | Collect batteries and radio filter parts without raising alarm. | Scavenge | ITM_CH008_RADIO_FILTER_PARTS | 1 | Main Quest objective 5. |
| OBJ_MQ008_006 | MQ_008 | 6 | Survive the bus-yard target priority encounter. | CombatDecision | LOC_CH008_ABANDONED_BUS_YARD | 1 | Main Quest objective 6. |
| OBJ_MQ008_007 | MQ_008 | 7 | Rescue or protect Phuc/recruit if possible. | Protect | npc_phuc | 1 | Main Quest objective 7. |
| OBJ_MQ008_008 | MQ_008 | 8 | Recover supplies from the old armory area. | Scavenge | LOC_CH008_OLD_ARMORY | 1 | Main Quest objective 8. |
| OBJ_MQ008_009 | MQ_008 | 9 | Retreat when the Tank/armored infected appears. | Retreat | ENM_CH008_TANK_FORESHADOW | 1 | Main Quest objective 9. |
| OBJ_MQ008_010 | MQ_008 | 10 | Receive permission to join MQ_009 Restore Radio. | UnlockQuest | MQ_009 | 1 | Main Quest objective 10. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ008_01_001 | SQ_008_01 | Hit infected targets without hitting the living target. | Aim stability tutorial complete. | SQ_Training_01. |
| OBJ_SQ008_02_001 | SQ_008_02 | Count and recover ammo from bus yard or old storage. | Ammo stock plus missing ammo clue. | SQ_Training_02. |
| OBJ_SQ008_03_001 | SQ_008_03 | Help Phuc practice loading and staying calm. | Phuc confidence seed; possible future payoff. | SQ_Training_03. |
| OBJ_SQ008_04_001 | SQ_008_04 | Find or return Mentor's child keepsake. | Mentor backstory hint. | SQ_Training_04. |
| OBJ_SQ008_05_001 | SQ_008_05 | Inspect the locked armory before opening it. | Avoids casualty and reveals Tank foreshadow. | SQ_Training_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ008_FRIENDLY_TARGET_HIT | MQ_008 | Player hits the living target during firearm drill. | Repeat drill; Mentor tension/lesson. | Scene 2. |
| FAIL_MQ008_STEALTH_ALARM | MQ_008 | Player makes too much noise in abandoned houses. | Attracts zombies; stealth run complication. | Scene 3. |
| FAIL_MQ008_PHUC_DOWNED | MQ_008 | Player fails target priority and Phuc is hurt/killed. | MentorRespect loss or alternate outcome. | Scene 4. |
| FAIL_MQ008_ARMORY_OVERCOMMIT | MQ_008 | Player disobeys retreat and pushes Tank/armory encounter. | Injury/casualty risk. | Scene 7. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ008_FIREARM_TIER_1 | MQ_008 | system_unlock | Firearm basics tier 1 | Rewards section. |
| REW_MQ008_STEALTH_TIER_1 | MQ_008 | system_unlock | Stealth basics tier 1 | Rewards section. |
| REW_MQ008_TARGET_PRIORITY | MQ_008 | system_unlock | Weak point/priority targeting | Rewards section. |
| REW_MQ008_RETREAT_VALID | MQ_008 | system_unlock | Retreat/avoidance as valid mission outcome | Rewards section. |
| REW_MQ008_MENTOR_RESPECT | MQ_008 | relationship_flag | MentorRespect +1 if player listens and retreats | Rewards section. |
| REW_MQ008_HOANG_PRAGMATISM | MQ_008 | relationship_flag | HoangPragmatism +1 if player values ammo/resources | Rewards section. |
| REW_MQ008_FIRST_CORRECT_CARTRIDGE | MQ_008 | item | ITM_CH008_FIRST_CORRECT_CARTRIDGE | Rewards section. |
| REW_MQ008_UNLOCK_MQ009 | MQ_008 | quest_unlock | MQ_009 Restore Radio | Rewards section and ending. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH008_AIM_STABILITY | MQ_008 | Aim stability | Breathing drill complete. |
| UNLOCK_CH008_FIRE_DISCIPLINE | MQ_008 | Friendly-fire discipline | Living target avoided. |
| UNLOCK_CH008_STEALTH_BASICS | MQ_008 | Stealth basics | Abandoned house run complete. |
| UNLOCK_CH008_NOISE_MANAGEMENT | MQ_008 | Noise management | Avoid broken glass/doors. |
| UNLOCK_CH008_TARGET_PRIORITY | MQ_008 | Target priority | Bus-yard encounter complete. |
| UNLOCK_CH008_RETREAT_OUTCOME | MQ_008 | Retreat as valid outcome | Armory retreat obeyed. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH008_RADIO_FILTER_PARTS_OBTAINED | MQ_008 | Player obtains parts for MQ_009. |
| FLAG_CH008_MENTOR_CHILD_TOKEN_SEEN | MQ_008 | Player sees Mentor's child keepsake. |
| FLAG_CH008_TANK_FORESHADOW_SEEN | MQ_008 | Tank/armored infected pounds inside old armory. |
| FLAG_CH008_RETREAT_LESSON_LEARNED | MQ_008 | Player retreats under Mentor's order. |
| FLAG_CH008_MQ009_RESTORE_RADIO_UNLOCKED | MQ_008 | Mentor allows radio mission participation. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_008_01 | First Shot | npc_mentor | Hit infected targets without hitting living target. | Aim stability/tutorial complete. | SQ_Training_01. |
| SQ_008_02 | Gather Ammo | npc_smith or comp_hoang | Count and recover ammo, noting missing box. | Sabotage seed for Chapters 10-11. | SQ_Training_02. |
| SQ_008_03 | Young Soldier Afraid of the Gun | npc_phuc | Help Phuc practice loading and calm breathing. | Phuc may later help Trung. | SQ_Training_03. |
| SQ_008_04 | Mentor's Keepsake | environmental | Find or return Mentor's child toy/photo. | Mentor backstory hint. | SQ_Training_04. |
| SQ_008_05 | Locked Armory | npc_smith | Inspect or open old armory and choose when to retreat. | Affects casualties/ammo reward and Tank knowledge. | SQ_Training_05. |

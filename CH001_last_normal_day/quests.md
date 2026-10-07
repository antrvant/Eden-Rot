# Quests - CH001

Metadata:

- chapterID: CH001
- sourceFilename: chapter_001_ngay_binh_thuong_cuoi_cung.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_001 | Escape Office | main | automatic | Chapter start after Trung leaves home for work | Trung escapes through the Base-level outdoor parking gate after surviving the infected Boss chase | Metadata lists Main Quest: MQ_001 - Escape Office; Main Quest section gives premise and objectives. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ001_001 | MQ_001 | 1 | Reach the first-floor glass meeting room on time. | GoTo | LOC_CH001_GLASS_MEETING_ROOM | 1 | Main Quest objective 1. |
| OBJ_MQ001_002 | MQ_001 | 2 | Check the phone when Mai calls. | Interact | ITM_CH001_TRUNG_PHONE | 1 | Main Quest objective 2 and Scene 2 phone call. |
| OBJ_MQ001_003 | MQ_001 | 3 | Recover the phone after the boss collects it. | Fetch | ITM_CH001_TRUNG_PHONE | 1 | Main Quest objective 3 and phone tray beat. |
| OBJ_MQ001_004 | MQ_001 | 4 | Investigate the scream near the elevator. | GoTo | LOC_CH001_ELEVATOR_HALLWAY | 1 | Main Quest objective 4. |
| OBJ_MQ001_005 | MQ_001 | 5 | Find an improvised weapon. | Fetch | ITM_CH001_FIRE_EXTINGUISHER | 1 | Main Quest objective 5 and Gameplay Beats. |
| OBJ_MQ001_006 | MQ_001 | 6 | Decide whether to help the coworker behind the glass. | MoralChoice | FLAG_CH001_COWORKER_01_RESCUE_DECIDED | 1 | Main Quest runtime objective 6 and DT_003. |
| OBJ_MQ001_007 | MQ_001 | 7 | Reach the stairs leading from Floor 1 down to the Base. | GoTo | LOC_CH001_EMERGENCY_STAIRS | 1 | Main Quest runtime objective 7. |
| OBJ_MQ001_008 | MQ_001 | 8 | Call Mai from the Base-level outdoor parking area. | GoTo | LOC_CH001_BASEMENT_PARKING | 1 | Main Quest runtime objective 8. Legacy location ID retained for compatibility. |
| OBJ_MQ001_009 | MQ_001 | 9 | Take the metal rod from the car trunk and escape the infected Boss through the parking gate. | Fetch | ITM_CH001_METAL_ROD | 1 | Main Quest runtime objective 9 and ending chase. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ001_01_001 | SQ_001_01 | Retrieve Trung's phone from the meeting room tray. | Unlocks phone log and Mai/Binh clue route. | SQ_Office_01. |
| OBJ_SQ001_01_002 | SQ_001_01 | Listen to Binh's voice message. | Adds emotional context and guilt/family flags. | SQ_Office_01 emotional reward. |
| OBJ_SQ001_02_001 | SQ_001_02 | Break or unlock the glass office door. | Can save npc_coworker_01 at time/health cost. | SQ_Office_02 and Scene 5. |
| OBJ_SQ001_02_002 | SQ_001_02 | Give the trapped coworker a tool without fully returning. | Sets aided outcome for later resolution. | DT_003 Choice C. |
| OBJ_SQ001_03_001 | SQ_001_03 | Recover Trung's car key among the Floor 1 desks. | Enables the Base outdoor-parking escape car. | SQ_Office_03. |
| OBJ_SQ001_03_002 | SQ_001_03 | Reach the outdoor parking area and take the metal rod from Trung's car trunk. | Arms Trung for the infected Boss chase and prepares the escape car. | SQ_Office_03 runtime objective. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ001_HEALTH_ZERO | MQ_001 | Trung is killed by infected during tutorial. | Reload checkpoint. | Gameplay tutorial combat beats imply survival challenge. |
| FAIL_SQ001_01_PHONE_LEFT | SQ_001_01 | Player leaves without the phone. | Chapter 02 must use another route to learn where Mai went. | SQ_Office_01 failure consequence. |
| FAIL_SQ001_02_COWORKER_DEAD | SQ_001_02 | Player hesitates too long or abandons rescue. | Sets guilt and blocks possible Chapter 05 return witness. | Main Quest rewards and continuity notes. |
| FAIL_SQ001_03_KEY_NOT_FOUND | SQ_001_03 | Player fails to identify or recover the car key clue. | Base parking escape gate remains blocked until the required car-preparation objective is resolved. | SQ_Office_03 runtime gate. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ001_MELEE_UNLOCK | MQ_001 | system_unlock | Basic melee | Rewards section. |
| REW_MQ001_FAMILY_OBJECTIVE | MQ_001 | quest_unlock | Go Home to Find Mai and Binh | Rewards section. |
| REW_MQ001_PHONE_LOG | MQ_001 | system_unlock | Phone log system | Rewards section. |
| REW_MQ001_COMPASSION | MQ_001 | moral_flag | Compassion +1 if coworker is rescued | Rewards section. |
| REW_MQ001_PRAGMATISM | MQ_001 | moral_flag | Pragmatism +1 if player runs to preserve health/speed | Rewards section. |
| REW_MQ001_GUILT | MQ_001 | moral_flag | Guilt +1 if hesitation causes NPC death | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH001_BASIC_INTERACTION | MQ_001 | Basic interaction | Pick up or inspect phone/items. |
| UNLOCK_CH001_DODGE | MQ_001 | Dodge tutorial | First infected lunge. |
| UNLOCK_CH001_BARRICADE | MQ_001 | Barricade tutorial | Use chair or door block during escape. |
| UNLOCK_CH001_STRUGGLE | MQ_001 | Struggle tutorial | Grab or infected close-combat prompt. |
| UNLOCK_CH001_MORAL_CHOICE | MQ_001 | Moral choice tutorial | Coworker rescue choice. |
| UNLOCK_CH001_LIGHT_EXPLORATION | MQ_001 | Light exploration | Car key search. |
| UNLOCK_CH001_CHASE | MQ_001 | Chase setpiece | Infected boss pursuit. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH001_PHONE_RECOVERED | MQ_001 | Player retrieves the phone. |
| FLAG_CH001_MAI_LOCATION_KNOWN | MQ_001 | Player reads Mai's message about taking Binh to her mother's home. |
| FLAG_CH001_COWORKER_01_RESCUED | MQ_001 | Player fully rescues npc_coworker_01. |
| FLAG_CH001_COWORKER_01_ABANDONED | MQ_001 | Player runs without helping. |
| FLAG_CH001_COWORKER_01_AIDED | MQ_001 | Player gives aid but does not fully rescue. |
| FLAG_CH001_OFFICE_ESCAPED | MQ_001 | Player exits through the Base-level outdoor parking gate. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_001_01 | Retrieve the Phone | automatic | Recover Trung's phone after the boss demands all phones be surrendered. | If missed, Chapter 02 opens without clear knowledge of Mai's route. | SQ_Office_01 - Lay Lai Dien Thoai. |
| SQ_001_02 | The Coworker Behind the Glass | npc_coworker_01 | Break the lock or glass door to rescue trapped coworkers. | If rescued, one NPC may return in Chapter 05 as a witness that Trung did not abandon people. | SQ_Office_02 - Nguoi O Lai Sau Canh Cua Kinh. |
| SQ_001_03 | Prepare the Escape Car | automatic | Recover Trung's key on Floor 1, reach the Base outdoor parking area, and take the metal rod from the trunk. | Reinforces survival distrust and prepares the final escape/chase. | SQ_Office_03 runtime implementation. |

## Runtime Flow Corrections (2026-08-17)

- `SQ_001_03` starts at `BEAT_EMERGENCY_STAIRS`, before the Player reaches the Base outdoor parking area; `BEAT_PARKING_ESCAPE` requires that quest to be completed.
- `BEAT_MISSED_CALL` requires the Office meeting flag and `ITM_CH001_TRUNG_PHONE`. Both its `StoryBeatTrigger` and companion `SceneEventTrigger` use the meeting flag, removing the former circular dependency on `FLAG_CH001_PHONE_RECOVERED`.
- `STATE_MISSED_CALL` now sets `FLAG_CH001_PHONE_RECOVERED`; `STATE_MAI_ROUTE_TEXT` gives `ITM_CH001_MAI_ROUTE_TEXT`.
- Selecting any Steve rescue option sets `FLAG_CH001_COWORKER_01_RESCUE_DECIDED`; the selected response then sets exactly one outcome flag (`RESCUED`, `ABANDONED`, or `AIDED`). `QuestManager.OnMoralChoiceMade` advances matching MoralChoice objectives when the flag is set.
- `MQ_001`, `SQ_001_01`, and `SQ_001_03` preserve fetched story items on completion so the phone, route clue, and car key are not consumed by generic Fetch cleanup.

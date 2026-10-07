# Quests - CH009

Metadata:

- chapterID: CH009
- sourceFilename: chapter_009_tin_hieu_cua_mai.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_009 | Restore Radio | main | npc_radio_operator / npc_mentor | FLAG_CH008_MQ009_RESTORE_RADIO_UNLOCKED is set | Mai's message recorded and retreat completed with recording | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ009_001 | MQ_009 | 1 | Listen to Mai's radio fragment replay. | TalkTo | npc_radio_operator | 1 | Main Quest objective 1. |
| OBJ_MQ009_002 | MQ_009 | 2 | Receive mission to retrieve filter/amplifier and recording tape. | TalkTo | npc_mentor | 1 | Main Quest objective 2. |
| OBJ_MQ009_003 | MQ_009 | 3 | Travel to old radio station with team. | GoTo | LOC_CH009_ROAD_TO_STATION | 1 | Main Quest objective 3. |
| OBJ_MQ009_004 | MQ_009 | 4 | Investigate false rescue frequency. | Investigate | LOC_CH009_ABANDONED_MARKET | 1 | Main Quest objective 4. |
| OBJ_MQ009_005 | MQ_009 | 5 | Start generator at radio station. | Interact | LOC_CH009_POST_OFFICE | 1 | Main Quest objective 5. |
| OBJ_MQ009_006 | MQ_009 | 6 | Collect filter, copper wire, fuse, cassette tape. | Gather | ITM_CH009_RADIO_PARTS | 1 | Main Quest objective 6. |
| OBJ_MQ009_007 | MQ_009 | 7 | Climb antenna and install filter. | Interact | LOC_CH009_ROOFTOP_ANTENNA | 1 | Main Quest objective 7. |
| OBJ_MQ009_008 | MQ_009 | 8 | Protect radio operator while tuning signal. | Protect | npc_radio_operator | 1 | Main Quest objective 8. |
| OBJ_MQ009_009 | MQ_009 | 9 | Record Mai's message. | Interact | ITM_CH009_RECORDING_TAPE | 1 | Main Quest objective 9. |
| OBJ_MQ009_010 | MQ_009 | 10 | Retreat when EDEN NODE jams signal and horde arrives. | Retreat | LOC_CH009_RETREAT_ROUTE | 1 | Main Quest objective 10. |
| OBJ_MQ009_011 | MQ_009 | 11 | Return to outpost with recording. | GoTo | LOC_CH009_OUTPOST_EVENING | 1 | Main Quest objective 11. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ009_01_001 | SQ_009_01 | Destroy false safe zone transmitter. | Prevent future survivor casualties. | SQ_009_01. |
| OBJ_SQ009_02_001 | SQ_009_02 | Collect 3 unsent letters from post office. | Lore items, morale bonus. | SQ_009_02. |
| OBJ_SQ009_03_001 | SQ_009_03 | Complete antenna repair without alarm. | Stealth skill validation. | SQ_009_03. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ009_HORDE_ALERTED | MQ_009 | Player alerts horde before antenna repair. | Combat encounter, possible injury. | Scene 6. |
| FAIL_MQ009_BROADCAST_CONTINUED | MQ_009 | Player continues broadcasting after Hoang warning. | Mai's position potentially compromised. | Scene 7. |
| FAIL_MQ009_RETREAT_REFUSED | MQ_009 | Player refuses to retreat. | Forced retreat by Mentor; relationship penalty. | Scene 8. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| RWD_MQ009_MAI_LOCATION | MQ_009 | evidence | Mai at northeast church with a girl | Recording content. |
| RWD_MQ009_BINH_LOCATION | MQ_009 | evidence | Binh taken to industrial zone | Recording content. |
| RWD_MQ009_YELLOW_COATS | MQ_009 | enemy_knowledge | Yellow coats hunting Binh specifically | Recording content. |
| RWD_MQ009_RECORDING_TAPE | MQ_009 | item | Mai's recording tape (replayable) | Scene 9. |
| RWD_MQ009_EDEN_SIGNAL | MQ_009 | lore | EDEN NODE ACTIVE signal detected | Scene 8. |
| RWD_MQ009_RADIO_OP_TRUST | MQ_009 | relationship_flag | Radio operator trust +1 | Scene 7. |
| RWD_MQ009_MENTOR_RESPECT | MQ_009 | relationship_flag | Mentor respect +1 (if retreats with recording) | Scene 8. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH009_DINNER_PLAYBACK | MQ_009 | Chapter 10 dinner scene with recording playback | Recording obtained. |
| UNLOCK_CH009_INDUSTRIAL_THREAD | MQ_009 | Industrial zone investigation thread | Binh location known. |
| UNLOCK_CH009_CHURCH_THREAD | MQ_009 | Northeast church investigation thread | Mai location known. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH008_MQ009_RESTORE_RADIO_UNLOCKED | MQ_009 | Required to start MQ_009. |
| FLAG_CH008_RADIO_FILTER_PARTS_OBTAINED | MQ_009 | Pre-existing parts for radio repair. |
| FLAG_CH009_MAI_SIGNAL_RECEIVED | MQ_009 | Mai's signal received through radio. |
| FLAG_CH009_RECORDING_OBTAINED | MQ_009 | Recording tape captured Mai's message. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_009_01 | Recording Tape | npc_radio_operator | Find cassette tape/storage to record Mai's signal. | Mai's recording tape, replayable emotional item. | Scene 2. |
| SQ_009_02 | Missing Components | npc_engineer | Find fuse, copper wire, filter in radio station. | Radio upgrade; one component in room with infected. | Scene 4. |
| SQ_009_03 | Rooftop Antenna | npc_radio_operator | Climb antenna, install filter at correct joint. | To hear loved ones, maintain breath and discipline at height. | Scene 6. |
| SQ_009_04 | False Frequency | environmental | Verify/detect fake "free safe zone" broadcast trap. | If not destroyed, other NPCs may die from false hope. | Scene 3. |
| SQ_009_05 | Unsent Letters | environmental | Collect 3 unsent letters to families. | Lore/morale; can be read at Chapter 10 dinner. | Scene 5. |

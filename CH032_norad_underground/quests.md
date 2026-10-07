# Quests - CH032

Metadata:

- chapterID: CH032
- sourceFilename: chapter_032_norad_duoi_long_dat.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_032 | Assault NORAD | main | npc_pike | CH031 completed; NORAD route unlocked | Satellite network partially online; King defeated; shelter rotation established; global broadcast window opened | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ032_01 | MQ_032 | 1 | Guide convoy to mountain corridor. | GoTo | LOC_CH032_MOUNTAIN_CORRIDOR | 1 | Main Quest objective 1. |
| OBJ_MQ032_02 | MQ_032 | 2 | Stabilize outer gate camp. | Social | LOC_CH032_OUTER_GATE | 1 | Main Quest objective 2. |
| OBJ_MQ032_03 | MQ_032 | 3 | Disable automated turrets. | Sabotage | LOC_CH032_OUTER_GATE | 1 | Main Quest objective 3. |
| OBJ_MQ032_04 | MQ_032 | 4 | Negotiate with Hayes and Sloane. | Dialogue | npc_hayes | 1 | Main Quest objective 4. |
| OBJ_MQ032_05 | MQ_032 | 5 | Classify EDENROT Shelter Capacity Engine. | Investigation | LOC_CH032_INTAKE_TUNNEL | 1 | Main Quest objective 5. |
| OBJ_MQ032_06 | MQ_032 | 6 | Use Mentor command code. | Interaction | LOC_CH032_SECURITY_VESTIBULE | 1 | Main Quest objective 6. |
| OBJ_MQ032_07 | MQ_032 | 7 | Establish shelter rotation protocol. | Social | LOC_CH032_INTAKE_TUNNEL | 1 | Main Quest objective 7. |
| OBJ_MQ032_08 | MQ_032 | 8 | Dispute capacity engine with public ledger. | Social | LOC_CH032_INTAKE_TUNNEL | 1 | Main Quest objective 8. |
| OBJ_MQ032_09 | MQ_032 | 9 | Prevent intake tunnel panic. | Protect | LOC_CH032_INTAKE_TUNNEL | 1 | Main Quest objective 9. |
| OBJ_MQ032_10 | MQ_032 | 10 | Restore lower bunker power. | Exploration | LOC_CH032_LOWER_BUNKER | 1 | Main Quest objective 10. |
| OBJ_MQ032_11 | MQ_032 | 11 | Investigate sealed infection breach. | Investigation | LOC_CH032_LOWER_BUNKER | 1 | Main Quest objective 11. |
| OBJ_MQ032_12 | MQ_032 | 12 | Split teams for assault. | Management | LOC_CH032_COMMAND_LIFT | 1 | Main Quest objective 12. |
| OBJ_MQ032_13 | MQ_032 | 13 | Defend civilian intake. | Combat | LOC_CH032_INTAKE_TUNNEL | 1 | Main Quest objective 13. |
| OBJ_MQ032_14 | MQ_032 | 14 | Reach deep command chamber. | GoTo | LOC_CH032_DEEP_COMMAND_CHAMBER | 1 | Main Quest objective 14. |
| OBJ_MQ032_15 | MQ_032 | 15 | Defeat King infected. | Boss | npc_king_infected | 1 | Main Quest objective 15. |
| OBJ_MQ032_16 | MQ_032 | 16 | Bring satellite interface online. | Interaction | LOC_CH032_SATELLITE_CONTROL_ROOM | 1 | Main Quest objective 16. |
| OBJ_MQ032_17 | MQ_032 | 17 | Block VALE command injection. | Interaction | LOC_CH032_SATELLITE_CONTROL_ROOM | 1 | Main Quest objective 17. |
| OBJ_MQ032_18 | MQ_032 | 18 | Set satellite safe mode. | Interaction | LOC_CH032_SATELLITE_CONTROL_ROOM | 1 | Main Quest objective 18. |
| OBJ_MQ032_19 | MQ_032 | 19 | Prepare global broadcast window. | Interaction | LOC_CH032_SATELLITE_CONTROL_ROOM | 1 | Main Quest objective 19. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ032_01_001 | SQ_032_01 | Collect names publicly and stop forged priority bands. | PublicIntakeLedger. | SQ_NORAD_01. |
| OBJ_SQ032_02_001 | SQ_032_02 | Present dog tag and complete legacy challenge response. | MentorCodeAccepted; emotional memory. | SQ_NORAD_02. |
| OBJ_SQ032_03_001 | SQ_032_03 | Classify medical urgency and create rotation instead of permanent exclusion. | ShelterRotationProtocol. | SQ_NORAD_03. |
| OBJ_SQ032_04_001 | SQ_032_04 | Identify pulse rhythm and reverse speakers against King. | KingPulseCountermeasure. | SQ_NORAD_04. |
| OBJ_SQ032_05_001 | SQ_032_05 | Air-gap core and manually approve safe mode. | GlobalBroadcastWindow. | SQ_NORAD_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ032_INTAKE_CRUSH | MQ_032 | Intake tunnel riot/crush kills civilians. | Civilian casualties. | Metadata. |
| FAIL_MQ032_MENTOR_CODE_MISSING | MQ_032 | Mentor code not recovered/entered. | Destructive breach required. | Metadata. |
| FAIL_MQ032_KING_REACHES_CIVILIANS | MQ_032 | King infected reaches civilian levels. | Mass casualties. | Metadata. |
| FAIL_MQ032_VALE_GAINS_CONTROL | MQ_032 | VALE gains command authority over satellite. | Automated targeting enabled. | Metadata. |
| FAIL_MQ032_CIVIL_WAR | MQ_032 | Bunker capacity decision creates faction civil war. | Alliance broken. | Metadata. |
| FAIL_MQ032_SATELLITE_DESTROYED | MQ_032 | Satellite interface destroyed before broadcast. | Global broadcast lost. | Metadata. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ032_NORAD_HUB | MQ_032 | location_unlock | NORAD bunker partial hub | Rewards section. |
| REW_MQ032_SATELLITE_ACCESS | MQ_032 | system_unlock | Satellite network partial access | Rewards section. |
| REW_MQ032_BROADCAST_WINDOW | MQ_032 | system_unlock | Global broadcast window | Rewards section. |
| REW_MQ032_KING_DATA | MQ_032 | lore_item | King infected data | Rewards section. |
| REW_MQ032_ROTATION_PROTOCOL | MQ_032 | governance_flag | Shelter rotation protocol | Rewards section. |
| REW_MQ032_MENTOR_PAYOFF | MQ_032 | story_flag | Mentor quest payoff (CQ_MENTOR_04) | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH032_NORAD_HUB | MQ_032 | NORAD bunker partial hub | Bunker secured. |
| UNLOCK_CH032_SATELLITE_ACCESS | MQ_032 | Satellite network partial access | Interface online. |
| UNLOCK_CH032_GLOBAL_BROADCAST | MQ_032 | Global broadcast window | Safe mode set. |
| UNLOCK_CH032_MQ033 | MQ_032 | MQ_033 Global Signal | Broadcast window opened. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH032_MENTOR_CODE_ACCEPTED | MQ_032 | Mentor legacy challenge passed. |
| FLAG_CH032_SHELTER_ROTATION_PROTOCOL | MQ_032 | Transparent triage established. |
| FLAG_CH032_KING_INFECTED_DEFEATED | MQ_032 | King destroyed in deep chamber. |
| FLAG_CH032_SATELLITE_NETWORK_PARTIAL_ONLINE | MQ_032 | Satellite interface activated. |
| FLAG_CH032_VALE_COMMAND_INJECTION_BLOCKED | MQ_032 | VALE denied target authority. |
| FLAG_CH032_GLOBAL_BROADCAST_WINDOW | MQ_032 | 4-hour window opened. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_032_01 | Steel Door and the List | npc_hayes | Collect names publicly; stop forged priority bands. | PublicIntakeLedger. | SQ_NORAD_01. |
| SQ_032_02 | Mentor's Command Code | npc_pike | Present dog tag; complete challenge response. | MentorCodeAccepted. | SQ_NORAD_02. |
| SQ_032_03 | Who Gets In | comp_mai | Classify urgency; create rotation instead of exclusion. | ShelterRotationProtocol. | SQ_NORAD_03. |
| SQ_032_04 | King Underground | comp_binh | Identify pulse rhythm; reverse speakers. | KingPulseCountermeasure. | SQ_NORAD_04. |
| SQ_032_05 | Satellite Wakes Up | npc_thu | Air-gap core; approve safe mode; reject targeting. | GlobalBroadcastWindow. | SQ_NORAD_05. |

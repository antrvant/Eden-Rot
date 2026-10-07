# Quests - CH006

Metadata:

- chapterID: CH006
- sourceFilename: chapter_006_nguoi_day_cach_song_sot.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_006 | Meet Mentor | main | automatic | Starts after MQ_005 when Trung and Hoang reach the real army outpost | Mentor accepts training Trung after the fence rescue test | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ006_001 | MQ_006 | 1 | Reach the real army outpost. | GoTo | LOC_CH006_REAL_OUTPOST_GATE | 1 | Main Quest objective 1. |
| OBJ_MQ006_002 | MQ_006 | 2 | Pass the bite inspection at the gate. | Inspect | LOC_CH006_DECONTAMINATION_LINE | 1 | Main Quest objective 2. |
| OBJ_MQ006_003 | MQ_006 | 3 | Deliver evidence from the false safe zone if collected. | EvidenceTurnIn | ITM_CH006_FALSE_SAFE_EVIDENCE_BUNDLE | 1 | Main Quest objective 3 and SQ_Outpost_04. |
| OBJ_MQ006_004 | MQ_006 | 4 | Meet the doctor in triage. | TalkTo | npc_doctor | 1 | Main Quest objective 4. |
| OBJ_MQ006_005 | MQ_006 | 5 | Visit the radio tent to check for Mai and Binh. | GoTo | LOC_CH006_RADIO_TENT | 1 | Main Quest objective 5. |
| OBJ_MQ006_006 | MQ_006 | 6 | Confront Mentor. | TalkTo | npc_mentor | 1 | Main Quest objective 6. |
| OBJ_MQ006_007 | MQ_006 | 7 | React to the radio fragment that sounds like Mai. | NarrativeChoice | ITM_CH006_NOISY_MAI_SIGNAL | 1 | Main Quest objective 7. |
| OBJ_MQ006_008 | MQ_006 | 8 | Protect or assist the young soldier outside the fence. | TimedRescue | npc_phuc | 1 | Main Quest objective 8. |
| OBJ_MQ006_009 | MQ_006 | 9 | Accept the training arc with Mentor. | ProgressionUnlock | npc_mentor | 1 | Main Quest objective 9. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ006_01_001 | SQ_006_01 | Help the doctor distribute scarce medicine. | Doctor trust and small medkit. | SQ_Outpost_01. |
| OBJ_SQ006_01_002 | SQ_006_01 | Find more antiseptic or medical supplies. | Improves triage outcome. | SQ_Outpost_01. |
| OBJ_SQ006_02_001 | SQ_006_02 | Search for the missing volunteer outside the outpost. | MentorRespect +1 if handled calmly. | SQ_Outpost_02. |
| OBJ_SQ006_03_001 | SQ_006_03 | Gather radio filter parts from supply depot or comms vehicle. | Improves odds of finding Mai signal in Chapter 09. | SQ_Outpost_03. |
| OBJ_SQ006_04_001 | SQ_006_04 | Turn in the fake military stamp to commander or Mentor. | Increases Army trust if explained clearly. | SQ_Outpost_04. |
| OBJ_SQ006_04_002 | SQ_006_04 | Give the fake stamp to Hoang for analysis or keep it. | Changes Army trust and Hoang pragmatism. | SQ_Outpost_04. |
| OBJ_SQ006_05_001 | SQ_006_05 | Identify the refugee hiding a bite. | Prevents triage outbreak risk. | SQ_Outpost_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ006_HEALTH_ZERO | MQ_006 | Trung dies during fence attack or outpost incident. | Reload checkpoint. | Scene 6. |
| FAIL_MQ006_GATE_REJECTED | MQ_006 | Player attacks outpost staff or fails bite check rules. | Outpost access blocked or hostile checkpoint state. | Scene 2. |
| FAIL_MQ006_PHUC_DEAD | MQ_006 | Player ignores or fails timed rescue. | MentorRespect lost; Phuc dies; training acceptance may be harsher. | Scene 6. |
| FAIL_SQ006_05_HIDDEN_BITE_TURNS | SQ_006_05 | Hidden bite is not discovered and patient turns. | Triage outbreak and trust loss. | SQ_Outpost_05. |
| FAIL_SQ006_03_NO_FILTER_PARTS | SQ_006_03 | Player ignores radio parts. | Lower future radio clue clarity. | SQ_Outpost_03. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ006_ARMY_OUTPOST_HUB | MQ_006 | hub_unlock | Army Outpost | Rewards section. |
| REW_MQ006_MENTOR_TRAINER | MQ_006 | trainer_unlock | npc_mentor | Rewards section. |
| REW_MQ006_ARMY_TRUST | MQ_006 | faction_unlock | Basic military trust | Rewards section. |
| REW_MQ006_RADIO_TIER_1 | MQ_006 | system_unlock | Radio clue system tier 1 | Rewards section. |
| REW_MQ006_NOISY_MAI_SIGNAL | MQ_006 | item | ITM_CH006_NOISY_MAI_SIGNAL | Rewards section. |
| REW_MQ006_FALSE_SAFE_EVIDENCE | MQ_006 | evidence | ITM_CH006_FALSE_SAFE_EVIDENCE_BUNDLE | Rewards section. |
| REW_MQ006_MENTOR_RESPECT | MQ_006 | relationship_flag | MentorRespect +1 if Phuc is rescued or Trung stays calm | Rewards section. |
| REW_MQ006_DISCIPLINE_SEED | MQ_006 | progression_flag | DisciplineSeed +1 when training is accepted | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH006_FACTION_VERIFICATION | MQ_006 | Faction verification | Reach real outpost gate. |
| UNLOCK_CH006_BITE_INSPECTION | MQ_006 | Suspicion/inspection | Bite check line. |
| UNLOCK_CH006_TRIAGE_CHOICE | MQ_006 | Resource moral choice | Doctor triage scene. |
| UNLOCK_CH006_RADIO_CLUE_TIER_1 | MQ_006 | Radio clue system tier 1 | Radio fragment heard. |
| UNLOCK_CH006_SKILL_GATE | MQ_006 | Mentor skill gate | Mentor confrontation. |
| UNLOCK_CH006_TIMED_RESCUE_COMBAT | MQ_006 | Combat + timed rescue | Fence test. |
| UNLOCK_CH006_TRAINING_ARC | MQ_006 | Training arc | Mentor accepts Trung. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH006_ARMY_OUTPOST_UNLOCKED | MQ_006 | Player reaches and passes initial outpost flow. |
| FLAG_CH006_RADIO_FRAGMENT_MAI_HEARD | MQ_006 | Radio plays noisy Mai-like fragment. |
| FLAG_CH006_PHUC_RESCUED | MQ_006 | Player rescues Phuc at the fence. |
| FLAG_CH006_MENTOR_RESPECT_PLUS | MQ_006 | Mentor sees Trung act with discipline/compassion. |
| FLAG_CH006_DISCIPLINE_SEED | MQ_006 | Trung accepts training. |
| FLAG_CH006_MENTOR_TRAINING_ACCEPTED | MQ_006 | Chapter ends with Mentor training unlock. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_006_01 | Trade Supplies for Medicine | npc_doctor | Help allocate medicine or find more antiseptic. | Doctor trust and medkit reward; cure ethics seed. | SQ_Outpost_01. |
| SQ_006_02 | Missing Volunteer | npc_young_guard | Find volunteer who left for water and did not return. | MentorRespect +1 if handled calmly. | SQ_Outpost_02. |
| SQ_006_03 | Radio Noise | npc_radio_operator | Gather filter parts to improve signal clarity. | Improves future Mai signal odds in Chapter 09. | SQ_Outpost_03. |
| SQ_006_04 | Fake Stamp | automatic if collected in CH005 | Turn in, keep, or ask Hoang to analyze fake military stamp. | Affects Army trust and Hoang pragmatism. | SQ_Outpost_04. |
| SQ_006_05 | The Lying Bite | bite inspection trigger | Discover or handle a refugee hiding a bite wound. | Tests compassion versus procedure. | SQ_Outpost_05. |

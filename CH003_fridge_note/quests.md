# Quests - CH003

Metadata:

- chapterID: CH003
- sourceFilename: chapter_003_loi_nhan_tren_tu_lanh.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_003 | Find First Clue | main | Mai's fridge note | Starts after Trung reads the fridge note and finds the apartment empty | Trung identifies the northern military checkpoint route from chalk marks, tracks, and Hoang's call | Metadata lists MQ_003 - Find First Clue; Main Quest section gives premise and objectives. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ003_001 | MQ_003 | 1 | Reread Mai's note on the fridge. | Inspect | ITM_CH003_FRIDGE_NOTE | 1 | Main Quest objective 1. |
| OBJ_MQ003_002 | MQ_003 | 2 | Search the apartment: living room, Binh's room, kitchen, and balcony. | Investigate | LOC_CH003_TRUNG_APARTMENT_1208 | 4 | Main Quest objective 2. |
| OBJ_MQ003_003 | MQ_003 | 3 | Find the first chalk mark outside the apartment. | Track | ITM_CH003_CHALK_ARROW | 1 | Main Quest objective 3. |
| OBJ_MQ003_004 | MQ_003 | 4 | Ask the neighbor about Mai and Binh. | TalkTo | npc_neighbor | 1 | Main Quest objective 4. |
| OBJ_MQ003_005 | MQ_003 | 5 | Follow the chalk marks down to the ground floor mini mart. | Track | LOC_CH003_GROUND_MINIMART | 1 | Main Quest objective 5. |
| OBJ_MQ003_006 | MQ_003 | 6 | Collect medicine, milk, or battery supplies if possible. | Scavenge | LOC_CH003_GROUND_MINIMART | 1 | Main Quest objective 6. |
| OBJ_MQ003_007 | MQ_003 | 7 | Check the apartment building's back exit. | GoTo | LOC_CH003_NORTH_BACK_ALLEY | 1 | Main Quest objective 7. |
| OBJ_MQ003_008 | MQ_003 | 8 | Determine Mai and Binh's next direction: north toward the military checkpoint. | IdentifyClue | ITM_CH003_NORTH_CHALK_MARK | 1 | Main Quest objective 8. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ003_01_001 | SQ_003_01 | Find five white chalk marks inside and around the apartment building. | Confirms Mai/Binh's route and unlocks tracking motif. | SQ_Apt_01. |
| OBJ_SQ003_02_001 | SQ_003_02 | Trade water, medicine, or food for neighbor information. | Reveals safer northern route; may affect Chapter 05 apartment NPC opinion. | SQ_Apt_02. |
| OBJ_SQ003_02_002 | SQ_003_02 | Expose or intimidate the lying neighbor. | Gets information faster but creates resentment. | DT_009. |
| OBJ_SQ003_03_001 | SQ_003_03 | Recover Ba Bay's medicine bag from the ground floor/medical room area. | Medkit x2 and possible future Ba Bay support. | SQ_Apt_03. |
| OBJ_SQ003_04_001 | SQ_003_04 | Open the locked apartment and identify whether someone inside is alive. | Can rescue `npc_locked_child` and receive clue about Mai's group. | SQ_Apt_04. |
| OBJ_SQ003_04_002 | SQ_003_04 | Mark the locked apartment for later instead of entering. | Avoids immediate risk but delays rescue. | Scene 5 choice. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ003_HEALTH_ZERO | MQ_003 | Trung is killed by apartment infected, trapped stairwell infected, or Bloater hazard. | Reload checkpoint. | Gameplay beats include locked apartment, stealth loot, and mutation hazard. |
| FAIL_MQ003_CLUE_MISSED | MQ_003 | Player leaves without identifying the north checkpoint clue. | Main quest cannot complete; return to back alley/clue search. | Main Quest objective 8. |
| FAIL_SQ003_03_MEDICINE_LEFT | SQ_003_03 | Player leaves Ba Bay's medicine behind. | Ba Bay's future support remains uncertain. | SQ_Apt_03. |
| FAIL_SQ003_04_CHILD_LEFT | SQ_003_04 | Player skips or abandons the locked child. | Guilt/Pragmatism route; clue may require alternate source. | SQ_Apt_04 and Scene 5. |
| FAIL_SQ003_BLOATER_NOISE | MQ_003 | Player makes loud noise near the bloated corpse. | Optional Bloater hazard may activate or force retreat. | Scene 4. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ003_TRACKING_CLUES | MQ_003 | system_unlock | Tracking clues | Rewards section. |
| REW_MQ003_NORTH_CHECKPOINT | MQ_003 | quest_unlock | Go to the northern military checkpoint | Rewards section and ending hook. |
| REW_MQ003_FOLDED_FAMILY_PHOTO | MQ_003 | item | ITM_CH003_FOLDED_FAMILY_PHOTO | Rewards section. |
| REW_MQ003_MAI_CHALK | MQ_003 | item | ITM_CH003_MAI_WHITE_CHALK | Rewards section. |
| REW_MQ003_FAMILY_TRUST | MQ_003 | moral_flag | FamilyTrust +1 when Trung trusts Mai's trail | Rewards section and DT_007. |
| REW_MQ003_COMPASSION | MQ_003 | moral_flag | Compassion +1 if the locked child is rescued | Rewards section and SQ_Apt_04. |
| REW_MQ003_PRAGMATISM | MQ_003 | moral_flag | Pragmatism +1 if Trung skips optional rescues to follow the trail fast | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH003_INVESTIGATION | MQ_003 | Investigation tutorial | Search the empty apartment. |
| UNLOCK_CH003_TRACKING_MARKERS | MQ_003 | Tracking marker system | Find first chalk arrow. |
| UNLOCK_CH003_SOCIAL_CHECK | MQ_003 | Dialogue/social check | Confront lying neighbor. |
| UNLOCK_CH003_STEALTH_LOOT | MQ_003 | Stealth loot | Enter mini mart near Bloater foreshadow. |
| UNLOCK_CH003_AVOIDANCE_HAZARD | MQ_003 | Avoidance/hazard tutorial | See bloated corpse mutation. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH003_TRACKING_CLUES_UNLOCKED | MQ_003 | Player finds and understands the chalk trail. |
| FLAG_CH003_BLOATER_FORESHADOW_SEEN | MQ_003 | Player sees bloated corpse in mini mart. |
| FLAG_CH003_LOCKED_CHILD_RESCUED | SQ_003_04 | Player rescues `npc_locked_child`. |
| FLAG_CH003_BA_BAY_MET | SQ_003_03 | Player meets Ba Bay. |
| FLAG_CH003_MEDICINE_RECOVERED | SQ_003_03 | Player recovers medicine bag. |
| FLAG_CH003_NORTH_CHECKPOINT_CLUE_UNLOCKED | MQ_003 | Player finds final north checkpoint arrow/tracks. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_003_01 | White Chalk Marks | Mai's note | Find five chalk marks and learn the tracking motif. | Establishes chalk as a continuing Mai/Binh trail motif in Chapters 04-05. | SQ_Apt_01. |
| SQ_003_02 | Neighbor Trade | Floor 9 neighbor | Trade, threaten, lie, or bypass to get information. | Affects how apartment NPCs speak about Trung in Chapter 05. | SQ_Apt_02. |
| SQ_003_03 | Ba Bay's Medicine Cabinet | npc_ba_bay | Recover medicine/antiseptic from the ground floor area. | Medkit x2; Ba Bay may become a future base/caretaker NPC if confirmed later. | SQ_Apt_03. |
| SQ_003_04 | The Locked Apartment | knocking inside apartment | Open the locked apartment, rescue the trapped child, or avoid risk. | Compassion +1 and clue about Mai's teacher group; unresolved name conflict tracked in validation. | SQ_Apt_04. |

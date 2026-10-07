# Quests - CH049

Metadata:

- chapterID: CH049
- sourceFilename: chapter_049_trai_tim_duoi_bang.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_049 | Destroy or Rewrite | main | char_trung | CH048 completed, under-ice entry available | Final choice conditions evaluated, options armed, final battlefield triggered, CH050 unlocked | Metadata and Main Quest. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ049_01 | MQ_049 | 1 | Enter under-ice Source access tunnel. | GoTo | LOC_CH049_UNDER_ICE_DOOR | 1 | Scene 1. |
| OBJ_MQ049_02 | MQ_049 | 2 | Establish Guardian Circle under ice. | Dialogue | char_mai | 1 | Scene 1. |
| OBJ_MQ049_03 | MQ_049 | 3 | Carry consent-bound Source dream rules into core. | System | char_mai | 1 | Scene 1. |
| OBJ_MQ049_04 | MQ_049 | 4 | Investigate Archive of Repetition. | Explore | LOC_CH049_ARCHIVE_CORRIDOR | 1 | Scene 2. |
| OBJ_MQ049_05 | MQ_049 | 5 | Receive Prime first contact. | Event | npc_prime | 1 | Scene 2. |
| OBJ_MQ049_06 | MQ_049 | 6 | Identify Merciful Erasure argument. | Lore | npc_prime | 1 | Scene 2. |
| OBJ_MQ049_07 | MQ_049 | 7 | Stabilize Hoang cold signal for warning. | Dialogue | comp_hoang | 1 | Scene 3. |
| OBJ_MQ049_08 | MQ_049 | 8 | Reach Source nursery threshold. | GoTo | LOC_CH049_NURSERY_THRESHOLD | 1 | Scene 4. |
| OBJ_MQ049_09 | MQ_049 | 9 | Survive Mother phase one. | Combat | npc_mother | 1 | Scene 5. |
| OBJ_MQ049_10 | MQ_049 | 10 | Refuse permanent Binh cure bridge. | Choice | npc_prime | 1 | Scene 6. |
| OBJ_MQ049_11 | MQ_049 | 11 | Reject child-as-infrastructure cure model. | Choice | npc_prime | 1 | Scene 6. |
| OBJ_MQ049_12 | MQ_049 | 12 | Redirect Mother nursery flows instead of destroying. | Puzzle | npc_mother | 1 | Scene 7. |
| OBJ_MQ049_13 | MQ_049 | 13 | Confront Prime's reset argument. | Dialogue | npc_prime | 1 | Scene 8. |
| OBJ_MQ049_14 | MQ_049 | 14 | Free Binh from forced core connection. | Rescue | char_binh | 1 | Scene 9. |
| OBJ_MQ049_15 | MQ_049 | 15 | Anchor Binh with names and trust. | Dialogue | char_binh | 1 | Scene 9. |
| OBJ_MQ049_16 | MQ_049 | 16 | Evaluate final choice conditions. | System | LOC_CH049_CHOICE_CONSOLE | 1 | Scene 11. |
| OBJ_MQ049_17 | MQ_049 | 17 | Arm destroy/reset/rewrite options. | System | LOC_CH049_CHOICE_CONSOLE | 1 | Scene 11. |
| OBJ_MQ049_18 | MQ_049 | 18 | Trigger final battlefield. | Event | LOC_CH049_CORE_CATHEDRAL | 1 | Scene 12. |
| OBJ_MQ049_19 | MQ_049 | 19 | Unlock Chapter 50 final choice. | Unlock | MQ_050 | 1 | Scene 12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ049_A_001 | SQ_049_A | Recover Patient Zero/Elise echo from Source archive. | EliseWitnessIntegrated; improves cure rewrite path. | SQ_049_A. |
| OBJ_SQ049_B_001 | SQ_049_B | Keep Hoang comm line stable for warning about relief traps. | HoangWarnedAboutCleanRelief flag. | SQ_049_B. |
| OBJ_SQ049_C_001 | SQ_049_C | Respect Rafi's refusal of Source scan. | ChildrenCollectiveConsentStrength high. | SQ_049_C. |
| OBJ_SQ049_D_001 | SQ_049_D | Use bio-covenant knowledge to redirect Mother nursery. | MotherNurseryPreservedPartial flag. | SQ_049_D. |
| OBJ_SQ049_E_001 | SQ_049_E | Use Mateo tap code as anchor rhythm for Binh inside core. | BinhAnchorCodeActive flag. | SQ_049_E. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ049_BINH_TRUST_LOW | MQ_049 | Binh trust too low to resist Prime. | Binh cannot resist internally; CH050 endings affected. | Scene 9. |
| FAIL_MQ049_CHILDREN_USED_AS_ARRAY | MQ_049 | Immune children used as resonance array. | Guardian Circle fails; humane rewrite locked. | Scene 5. |
| FAIL_MQ049_MOTHER_DESTROYED_CARELESSLY | MQ_049 | Mother nursery destroyed entirely. | Rewrite possibility damaged. | Scene 7. |
| FAIL_MQ049_RESET_AUTHORIZED_EARLY | MQ_049 | Prime reset authorized before final choice. | Bad ending setup. | Scene 8. |
| FAIL_MQ049_GUARDIAN_CIRCLE_ABANDONED | MQ_049 | Guardian Circle abandoned under planetary pressure. | Humane paths locked. | Scene 1. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ049_FINAL_CHOICE_MATRIX | MQ_049 | system_unlock | Destroy/Reset/Rewrite/Hybrid conditions | Scene 11. |
| REW_MQ049_EDENROT_MERCIFUL_ERASURE | MQ_049 | system_unlock | Prime's reset/cure temptation classifier | Scene 2. |
| REW_MQ049_SOURCE_CORE | MQ_049 | system_unlock | Final battlefield environment | Scene 12. |
| REW_MQ049_BINH_TRUST_CHECK | MQ_049 | system_unlock | Ending condition evaluation | Scene 9. |
| REW_MQ049_MOTHER_NURSERY | MQ_049 | system_unlock | Preserved/destroyed ecology state | Scene 7. |
| REW_MQ049_PRIME_ARGUMENT | MQ_049 | system_unlock | Final antagonist logic | Scene 8. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH049_SOURCE_ENTRY | MQ_049 | Under-ice Source access | Chapter begins. |
| UNLOCK_CH049_MOTHER_ENCOUNTER | MQ_049 | Mother boss fight | Nursery threshold reached. |
| UNLOCK_CH049_CHOICE_MATRIX | MQ_049 | Final choice evaluation system | Core cathedral reached. |
| UNLOCK_CH049_CH050 | MQ_049 | Chapter 50 Final Choice | Final battlefield triggered. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH049_EDENROT_MERCIFUL_ERASURE_CATHEDRAL_IDENTIFIED | MQ_049 | Prime's temptation pattern identified. |
| FLAG_CH049_SOURCE_DREAM_DATA_CONSENT_BOUND_CARRIED_INTO_CORE | MQ_049 | Consent rules carry into Source analysis. |
| FLAG_CH049_CHILD_INFRASTRUCTURE_CURE_MODEL_REJECTED | MQ_049 | Permanent Binh bridge refused. |
| FLAG_CH049_BRIDGE_DATA_NOT_USED_DURING_VIOLATION | MQ_049 | Bridge data not used during Binh's forced connection. |
| FLAG_CH049_BINH_STOP_WORD_HONORED_SOURCE | MQ_049 | Stop word honored when Binh connected. |
| FLAG_CH049_CH50_FINAL_CHOICE_UNLOCKED | MQ_049 | Chapter 50 unlocked. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_049_A | Elise Echo | npc_elise_echo | Recover Patient Zero echo from Source archive. | EliseWitnessIntegrated; improves cure rewrite. | SQ_049_A. |
| SQ_049_B | Hoang Warning | comp_hoang | Keep Hoang comm line stable for relief trap warning. | HoangWarnedAboutCleanRelief flag. | SQ_049_B. |
| SQ_049_C | Rafi Says No Again | npc_rafi | Respect Rafi's refusal of Source scan. | ChildrenCollectiveConsentStrength high. | SQ_049_C. |
| SQ_049_D | Nia's Covenant Under Ice | npc_nia | Use bio-covenant to redirect Mother nursery. | MotherNurseryPreservedPartial flag. | SQ_049_D. |
| SQ_049_E | Mateo Anchor Code | npc_mateo | Mateo tap code becomes Binh's anchor rhythm. | BinhAnchorCodeActive flag. | SQ_049_E. |

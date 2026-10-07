# Quests - CH045

Metadata:

- chapterID: CH045
- sourceFilename: chapter_045_ke_ban_minh_hai_lan.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_045 | Confront Hoang | main | automatic | Hoang appears at inner gate in Architect armor | Hoang fate chosen; Orison child transfer discovered; Chapter 46 unlocked | Metadata: MQ_045 - Confront Hoang. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ045_001 | MQ_045 | 1 | Face Hoang at inner gate. | GoTo | LOC_CH045_INNER_GATE | 1 | Scene 1. |
| OBJ_MQ045_002 | MQ_045 | 2 | Identify PAIN RELIEF OWNERSHIP LOOP. | Interact | LOC_CH045_INNER_GATE | 1 | Scene 1; EDENROT marker. |
| OBJ_MQ045_003 | MQ_045 | 3 | Reject Binh interface demand. | Choice | LOC_CH045_INNER_GATE | 1 | Scene 2. |
| OBJ_MQ045_004 | MQ_045 | 4 | Enter Aster memory chamber. | GoTo | LOC_CH045_MEMORY_CHAMBER | 1 | Scene 3. |
| OBJ_MQ045_005 | MQ_045 | 5 | Survive Hoang non-lethal assault. | CombatOrEscape | LOC_CH045_CITADEL_CORE_APPROACH | 1 | Scene 4. |
| OBJ_MQ045_006 | MQ_045 | 6 | Confront smoke and debt memory. | Dialogue | LOC_CH045_MEMORY_CHAMBER | 1 | Scene 5. |
| OBJ_MQ045_007 | MQ_045 | 7 | Confront coordinate betrayal memory. | Dialogue | LOC_CH045_MEMORY_CHAMBER | 1 | Scene 6. |
| OBJ_MQ045_008 | MQ_045 | 8 | Refuse child pulse stabilization. | Choice | LOC_CH045_COMMAND_OVERLAY_ZONE | 1 | Scene 7. |
| OBJ_MQ045_009 | MQ_045 | 9 | Establish relief is not consent. | Dialogue | LOC_CH045_COMMAND_OVERLAY_ZONE | 1 | Scene 7. |
| OBJ_MQ045_010 | MQ_045 | 10 | Disable armor command nodes. | Combat | LOC_CH045_COMMAND_OVERLAY_ZONE | 1 | Scene 8. |
| OBJ_MQ045_011 | MQ_045 | 11 | Protect Yusuf if he volunteers. | Choice | LOC_CH045_COMMAND_OVERLAY_ZONE | 1 | Scene 8. |
| OBJ_MQ045_012 | MQ_045 | 12 | Expose sync spine. | Combat | LOC_CH045_COMMAND_OVERLAY_ZONE | 1 | Scene 8. |
| OBJ_MQ045_013 | MQ_045 | 13 | Choose Hoang fate. | Choice | LOC_CH045_CHOICE_CHAMBER | 1 | Scene 9. |
| OBJ_MQ045_014 | MQ_045 | 14 | Capture Hoang (canon). | CombatOrEscape | LOC_CH045_CHOICE_CHAMBER | 1 | Scene 10. |
| OBJ_MQ045_015 | MQ_045 | 15 | Interrupt ownership loop. | Interact | LOC_CH045_RESTRAINT_AREA | 1 | Scene 10. |
| OBJ_MQ045_016 | MQ_045 | 16 | Stabilize Hoang in stasis. | Interact | LOC_CH045_RESTRAINT_AREA | 1 | Scene 10. |
| OBJ_MQ045_017 | MQ_045 | 17 | Discover Orison child transfer. | Interact | LOC_CH045_PRISON_LAB_ENTRANCE | 1 | Scene 11. |
| OBJ_MQ045_018 | MQ_045 | 18 | Unlock Chapter 46 Free Children. | Progression | LOC_CH045_PRISON_LAB_ENTRANCE | 1 | Scene 12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ045_A_001 | SQ_045_A | Recover Hoang's signed restraint order from Cairo data. | HoangRestraintOrderInvoked flag. | SQ_045_A. |
| OBJ_SQ045_B_001 | SQ_045_B | Find optional smoke memory shard from early apocalypse. | FriendshipDebtAcknowledged flag. | SQ_045_B. |
| OBJ_SQ045_C_001 | SQ_045_C | Quarantine armor sync data; keep only mechanical weakness map. | ArmorEthicsMaintained flag. | SQ_045_C. |
| OBJ_SQ045_D_001 | SQ_045_D | Allow Yusuf to assist only after clear consent and safe distance. | YusufAgencyRespected flag. | SQ_045_D. |
| OBJ_SQ045_E_001 | SQ_045_E | Binh directly tells Hoang he loves him and refuses him. | BinhBoundaryWithLovedOne flag. | SQ_045_E. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ045_BINH_COERCED | MQ_045 | Binh coerced into pulse. | Major trust damage; CureMoralFlag broken. | Failure Conditions. |
| FAIL_MQ045_HOANG_KILLED | MQ_045 | Hoang killed unintentionally. | Deep family trauma; redemption arc removed. | Failure Conditions. |
| FAIL_MQ045_HOANG_ESCAPES | MQ_045 | Hoang escapes with full sync. | Stronger enemy in Chapter 47. | Failure Conditions. |
| FAIL_MQ045_YUSUF_USED | MQ_045 | Yusuf used without consent. | Personhood violated. | Failure Conditions. |
| FAIL_MQ045_SYNC_SPINE_INTACT | MQ_045 | Armor sync spine remains intact. | Hoang cannot be stabilized. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ045_HOANG_FATE | MQ_045 | fate_lock | HoangCapturedAlive | Completion. |
| REW_MQ045_OWNERSHIP_BREAK | MQ_045 | knowledge | OwnershipLoopInterrupted | Completion. |
| REW_MQ045_RELIEF_CONSENT | MQ_045 | knowledge | ReliefIsNotConsent | Completion. |
| REW_MQ045_PRISON_ROUTE | MQ_045 | route_unlock | PrisonLabWingUnlocked | Completion. |
| REW_MQ045_CH046_ACCESS | MQ_045 | chapter_unlock | Chapter 46 Free Children | Completion. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH045_FATE_CHOICE | MQ_045 | Hoang fate branch (kill/spare/capture) | Reach choice chamber. |
| UNLOCK_CH045_NON_LETHAL_TARGETING | MQ_045 | Armor joint and sync spine targeting | Enter combat phase. |
| UNLOCK_CH045_MEMORY_DIALOGUE | MQ_045 | Truth-based memory dialogue system | Enter memory chamber. |
| UNLOCK_CH045_BOUNDARY_SYSTEM | MQ_045 | Binh can refuse loved NPC requests | Binh refuses pulse. |
| UNLOCK_CH045_PRISON_LAB_WING | MQ_045 | Chapter 46 route | Capture Hoang; discover transfer. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH045_PAIN_RELIEF_OWNERSHIP_LOOP | MQ_045 | Samir classifies armor loop. |
| FLAG_CH045_RELIEF_NOT_CONSENT | MQ_045 | Mai establishes before Binh pulse demand. |
| FLAG_CH045_BINH_PULSE_REFUSED | MQ_045 | All refuse Binh interface demand. |
| FLAG_CH045_HOANG_CAPTURED_ALIVE | MQ_045 | Canon capture in stasis restraint. |
| FLAG_CH045_OWNERSHIP_LOOP_INTERRUPTED | MQ_045 | Samir installs restraint mode. |
| FLAG_CH045_ORISON_CHILD_TRANSFER | MQ_045 | Amelie discovers children moving. |
| FLAG_CH045_CH046_UNLOCKED | MQ_045 | Prison/lab wing door opens. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_045_A | The Old Restraint Order | automatic | Recover Hoang's signed restraint order from Cairo data. | HoangRestraintOrderInvoked; opens capture dialogue. | SQ_045_A. |
| SQ_045_B | Smoke Memory | automatic | Find optional memory shard where Hoang saved Trung in smoke. | FriendshipDebtAcknowledged; nuanced dialogue. | SQ_045_B. |
| SQ_045_C | No Clean Data | char_samir | Quarantine armor sync data tied to coercion; keep weakness map only. | ArmorEthicsMaintained. | SQ_045_C. |
| SQ_045_D | Yusuf's Choice | char_yusuf | Allow Yusuf to volunteer scanner distraction at safe distance. | YusufAgencyRespected. | SQ_045_D. |
| SQ_045_E | Binh Says No | char_binh | Binh directly tells Hoang he loves him and refuses him. | BinhBoundaryWithLovedOne; weakens Aster guilt leverage. | SQ_045_E. |

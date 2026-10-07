# Quests - CH042

Metadata:

- chapterID: CH042
- sourceFilename: chapter_042_mau_cua_con.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_042 | Decide Cure Protocol | main | automatic | Chapter start after Cairo evacuation to mobile lab | Blood Protocol established, minimal sample collected, firewall verified, Amazon route selected, cure moral flag locked | Metadata: Main Quest MQ_042 - Decide Cure Protocol. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| MQ_042_01 | MQ_042 | 1 | Stabilize mobile lab systems after Cairo evacuation. | Interact | LOC_CH042_MOBILE_LAB | 1 | Scene 01 - Mobile Lab Does Not Sleep. |
| MQ_042_02 | MQ_042 | 2 | Review first cure data and batch failure analysis. | Interact | ITM_CH042_CURE_DATA_RECORD | 1 | Scene 01 - Samir replays data. |
| MQ_042_03 | MQ_042 | 3 | Tell Binh the truth about resonance in age-appropriate language. | Dialogue | char_binh | 1 | Scene 02 - The Word No One Says. DT_262, DT_263. |
| MQ_042_04 | MQ_042 | 4 | Resolve the guardian conflict between Trung and Mai. | Choice | char_trung;char_mai | 1 | Scene 03 - Guardian Fight. |
| MQ_042_05 | MQ_042 | 5 | Establish the EDENROT CLASS: CHILD CONSENT FIREWALL. | Interact | ITM_CH042_BLOOD_PROTOCOL_DOC | 1 | Scene 04 - Ethics Table. |
| MQ_042_06 | MQ_042 | 6 | Draft Blood Protocol clauses and reject coercive wording. | Choice | ITM_CH042_BLOOD_PROTOCOL_DOC | 1 | Scene 04 - Protocol clause drafting. |
| MQ_042_07 | MQ_042 | 7 | Confirm Binh's informed consent and stop word choice. | Dialogue | char_binh | 1 | Scene 04 - Binh chooses stop word. |
| MQ_042_08 | MQ_042 | 8 | Secure communications against Masud's rumor. | Choice | LOC_CH042_AMAZON_PLANNING_ROOM | 1 | Scene 06 - Masud's Rumor. |
| MQ_042_09 | MQ_042 | 9 | Collect minimal blood sample from Binh. | Interact | char_binh | 1 | Scene 07 - The Small Needle. |
| MQ_042_10 | MQ_042 | 10 | Honor Binh's stop word and stop procedure immediately. | Choice | char_binh | 1 | Scene 07 - Stop word prompt. |
| MQ_042_11 | MQ_042 | 11 | Verify firewall by honoring stop word. | System | ITM_CH042_BLOOD_PROTOCOL_DOC | 1 | Scene 07 - Firewall verification. |
| MQ_042_12 | MQ_042 | 12 | Reconfirm consent or abort procedure. | Choice | char_binh | 1 | Scene 07 - Binh re-consents. |
| MQ_042_13 | MQ_042 | 13 | Run limited stability test on Binh's sample. | Interact | ITM_CH042_BINH_BLOOD_SAMPLE | 1 | Scene 08 - The Better Batch. |
| MQ_042_14 | MQ_042 | 14 | Refuse extra extraction despite Samir's request. | Choice | char_samir | 1 | Scene 08 - Refuse extra test. |
| MQ_042_15 | MQ_042 | 15 | Decode Architect beacon to reveal Amazon coordinates. | Interact | ITM_CH042_ARCHITECT_BEACON | 1 | Scene 10 - Beacon Decryption. |
| MQ_042_16 | MQ_042 | 16 | Select Amazon approach route. | Choice | LOC_CH042_AMAZON_PLANNING_ROOM | 1 | Scene 10 - Route selection. |
| MQ_042_17 | MQ_042 | 17 | Lock cure moral flag: ConsentFirst. | System | FLAG_CH042_CURE_MORAL_FLAG | 1 | Scene 08 / Scene 10. |
| MQ_042_18 | MQ_042 | 18 | Unlock flooded Amazon chapter. | System | FLAG_CH042_CHAPTER_043_FLOODED_AMAZON_UNLOCKED | 1 | Scene 10 / Scene 12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ042_A_001 | SQ_042_A | Contact Cairo refugee relay to search for Lina. | Yusuf morale outcome. | SQ_042_A - Lina's Name. |
| OBJ_SQ042_A_002 | SQ_042_A | Cross-check triage ledger for Lina's name. | Information or grief. | SQ_042_A. |
| OBJ_SQ042_B_001 | SQ_042_B | Let Binh choose his stop word from options. | BinhStopWordChosen = true. | SQ_042_B - Stop Word. |
| OBJ_SQ042_C_001 | SQ_042_C | Let Hoang sign a self-restraint statement. | HoangSelfAwareness = true. | SQ_042_C - Hoang's Demand. |
| OBJ_SQ042_D_001 | SQ_042_D | Send non-human false beacon as cover. | MasudRouteConfused = true. | SQ_042_D - False Child. |
| OBJ_SQ042_E_001 | SQ_042_E | Accept Nia's enzyme covenant clause. | BioCovenantMaintained = true. | SQ_042_E - Nia's Clause. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ042_BINH_DISTRUST_HIGH | MQ_042 | BinhDistrust exceeds threshold from dishonest answers. | Binh refuses consent; chapter branches to ethical abort path. | Scene 02 dialogue tree: wrong answers increase BinhDistrust. |
| FAIL_MQ042_STOP_WORD_IGNORED | MQ_042 | Player ignores stop word during procedure. | Hard fail: procedure auto-stops, BinhDistrust spikes, Mai removes medical access. | Scene 07 implementation notes. |
| FAIL_MQ042_EXTRA_EXTRACTION | MQ_042 | Player pushes extra test despite Binh's fever. | Severe fever; Binh weakened; cure moral flag corrupted. | Scene 08 canon: refuse extra test. |
| FAIL_MQ042_MASUD_EXPOSES_ROUTE | MQ_042 | Comms deception fails or blackout chosen. | Convoy route exposed to raiders and Sable remnant. | Scene 06 comms choice. |
| FAIL_MQ042_BEACON_DECRYPT_FAIL | MQ_042 | Missing stable micro-test data. | Partial beacon only; Amazon route less precise. | Scene 10 fail-forward note. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ042_CURE_STABILITY | MQ_042 | system_unlock | Improved enzyme stability model | Scene 08 - Better Batch micro-test results. |
| REW_MQ042_BLOOD_PROTOCOL | MQ_042 | system_unlock | Blood Protocol consent framework for child/immune research | Scene 04 - Ethics Table. |
| REW_MQ042_STOP_WORD_MECHANIC | MQ_042 | system_unlock | Procedure abort mechanic via stop word | Scene 07 - The Small Needle. |
| REW_MQ042_CURE_MORAL_FLAG | MQ_042 | moral_flag | CureMoralFlag = ConsentFirst | Scene 08 / implementation notes. |
| REW_MQ042_AMAZON_ROUTE | MQ_042 | quest_unlock | Flooded Amazon chapter route | Scene 10 - Beacon Decryption. |
| REW_MQ042_CHILD_CONSENT_FIREWALL | MQ_042 | system_unlock | EDENROT ethical firewall around child/immune research | Scene 04 - Ethics Table. |
| REW_MQ042_ORISON_THREAT | MQ_042 | enemy_knowledge | Orison/Architect child program threat revealed | Scene 10 - Beacon Decryption. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH042_BLOOD_PROTOCOL | MQ_042 | Blood Protocol system | Ethics Table completed. |
| UNLOCK_CH042_STOP_WORD | MQ_042 | Stop word mechanic | Binh chooses stop word. |
| UNLOCK_CH042_FIREWALL | MQ_042 | Child Consent Firewall | Protocol header written. |
| UNLOCK_CH042_AMAZON_MAP | MQ_042 | Aster Node map | Beacon decrypted. |
| UNLOCK_CH042_ORISON_THREAT | MQ_042 | Orison threat thread | Beacon reveals child resonance chamber. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH042_MOBILE_LAB_STABILIZED | MQ_042 | Scene 01 lab stabilization complete. |
| FLAG_CH042_BINH_TRUTH_CONVERSATION_COMPLETE | MQ_042 | Scene 02 dialogue tree completed honestly. |
| FLAG_CH042_GUARDIAN_CONFLICT_RESOLVED | MQ_042 | Scene 03 argument resolved. |
| FLAG_CH042_BLOOD_PROTOCOL_ESTABLISHED | MQ_042 | Scene 04 protocol drafted. |
| FLAG_CH042_BINH_STOP_WORD_CHOSEN | MQ_042 | Scene 04 or SQ_042_B. |
| FLAG_CH042_MINIMAL_BLOOD_SAMPLE_COLLECTED | MQ_042 | Scene 07 sample collected. |
| FLAG_CH042_STOP_WORD_HONORED_FIREWALL_VERIFIED | MQ_042 | Scene 07 stop word honored. |
| FLAG_CH042_EXTRA_EXTRACTION_REFUSED | MQ_042 | Scene 08 refused extra test. |
| FLAG_CH042_ARCHITECT_BEACON_DECODED | MQ_042 | Scene 10 beacon decrypted. |
| FLAG_CH042_FLOODED_AMAZON_ROUTE_CHOSEN | MQ_042 | Scene 10 route selected. |
| FLAG_CH042_CURE_MORAL_FLAG | MQ_042 | Scene 08 or Scene 10. |
| FLAG_CH042_CHAPTER_043_FLOODED_AMAZON_UNLOCKED | MQ_042 | Scene 10 or Scene 12. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_042_A | Lina's Name | npc_yusuf | Search Cairo refugee relay for Yusuf's sister Lina. | Lina found: Yusuf morale high. Lina unknown: grief risk. Lie: trust loss. Canon: location unknown, Mai refuses to lie. | SQ_042_A. |
| SQ_042_B | Stop Word | char_binh | Binh chooses a stop word for medical procedures. | Options: Den Do, Dung Lai, Nha. Canon: Den Do (red light). | SQ_042_B. |
| SQ_042_C | Hoang's Demand | comp_hoang | Hoang signs statement forbidding himself from pressuring Binh. | Unlocks HoangSelfAwareness = true. Chapter 45 confrontation gains extra dialogue. | SQ_042_C. |
| SQ_042_D | False Child | automatic | Correct or use Masud's decoy child rumor as cover. | Good: send non-human beacon. Do not endanger real civilians. Canon: drone false beacon. | SQ_042_D. |
| SQ_042_E | Nia's Clause | npc_nia | Add clause: no cure protocol can damage living enzyme cycle. | BioCovenantMaintained = true. Tribal alliance remains high. | SQ_042_E. |

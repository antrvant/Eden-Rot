# Quests - CH044

Metadata:

- chapterID: CH044
- sourceFilename: chapter_044_thanh_tri_trong_than_cay.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_044 | Breach Citadel | main | automatic | Party reaches outer citadel door in giant tree | Citadel breached; Orison records recovered; Hoang armor revealed; Chapter 45 unlocked | Metadata: MQ_044 - Breach Citadel. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ044_001 | MQ_044 | 1 | Mark outer citadel entry route. | Interact | LOC_CH044_TREE_CITADEL_ENTRY | 1 | Scene 1. |
| OBJ_MQ044_002 | MQ_044 | 2 | Identify EDENROT CLASS: FINAL CALCULATION CITADEL. | Interact | LOC_CH044_TREE_CITADEL_ENTRY | 1 | Scene 1; EDENROT marker. |
| OBJ_MQ044_003 | MQ_044 | 3 | Enter tree citadel with Mai group. | GoTo | LOC_CH044_TREE_CITADEL_ENTRY | 1 | Scene 1. |
| OBJ_MQ044_004 | MQ_044 | 4 | Restore flooded engine station with Trung group. | Puzzle | LOC_CH044_FLOODED_ENGINE_STATION | 1 | Scene 2; pump puzzle. |
| OBJ_MQ044_005 | MQ_044 | 5 | Survive Hoang root-signal tunnel. | GoTo | LOC_CH044_ROOT_SIGNAL_TUNNEL | 1 | Scene 3. |
| OBJ_MQ044_006 | MQ_044 | 6 | Investigate Hall of Last Calculations. | GoTo | LOC_CH044_HALL_LAST_CALCULATIONS | 1 | Scene 4. |
| OBJ_MQ044_007 | MQ_044 | 7 | Recover Orison intake records. | Fetch | LOC_CH044_ORISON_INTAKE | 1 | Scene 5. |
| OBJ_MQ044_008 | MQ_044 | 8 | Survive Banshee first tone. | CombatOrEscape | LOC_CH044_BANSHEE_FIRST_CORRIDOR | 1 | Scene 6. |
| OBJ_MQ044_009 | MQ_044 | 9 | Open pressure lock route from engine station. | Puzzle | LOC_CH044_FLOODED_ENGINE_STATION | 1 | Scene 7. |
| OBJ_MQ044_010 | MQ_044 | 10 | Confront Aster ideology. | Dialogue | LOC_CH044_ASTER_MIRROR_ROOM | 1 | Scene 8. |
| OBJ_MQ044_011 | MQ_044 | 11 | Refuse final calculation. | Dialogue | LOC_CH044_ASTER_MIRROR_ROOM | 1 | Scene 8. |
| OBJ_MQ044_012 | MQ_044 | 12 | Resist Binh scanner shortcut. | Choice | LOC_CH044_REUNION_GLASS_WALL | 1 | Scene 11. |
| OBJ_MQ044_013 | MQ_044 | 13 | Disable Banshee chamber ethically. | Puzzle | LOC_CH044_BANSHEE_CHAMBER | 1 | Scene 10. |
| OBJ_MQ044_014 | MQ_044 | 14 | Protect child recordings. | Choice | LOC_CH044_BANSHEE_CHAMBER | 1 | Scene 10. |
| OBJ_MQ044_015 | MQ_044 | 15 | Align parallel manual locks for reunion. | Puzzle | LOC_CH044_REUNION_GLASS_WALL | 1 | Scene 11. |
| OBJ_MQ044_016 | MQ_044 | 16 | Reach inner gate. | GoTo | LOC_CH044_INNER_GATE | 1 | Scene 12. |
| OBJ_MQ044_017 | MQ_044 | 17 | Witness Hoang Architect armor reveal. | Cutscene | LOC_CH044_INNER_GATE | 1 | Scene 12. |
| OBJ_MQ044_018 | MQ_044 | 18 | Unlock Chapter 45 Confront Hoang. | Progression | LOC_CH044_INNER_GATE | 1 | Scene 12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ044_A_001 | SQ_044_A | Find and destroy Orison emergency consent forms. | OrisonConsentLieExposed flag. | SQ_044_A. |
| OBJ_SQ044_B_001 | SQ_044_B | Protect Yusuf biosignature from scanner exploitation. | YusufPersonhoodProtected flag. | SQ_044_B. |
| OBJ_SQ044_C_001 | SQ_044_C | Quarantine Samir's unethical child data. | UnethicalDataQuarantined flag. | SQ_044_C. |
| OBJ_SQ044_D_001 | SQ_044_D | Jam root pump mechanically instead of poisoning. | BioCovenantMaintained flag. | SQ_044_D. |
| OBJ_SQ044_E_001 | SQ_044_E | Accept or reject Hoang's minute of pain silence. | HoangPainSilenced flag; HoangArchitectSync medium. | SQ_044_E. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ044_BINH_SCANNED | MQ_044 | Binh forced into scanner shortcut. | CureMoralFlag damaged; Mai trust drops. | Failure Conditions. |
| FAIL_MQ044_RECORDINGS_DESTROYED | MQ_044 | Child recordings destroyed unnecessarily. | Chapter 46 rescue harder. | Failure Conditions. |
| FAIL_MQ044_HOANG_FULL_SYNC | MQ_044 | Hoang full sync reaches irreversible threshold. | Chapter 45 confrontation compromised. | Failure Conditions. |
| FAIL_MQ044_ENGINE_FLOODED | MQ_044 | Engine station floods route completely. | Trung route lost. | Failure Conditions. |
| FAIL_MQ044_BANSHEE_FRIENDLY_FIRE | MQ_044 | Banshee causes friendly fire or trust collapse. | Group cohesion damaged. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ044_CITADEL_ENTRY | MQ_044 | route_unlock | Outer citadel breached | Completion. |
| REW_MQ044_ORISON_DATA | MQ_044 | data_item | OrisonRecordsRecovered | Completion. |
| REW_MQ044_ASTER_IDEOLOGY | MQ_044 | knowledge | AsterIdeologyRevealed | Completion. |
| REW_MQ044_BANSHEE_KNOWLEDGE | MQ_044 | knowledge | Sonic threat defense learned | Completion. |
| REW_MQ044_CH045_ACCESS | MQ_044 | chapter_unlock | Chapter 45 Confront Hoang | Completion. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH044_SPLIT_ROUTES | MQ_044 | Citadel split-route puzzles | Enter citadel with split party. |
| UNLOCK_CH044_SONIC_THREAT | MQ_044 | Sonic threat mechanics | Survive Banshee first tone. |
| UNLOCK_CH044_ASTER_DIALOGUE | MQ_044 | Aster ideology dialogue system | Enter Hall of Last Calculations. |
| UNLOCK_CH044_ORISON_RECORDS | MQ_044 | Child rescue target data | Recover Orison intake records. |
| UNLOCK_CH044_HOANG_ARMOR_STATE | MQ_044 | Hoang Architect armor state | Hoang armor reveal at inner gate. |
| UNLOCK_CH045_CONFRONT_HOANG | MQ_044 | Chapter 45 | Reach inner gate cliffhanger. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH044_OUTER_CITADEL_ENTERED | MQ_044 | Mai group enters tree citadel. |
| FLAG_CH044_EDENROT_FINAL_CALC_CITADEL | MQ_044 | EDENROT marker identified at entry. |
| FLAG_CH044_FINAL_CALCULATION_REFUSED | MQ_044 | Mai/Binh refuse Aster's ideology. |
| FLAG_CH044_ORISON_RECORDS_RECOVERED | MQ_044 | Child intake records taken. |
| FLAG_CH044_CONSENT_FORGERY_EXPOSED | MQ_044 | Civilization Continuity Override torn up. |
| FLAG_CH044_BANSHEE_CHAMBER_DISABLED | MQ_044 | Banshee disabled with counter-tone. |
| FLAG_CH044_CHILD_RECORDINGS_PROTECTED | MQ_044 | Recordings preserved during Banshee disable. |
| FLAG_CH044_BINH_SCANNER_REFUSED | MQ_044 | All refuse scanner shortcut. |
| FLAG_CH044_HOANG_ARCHITECT_ARMOR_REVEALED | MQ_044 | Hoang appears in Architect armor. |
| FLAG_CH044_CH045_UNLOCKED | MQ_044 | Chapter 45 unlocked. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_044_A | Emergency Consent Forms | automatic | Find and destroy Orison forms pre-authorizing child procedures. | OrisonConsentLieExposed; Mai gains CH046 dialogue. | SQ_044_A. |
| SQ_044_B | The Cured Anomaly | automatic | Hide Yusuf biosignature or protect from scanner. | YusufPersonhoodProtected. | SQ_044_B. |
| SQ_044_C | Samir's Temptation | char_samir | Quarantine unethical child research data. | UnethicalDataQuarantined. | SQ_044_C. |
| SQ_044_D | Iara's Sabotage | char_iara | Jam root pump mechanically, not poison. | BioCovenantMaintained. | SQ_044_D. |
| SQ_044_E | Hoang's Minute | char_hoang | Accept or reject one minute of pain silence. | HoangPainSilenced; HoangArchitectSync medium. | SQ_044_E. |

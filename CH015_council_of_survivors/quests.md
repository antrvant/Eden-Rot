# Quests - CH015

Metadata:

- chapterID: CH015
- sourceFilename: chapter_015_hoi_dong_cua_nhung_ke_song_sot.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_015 | Form Council | main | npc_worker_lead (trigger); char_trung (protagonist) | First night in base "Home"; fever crisis begins. | Council formed with seats defined; first strategic vote held; `HoangStrikeFirstVote` recorded. | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ015_01 | MQ_015 | 1 | Respond to fever outbreak in Classroom 3B. | GoTo | LOC_CH015_CLASS_3B | 1 | Scene 1. |
| OBJ_MQ015_02 | MQ_015 | 2 | Secure and inspect medicine from EDEN package. | Investigate | ITM_CH015_EDEN_FEVER_MEDICINE | 1 | Scene 1. |
| OBJ_MQ015_03 | MQ_015 | 3 | Test medicine for tampering with Doctor. | Interact | npc_doctor | 1 | Scene 1 and Scene 5. |
| OBJ_MQ015_04 | MQ_015 | 4 | Investigate strangers at the gate. | GoTo | LOC_CH015_CONSTRUCTION_SITE | 1 | Scene 2. |
| OBJ_MQ015_05 | MQ_015 | 5 | Apply admission and quarantine rules to strangers. | Decision | LOC_CH015_TEMP_QUARANTINE | 1 | Scene 2. |
| OBJ_MQ015_06 | MQ_015 | 6 | Attend emergency survivor meeting in teacher's room. | GoTo | LOC_CH015_TEACHER_ROOM | 1 | Scene 3. |
| OBJ_MQ015_07 | MQ_015 | 7 | Decide council structure and representatives. | Decision | LOC_CH015_TEACHER_ROOM | 1 | Scene 4. |
| OBJ_MQ015_08 | MQ_015 | 8 | Vote on medicine usage for fever child. | Decision | LOC_CH015_TEACHER_ROOM | 1 | Scene 5. |
| OBJ_MQ015_09 | MQ_015 | 9 | Interrogate or question the fake mother scout. | Investigate | npc_fake_mother | 1 | Scene 6. |
| OBJ_MQ015_10 | MQ_015 | 10 | Extract EDEN cache intel from scout. | Investigate | npc_fake_mother | 1 | Scene 6. |
| OBJ_MQ015_11 | MQ_015 | 11 | Establish rule against calling children by enemy classifications. | Decision | LOC_CH015_TEACHER_ROOM | 1 | Scene 4. |
| OBJ_MQ015_12 | MQ_015 | 12 | Hold first council strategic vote: defend, recon, or strike. | Decision | LOC_CH015_TEACHER_ROOM | 1 | Scene 7. |
| OBJ_MQ015_13 | MQ_015 | 13 | Establish Council governance system. | Unlock | LOC_CH015_TEACHER_ROOM | 1 | Scene 7. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ015_01_001 | SQ_Council_01 | Detect inconsistencies in stranger's story from gate. | Early warning of infiltration; better quarantine outcome. | Scene 2. |
| OBJ_SQ015_02_001 | SQ_Council_02 | Prevent adults from calling medicine "Binh's price" in front of children. | Protects Binh's emotional state; reduces guilt thread. | Scene 1 and DT_058. |
| OBJ_SQ015_03_001 | SQ_Council_03 | Record dissent publicly when council votes. | Council legitimacy improves; trust system unlocked. | Scene 4. |
| OBJ_SQ015_04_001 | SQ_Council_04 | Prevent rumor that Binh caused sickness. | Reduces `EdenrotParanoia`; later base votes are less harsh. | SQ_Council_04B. |
| OBJ_SQ015_05_001 | SQ_Council_05 | Find hidden yellow thread/token on fake mother. | Confirms EDEN connection without torture. | Scene 6. |
| OBJ_SQ015_05_002 | SQ_Council_05 | Protect the child Phuc used as cover. | Child morale; Phuc remains in base as continuity asset. | Scene 6. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ015_UNTESTED_MEDICINE | MQ_015 | Give untested medicine too fast. | Fever child may worsen; trust in Doctor drops. | Rewards. |
| FAIL_MQ015_REFUSE_ALL_MEDICINE | MQ_015 | Refuse all medicine. | Child survives or dies based on prior water quest; morale hit. | Rewards. |
| FAIL_MQ015_STRANGER_BYPASS_QUARANTINE | MQ_015 | Let stranger bypass quarantine. | Scout reaches classroom and identifies Binh. | Rewards. |
| FAIL_MQ015_EXECUTE_SCOUT | MQ_015 | Execute scout publicly. | Hoang trust up, Mai/Binh trust down, council legitimacy damaged. | Rewards. |
| FAIL_MQ015_REFUSE_COUNCIL | MQ_015 | Refuse council formation. | Worker faction resentment; later betrayal risk. | Rewards. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ015_COUNCIL_GOVERNANCE | MQ_015 | system_unlock | Council governance system | Rewards section. |
| REW_MQ015_MEDICINE_ALLOCATION | MQ_015 | system_unlock | Medicine allocation choices | Rewards section. |
| REW_MQ015_QUARANTINE_POLICY | MQ_015 | system_unlock | Quarantine policy rules | Rewards section. |
| REW_MQ015_EDEN_SCOUT_INTEL | MQ_015 | intel_unlock | EDEN scout intel and cache location | Rewards section. |
| REW_MQ015_HOANG_STRIKE_VOTE | MQ_015 | flag | `HoangStrikeFirstVote` recorded | Rewards section. |
| REW_MQ015_BASE_TRUST_INITIAL | MQ_015 | flag | `BaseTrustInitial` trust system | Rewards section. |
| REW_MQ015_BINH_GUILT_THREAD | MQ_015 | continuity_flag | `BinhGuiltThread` emotional arc | Rewards section. |
| REW_MQ015_EDENROT_PARANOIA | MQ_015 | continuity_flag | `EdenrotParanoiaThread` social rot | Rewards section. |
| REW_MQ015_FIRST_VOTE_SLIP | MQ_015 | item | ITM_CH015_FIRST_VOTE_SLIP | Rewards section. |
| REW_MQ015_COUNCIL_RULEBOOK | MQ_015 | item | ITM_CH015_COUNCIL_RULEBOOK | Rewards section. |
| REW_MQ015_EDENROT_NODE_NOTICE | MQ_015 | item | ITM_CH015_EDENROT_NODE_NOTICE | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH015_COUNCIL_SYSTEM | MQ_015 | Council Governance | Council seats defined and first vote held. |
| UNLOCK_CH015_VOTING_SYSTEM | MQ_015 | Voting/Consensus | Council votes on medicine and strategic decision. |
| UNLOCK_CH015_EMERGENCY_AUTHORITY | MQ_015 | Emergency Authority | 30-minute commander override during attack. |
| UNLOCK_CH015_QUARANTINE_ETHICS | MQ_015 | Quarantine Ethics | Doctor gets 2-hour quarantine authority. |
| UNLOCK_CH015_MEDICINE_ALLOCATION | MQ_015 | Medicine Allocation | Council decides medicine use. |
| UNLOCK_CH015_INFILTRATION_SUSPICION | MQ_015 | Infiltration Suspicion | Scout exposed; future admission rules stricter. |
| UNLOCK_CH015_REPUTATION_GROUPS | MQ_015 | Base Reputation Groups | Family Core, Workers, Children, Medical, Security. |
| UNLOCK_CH015_EDENROT_PARANOIA | MQ_015 | Edenrot Paranoia | Rumor, labels, and language of enemy as internal rot. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH015_COUNCIL_FORMED | MQ_015 | Council seats defined and first vote held. |
| FLAG_CH015_HOANG_STRIKE_FIRST_VOTE | MQ_015 | Hoang votes to strike EDEN cache. |
| FLAG_CH015_RECON_BEFORE_STRIKE | MQ_015 | Council majority votes recon. |
| FLAG_CH015_MEDICINE_FROM_EDEN_USED | MQ_015 | Fever child receives tested medicine. |
| FLAG_CH015_FAKE_MOTHER_SCOUT_CAPTURED | MQ_015 | Scout exposed and detained. |
| FLAG_CH015_BINH_GUILT_THREAD | MQ_015 | Binh begins guilt arc. |
| FLAG_CH015_EDENROT_PARANOIA_THREAD | MQ_015 | Social distrust spreads. |
| FLAG_CH015_ENEMY_CLASSIFICATION_REJECTED | MQ_015 | Council bans enemy codes for children. |
| FLAG_CH015_MQ_COMPLETE | MQ_015 | Quest completes. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Council_01 | Stranger Outside Gate | comp_hoang | Question stranger from gate; screen for bites; decide quarantine conditions. | If handled humanely, council gains legitimacy; if brutal, EDEN gets propaganda. | SQ_Council_01. |
| SQ_Council_02 | Fever Medicine | npc_doctor | Inspect medicine; test for tampering; decide dosage; inform caregivers. | Sets medical ethics and trust in Doctor. | SQ_Council_02. |
| SQ_Council_03 | First Vote | npc_worker_lead | Gather concerns; draft seats; decide emergency authority; cast first vote. | Unlocks governance UI/system. | SQ_Council_03. |
| SQ_Council_04 | Sickness in Classroom | char_mai | Separate fever case without exile; reassure children; clean water source. | Child morale and medical trust. | SQ_Council_04. |
| SQ_Council_04B | Eden Node Rumor | npc_base_survivor | Identify who repeated classification; hold clarification; restate classroom rule. | Reduces `EdenrotParanoia`; if failed, later votes harsher around Binh. | SQ_Council_04B. |
| SQ_Council_05 | Scout Pretending to Be Mother | char_mai | Compare story with child reactions; find hidden token; question without torture; decide fate. | Unlocks EDEN cache coordinates; affects Mai/Hoang trust. | SQ_Council_05. |

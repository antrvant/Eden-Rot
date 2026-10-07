# Quests - CH016

Metadata:

- chapterID: CH016
- sourceFilename: chapter_016_mien_dich.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_016 | Test Immunity | main | npc_doctor (proposal); char_trung (protagonist) | Fever child survived in CH015; Doctor observes Binh did not fever after exposure. | Dormancy test completed; Cure Ethics established; Cult rumor received; Binh reclaims sample label. | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ016_01 | MQ_016 | 1 | Attend Doctor's immunity proposal in library medical room. | GoTo | LOC_CH016_SCHOOL_LIBRARY_MED | 1 | Scene 1. |
| OBJ_MQ016_02 | MQ_016 | 2 | Vote to prepare lab without immediate blood draw. | Decision | LOC_CH016_COUNCIL_MEETING_ROOM | 1 | Scene 1. |
| OBJ_MQ016_03 | MQ_016 | 3 | Travel to abandoned medical station. | GoTo | LOC_CH016_ABANDONED_MED_STATION | 1 | Scene 2. |
| OBJ_MQ016_04 | MQ_016 | 4 | Retrieve microscope, sterile needles, sample vials, alcohol, generator parts. | Collect | LOC_CH016_ABANDONED_MED_STATION | 5 | Scene 2. |
| OBJ_MQ016_05 | MQ_016 | 5 | Document Cult symbol at clinic. | Investigate | LOC_CH016_ABANDONED_MED_STATION | 1 | Scene 2. |
| OBJ_MQ016_06 | MQ_016 | 6 | Explain immunity testing to Binh in age-appropriate language. | Interact | char_binh | 1 | Scene 3. |
| OBJ_MQ016_07 | MQ_016 | 7 | Draft blood/consent rules with council. | Decision | LOC_CH016_COUNCIL_MEETING_ROOM | 1 | Scene 4. |
| OBJ_MQ016_08 | MQ_016 | 8 | Let Binh decide whether to participate. | Decision | char_binh | 1 | Scene 5. |
| OBJ_MQ016_09 | MQ_016 | 9 | Respect Binh's stop signal during blood draw. | Decision | char_binh | 1 | Scene 5. |
| OBJ_MQ016_10 | MQ_016 | 10 | Draw minimal blood sample under consent protocol. | Interact | npc_doctor | 1 | Scene 5. |
| OBJ_MQ016_11 | MQ_016 | 11 | Run first dormancy test in temporary lab. | Interact | npc_doctor | 1 | Scene 6. |
| OBJ_MQ016_12 | MQ_016 | 12 | Decide classification and public wording of results. | Decision | LOC_CH016_COUNCIL_MEETING_ROOM | 1 | Scene 6. |
| OBJ_MQ016_13 | MQ_016 | 13 | Reject EDEN/Cult labels in medical records. | Decision | LOC_CH016_COUNCIL_MEETING_ROOM | 1 | Scene 4, Scene 6. |
| OBJ_MQ016_14 | MQ_016 | 14 | Investigate radio rumor about immune child. | Investigate | LOC_CH016_RADIO_CORNER | 1 | Scene 7. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ016_01_001 | SQ_Immunity_01 | Sit with Binh without interrogation after council talk. | Binh trust up; reduces guilt thread. | SQ_Immunity_01. |
| OBJ_SQ016_01_002 | SQ_Immunity_01 | Let Binh ask one hard question and give truthful response. | Family trust increase. | SQ_Immunity_01. |
| OBJ_SQ016_02_001 | SQ_Immunity_02 | Choose between medicines and lab equipment at carry limit. | Better lab quality or more immediate medicine. | SQ_Immunity_02. |
| OBJ_SQ016_02_002 | SQ_Immunity_02 | Clear infected medical ward at abandoned clinic. | Safe access to supplies. | SQ_Immunity_02. |
| OBJ_SQ016_03_001 | SQ_Immunity_03 | Find missing microscope lens. | Improves dormancy test reliability. | SQ_Immunity_03. |
| OBJ_SQ016_03_002 | SQ_Immunity_03 | Repair light source using generator/battery. | Lab functionality. | SQ_Immunity_03. |
| OBJ_SQ016_03_003 | SQ_Immunity_03 | Assign lab guard. | Lab security. | SQ_Immunity_03. |
| OBJ_SQ016_04_001 | SQ_Immunity_04 | Tune radio at night and identify repeated phrase. | Unlocks Cult threat meter. | SQ_Immunity_04. |
| OBJ_SQ016_04_002 | SQ_Immunity_04 | Question Hanh about rumor routes. | Intel on Cult network. | SQ_Immunity_04. |
| OBJ_SQ016_04_003 | SQ_Immunity_04 | Decide whether to jam, respond, or listen silently to Cult radio. | Affects Cult approach speed. | SQ_Immunity_04. |
| OBJ_SQ016_04B_001 | SQ_Immunity_04B | Let Binh reject B-07 label and write his own name on sample. | Unlocks ethical sample tracking; reduces EdenrotParanoia. | SQ_Immunity_04B. |
| OBJ_SQ016_05_001 | SQ_Immunity_05 | Stop blood draw immediately when Binh says stop. | Major family trust increase. | SQ_Immunity_05. |
| OBJ_SQ016_05_002 | SQ_Immunity_05 | Offer delay and let Binh choose who stays. | Consent integrity. | SQ_Immunity_05. |
| OBJ_SQ016_05_003 | SQ_Immunity_05 | Resume only if Binh chooses to. | Consent respected. | SQ_Immunity_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ016_FORCE_TEST | MQ_016 | Force test without consent. | Massive Family Trust loss; Cure Ethics fail seed. | Fail States. |
| FAIL_MQ016_HIDE_FROM_COUNCIL | MQ_016 | Hide test from council. | Worker trust collapse; Hoang may use secrecy later. | Fail States. |
| FAIL_MQ016_INFECTED_SAMPLE | MQ_016 | Bring infected sample unsafely. | Clinic contamination event. | Fail States. |
| FAIL_MQ016_PUBLICIZE_RESULT | MQ_016 | Publicize result too broadly. | Cult/EDEN threat escalates faster. | Fail States. |
| FAIL_MQ016_REFUSE_ALL_TESTING | MQ_016 | Refuse all testing. | Binh trust may hold, but cure research delayed and Doctor conflict rises. | Fail States. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ016_CURE_RESEARCH | MQ_016 | system_unlock | Cure Research path | Rewards. |
| REW_MQ016_CONSENT_PROTOCOL | MQ_016 | system_unlock | BinhConsentProtocol | Rewards. |
| REW_MQ016_VIRAL_DORMANCY_LORE | MQ_016 | lore_unlock | ViralDormancyLore | Rewards. |
| REW_MQ016_EDENROT_DORMANCY_LORE | MQ_016 | lore_unlock | EdenrotDormancyLore | Rewards. |
| REW_MQ016_TEMPORARY_LAB | MQ_016 | system_unlock | Temporary lab station in library | Rewards. |
| REW_MQ016_SAMPLE_A | MQ_016 | item | ITM_CH016_BINH_BLOOD_SAMPLE_A | Rewards. |
| REW_MQ016_OLD_MICROSCOPE | MQ_016 | item | ITM_CH016_OLD_MICROSCOPE | Rewards. |
| REW_MQ016_DORMANCY_RESPONSE | MQ_016 | lore | Eden Strain dormancy response | Rewards. |
| REW_MQ016_SILENCED_NOT_PURIFIED | MQ_016 | lore | Edenrot can be silenced, not purified | Rewards. |
| REW_MQ016_CULT_THREAT_FLAG | MQ_016 | flag | CultHeardOfBinh | Rewards. |
| REW_MQ016_CURE_ETHICS_FLAG | MQ_016 | moral_flag | CureEthicsStarted | Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH016_CURE_RESEARCH | MQ_016 | Cure Research | Dormancy test completed; lab established. |
| UNLOCK_CH016_CONSENT_SYSTEM | MQ_016 | Medical Consent System | Cure Ethics protocol drafted and voted. |
| UNLOCK_CH016_DORMANCY_LORE | MQ_016 | Viral Dormancy Concept | Doctor observes dormancy under microscope. |
| UNLOCK_CH016_EDENROT_DORMANCY | MQ_016 | Edenrot Dormancy Interpretation | Dormancy connected to Edenrot silence concept. |
| UNLOCK_CH016_CULT_RUMOR_TRACKING | MQ_016 | Cult Rumor Tracking | Radio fragment and Hanh intel combined. |
| UNLOCK_CH016_BINH_TRUST_MILESTONES | MQ_016 | Binh Trust Milestones | Consent respected; voluntary sample; label reclaimed. |
| UNLOCK_CH016_SAMPLE_ETHICS | MQ_016 | Ethical Sample Tracking | Binh writes own name on sample; council-medical access seal. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH016_CURE_ETHICS_STARTED | MQ_016 | Council drafts and votes on blood/consent rules. |
| FLAG_CH016_BINH_CONSENT_PROTOCOL | MQ_016 | Formal consent process established. |
| FLAG_CH016_BINH_SAID_STOP_RESPECTED | MQ_016 | Binh panics; everyone stops. |
| FLAG_CH016_BINH_VOLUNTARY_SAMPLE_A | MQ_016 | Binh consents after pause; sample drawn. |
| FLAG_CH016_VIRAL_DORMANCY_DISCOVERED | MQ_016 | Doctor observes dormancy under microscope. |
| FLAG_CH016_EDENROT_DORMANCY_LORE | MQ_016 | Dormancy linked to Edenrot silence. |
| FLAG_CH016_ENEMY_LABELS_REJECTED_RECORD | MQ_016 | Council bans B-07, Eden Node, asset in records. |
| FLAG_CH016_CULT_HEARD_OF_BINH | MQ_016 | Radio picks up Cult chant. |
| FLAG_CH016_CULT_SYMBOL_FOUND | MQ_016 | Cult symbol documented at clinic. |
| FLAG_CH016_CULT_SYMBOL_PERIMETER | MQ_016 | Cult symbol found on tree outside fence. |
| FLAG_CH016_BINH_WROTE_CONSENT_NOTE | MQ_016 | Binh writes "Con noi co" on sample label. |
| FLAG_CH016_MQ_COMPLETE | MQ_016 | Quest completes. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Immunity_01 | Blood Is Not Currency | char_binh | Notice Binh withdrawing; sit without interrogation; explain helping vs being used; let Binh ask one hard question. | Binh trust up if honest and gentle. | SQ_Immunity_01. |
| SQ_Immunity_02 | Abandoned Medical Station | npc_doctor | Reach clinic; clear infected ward; open locked lab cabinet; choose medicines vs equipment; document Cult symbol. | Better lab quality or more immediate medicine. | SQ_Immunity_02. |
| SQ_Immunity_03 | Microscope Man | npc_doctor | Find missing lens; repair light source; sterilize slides; assign lab guard. | Improves reliability of dormancy result. | SQ_Immunity_03. |
| SQ_Immunity_04 | Believer Rumors | npc_radio_operator | Tune radio at night; identify repeated phrase; question Hanh; mark Cult approach path; decide jam/respond/listen. | Unlocks Cult threat meter. | SQ_Immunity_04. |
| SQ_Immunity_04B | Name on the Vial | char_binh | Inspect sample label; choose naming convention; let Binh reject B-07 and write own name; add consent note; seal under council-medical access. | Unlocks ethical sample tracking; reduces EdenrotParanoia. | SQ_Immunity_04B. |
| SQ_Immunity_05 | Right to Say No | char_binh | Stop immediately when Binh panics; reassure no penalty; offer delay; let Binh choose who stays; resume only if chosen. | Major Family Trust increase if respected. | SQ_Immunity_05. |

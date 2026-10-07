# Quests - CH036

Metadata:

- chapterID: CH036
- sourceFilename: chapter_036_paris_khong_anh_den.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_036 | Find Research Archive | main | automatic | Group arrives at frozen Paris outskirts | Archive recovered; Swiss Alpine route confirmed; Chapter 37 unlocked | Metadata: MQ_036 - Find Research Archive. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ036_001 | MQ_036 | 1 | Approach frozen Paris through rail route. | GoTo | LOC_CH036_FROZEN_RAIL | 1 | Main Quest objective 1. |
| OBJ_MQ036_002 | MQ_036 | 2 | Avoid surface ice horde patrols. | Stealth | LOC_CH036_FROZEN_RAIL | 1 | Main Quest objective 2. |
| OBJ_MQ036_003 | MQ_036 | 3 | Locate metro entrance marker. | GoTo | LOC_CH036_METRO_ENTRANCE | 1 | Main Quest objective 3. |
| OBJ_MQ036_004 | MQ_036 | 4 | Verify Rebirth identity with child-safety phrase. | Dialogue | LOC_CH036_METRO_ENTRANCE | 1 | Main Quest objective 4; DT_208. |
| OBJ_MQ036_005 | MQ_036 | 5 | Meet Teacher Amelie and metro school. | GoTo | LOC_CH036_METRO_SCHOOL | 1 | Main Quest objective 5. |
| OBJ_MQ036_006 | MQ_036 | 6 | Attend morning roll call. | Interact | LOC_CH036_METRO_SCHOOL | 1 | Main Quest objective 6; DT_209. |
| OBJ_MQ036_007 | MQ_036 | 7 | Assess shelter needs and missing children ledger. | Interact | LOC_CH036_SHELTER_STORAGE | 1 | Main Quest objective 7. |
| OBJ_MQ036_008 | MQ_036 | 8 | Investigate first Mimic lure. | GoTo | LOC_CH036_SERVICE_TUNNEL | 1 | Main Quest objective 8; Scene 5. |
| OBJ_MQ036_009 | MQ_036 | 9 | Protect child from false voice. | Protect | npc_mathis | 1 | Main Quest objective 9. |
| OBJ_MQ036_010 | MQ_036 | 10 | Reach station library/archive vault. | GoTo | LOC_CH036_STATION_LIBRARY | 1 | Main Quest objective 10. |
| OBJ_MQ036_011 | MQ_036 | 11 | Unlock courier cache with Celine. | Puzzle | LOC_CH036_STATION_LIBRARY | 1 | Main Quest objective 11. |
| OBJ_MQ036_012 | MQ_036 | 12 | Recover Patient Zero transfer logs. | Fetch | ITM_CH036_PATIENT_ZERO_ARCHIVE | 1 | Main Quest objective 12. |
| OBJ_MQ036_013 | MQ_036 | 13 | Survive Mimic attendance attack. | CombatOrEscape | LOC_CH036_PLATFORM_CORRIDOR | 1 | Main Quest objective 13; Scene 7. |
| OBJ_MQ036_014 | MQ_036 | 14 | Extract archive through flooded tunnel. | Escort | LOC_CH036_FLOODED_TUNNEL | 1 | Main Quest objective 14. |
| OBJ_MQ036_015 | MQ_036 | 15 | Confirm Swiss Alpine route. | Interact | LOC_CH036_SHELTER_AFTER | 1 | Main Quest objective 15. |
| OBJ_MQ036_016 | MQ_036 | 16 | Unlock Chapter 37 Alps tunnels. | Progression | LOC_CH036_SHELTER_AFTER | 1 | Main Quest objective 16. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ036_01_001 | SQ_PARIS_01 | Help update attendance ledger. | ParisAttendanceLedger flag. | SQ_Paris_01. |
| OBJ_SQ036_02_001 | SQ_PARIS_02 | Allocate Rebirth supplies to school shelter. | ParisSchoolStabilized flag. | SQ_Paris_02. |
| OBJ_SQ036_03_001 | SQ_PARIS_03 | Gather Mimic voice samples. | MimicVoiceRuleLearned flag. | SQ_Paris_03. |
| OBJ_SQ036_04_001 | SQ_PARIS_04 | Find manual catalog card for archive vault. | ResearchCourierCache flag. | SQ_Paris_04. |
| OBJ_SQ036_05_001 | SQ_PARIS_05 | Recover name tags/items of missing children. | Child morale and Mimic resistance. | SQ_Paris_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ036_CHILD_LURED | MQ_036 | Mimic lures a child beyond barricade. | Major trust loss; Amelie seals shelter. | Failure Conditions. |
| FAIL_MQ036_ARCHIVE_FLOODED | MQ_036 | Archive destroyed by flood/ice. | Patient Zero clue lost. | Failure Conditions. |
| FAIL_MQ036_TRUST_LOST | MQ_036 | Amelie loses trust and seals shelter. | No further Paris support. | Failure Conditions. |
| FAIL_MQ036_ICE_BREACH | MQ_036 | Ice horde breaches school platform. | Children endangered. | Failure Conditions. |
| FAIL_MQ036_BINH_ISOLATED | MQ_036 | Binh isolated by fake voice. | Emotional damage; trust loss. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ036_ARCHIVE | MQ_036 | data_item | PatientZeroArchiveSecured | Completion Rewards. |
| REW_MQ036_ROUTE | MQ_036 | route_unlock | Swiss Alpine Lab route | Completion Rewards. |
| REW_MQ036_MIMIC_RULE | MQ_036 | knowledge | Mimic voice rule | Completion Rewards. |
| REW_MQ036_ALLY | MQ_036 | faction_unlock | Paris School ally | Completion Rewards. |
| REW_MQ036_TRUST | MQ_036 | reputation | Teacher Amelie trust | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH036_METRO_HUB | MQ_036 | Paris metro shelter hub | Enter metro school. |
| UNLOCK_CH036_MIMIC_ENEMY | MQ_036 | Mimic enemy type | First Mimic encounter survived. |
| UNLOCK_CH036_ARCHIVE_MECHANICS | MQ_036 | Archive retrieval mechanics | Unlock courier cache. |
| UNLOCK_CH036_ALPS_ROUTE | MQ_036 | Swiss Alps route | Confirm archive data. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH036_PATIENT_ZERO_ARCHIVE_SECURED | MQ_036 | Archive recovered from vault. |
| FLAG_CH036_SWISS_ALPINE_ROUTE_UNLOCKED | MQ_036 | Doctor confirms transfer logs. |
| FLAG_CH036_MIMIC_VOICE_RULE_LEARNED | SQ_PARIS_03 | Group learns voice rule. |
| FLAG_CH036_PARIS_SCHOOL_TRUST_HIGH | MQ_036 | School stabilized and trust earned. |
| FLAG_CH036_DATA_FOLLOWS_PEOPLE | MQ_036 | Trung carries child, gives archive to Doctor. |
| FLAG_CH036_ECHO_MEMORY_TRAP_SURVIVED | MQ_036 | Group attendance breaks Mimic trap. |
| FLAG_CH036_BINH_ALPS_SIGNAL | MQ_036 | Binh senses non-radio call from Alps. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_PARIS_01 | Attendance Every Morning | char_teacher_amelie | Help update attendance ledger and record names for Eli/NORAD archive. | ParisAttendanceLedger. | SQ_Paris_01. |
| SQ_PARIS_02 | Limits of the Classroom | char_teacher_amelie | Allocate supplies, repair battery bank, establish relay with Ingrid/Moreno. | ParisSchoolStabilized. | SQ_Paris_02. |
| SQ_PARIS_03 | Voice in the Tunnel | automatic | Gather voice samples, create no-follow rule, identify Mimic pattern. | MimicVoiceRuleLearned. | SQ_Paris_03. |
| SQ_PARIS_04 | Library Under the Station | char_celine | Find manual catalog card, unlock cache, protect Celine. | ResearchCourierCache. | SQ_Paris_04. |
| SQ_PARIS_05 | Names of Absent Children | automatic | Recover name tags/items, return to attendance wall, resist Mimic using names. | Child morale / Mimic resistance. | SQ_Paris_05. |

# Quests - CH040

Metadata:

- chapterID: CH040
- sourceFilename: chapter_040_bo_lac_cua_nhung_hat_giong.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_040 | Earn Tribal Alliance | main | automatic | Group enters seed village | Tribal alliance earned; proper enzyme sample secured; Cairo route confirmed | Metadata: MQ_040 - Earn Tribal Alliance. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ040_001 | MQ_040 | 1 | Enter seed village through living bridge. | GoTo | LOC_CH040_LIVING_BRIDGE | 1 | Main Quest objective 1. |
| OBJ_MQ040_002 | MQ_040 | 2 | Follow entry rules and disarm/wrap weapons. | Interact | LOC_CH040_LIVING_BRIDGE | 1 | Main Quest objective 2. |
| OBJ_MQ040_003 | MQ_040 | 3 | Identify EDENROT seed covenant marker. | Observe | LOC_CH040_LIVING_BRIDGE | 1 | Main Quest objective 3. |
| OBJ_MQ040_004 | MQ_040 | 4 | Sit through listening circle testimonies. | Dialogue | LOC_CH040_COUNCIL_PLATFORM | 1 | Main Quest objective 4. |
| OBJ_MQ040_005 | MQ_040 | 5 | Present anti-growth compound honestly. | Dialogue | LOC_CH040_TOXIC_PIT | 1 | Main Quest objective 5. |
| OBJ_MQ040_006 | MQ_040 | 6 | Surrender/seal toxic weapon. | Choice | LOC_CH040_TOXIC_PIT | 1 | Main Quest objective 6. |
| OBJ_MQ040_007 | MQ_040 | 7 | Remove extraction insurance from Rebirth inventory. | Interact | LOC_CH040_TOXIC_PIT | 1 | Main Quest objective 7. |
| OBJ_MQ040_008 | MQ_040 | 8 | Visit seed vault shrine. | GoTo | LOC_CH040_SEED_VAULT | 1 | Main Quest objective 8. |
| OBJ_MQ040_009 | MQ_040 | 9 | Align cure formula with enzyme ecological cycle. | Puzzle | LOC_CH040_SEED_VAULT | 1 | Main Quest objective 9. |
| OBJ_MQ040_010 | MQ_040 | 10 | Participate in children seed class. | Interact | LOC_CH040_CHILDREN_CLASS | 1 | Main Quest objective 10. |
| OBJ_MQ040_011 | MQ_040 | 11 | Defend village from raider retaliation. | Combat | LOC_CH040_VILLAGE_PERIMETER | 1 | Main Quest objective 11. |
| OBJ_MQ040_012 | MQ_040 | 12 | Protect seed vault without toxic compound. | Combat | LOC_CH040_VILLAGE_PERIMETER | 1 | Main Quest objective 12. |
| OBJ_MQ040_013 | MQ_040 | 13 | Harvest proper enzyme under Nia's guidance. | Interact | LOC_CH040_ENZYME_GROVE | 1 | Main Quest objective 13. |
| OBJ_MQ040_014 | MQ_040 | 14 | Ratify seed covenant alliance. | Dialogue | LOC_CH040_COUNCIL_AGAIN | 1 | Main Quest objective 14. |
| OBJ_MQ040_015 | MQ_040 | 15 | Confirm viability with Cairo. | Interact | LOC_CH040_COUNCIL_AGAIN | 1 | Main Quest objective 15. |
| OBJ_MQ040_016 | MQ_040 | 16 | Negotiate two-way alliance terms. | Dialogue | LOC_CH040_COUNCIL_AGAIN | 1 | Main Quest objective 16. |
| OBJ_MQ040_017 | MQ_040 | 17 | Prepare enzyme transport to Cairo. | Interact | LOC_CH040_RIVER_DEPARTURE | 1 | Main Quest objective 17. |
| OBJ_MQ040_018 | MQ_040 | 18 | Unlock Chapter 41 Cairo Siege. | Progression | LOC_CH040_RIVER_DEPARTURE | 1 | Main Quest objective 18. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ040_COMPOUND_HIDDEN | MQ_040 | Toxic compound hidden and discovered. | Alliance collapse. | Failure Conditions. |
| FAIL_MQ040_SEED_VAULT_DAMAGED | MQ_040 | Seed vault damaged in defense. | Knowledge loss; trust damage. | Failure Conditions. |
| FAIL_MQ040_BRIDGE_BURNED | MQ_040 | Raiders burn living bridge. | Isolation; route loss. | Failure Conditions. |
| FAIL_MQ040_UNAUTHORIZED_SAMPLE | MQ_040 | Doctor takes unauthorized sample. | Alliance collapse. | Failure Conditions. |
| FAIL_MQ040_LISTENING_DISRESPECTED | MQ_040 | Listening circle interrupted or disrespected. | Trust loss. | Failure Conditions. |
| FAIL_MQ040_ENZYME_CONTAMINATED | MQ_040 | Enzyme harvest contaminated. | Useless sample. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ040_ALLIANCE | MQ_039 | faction_unlock | TribalAllianceEarned | Completion Rewards. |
| REW_MQ040_ENZYME | MQ_040 | data_item | ProperBioEnzymeSample | Completion Rewards. |
| REW_MQ040_CODEX | MQ_040 | knowledge | BioKnowledgeCodex | Completion Rewards. |
| REW_MQ040_CAIRO_ROUTE | MQ_040 | route_unlock | Cairo route priority | Completion Rewards. |
| REW_MQ040_TRUST | MQ_040 | reputation | AllianceTrust increase | Completion Rewards. |
| REW_MQ040_ETHICS | MQ_040 | moral | CureEthics increase | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH040_TRIBAL_ALLIANCE | MQ_040 | Tribal alliance | Seed covenant ratified. |
| UNLOCK_CH040_PROPER_ENZYME | MQ_040 | Proper bio-enzyme sample | Enzyme harvested under Nia guidance. |
| UNLOCK_CH040_BIO_CODEX | MQ_040 | Bio-knowledge codex | Formula aligned with ecology. |
| UNLOCK_CH040_TOXIC_REMOVED | MQ_040 | Toxic weapon removed | Compound surrendered. |
| UNLOCK_CH040_CAIRO_ROUTE | MQ_040 | Cairo route | Chapter 41 unlocked. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_SEED_01 | The Listening Circle | char_elder_ama | Hear testimonies fully; summarize back without defending; record obligations. | ListeningCircleRespected. | SQ_Seed_01. |
| SQ_SEED_02 | Seeds and Formulas | char_nia | Decode Nia's cycle map; pair mutation phases with enzyme seasons; identify harvest window. | BioKnowledgeCodex. | SQ_Seed_02. |
| SQ_SEED_03 | The Root-Cutting Weapon | char_thu | Present compound; choose surrender/seal/destroy; keep inert research note. | ToxicWeaponSurrendered. | SQ_Seed_03. |
| SQ_SEED_04 | Mai's Lesson | char_mai | Help children map weather signs; plant a memory seed; record lesson for future schools. | SeedLessonRecorded. | SQ_Seed_04. |
| SQ_SEED_05 | Promise to Cairo | npc_cairo_samir | Explain harvest ethics to Samir; prepare cold/live transport; set siege rendezvous. | CairoEnzymeTransportReady. | SQ_Seed_05. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|

# Quests - CH039

Metadata:

- chapterID: CH039
- sourceFilename: chapter_039_rung_an_thanh_pho.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_039 | Enter Bio-Jungle | main | automatic | Group arrives at Africa bio-zone | Ethical enzyme trace collected; tribal elder invitation received | Metadata: MQ_039 - Enter Bio-Jungle. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ039_001 | MQ_039 | 1 | Enter overgrown airport bio-zone. | GoTo | LOC_CH039_OVERGROWN_AIRPORT | 1 | Main Quest objective 1. |
| OBJ_MQ039_002 | MQ_039 | 2 | Adapt to heat/humidity survival. | Survival | LOC_CH039_OVERGROWN_AIRPORT | 1 | Main Quest objective 2. |
| OBJ_MQ039_003 | MQ_039 | 3 | Identify EDENROT living-consent canopy classification. | Observe | LOC_CH039_OVERGROWN_AIRPORT | 1 | Main Quest objective 3. |
| OBJ_MQ039_004 | MQ_039 | 4 | Traverse jungle-swallowed city. | GoTo | LOC_CH039_SWALLOWED_CITY | 1 | Main Quest objective 4. |
| OBJ_MQ039_005 | MQ_039 | 5 | Avoid/handle overgrown infected. | Stealth | LOC_CH039_SWALLOWED_CITY | 1 | Main Quest objective 5. |
| OBJ_MQ039_006 | MQ_039 | 6 | Encounter Kito and survive trap. | Dialogue | LOC_CH039_CANOPY_CROSSING | 1 | Main Quest objective 6. |
| OBJ_MQ039_007 | MQ_039 | 7 | Earn provisional guide trust. | Dialogue | LOC_CH039_CANOPY_CROSSING | 1 | Main Quest objective 7. |
| OBJ_MQ039_008 | MQ_039 | 8 | Locate raider extraction site. | GoTo | LOC_CH039_OLD_HOSPITAL | 1 | Main Quest objective 8. |
| OBJ_MQ039_009 | MQ_039 | 9 | Rescue captured locals. | Rescue | LOC_CH039_OLD_HOSPITAL | 1 | Main Quest objective 9. |
| OBJ_MQ039_010 | MQ_039 | 10 | Stop destructive enzyme harvest. | CombatOrPuzzle | LOC_CH039_OLD_HOSPITAL | 1 | Main Quest objective 10. |
| OBJ_MQ039_011 | MQ_039 | 11 | Meet healer Nia. | GoTo | LOC_CH039_NIA_GROVE | 1 | Main Quest objective 11. |
| OBJ_MQ039_012 | MQ_039 | 12 | Learn enzyme ecological conditions. | Dialogue | LOC_CH039_NIA_GROVE | 1 | Main Quest objective 12. |
| OBJ_MQ039_013 | MQ_039 | 13 | Acknowledge living consent canopy rules. | Dialogue | LOC_CH039_NIA_GROVE | 1 | Main Quest objective 13. |
| OBJ_MQ039_014 | MQ_039 | 14 | Visit memorial grove respectfully. | Interact | LOC_CH039_MEMORIAL_GROVE | 1 | Main Quest objective 14. |
| OBJ_MQ039_015 | MQ_039 | 15 | Defend wounded bio-network node. | Combat | LOC_CH039_BIO_NETWORK_NODE | 1 | Main Quest objective 15. |
| OBJ_MQ039_016 | MQ_039 | 16 | Collect ethical enzyme trace. | Fetch | ITM_CH039_ETHICAL_ENZYME_TRACE | 1 | Main Quest objective 16. |
| OBJ_MQ039_017 | MQ_039 | 17 | Receive tribal elder invitation/condition. | Dialogue | LOC_CH039_RIVER_CROSSING | 1 | Main Quest objective 17. |
| OBJ_MQ039_018 | MQ_039 | 18 | Unlock Chapter 40 alliance trial. | Progression | LOC_CH039_RIVER_CROSSING | 1 | Main Quest objective 18. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ039_NODE_POISONED | MQ_039 | Bio-network node poisoned or burned. | Enzyme source destroyed. | Failure Conditions. |
| FAIL_MQ039_LOCALS_KILLED | MQ_039 | Captured locals killed by raiders. | Trust loss; alliance impossible. | Failure Conditions. |
| FAIL_MQ039_KITO_ABANDONS | MQ_039 | Kito abandons team. | No guide; lost in bio-zone. | Failure Conditions. |
| FAIL_MQ039_DOCTOR_EXTRACTS | MQ_039 | Doctor extracts without permission. | Alliance collapse. | Failure Conditions. |
| FAIL_MQ039_TOXIC_DEPLOYED | MQ_039 | Anti-growth weapon deployed near memorial/grove. | Network harm; trust destruction. | Failure Conditions. |
| FAIL_MQ039_ENZYME_CONTAMINATED | MQ_039 | Enzyme trace contaminated. | Useless sample. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ039_ENZYME | MQ_039 | data_item | EthicalEnzymeTrace | Completion Rewards. |
| REW_MQ039_ALLY | MQ_039 | faction_unlock | Kito/Nia provisional alliance | Completion Rewards. |
| REW_MQ039_SURVIVAL | MQ_039 | knowledge | Bio-zone survival knowledge | Completion Rewards. |
| REW_MQ039_INVITATION | MQ_039 | progression | Tribal council invitation | Completion Rewards. |
| REW_MQ039_CH40 | MQ_039 | route_unlock | Chapter 40 unlock | Completion Rewards. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_BIO_01 | Airport Swallowed by Roots | automatic | Secure landing zone; recover WHO/AU markers; avoid root sinkholes. | BioZoneEntryCache. | SQ_Bio_01. |
| SQ_BIO_02 | City Under the Canopy | automatic | Map safe canopy routes; avoid vibration-sensitive infected; recover city memory tokens. | CanopyRouteMap. | SQ_Bio_02. |
| SQ_BIO_03 | Enzyme Does Not Stand Alone | automatic | Observe plant/fungus/infected decay interaction; record Nia's conditions; collect naturally shed resin. | EthicalEnzymeTrace. | SQ_Bio_03. |
| SQ_BIO_04 | The Forest Does Not Betray | automatic | Follow silent route; stop when birds stop; do not cut marked vines. | KitoTrust. | SQ_Bio_04. |
| SQ_BIO_05 | The Trees Know the Names of the Dead | automatic | Repair raider damage; ask before recording names; leave offering. | MemorialGroveRespected. | SQ_Bio_05. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|

# Quests - CH025

Metadata:

- chapterID: CH025
- sourceFilename: chapter_025_vuot_thai_binh_duong.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_025 | Cross Pacific | main | char_trung | Warship secured and Pacific crossing unlocked | West Coast reached under aerial observation | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ025_01 | MQ_025 | 1 | Assign warship and Nha Di roles. | Decision | LOC_CH025_WARSHIP_DECK | 1 | Main Quest objective 1. |
| OBJ_MQ025_02 | MQ_025 | 2 | Define heavy weapons rules. | Decision | LOC_CH025_CIC_BRIDGE | 1 | Main Quest objective 2. |
| OBJ_MQ025_03 | MQ_025 | 3 | Set Pacific course. | Navigation | LOC_CH025_CIC_BRIDGE | 1 | Main Quest objective 3. |
| OBJ_MQ025_04 | MQ_025 | 4 | Share calm night. | Story | LOC_CH025_NHA_DI_DECK | 1 | Main Quest objective 4. |
| OBJ_MQ025_05 | MQ_025 | 5 | Detect satellite ping. | Detection | LOC_CH025_RADIO_RADAR_ROOM | 1 | Main Quest objective 5. |
| OBJ_MQ025_06 | MQ_025 | 6 | Trace coordinate refinement. | Investigation | LOC_CH025_RADIO_RADAR_ROOM | 1 | Main Quest objective 6. |
| OBJ_MQ025_07 | MQ_025 | 7 | Track sea horde convergence. | Detection | LOC_CH025_WARSHIP_DECK | 1 | Main Quest objective 7. |
| OBJ_MQ025_08 | MQ_025 | 8 | Reject full autonomous defense. | Decision | LOC_CH025_CIC_BRIDGE | 1 | Main Quest objective 8. |
| OBJ_MQ025_09 | MQ_025 | 9 | Deploy decoys and limited fire. | Combat | LOC_CH025_WARSHIP_EXTERIOR | 1 | Main Quest objective 9. |
| OBJ_MQ025_10 | MQ_025 | 10 | Protect Nha Di lines. | Defense | LOC_CH025_WARSHIP_EXTERIOR | 1 | Main Quest objective 10. |
| OBJ_MQ025_11 | MQ_025 | 11 | Survive swimmer boarding. | Combat | LOC_CH025_WARSHIP_EXTERIOR | 1 | Main Quest objective 11. |
| OBJ_MQ025_12 | MQ_025 | 12 | Reach West Coast approach. | Navigation | LOC_CH025_WEST_COAST_APPROACH | 1 | Main Quest objective 12. |
| OBJ_MQ025_13 | MQ_025 | 13 | Detect aerial observer. | Detection | LOC_CH025_WEST_COAST_APPROACH | 1 | Main Quest objective 13. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ025_01_001 | SQ_PACIFIC_01 | Let children name stars and sea sounds. | Family trust and morale. | SQ_Pacific_01. |
| OBJ_SQ025_02_001 | SQ_PACIFIC_02 | Store rules in both ship AI and written log. | Weapons ethics system durability. | SQ_Pacific_02. |
| OBJ_SQ025_03_001 | SQ_PACIFIC_03 | Find hidden coordinate log and decide confession timing. | Hoang trust branch. | SQ_Pacific_03. |
| OBJ_SQ025_04_001 | SQ_PACIFIC_04 | Avoid full automation during sea horde. | Resource/ammo/moral state preservation. | SQ_Pacific_04. |
| OBJ_SQ025_05_001 | SQ_PACIFIC_05 | Create private moment for Hoang confession. | Chapter 26/Hoang arc setup. | SQ_Pacific_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ025_FULL_AUTONOMOUS | MQ_025 | Allow full autonomous weapons. | High casualties, moral flag loss, Aster gains system insight. | Main Quest. |
| FAIL_MQ025_IGNORE_SATELLITE | MQ_025 | Ignore satellite ping. | Horde hits unprepared. | Main Quest. |
| FAIL_MQ025_CUT_NHA_DI_EARLY | MQ_025 | Cut Nha Di loose too early. | Home/morale rupture. | Main Quest. |
| FAIL_MQ025_EXCESS_AMMO | MQ_025 | Use too much ammo. | Chapter 26 landing weaker. | Main Quest. |
| FAIL_MQ025_HOANG_HIDES_ALL | MQ_025 | Hoang hides all logs. | Later trust collapse more severe. | Main Quest. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ025_PACIFIC_CROSSING | MQ_025 | navigation | Pacific crossing completed | Main Quest rewards. |
| REW_MQ025_COMMAND_STABILIZED | MQ_025 | system_unlock | Warship command stabilized | Main Quest rewards. |
| REW_MQ025_SEA_HORDE_CODEX | MQ_025 | codex_unlock | Sea horde codex entry | Main Quest rewards. |
| REW_MQ025_SATELLITE_THREAT | MQ_025 | threat_intel | Satellite threat unlocked | Main Quest rewards. |
| REW_MQ025_CALM_NIGHT | MQ_025 | morale_anchor | Family calm-night memory | Main Quest rewards. |
| REW_MQ025_ACT5_UNLOCK | MQ_025 | quest_unlock | Act 5 unlocked | Main Quest rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH025_OCEAN_CROSSING | MQ_025 | Ocean crossing route | Pacific crossing complete. |
| UNLOCK_CH025_SATELLITE_THREAT | MQ_025 | Satellite tracking threat | Satellite ping detected. |
| UNLOCK_CH025_SEA_HORDE_CODEX | MQ_025 | Sea horde large-scale encounter | Sea horde survived. |
| UNLOCK_CH025_ACT5 | MQ_025 | Act 5 North America | West Coast reached. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH025_SATELLITE_THREAT_UNLOCKED | MQ_025 | Satellite ping detected. |
| FLAG_CH025_EDENROT_ORBITAL_CONVERGENCE | MQ_025 | Classification recorded. |
| FLAG_CH025_HOANG_SEES_CONSEQUENCE | MQ_025 | Hoang sees satellite ping consequence. |
| FLAG_CH025_SEA_HORDE_SUMMONED | MQ_025 | Satellite pulse summons horde. |
| FLAG_CH025_PACIFIC_CROSSING_COMPLETE | MQ_025 | West Coast in sight. |
| FLAG_CH025_AERIAL_OBSERVER_TRACKING | MQ_025 | Drone/satellite detected near coast. |
| FLAG_CH025_ACT5_UNLOCKED | MQ_025 | Act 5 begins. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_PACIFIC_01 | Rare Calm Night | comp_mai | Share meal, let children name stars, talk with family, decide Hoang watch. | Family trust and morale anchor. | SQ_Pacific_01. |
| SQ_PACIFIC_02 | Rules For Big Guns | char_trung | Review weapon modes, define allowed targets, create council override, store rules. | Weapons ethics system. | SQ_Pacific_02. |
| SQ_PACIFIC_03 | Satellite Signal | comp_hoang | Detect ping, trace handshake, find hidden coordinate log, decide confession timing. | Hoang trust branch. | SQ_Pacific_03. |
| SQ_PACIFIC_04 | Something Below Is Coming | npc_doctor | Track sonar contacts, deploy decoys, defend Nha Di lines, avoid full automation. | Resource/ammo/moral state. | SQ_Pacific_04. |
| SQ_PACIFIC_05 | Hoang's Truth | comp_hoang | Create private moment, choose confession timing, preserve/delete log. | Chapter 26/Hoang arc. | SQ_Pacific_05. |

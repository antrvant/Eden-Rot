# Quests - CH024

Metadata:

- chapterID: CH024
- sourceFilename: chapter_024_tau_chien_khong_thuyen_truong.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_024 | Secure Warship | main | npc_dead_captain (logs) | Group reaches fallen naval base with naval code fragment | Warship secured, weapons-safe rules defined, Hoang sends hidden coordinates | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ024_01 | MQ_024 | 1 | Approach fallen naval base. | GoTo | LOC_CH024_NAVAL_BASE | 1 | Main Quest objective 1. |
| OBJ_MQ024_02 | MQ_024 | 2 | Avoid automated defense fire. | Stealth | LOC_CH024_MILITARY_PIER | 1 | Main Quest objective 2. |
| OBJ_MQ024_03 | MQ_024 | 3 | Dock Nha Di in blind spot. | Navigation | LOC_CH024_MILITARY_PIER | 1 | Main Quest objective 3. |
| OBJ_MQ024_04 | MQ_024 | 4 | Board warship. | GoTo | LOC_CH024_DECK_CWS | 1 | Main Quest objective 4. |
| OBJ_MQ024_05 | MQ_024 | 5 | Reach captain quarters. | GoTo | LOC_CH024_CAPTAIN_QUARTERS | 1 | Main Quest objective 5. |
| OBJ_MQ024_06 | MQ_024 | 6 | Recover captain authority token. | Retrieve | ITM_CH024_CAPTAIN_AUTHORITY_TOKEN | 1 | Main Quest objective 6. |
| OBJ_MQ024_07 | MQ_024 | 7 | Enter CIC. | GoTo | LOC_CH024_CIC | 1 | Main Quest objective 7. |
| OBJ_MQ024_08 | MQ_024 | 8 | Combine naval codes and captain authority. | Puzzle | ITM_CH024_NAVAL_CODE_FRAGMENT | 1 | Main Quest objective 8. |
| OBJ_MQ024_09 | MQ_024 | 9 | Stop turret targeting Nha Di. | Combat/Hack | ENM_CH024_CWS_TURRET | 1 | Main Quest objective 9. |
| OBJ_MQ024_10 | MQ_024 | 10 | Clear cyber-infected sailors. | Combat | ENM_CH024_CYBER_INFECTED_SAILOR | 1 | Main Quest objective 10. |
| OBJ_MQ024_11 | MQ_024 | 11 | Define weapons-safe rules. | Decision | LOC_CH024_CIC | 1 | Main Quest objective 11. |
| OBJ_MQ024_12 | MQ_024 | 12 | Secure warship. | Complete | LOC_CH024_CIC | 1 | Main Quest objective 12. |
| OBJ_MQ024_13 | MQ_024 | 13 | Detect or miss coordinate send. | Hidden | ITM_CH024_HOANG_COORDINATE_PACKET | 1 | Main Quest objective 13. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ024_01_001 | SQ_WARSHIP_01 | Listen to captain's final log before assuming command. | Stronger ethical framework for weapons rules. | SQ_Warship_01. |
| OBJ_SQ024_02_001 | SQ_WARSHIP_02 | Open sealed quarters without rushing. | Captain authority and morale boost. | SQ_Warship_02. |
| OBJ_SQ024_03_001 | SQ_WARSHIP_03 | Physically jam turret (optional). | Extra time for CIC hack. | SQ_Warship_03. |
| OBJ_SQ024_04_001 | SQ_WARSHIP_04 | Share officer logs with crew. | Ship AI understanding. | SQ_Warship_04. |
| OBJ_SQ024_05_001 | SQ_WARSHIP_05 | Notice suspicious log and trace outbound signal. | Evidence of Hoang betrayal. | SQ_Warship_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ024_DEFENSE_TRIGGERED | MQ_024 | Trigger defense early. | Nha Di damaged. | Main Quest. |
| FAIL_MQ024_CAPTAIN_LOG_SKIPPED | MQ_024 | Skip captain log. | Command ethics weaker; AI harder to convince. | Main Quest. |
| FAIL_MQ024_ASTER_FULL_SYNC | MQ_024 | Let Aster fully sync. | Binh exact location compromised. | Main Quest. |
| FAIL_MQ024_AGGRESSIVE_WEAPONS | MQ_024 | Activate weapons aggressively. | Mai/Binh trust loss. | Main Quest. |
| FAIL_MQ024_MANUAL_OVERRIDE_FAILED | MQ_024 | Fail manual override. | Nha Di destroyed/major casualty. | Main Quest. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ024_WARSHIP | MQ_024 | asset | Warship secured | Main Quest rewards. |
| REW_MQ024_PACIFIC_CROSSING | MQ_024 | system_unlock | Pacific crossing capability | Main Quest rewards. |
| REW_MQ024_HEAVY_DEFENSE | MQ_024 | system_unlock | Heavy defense systems locked/unlocked by ethics state | Main Quest rewards. |
| REW_MQ024_CAPTAIN_LOG | MQ_024 | lore_item | Captain log recovered | Main Quest rewards. |
| REW_MQ024_AI_PARTIAL_COMPLIANCE | MQ_024 | system_unlock | Ship AI partial compliance with council rules | Main Quest rewards. |
| REW_MQ024_HOANG_BETRAYAL_FLAG | MQ_024 | flag | Hoang coordinate betrayal flag set | Main Quest rewards. |
| REW_MQ024_CH025_SETUP | MQ_024 | quest_unlock | Chapter 25 satellite pursuit setup | Main Quest rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH024_PACIFIC_CROSSING | MQ_024 | Pacific crossing route | Warship secured. |
| UNLOCK_CH024_HEAVY_DEFENSE_ETHICS | MQ_024 | Heavy defense ethics UI/rules | Weapons-safe doctrine defined. |
| UNLOCK_CH024_CH025 | MQ_024 | Chapter 25 access | Warship secured and Nha Di docked. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH024_CAPTAIN_AUTHORITY_RECOVERED | MQ_024 | Player recovers captain token from quarters. |
| FLAG_CH024_TRUNG_PROVISIONAL_COMMANDER | MQ_024 | Trung assumes provisional command with council witness. |
| FLAG_CH024_WEAPONS_SAFE_DEFINED | MQ_024 | Weapons-safe rules logged in ship AI. |
| FLAG_CH024_HOANG_SENT_COORDINATES | MQ_024 | Hoang sends coordinate packet during admin window crisis. |
| FLAG_CH024_AUTONOMOUS_WARSHIP_HANDSHAKE | MQ_024 | Aster accepts warship handshake. |
| FLAG_CH024_PACIFIC_CROSSING_UNLOCKED | MQ_024 | Warship capability enables Pacific crossing. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_WARSHIP_01 | Captain's Authority | npc_dead_captain (logs) | Find bridge access, recover captain token, listen to final log, decide provisional command. | Command legitimacy for warship. | SQ_Warship_01. |
| SQ_WARSHIP_02 | Locked Captain's Quarters | environmental | Open sealed quarters, avoid infected officer, recover family photo/log. | Captain authority and morale. | SQ_Warship_02. |
| SQ_WARSHIP_03 | Automated Weapons | npc_ship_ai | Identify target lock, cut power or hack override, set weapons-safe rule. | Heavy weapons ethics system. | SQ_Warship_03. |
| SQ_WARSHIP_04 | Officer's Log | environmental | Collect officer logs, piece contradictory orders, learn AI misclassified captain. | Ship AI understanding. | SQ_Warship_04. |
| SQ_WARSHIP_05 | Coordinates Sent | comp_hoang | Notice suspicious log, ask Hoang or inspect system, trace outbound signal. | Chapter 25 pursuit intensity. | SQ_Warship_05. |

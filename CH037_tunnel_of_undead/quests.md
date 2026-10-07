# Quests - CH037

Metadata:

- chapterID: CH037
- sourceFilename: chapter_037_duong_ham_cua_ke_khong_chet.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_037 | Reach Alpine Lab | main | automatic | Group departs Paris metro with archive | Alpine Lab 7 outer gate opened; vestibule entered for Chapter 38 | Metadata: MQ_037 - Reach Alpine Lab. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ037_001 | MQ_037 | 1 | Depart Paris metro with Amelie route notes. | GoTo | LOC_CH037_PARIS_DEPARTURE | 1 | Main Quest objective 1. |
| OBJ_MQ037_002 | MQ_037 | 2 | Follow rail corridor toward Geneva. | GoTo | LOC_CH037_RAIL_TUNNEL | 1 | Main Quest objective 2. |
| OBJ_MQ037_003 | MQ_037 | 3 | Respond to Binh's first non-audio signal event. | Dialogue | LOC_CH037_RAIL_TUNNEL | 1 | Main Quest objective 3. |
| OBJ_MQ037_004 | MQ_037 | 4 | Establish three-source route rule. | Dialogue | LOC_CH037_MAINTENANCE_ALCOVE | 1 | Main Quest objective 4. |
| OBJ_MQ037_005 | MQ_037 | 5 | Reach abandoned Geneva quarantine checkpoint. | GoTo | LOC_CH037_GENEVA_CHECKPOINT | 1 | Main Quest objective 5. |
| OBJ_MQ037_006 | MQ_037 | 6 | Recover Margot recordings and transfer logs. | Fetch | ITM_CH037_MARGOT_RECORDINGS | 1 | Main Quest objective 6. |
| OBJ_MQ037_007 | MQ_037 | 7 | Identify dormant infected pulse behavior. | Observe | LOC_CH037_MORGUE_TUNNEL | 1 | Main Quest objective 7. |
| OBJ_MQ037_008 | MQ_037 | 8 | Traverse morgue tunnel safely. | Stealth | LOC_CH037_MORGUE_TUNNEL | 1 | Main Quest objective 8. |
| OBJ_MQ037_009 | MQ_037 | 9 | Manage oxygen in Alpine service tunnels. | Survival | LOC_CH037_ALPINE_TUNNEL | 1 | Main Quest objective 9. |
| OBJ_MQ037_010 | MQ_037 | 10 | Resolve maintenance AI contradiction. | Puzzle | LOC_CH037_ALPINE_TUNNEL | 1 | Main Quest objective 10. |
| OBJ_MQ037_011 | MQ_037 | 11 | Cross avalanche gallery under drone fire. | CombatOrTraverse | LOC_CH037_AVALANCHE_GALLERY | 1 | Main Quest objective 11. |
| OBJ_MQ037_012 | MQ_037 | 12 | Reach Alpine Lab 7 outer gate. | GoTo | LOC_CH037_ALPINE_LAB_GATE | 1 | Main Quest objective 12. |
| OBJ_MQ037_013 | MQ_037 | 13 | Use Patient Zero archive key. | Interact | LOC_CH037_ALPINE_LAB_GATE | 1 | Main Quest objective 13. |
| OBJ_MQ037_014 | MQ_037 | 14 | Reject invasive biomarker prompt. | Choice | LOC_CH037_ALPINE_LAB_GATE | 1 | Main Quest objective 14. |
| OBJ_MQ037_015 | MQ_037 | 15 | Unlock lab vestibule for Chapter 38. | Progression | LOC_CH037_LAB_VESTIBULE | 1 | Main Quest objective 15. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ037_01_001 | SQ_ALPS_01 | Let Binh describe signal without interruption. | BinhSignalConsentRespected. | SQ_Alps_01. |
| OBJ_SQ037_02_001 | SQ_ALPS_02 | Recover nurse Margot recordings. | GenevaQuarantineLogs. | SQ_Alps_02. |
| OBJ_SQ037_03_001 | SQ_ALPS_03 | Repair airflow valve in Alpine tunnel. | TunnelAirflowManual. | SQ_Alps_03. |
| OBJ_SQ037_04_001 | SQ_ALPS_04 | Observe dormant infected pulse cycle. | DormantPulseCountermeasure. | SQ_Alps_04. |
| OBJ_SQ037_05_001 | SQ_ALPS_05 | Build scanner spoof to avoid invasive scan. | AlpineGateOpenedEthically. | SQ_Alps_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ037_SIGNAL_OVERUSE | MQ_037 | Binh signal overused causing panic. | Trust loss; Binh isolation. | Failure Conditions. |
| FAIL_MQ037_DORMANT_WAKE | MQ_037 | Dormant infected wake in enclosed tunnel. | Combat in low oxygen. | Failure Conditions. |
| FAIL_MQ037_OXYGEN_DEPLETED | MQ_037 | Oxygen runs out in Alpine tunnel. | Health damage or death. | Failure Conditions. |
| FAIL_MQ037_AVALANCHE_BLOCKS | MQ_037 | Avalanche blocks main route before crossing. | Route lost. | Failure Conditions. |
| FAIL_MQ037_ARCHIVE_KEY_LOST | MQ_037 | Patient Zero archive key lost. | Cannot open lab gate. | Failure Conditions. |
| FAIL_MQ037_INVASIVE_SCAN | MQ_037 | Invasive scan accepted without consent. | Protocol violation. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ037_LAB_ACCESS | MQ_037 | route_unlock | Alpine Lab access | Completion Rewards. |
| REW_MQ037_DORMANT_COUNTER | MQ_037 | knowledge | Dormant infected counter | Completion Rewards. |
| REW_MQ037_THREE_SOURCE | MQ_037 | system_rule | Three-source route rule | Completion Rewards. |
| REW_MQ037_QUARANTINE_LORE | MQ_037 | lore | Geneva quarantine lore | Completion Rewards. |
| REW_MQ037_PZ_CONFIRMATION | MQ_037 | data | Patient Zero containment confirmation | Completion Rewards. |
| REW_MQ037_PLAGUE_DOCTOR | MQ_037 | lore_hook | Plague Doctor symbol/lore hook | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH037_SIGNAL_SENSITIVITY | MQ_037 | Binh signal sensitivity system | First non-audio signal event. |
| UNLOCK_CH037_DORMANT_INFECTED | MQ_037 | Dormant infected enemy behavior | Morgue tunnel encounter. |
| UNLOCK_CH037_THREE_SOURCE_RULE | MQ_037 | Three-source route rule | Maintenance alcove dialogue. |
| UNLOCK_CH037_ALPS_ROUTE | MQ_037 | Alpine Lab outer perimeter | Cross avalanche gallery. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH037_THREE_SOURCE_ROUTE_RULE | MQ_037 | Thu proposes rule; group agrees. |
| FLAG_CH037_BINH_SIGNAL_CONSENT_RESPECTED | SQ_ALPS_01 | Doctor asks Binh consent before scanning. |
| FLAG_CH037_GENEVA_QUARANTINE_LOGS | SQ_ALPS_02 | Margot recordings recovered. |
| FLAG_CH037_DORMANT_PULSE_COUNTERMEASURE | SQ_ALPS_04 | Pulse cycle observed and dampened. |
| FLAG_CH037_TUNNEL_AIRFLOW_MANUAL | SQ_ALPS_03 | Manual airflow path chosen. |
| FLAG_CH037_INVASIVE_PROMPT_REFUSED | MQ_037 | Group refuses biomarker scan. |
| FLAG_CH037_ALPINE_GATE_OPENED_ETHICALLY | MQ_037 | Gate opened with key and voice, no blood. |
| FLAG_CH037_DORMANT_SIGNAL_ARTERY_OPENED | MQ_037 | Lab vestibule opened. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_ALPS_01 | The Call Not Through Radio | char_binh | Let Binh describe without interruption; ask consent for observation; compare against physical evidence. | BinhSignalConsentRespected. | SQ_Alps_01. |
| SQ_ALPS_02 | Geneva Quarantine Station | automatic | Recover Margot recordings; find locked-out civilians list; confirm Patient Zero transfer. | GenevaQuarantineLogs. | SQ_Alps_02. |
| SQ_ALPS_03 | The Tunnel That Breathes | automatic | Repair airflow valve; choose safe oxygen route; avoid CO2 pockets. | TunnelAirflowManual. | SQ_Alps_03. |
| SQ_ALPS_04 | Those Who Have Not Died | automatic | Observe pulse cycle; mark safe windows; create pulse dampener. | DormantPulseCountermeasure. | SQ_Alps_04. |
| SQ_ALPS_05 | The Outer Gate of the Lab | automatic | Use archive key; build scanner spoof; refuse blood/biomarker sample. | AlpineGateOpenedEthically. | SQ_Alps_05. |

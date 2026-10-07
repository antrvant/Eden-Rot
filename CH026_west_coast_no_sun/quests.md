# Quests - CH026

Metadata:

- chapterID: CH026
- sourceFilename: chapter_026_bo_tay_khong_con_mat_troi.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_026 | Land in America | main | char_trung | West Coast reached after Pacific crossing | Landing complete, Mara contacted, Rebirth named, drone tracked, Silicon Valley route unlocked | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ026_01 | MQ_026 | 1 | Approach smoke-covered West Coast. | GoTo | LOC_CH026_WEST_COAST_APPROACH | 1 | Main Quest objective 1. |
| OBJ_MQ026_02 | MQ_026 | 2 | Track aerial observer without auto-firing. | Stealth | ENM_CH026_DRONE_WATCHER | 1 | Main Quest objective 2. |
| OBJ_MQ026_03 | MQ_026 | 3 | Launch landing party. | GoTo | LOC_CH026_LANDING_BEACH | 1 | Main Quest objective 3. |
| OBJ_MQ026_04 | MQ_026 | 4 | Secure old Coast Guard station. | Clear | LOC_CH026_COAST_GUARD_STATION | 1 | Main Quest objective 4. |
| OBJ_MQ026_05 | MQ_026 | 5 | Disable automated turret. | Puzzle | ENM_CH026_COASTAL_TURRET | 1 | Main Quest objective 5. |
| OBJ_MQ026_06 | MQ_026 | 6 | Meet Mara's survivor group. | Social | npc_mara | 1 | Main Quest objective 6. |
| OBJ_MQ026_07 | MQ_026 | 7 | Establish Rebirth identity externally. | Social | LOC_CH026_HIGHWAY_OVERPASS | 1 | Main Quest objective 7. |
| OBJ_MQ026_08 | MQ_026 | 8 | Bring Binh ashore after station secured. | Escort | comp_binh | 1 | Main Quest objective 8. |
| OBJ_MQ026_09 | MQ_026 | 9 | Decode drone tracking pulse. | Investigation | ENM_CH026_DRONE_WATCHER | 1 | Main Quest objective 9. |
| OBJ_MQ026_10 | MQ_026 | 10 | Scout highway to Silicon Valley route. | Exploration | LOC_CH026_HIGHWAY | 1 | Main Quest objective 10. |
| OBJ_MQ026_11 | MQ_026 | 11 | Interrupt Hoang confession. | Story | comp_hoang | 1 | Main Quest objective 11. |
| OBJ_MQ026_12 | MQ_026 | 12 | Set shore camp protocol. | Decision | LOC_CH026_LANDING_BEACH | 1 | Main Quest objective 12. |
| OBJ_MQ026_13 | MQ_026 | 13 | Unlock Silicon Graveyard route. | Unlock | LOC_CH026_HIGHWAY | 1 | Main Quest objective 13. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ026_01_001 | SQ_WEST_01 | Mark smoke-safe route on beach. | Landing safety established. | SQ_West_01. |
| OBJ_SQ026_02_001 | SQ_WEST_02 | Avoid immediate drone destruction and decode outgoing packet. | Drone/satellite threat confirmed. | SQ_West_02. |
| OBJ_SQ026_03_001 | SQ_WEST_03 | Lower weapons and offer medical aid to Mara's group. | Local reputation established. | SQ_West_03. |
| OBJ_SQ026_04_001 | SQ_WEST_04 | Decide whether to lower, repair, or leave station flag. | Cultural respect moment. | SQ_West_04. |
| OBJ_SQ026_05_001 | SQ_WEST_05 | Create private dialogue for Hoang confession before emergency. | Hoang trust pressure. | SQ_West_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ026_AUTO_FIRE_DRONE | MQ_026 | Auto-fire on drone. | Reveals warship fully, escalates satellite response. | Main Quest. |
| FAIL_MQ026_THREATEN_MARA | MQ_026 | Threaten Mara's group. | Lose first local ally. | Main Quest. |
| FAIL_MQ026_BINH_EARLY | MQ_026 | Bring Binh ashore too early. | Drone locks stronger. | Main Quest. |
| FAIL_MQ026_IGNORE_TURRET | MQ_026 | Ignore turret. | Casualty risk. | Main Quest. |
| FAIL_MQ026_HIDE_REBIRTH | MQ_026 | Hide Rebirth identity. | Future trust lower. | Main Quest. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ026_NORTH_AMERICA | MQ_026 | region_unlock | North America unlocked | Main Quest rewards. |
| REW_MQ026_MARA_CONTACT | MQ_026 | relationship | Mara/local survivor contact | Main Quest rewards. |
| REW_MQ026_SILICON_ROUTE | MQ_026 | navigation | Silicon Valley route | Main Quest rewards. |
| REW_MQ026_DRONE_CODEX | MQ_026 | codex_unlock | Drone observer codex | Main Quest rewards. |
| REW_MQ026_REBIRTH_NAME | MQ_026 | faction_unlock | Rebirth Alliance external identity | Main Quest rewards. |
| REW_MQ026_SHORE_CAMP | MQ_026 | asset | Shore landing camp | Main Quest rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH026_NORTH_AMERICA | MQ_026 | North America region | Landing complete. |
| UNLOCK_CH026_SILICON_VALLEY | MQ_026 | Silicon Valley route | Highway scouted. |
| UNLOCK_CH026_REBIRTH_EXTERNAL | MQ_026 | Rebirth Alliance external name | Mara contacted. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH026_MARA_CONTACT | MQ_026 | First contact with Mara established. |
| FLAG_CH026_REBIRTH_ALLIANCE_NAMED | MQ_026 | Rebirth name used with outsiders. |
| FLAG_CH026_DRONE_TRACKED_BINH | MQ_026 | Drone shifts to tracking Binh. |
| FLAG_CH026_IMMUNE_VECTOR_LANDED | MQ_026 | Drone transmits IMMUNE VECTOR LANDED. |
| FLAG_CH026_SILICON_VALLEY_ROUTE | MQ_026 | Route to Silicon Valley identified. |
| FLAG_CH026_HOANG_CONFESSION_INTERRUPTED_AGAIN | MQ_026 | Hoang confession cut by drone alarm. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_WEST_01 | Land Does Not Save | char_trung | Scout beach, mark smoke-safe route, clear station, secure supplies. | Landing safety established. | SQ_West_01. |
| SQ_WEST_02 | Drone Overhead | comp_hoang | Track drone path, avoid destruction, jam/spoof signal, decode packet. | Drone/satellite threat confirmed. | SQ_West_02. |
| SQ_WEST_03 | The First Americans | npc_mara | Lower weapons, offer medical aid, state intent, accept local boundaries. | Local reputation established. | SQ_West_03. |
| SQ_WEST_04 | Upside Down Flag | npc_mara | Inspect station flag, decide lower/repair/leave, hear Mara's explanation. | Cultural respect moment. | SQ_West_04. |
| SQ_WEST_05 | Interrupted Confession | comp_hoang | Create private dialogue, hear partial confession, emergency interrupts. | Hoang trust pressure. | SQ_West_05. |

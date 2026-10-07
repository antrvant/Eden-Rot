# Quests - CH013

Metadata:

- chapterID: CH013
- sourceFilename: chapter_013_dua_tre_khong_khoc.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_013 | Rescue Binh | main | char_mai | Starts after CH012 confirms Binh's location at the industrial zone | Trung, Mai, and Binh escape the factory and reunite outside the fence | Metadata and Main Quest. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ013_001 | MQ_013 | 1 | Reach the factory perimeter and observe from a distance. | GoTo | LOC_CH013_FACTORY_PERIMETER | 1 | Scene 1. |
| OBJ_MQ013_002 | MQ_013 | 2 | Scout the main gate and find a hidden entry point. | Investigate | LOC_CH013_TRUCK_GATE | 1 | Scene 1. |
| OBJ_MQ013_003 | MQ_013 | 3 | Follow Binh's marks and traces into the factory. | Investigate | LOC_CH013_PACKING_WORKSHOP | 1 | Scene 1, Scene 3. |
| OBJ_MQ013_004 | MQ_013 | 4 | Meet and question Ong Tu Nieu in the cafeteria. | TalkTo | npc_ong_tu_nieu | 1 | Scene 2. |
| OBJ_MQ013_005 | MQ_013 | 5 | Obtain the floor plan of the children's area from Ong Tu Nieu. | Obtain | ITM_CH013_FACTORY_FLOOR_PLAN | 1 | Scene 2. |
| OBJ_MQ013_006 | MQ_013 | 6 | Cross the worker floor without triggering the alarm. | Stealth | LOC_CH013_PACKING_WORKSHOP | 1 | Scene 3. |
| OBJ_MQ013_007 | MQ_013 | 7 | Find the child ledger and locate B-07 information. | Investigate | LOC_CH013_MANAGER_OFFICE | 1 | Scene 4. |
| OBJ_MQ013_008 | MQ_013 | 8 | Reach the children's detention room. | GoTo | LOC_CH013_CHILDREN_DETENTION | 1 | Scene 5. |
| OBJ_MQ013_009 | MQ_013 | 9 | Find Binh in the temporary medical room. | GoTo | LOC_CH013_TEMP_MEDICAL_ROOM | 1 | Scene 6. |
| OBJ_MQ013_010 | MQ_013 | 10 | Confront Factory Boss and escape. | Escape | LOC_CH013_LOADING_YARD | 1 | Scene 7. |
| OBJ_MQ013_011 | MQ_013 | 11 | Survive the cold storage lot escape. | Escape | LOC_CH013_COLD_STORAGE | 1 | Scene 8. |
| OBJ_MQ013_012 | MQ_013 | 12 | Decide whether to rescue the locked children. | Choice | LOC_CH013_LOADING_YARD | 1 | Scene 9. |
| OBJ_MQ013_013 | MQ_013 | 13 | Leave the factory with Binh. | GoTo | LOC_CH013_OUTSIDE_FENCE | 1 | Scene 10. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ013_01_001 | SQ_013_01 | Discover hidden rice in Ong Tu Nieu's coat. | Unlocks soft dialogue path with Ong Tu Nieu. | Scene 2. |
| OBJ_SQ013_02_001 | SQ_013_02 | Free the forced workers quietly. | Workers create distraction later; increases chaos. | Scene 3. |
| OBJ_SQ013_03_001 | SQ_013_03 | Find Binh's teddy bear in the children's room. | Binh trusts faster; unique end-chapter dialogue. | Scene 5. |
| OBJ_SQ013_04_001 | SQ_013_04 | Take the child ledger from the manager's office. | Missing children chain and EDEN lore unlock. | Scene 4. |
| OBJ_SQ013_05_001 | SQ_013_05 | Survive the cold storage Spitter encounter. | Foreshadows Spitter enemy type. | Scene 8. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ013_EARLY_ALARM | MQ_013 | Alarm triggers too early. | Increased guard patrol; children relocated; harder escape. | Implementation Notes. |
| FAIL_MQ013_ONG_TU_NIEU_DIES | MQ_013 | Ong Tu Nieu dies before giving information. | Player must find route through environmental puzzle. | Implementation Notes. |
| FAIL_MQ013_NO_WORKER_DISTRACTION | MQ_013 | Worker uprising not activated. | Factory Boss has more guards at Scene 7. | Implementation Notes. |
| FAIL_MQ013_LEDGER_SKIPPED | MQ_013 | Child ledger not retrieved. | Immunity arc still opens but missing evidence and children list. | Implementation Notes. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ013_BINH_COMPANION | MQ_013 | companion_unlock | Binh joins as companion/family member | Rewards section. |
| REW_MQ013_MAI_ROLE_EXPANSION | MQ_013 | role_expansion | Mai becomes Tracker/Caretaker active gameplay role | Rewards section. |
| REW_MQ013_ONG_TU_NIEU_NPC | MQ_013 | npc_unlock | Ong Tu Nieu available for base (conditional) | Rewards section. |
| REW_MQ013_TEDDY_BEAR | MQ_013 | item | ITM_CH013_BINH_TEDDY_BEAR | Rewards section. |
| REW_MQ013_CHILD_LEDGER | MQ_013 | item | ITM_CH013_CHILD_LEDGER | Rewards section. |
| REW_MQ013_SILENT_BLOOD_LORE | MQ_013 | lore_item | ITM_CH013_EDEN_NODE_NOTE | Rewards section. |
| REW_MQ013_EDENROT_CLASS_UPDATE | MQ_013 | lore_update | EDENROT CLASS: SILENT BLOOD / EDEN NODE | Rewards section. |
| REW_MQ013_CHILDCARE_UNLOCK | MQ_013 | system_unlock | Childcare/school morale system for base | Rewards section. |
| REW_MQ013_FAMILY_REUNITED | MQ_013 | major_flag | FLAG_CH013_FAMILY_REUNITED_ACT2 | Rewards section. |
| REW_MQ013_IMMUNITY_MYSTERY | MQ_013 | major_flag | FLAG_CH013_BINH_IMMUNITY_MYSTERY_STARTED | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH013_BINH_COMPANION | MQ_013 | Binh companion/family | Medical room reunion complete. |
| UNLOCK_CH013_MAI_TRACKER | MQ_013 | Mai Tracker/Caretaker role | Chapter progression through factory. |
| UNLOCK_CH013_ONG_TU_NIEU_BASE | MQ_013 | Ong Tu Nieu base NPC | Ong Tu Nieu survives and joins group. |
| UNLOCK_CH013_CHILDCARE_SYSTEM | MQ_013 | Childcare/school morale system | Children rescued; base-building motivation. |
| UNLOCK_CH013_EDEN_LORE_CHAIN | MQ_013 | EDEN/Edenrot lore chain | Child ledger taken; Silent Blood discovered. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH013_BINH_FOUND | MQ_013 | Player locates Binh in medical room. |
| FLAG_CH013_FAMILY_REUNITED_ACT2 | MQ_013 | Trung, Mai, Binh reunited in medical room. |
| FLAG_CH013_BINH_IMMUNITY_MYSTERY_STARTED | MQ_013 | Binh reveals scratch from infected with no fever. |
| FLAG_CH013_EDENROT_RESPONSE_CLASS_FOUND | MQ_013 | Player reads child ledger Edenrot Response column. |
| FLAG_CH013_SILENT_BLOOD_LORE | MQ_013 | Ong Tu Nieu delivers torn page with EDENROT CLASS: SILENT BLOOD. |
| FLAG_CH013_FACTORY_BOSS_SURVIVED | MQ_013 | Factory Boss escapes or body unconfirmed. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_013_01 | Old Cook | npc_ong_tu_nieu | Discover hidden rice; choose approach (threaten/persuade/observe); get floor plan; decide whether to bring Ong Tu Nieu. | If saved: base food NPC and redemption arc. If left: worker group gets his help but Trung loses Binh's detention story. | SQ_Factory_01. |
| SQ_013_02 | Forced Workers | npc_worker_lead | Talk to worker lead; disable chain/PA; create distraction; bring worker lead to loading yard. | Saved workers provide crafting/building knowledge for first base. | SQ_Factory_02. |
| SQ_013_03 | Binh's Teddy Bear | environmental | Find teddy bear in children's room; check stitching on back; give to Binh at right time. | If given at right moment: Binh trusts faster; unique end-chapter dialogue. | SQ_Factory_03. |
| SQ_013_04 | Children's Logbook | environmental | Open safe in manager's office; read fever/reaction/transfer columns; choose to take, burn, or falsify. | Taking unlocks missing children chain and EDEN lore. Burning protects Binh temporarily but losesclues. | SQ_Factory_04. |
| SQ_013_05 | Cold Storage Lot | environmental | Discover chained infected; manage lock system; find exit through cold room; survive Spitter foreshadow acid spit. | Foreshadows Spitter enemy and future biological weaponization question. | SQ_Factory_05. |

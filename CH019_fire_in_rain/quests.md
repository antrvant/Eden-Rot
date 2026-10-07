# Quests - CH019

Metadata:

- chapterID: CH019
- sourceFilename: chapter_019_lua_trong_mua.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_019 | Rescue Mai | main | char_trung (protagonist) | Mai captured in Chapter 18; base still smoking from raid. | Mai rescued; Architect file recovered; Hoang fate decided; classroom rule repaired; Act 3 complete. | Metadata, Main Quest section. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ019_01 | MQ_019 | 1 | Decode Mai's chalk mark on the desk. | Investigate | ITM_CH019_MAI_CHALK | 1 | Scene 1, DT_081. |
| OBJ_MQ019_02 | MQ_019 | 2 | Decide Hoang's role in rescue: tied, guarded, or armed under watch. | Decision | comp_hoang | 1 | Scene 1, SQ_FireRain_02. |
| OBJ_MQ019_03 | MQ_019 | 3 | Track the fort route through rain-soaked forest. | GoTo | LOC_CH019_RAINY_FOREST_ROAD | 1 | Scene 2, DT_082. |
| OBJ_MQ019_04 | MQ_019 | 4 | Infiltrate the bandit brick factory. | GoTo | LOC_CH019_BANDIT_FORT | 1 | Scene 4. |
| OBJ_MQ019_05 | MQ_019 | 5 | Locate and follow Mai's internal chalk trail inside the fort. | Investigate | LOC_CH019_BANDIT_FORT | 1 | Scene 3. |
| OBJ_MQ019_06 | MQ_019 | 6 | Disable bandit checkpoint comms and server lock. | Interact | LOC_CH019_SERVER_ROOM | 1 | Scene 5. |
| OBJ_MQ019_07 | MQ_019 | 7 | Recover Architect/EDEN broker files from server. | Investigate | ITM_CH019_ARCHITECT_BROKER_DRIVE | 1 | Scene 5, DT_084. |
| OBJ_MQ019_08 | MQ_019 | 8 | Identify Edenrot dormancy hunt and naval route in server data. | Investigate | LOC_CH019_SERVER_ROOM | 1 | Scene 5. |
| OBJ_MQ019_09 | MQ_019 | 9 | Rescue Mai from bandit lieutenant. | Combat | char_mai | 1 | Scene 6. |
| OBJ_MQ019_10 | MQ_019 | 10 | Escape fire, rain, and horde chaos from the fort. | GoTo | LOC_CH019_FLOODED_YARD | 1 | Scene 6. |
| OBJ_MQ019_11 | MQ_019 | 11 | Decide whether to save or leave Hoang on the canal bridge. | Decision | comp_hoang | 1 | Scene 7, DT_085. |
| OBJ_MQ019_12 | MQ_019 | 12 | Return to base. | GoTo | LOC_CH019_BASE_HOME | 1 | Scene 8. |
| OBJ_MQ019_13 | MQ_019 | 13 | Decode server files and unlock naval route with Doctor. | Interact | npc_doctor | 1 | Scene 8. |
| OBJ_MQ019_14 | MQ_019 | 14 | Repair the classroom blackboard rule. | Interact | LOC_CH019_CLASS_3B_AFTER | 1 | Scene 8. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ019_01_001 | SQ_FireRain_01 | Decode all three-stripe chalk marks along the forest route. | Faster rescue; more Mai agency revealed. | SQ_FireRain_01. |
| OBJ_SQ019_01_002 | SQ_FireRain_01 | Identify false chalk mark planted by bandits. | Avoids ambush; trust in Mai's trail confirmed. | SQ_FireRain_01. |
| OBJ_SQ019_02_001 | SQ_FireRain_02 | Stop Hoang from making solo revenge attempt during mission. | Hoang fate less darkened; Binh trust preserved. | SQ_FireRain_02. |
| OBJ_SQ019_03_001 | SQ_FireRain_03 | Choose to delete, copy, or broadcast server files. | Affects Act 4 intel availability and EDEN awareness. | SQ_FireRain_03. |
| OBJ_SQ019_04_001 | SQ_FireRain_04 | Prevent fuel tank explosion near prisoners in flooded yard. | More survivors extracted; higher mission risk. | SQ_FireRain_04. |
| OBJ_SQ019_04_002 | SQ_FireRain_04 | Use rain and sluice to cross fire breaks safely. | Safer escape path; environmental puzzle. | SQ_FireRain_04. |
| OBJ_SQ019_05_001 | SQ_FireRain_05 | Let children rewrite the blackboard rule themselves. | Child morale recovery; Binh agency. | SQ_FireRain_05. |
| OBJ_SQ019_05_002 | SQ_FireRain_05 | Let So 4 choose a symbol or name space on the board. | So 4 identity seed; not yet a name but not empty. | SQ_FireRain_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ019_REFUSE_HOANG_GUIDANCE | MQ_019 | Refuse Hoang's guidance entirely. | Longer route; Mai danger rises; team takes wrong path. | Fail States. |
| FAIL_MQ019_TRUST_HOANG_FULLY | MQ_019 | Trust Hoang fully without restraint. | Hoang may make risky solo choice; mission compromised. | Fail States. |
| FAIL_MQ019_IGNORE_SERVER | MQ_019 | Ignore server room objective. | Miss Architect file; delay Act 4 unlock. | Fail States. |
| FAIL_MQ019_SHOOT_LIEUTENANT_RECKLESSLY | MQ_019 | Shoot lieutenant without regard for Mai as shield. | Mai wounded; rescue incomplete. | Fail States. |
| FAIL_MQ019_LEAVE_HOANG_TO_DIE | MQ_019 | Leave Hoang to die on the canal bridge. | Hoang fate darkens; Binh trust changes; moral cost. | Fail States. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ019_MAI_RESCUED | MQ_019 | character_rescue | Mai returned to base | Rewards. |
| REW_MQ019_ARCHITECT_FILE | MQ_019 | intel_unlock | Architect/EDEN broker file recovered | Rewards. |
| REW_MQ019_EDENROT_CONFIRMATION | MQ_019 | lore_unlock | Edenrot dormancy confirmed by Architect broker files | Rewards. |
| REW_MQ019_NAVAL_ROUTE | MQ_019 | route_unlock | Maritime route and naval key trace | Rewards. |
| REW_MQ019_BANDIT_FORT_WEAKENED | MQ_019 | world_state | Bandit fort loses comms and server | Rewards. |
| REW_MQ019_HOANG_FATE_PENDING | MQ_019 | continuity_flag | Hoang fate unresolved; council to judge | Rewards. |
| REW_MQ019_ACT3_COMPLETE | MQ_019 | progression | Act 3 closes | Rewards. |
| REW_MQ019_MAI_CHALK_ROUTE | MQ_019 | item | ITM_CH019_MAI_CHALK | Rewards. |
| REW_MQ019_ARCHITECT_DRIVE | MQ_019 | item | ITM_CH019_ARCHITECT_BROKER_DRIVE | Rewards. |
| REW_MQ019_HOANG_SPARED_FLAG | MQ_019 | moral_flag | HoangSparedInFrontOfBinh | Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH019_NAVAL_ROUTE | MQ_019 | Naval Route to Coast | Server files decoded; maritime route confirmed. |
| UNLOCK_CH019_ACT4_EAST_ASIA | MQ_019 | Act 4: East Asia & Naval Key | Architect file recovered; Edenrot dormancy confirmed. |
| UNLOCK_CH019_LEAVE_BASE_SOON | MQ_019 | Prepare to Leave Home | Base location compromised; bandits know, Cult approaching, EDEN aware. |
| UNLOCK_CH019_HOANG_COUNCIL_TRIAL | MQ_019 | Hoang Council Judgment | Hoang detained; council must decide status. |
| UNLOCK_CH019_MAI_ADVOCATE_CONTINUES | MQ_019 | Mai Advocate Role Continues | Mai rescued; resumes Children/Family council seat. |
| UNLOCK_CH019_EDENROT_HUNT_AWARENESS | MQ_019 | Edenrot Hunt Awareness | Group learns Architects actively track dormancy and immune children. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH019_MAI_RESCUED | MQ_019 | Mai escapes fort with Trung's team. |
| FLAG_CH019_HOANG_SPARED_IN_FRONT_OF_BINH | MQ_019 | Trung does not kill Hoang; Binh sees or learns of decision. |
| FLAG_CH019_ARCHITECT_FILE_RECOVERED | MQ_019 | Server drive copied and extracted from fort. |
| FLAG_CH019_EDENROT_DORMANCY_CONFIRMED | MQ_019 | Doctor decodes EDENROT DORMANCY RESPONSE file. |
| FLAG_CH019_NAVAL_ROUTE_UNLOCKED | MQ_019 | Maritime route and naval key trace identified. |
| FLAG_CH019_BANDIT_FORT_WEAKENED | MQ_019 | Fort burns; comms and server destroyed or taken. |
| FLAG_CH019_HOANG_FATE_PENDING_COUNCIL | MQ_019 | Hoang returned alive but detained. |
| FLAG_CH019_BINH_JUSTICE_QUESTION | MQ_019 | Binh asks why Trung did not kill Hoang. |
| FLAG_CH019_CLASSROOM_RULE_REPAIRED | MQ_019 | Blackboard rule rewritten by Binh/S04/Mai. |
| FLAG_CH019_ACT3_COMPLETE | MQ_019 | Act 3 emotional and narrative arc closed. |
| FLAG_CH019_LEAVE_FIRST_BASE_SOON | MQ_019 | Group must prepare to leave "Home." |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_FireRain_01 | Mai's Chalk Marks | char_trung | Decode three-stripe chalk marks; follow protected marks under eaves; identify false mark; reach internal route. | Faster rescue and more Mai agency; trust in partner's intelligence. | SQ_FireRain_01. |
| SQ_FireRain_02 | Tied Prisoner | comp_hoang | Choose Hoang's restraint level; let Hoang disable traps; stop Hoang from solo revenge; decide post-mission status. | Affects Hoang fate; council trust. | SQ_FireRain_02. |
| SQ_FireRain_03 | Server in Brick Factory | char_trung | Restore generator; bypass lock; download files; choose delete/copy/broadcast; escape before fire spreads. | Architect knowledge and naval route availability. | SQ_FireRain_03. |
| SQ_FireRain_04 | Fire Burning Under Rain | npc_worker_lead | Avoid steam/smoke; open sluice or roof drainage; use rain to cross fire breaks; prevent fuel tank explosion near prisoners. | More survivors or higher risk. | SQ_FireRain_04. |
| SQ_FireRain_05 | Blackboard Corrected | char_binh | Clean bullet mark on blackboard; let children rewrite rule; decide whether to mention Mai's capture honestly; let So 4 choose symbol. | Child morale recovery; honesty policy. | SQ_FireRain_05. |

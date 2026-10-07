# Quests - CH020

Metadata:

- chapterID: CH020
- sourceFilename: chapter_020_bien_dong_day_xac.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_020 | Reach the Coast | main | Architect drive route | After CH019; Architect drive obtained and Mai rescued | Group survives first bio-storm at sea | Metadata and Main Quest. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ020_001 | MQ_020 | 1 | Hold council judgment on Hoang's status. | Decision | comp_hoang | 1 | Scene 1. |
| OBJ_MQ020_002 | MQ_020 | 2 | Choose travel team and assign base caretakers. | Decision | LOC_CH020_BASE_HOME | 1 | Scene 2. |
| OBJ_MQ020_003 | MQ_020 | 3 | Say goodbye to Classroom 3B and the blackboard. | Interact | LOC_CH020_CLASSROOM_3B | 1 | Scene 2, DT_088. |
| OBJ_MQ020_004 | MQ_020 | 4 | Follow Architect naval route toward the Mekong. | Travel | LOC_CH020_ROAD_TO_MEKONG | 1 | Scene 3. |
| OBJ_MQ020_005 | MQ_020 | 5 | Cross the corpse-filled river silently. | Stealth | LOC_CH020_CANAL_SYSTEM | 1 | Scene 3. |
| OBJ_MQ020_006 | MQ_020 | 6 | Negotiate passage with river pilot Lam. | TalkTo | npc_lam | 1 | Scene 4, DT_089. |
| OBJ_MQ020_007 | MQ_020 | 7 | Reach the coastal fishing port. | Travel | LOC_CH020_COASTAL_FISHING_PORT | 1 | Scene 5. |
| OBJ_MQ020_008 | MQ_020 | 8 | Secure the unnamed vessel. | Interact | LOC_CH020_UNNAMED_CARGO_SHIP | 1 | Scene 5. |
| OBJ_MQ020_009 | MQ_020 | 9 | Repair and fuel the boat under attack. | Action | LOC_CH020_UNNAMED_CARGO_SHIP | 1 | Scene 5. |
| OBJ_MQ020_010 | MQ_020 | 10 | Escape the port from bandits and drowned infected. | Combat | LOC_CH020_COASTAL_FISHING_PORT | 1 | Scene 5. |
| OBJ_MQ020_011 | MQ_020 | 11 | Leave the Vietnam coast. | Travel | LOC_CH020_NEARSHORE_WATERS | 1 | Scene 6. |
| OBJ_MQ020_012 | MQ_020 | 12 | Survive the first bio-storm at sea. | Survive | LOC_CH020_OPEN_SEA_NIGHT | 1 | Scene 7. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ020_01_001 | SQ_Coast_01 | Take a portable symbol from the classroom. | Portable home symbol; chalk fragment. | SQ_Coast_01. |
| OBJ_SQ020_02_001 | SQ_Coast_02 | Let Binh hear part of Hoang's judgment. | Binh trust/healing milestone. | SQ_Coast_02. |
| OBJ_SQ020_03_001 | SQ_Coast_03 | Collect a water sample from Edenrot river. | Maritime infection lore; Doctor research. | SQ_Coast_03. |
| OBJ_SQ020_04_001 | SQ_Coast_04 | Decide a name for the boat. | Vessel identity; morale. | SQ_Coast_04. |
| OBJ_SQ020_05_001 | SQ_Coast_05 | Give chalk to So 4 or keep it. | Binh trust/healing; connection to base. | SQ_Coast_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ020_HOANG_EXILED_EARLY | MQ_020 | Exile Hoang before route decoded. | Travel path harder; more bandit ambush. | Fail States. |
| FAIL_MQ020_TOO_MANY_REFUGEES | MQ_020 | Bring too many refugees on boat. | Boat capacity crisis. | Fail States. |
| FAIL_MQ020_RIVER_NOISE | MQ_020 | Use engine or make noise during river crossing. | Drowned infected attack during crossing. | Fail States. |
| FAIL_MQ020_NEGOTIATION_FAILED | MQ_020 | Fail to negotiate with Lam or Thu. | Must steal boat; reputation hit. | Fail States. |
| FAIL_MQ020_PORT_DELAY | MQ_020 | Delay too long at fishing port. | Bandit pursuers catch up; casualty risk. | Fail States. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ020_BOAT_TRAVEL | MQ_020 | system_unlock | Boat travel unlocked | Rewards section. |
| REW_MQ020_MARITIME_ROUTE | MQ_020 | quest_unlock | Maritime route unlocked | Rewards section. |
| REW_MQ020_NPC_LAM | MQ_020 | companion_unlock | Lam joins as river pilot | Rewards section. |
| REW_MQ020_NPC_THU | MQ_020 | companion_unlock | Thu joins as coastal mechanic | Rewards section. |
| REW_MQ020_CHALK_FRAGMENT | MQ_020 | item | ITM_CH020_CHALK_FRAGMENT_CLASSROOM_3B | Rewards section. |
| REW_MQ020_ARCHITECT_NAVAL_ROUTE | MQ_020 | item | ITM_CH020_ARCHITECT_NAVAL_ROUTE | Rewards section. |
| REW_MQ020_BIO_STORM_ENCOUNTERED | MQ_020 | threat_flag | BioStormEncountered | Rewards section. |
| REW_MQ020_MARITIME_EDENROT_ENTERED | MQ_020 | threat_flag | MaritimeEdenrotZoneEntered | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH020_BOAT_TRAVEL | MQ_020 | Boat Travel | Vessel secured and launched. |
| UNLOCK_CH020_MARITIME_HAZARD | MQ_020 | Maritime Hazard System | Edenrot zone entered. |
| UNLOCK_CH020_DROWNED_INFECTED | MQ_020 | Drowned Infected Ecology | River drowned encountered. |
| UNLOCK_CH020_MOBILE_BASE | MQ_020 | Mobile Base / Vessel Prep | Ship becomes travel base. |
| UNLOCK_CH020_NAVAL_ROUTE_OBJECTIVE | MQ_020 | Naval Route Objective Chain | Architect route decoded. |
| UNLOCK_CH020_COASTAL_FACTIONS | MQ_020 | Coastal Factions / Trade | Lam and Thu introduced. |
| UNLOCK_CH020_EDENROT_ZONES | MQ_020 | Edenrot Maritime Zones | Edenrot classified. |
| UNLOCK_CH020_BIO_STORM_TRACKING | MQ_020 | Bio-Storm Signal Tracking | EDEN NODE ACTIVE detected. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH020_HOANG_MONITORED_COMPANION | MQ_020 | Council judgment resolves. |
| FLAG_CH020_FIRST_BASE_CARETAKERS_ASSIGNED | MQ_020 | Travel team and caretakers chosen. |
| FLAG_CH020_BINH_LEFT_NAME_ON_BOARD | MQ_020 | Binh chooses not to erase name. |
| FLAG_CH020_PORTABLE_HOME_SYMBOL | MQ_020 | Mai takes chalk fragment. |
| FLAG_CH020_RIVER_DROWNED_ENCOUNTERED | MQ_020 | Drowned infected stir during river crossing. |
| FLAG_CH020_BOAT_UNLOCKED | MQ_020 | Ship secured and launched. |
| FLAG_CH020_VIETNAM_COAST_DEPARTED | MQ_020 | Ship leaves coast. |
| FLAG_CH020_BIO_STORM_ENCOUNTERED | MQ_020 | Bio-storm begins at sea. |
| FLAG_CH020_EDEN_NODE_ACTIVE_SIGNAL | MQ_020 | Radio picks up EDEN NODE ACTIVE. |
| FLAG_CH020_MARITIME_RELAY_ONLINE | MQ_020 | Radio picks up MARITIME RELAY ONLINE. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Coast_01 | Leaving Home | char_mai | Assign caretakers, divide supplies, leave blackboard message, take portable symbol. | Base morale and future return state. | SQ_Coast_01. |
| SQ_Coast_02 | Hoang's Trial | council | Hear charges, hear Hoang's admission, decide temporary status, explain to Binh. | Hoang companion state. | SQ_Coast_02. |
| SQ_Coast_03 | Corpse-Laden River | npc_lam | Scout current, avoid corpse clusters, cross silently, collect sample optional. | Maritime infection lore. | SQ_Coast_03. |
| SQ_Coast_04 | Nameless Ship | npc_thu | Inspect boat, retrieve filter/fuel, defend mechanic, decide boat name. | Unlock vessel as mobile base. | SQ_Coast_04. |
| SQ_Coast_05 | River Carrying Names | char_binh | Talk with Binh at blackboard, choose keep/copy/erase name, give chalk to So 4. | Binh trust/healing. | SQ_Coast_05. |

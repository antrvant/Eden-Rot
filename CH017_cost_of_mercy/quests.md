# Quests - CH017

Metadata:

- chapterID: CH017
- sourceFilename: chapter_017_cai_gia_cua_long_thuong.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_017 | Save or Secure | main | char_trung | Distress signal received from refugee convoy | Convoy rescued (partial); supply theft investigated; bandit checkpoint marker found | Metadata and Main Quest. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ017_001 | MQ_017 | 1 | Receive refugee convoy distress signal. | Listen | LOC_CH017_RADIO_CORNER | 1 | Scene 1. |
| OBJ_MQ017_002 | MQ_017 | 2 | Convene council emergency vote. | Decision | LOC_CH017_TEACHERS_ROOM | 1 | Scene 2. |
| OBJ_MQ017_003 | MQ_017 | 3 | Choose rescue loadout: medicine, ammo, fuel, labor. | Decision | FAC_CH017_BASE_COMMUNITY | 1 | Scene 2. |
| OBJ_MQ017_004 | MQ_017 | 4 | Reach collapsed bridge. | GoTo | LOC_CH017_COLLAPSED_BRIDGE | 1 | Scene 3. |
| OBJ_MQ017_005 | MQ_017 | 5 | Assess convoy authenticity and threats. | Investigate | LOC_CH017_CONVOY_SITE | 1 | Scene 3. |
| OBJ_MQ017_006 | MQ_017 | 6 | Assess Edenrot exposure risk and quarantine needs. | Investigate | LOC_CH017_COLLAPSED_BRIDGE | 1 | Scene 3. |
| OBJ_MQ017_007 | MQ_017 | 7 | Triage injured refugees. | Interact | npc_injured_father | 1 | Scene 3. |
| OBJ_MQ017_008 | MQ_017 | 8 | Recover medicine or fuel from trapped vehicle. | Decision | LOC_CH017_FUEL_DEPOT | 1 | Scene 4. |
| OBJ_MQ017_009 | MQ_017 | 9 | Rescue children and priority wounded. | Rescue | npc_refugee_children | 1 | Scene 5. |
| OBJ_MQ017_010 | MQ_017 | 10 | Hold bridge during horde approach. | Combat | LOC_CH017_COLLAPSED_BRIDGE | 1 | Scene 6. |
| OBJ_MQ017_011 | MQ_017 | 11 | Return refugees to base/quarantine. | GoTo | LOC_CH017_BASE_NHA | 1 | Scene 7. |
| OBJ_MQ017_012 | MQ_017 | 12 | Allocate reduced rations. | Decision | npc_ong_tu_nieu | 1 | Scene 7. |
| OBJ_MQ017_013 | MQ_017 | 13 | Investigate night supply theft. | Investigate | LOC_CH017_SUPPLY_ROOM | 1 | Scene 8. |
| OBJ_MQ017_014 | MQ_017 | 14 | Discover bandit checkpoint marker. | Investigate | LOC_CH017_SUPPLY_ROOM | 1 | Scene 8. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ017_01_001 | SQ_Mercy_01 | Identify Ba Sau as convoy leader. | Faster coordination; more refugees survive. | SQ_Mercy_01. |
| OBJ_SQ017_01_002 | SQ_Mercy_01 | Count children and wounded before rescue. | Better triage; fewer casualties. | SQ_Mercy_01. |
| OBJ_SQ017_01_003 | SQ_Mercy_01 | Decide who crosses the bridge first. | Affects casualty count and morale. | SQ_Mercy_01. |
| OBJ_SQ017_02_001 | SQ_Mercy_02 | Reach trapped vehicle at fuel depot. | Access to medicine or fuel cargo. | SQ_Mercy_02. |
| OBJ_SQ017_02_002 | SQ_Mercy_02 | Pick cargo priority: medicine or fuel. | Affects Doctor lab progress or generator. | SQ_Mercy_02. |
| OBJ_SQ017_02_003 | SQ_Mercy_02 | Defend loader during horde approach. | Prevents additional casualties. | SQ_Mercy_02. |
| OBJ_SQ017_03_001 | SQ_Mercy_03 | Find child under bus. | Unlocks So 4 rescue. | SQ_Mercy_03. |
| OBJ_SQ017_03_002 | SQ_Mercy_03 | Avoid forcing name on child. | Trust building with So 4. | SQ_Mercy_03. |
| OBJ_SQ017_03_003 | SQ_Mercy_03 | Offer temporary name or token. | Child accepts "So 4" as temporary name. | SQ_Mercy_03. |
| OBJ_SQ017_03_004 | SQ_Mercy_03 | Bring child to Mai's classroom. | Child safe in 3B. | SQ_Mercy_03. |
| OBJ_SQ017_04_001 | SQ_Mercy_04 | Spot cut brake line or moved road sign. | Bandit sabotage confirmed. | SQ_Mercy_04. |
| OBJ_SQ017_04_002 | SQ_Mercy_04 | Track signal mirror or glint from toll station. | Bandit spotter identified. | SQ_Mercy_04. |
| OBJ_SQ017_04_003 | SQ_Mercy_04 | Choose: pursue spotter or continue rescue. | Affects rescue speed and intel. | SQ_Mercy_04. |
| OBJ_SQ017_04B_001 | SQ_Mercy_04B | Inspect green root/fungal growth near bridge. | Edenrot exposure confirmed. | SQ_Mercy_04B. |
| OBJ_SQ017_04B_002 | SQ_Mercy_04B | Mark quarantine group without dehumanizing labels. | Humane quarantine protocol. | SQ_Mercy_04B. |
| OBJ_SQ017_04B_003 | SQ_Mercy_04B | Prevent rumor that Binh can safely lead through Edenrot. | Reduces Binh exposure risk. | SQ_Mercy_04B. |
| OBJ_SQ017_05_001 | SQ_Mercy_05 | Help Ong Tu Nieu calculate rations. | Fair ration policy. | SQ_Mercy_05. |
| OBJ_SQ017_05_002 | SQ_Mercy_05 | Decide child/adult/worker portions. | Morale shift by group. | SQ_Mercy_05. |
| OBJ_SQ017_05_003 | SQ_Mercy_05 | Prevent shame-based sharing by children. | Binh protected from guilt obligation. | SQ_Mercy_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ017_REFUSE_RESCUE | MQ_017 | Refuse rescue entirely. | Convoy mostly dies; Compassion down; Hoang security up; Mai/Binh trust hit. | Fail States. |
| FAIL_MQ017_OVERCOMMIT | MQ_017 | Overcommit rescue to base. | Base perimeter weak; theft/raid risk increases. | Fail States. |
| FAIL_MQ017_IGNORE_BANDITS | MQ_017 | Ignore bandit signs. | Chapter 18 ambush harder. | Fail States. |
| FAIL_MQ017_CARGO_OVER_PEOPLE | MQ_017 | Save cargo over people. | Refugees distrust base; Binh guilt worsens. | Fail States. |
| FAIL_MQ017_PEOPLE_OVER_CARGO | MQ_017 | Save people over all cargo. | Supply shortage severe; worker unrest. | Fail States. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ017_NEW_SURVIVORS | MQ_017 | npc_unlock | Refugee survivors join base | Rewards. |
| REW_MQ017_BA_SAU | MQ_017 | npc_unlock | Ba Sau as potential refugee representative (conditional) | Rewards. |
| REW_MQ017_SO4 | MQ_017 | npc_unlock | So 4 joins Mai's classroom | Rewards. |
| REW_MQ017_BANDIT_INTEL | MQ_017 | intel | Bandit checkpoint route information | Rewards. |
| REW_MQ017_COMPASSION_FLAG | MQ_017 | flag | CompassionUp moral flag | Rewards. |
| REW_MQ017_PRAGMATISM_FLAG | MQ_017 | flag | PragmatismUp moral flag (if different choice) | Rewards. |
| REW_MQ017_RESOURCE_CONSEQUENCE | MQ_017 | resource_penalty | Food/medicine/fuel reduced | Rewards. |
| REW_MQ017_BANDITS_KNOW_PATTERN | MQ_017 | threat_flag | BanditsKnowRescuePattern | Rewards. |
| REW_MQ017_EDENROT_RUMOR | MQ_017 | threat_flag | EdenrotRumorFollowsBase | Rewards. |
| REW_MQ017_HOANG_RESENTMENT | MQ_017 | relationship_flag | HoangSupplyResentment | Rewards. |
| REW_MQ017_REFUGEE_CRISIS | MQ_017 | world_state_flag | RefugeeIntakeCrisis | Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH017_REFUGEE_INTAKE | MQ_017 | Refugee intake system | Refugees brought to base. |
| UNLOCK_CH017_SUPPLY_THEFT_INVESTIGATION | MQ_017 | Supply theft investigation | Theft discovered. |
| UNLOCK_CH017_BANDIT_CHECKPOINT_MAP | MQ_017 | Bandit checkpoint map | Marker found and decoded. |
| UNLOCK_CH017_EDENROT_QUARANTINE | MQ_017 | Edenrot quarantine protocol | Edenrot exposure assessed. |
| UNLOCK_CH017_RATION_POLICY | MQ_017 | Ration policy system | Reduced rations allocated. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH017_CONVOY_DISTRESS_RECEIVED | MQ_017 | Radio signal received. |
| FLAG_CH017_LIMITED_RESCUE_APPROVED | MQ_017 | Council vote passes. |
| FLAG_CH017_HOANG_DISSENT_RESCUE | MQ_017 | Hoang votes against. |
| FLAG_CH017_BANDIT_MARKER_FOUND | MQ_017 | Red cloth marker found at bridge. |
| FLAG_CH017_MEDICINE_OVER_FUEL | MQ_017 | Medicine chosen at depot. |
| FLAG_CH017_REFUGEES_SAVED | MQ_017 | Variable refugee count. |
| FLAG_CH017_BA_SAU_SURVIVED | MQ_017 | Ba Sau pulled from bridge. |
| FLAG_CH017_NAMELESS_CHILD_SAVED | MQ_017 | So 4 rescued. |
| FLAG_CH017_SUPPLY_SHORTAGE_SEVERE | MQ_017 | Rations reduced. |
| FLAG_CH017_LAB_RESEARCH_DELAYED | MQ_017 | Doctor uses lab supplies. |
| FLAG_CH017_WORKER_RESENTMENT_UP | MQ_017 | Worker Lead complains. |
| FLAG_CH017_HOANG_SUPPLY_RESENTMENT | MQ_017 | Hoang records losses. |
| FLAG_CH017_EDENROT_RUMOR_FOLLOWS_BASE | MQ_017 | Refugees bring rumors. |
| FLAG_CH017_EDENROT_EXPOSURE_PROTOCOL | MQ_017 | Quarantine marked. |
| FLAG_CH017_SUPPLY_THEFT_TRIGGERED | MQ_017 | Night theft occurs. |
| FLAG_CH017_BANDIT_CHECKPOINT_LEAD | MQ_017 | Hoang copies checkpoint location. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Mercy_01 | Stuck Convoy | npc_ba_sau | Identify leader, count children/wounded, stabilize bridge route, decide crossing order, prevent panic. | More refugees survive if order maintained. | SQ_Mercy_01. |
| SQ_Mercy_02 | Medicine or Fuel | npc_doctor | Reach vehicle, pick cargo priority, defend loader, escape before horde. | Affects Doctor lab progress or generator/security. | SQ_Mercy_02. |
| SQ_Mercy_03 | Nameless Child | char_mai | Find child under bus, avoid forcing name, offer temporary name/token, bring to classroom, let Binh decide sharing. | Child joins class; Binh healing mirror. | SQ_Mercy_03. |
| SQ_Mercy_04 | Trapped Fuel Depot | comp_hoang | Spot sabotage, track spotter, choose pursue or continue, recover bandit marker. | Bandit intel for Chapter 18. | SQ_Mercy_04. |
| SQ_Mercy_04B | Edenrot Edge by the Bridge | npc_ba_sau | Inspect fungal growth, identify exposed refugees, mark quarantine humanely, decide burn/avoid/document, prevent Binh rumor. | Unlocks EdenrotExposureProtocol. | SQ_Mercy_04B. |
| SQ_Mercy_05 | Sharing the Bowl | npc_ong_tu_nieu | Calculate rations, decide portions, address complaints, prevent shame-sharing, record policy. | Morale shifts by group. | SQ_Mercy_05. |

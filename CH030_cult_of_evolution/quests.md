# Quests - CH030

Metadata:

- chapterID: CH030
- sourceFilename: chapter_030_cult_of_evolution.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_030 | Infiltrate Cult | main | npc_mara | Red Canyon route identified from radar | Children rescued, ritual disrupted, Hoang departed, Heartland route unlocked | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ030_01 | MQ_030 | 1 | Follow Red Canyon radar route. | GoTo | LOC_CH030_RED_CANYON | 1 | Main Quest objective 1. |
| OBJ_MQ030_02 | MQ_030 | 2 | Avoid cult scout kites and canyon watchers. | Stealth | LOC_CH030_DESERT_CONVOY_ROUTE | 1 | Main Quest objective 2. |
| OBJ_MQ030_03 | MQ_030 | 3 | Enter pilgrimage camp. | GoTo | LOC_CH030_PILGRIMAGE_CAMP | 1 | Main Quest objective 3. |
| OBJ_MQ030_04 | MQ_030 | 4 | Classify EDENROT Ascension Doctrine. | Investigation | LOC_CH030_PILGRIMAGE_CAMP | 1 | Main Quest objective 4. |
| OBJ_MQ030_05 | MQ_030 | 5 | Acquire pilgrim cover identities. | Social | LOC_CH030_PILGRIMAGE_CAMP | 1 | Main Quest objective 5. |
| OBJ_MQ030_06 | MQ_030 | 6 | Attend Prophet Dao sermon. | Social | LOC_CH030_CAVE_TEMPLE | 1 | Main Quest objective 6. |
| OBJ_MQ030_07 | MQ_030 | 7 | Prevent Binh isolation by Cult. | Protect | comp_binh | 1 | Main Quest objective 7. |
| OBJ_MQ030_08 | MQ_030 | 8 | Locate canyon nursery. | GoTo | LOC_CH030_NURSERY | 1 | Main Quest objective 8. |
| OBJ_MQ030_09 | MQ_030 | 9 | Build trust with kidnapped children. | Social | npc_noah | 1 | Main Quest objective 9. |
| OBJ_MQ030_10 | MQ_030 | 10 | Inspect ascension masks. | Investigation | LOC_CH030_PREPARATION_CHAMBER | 1 | Main Quest objective 10. |
| OBJ_MQ030_11 | MQ_030 | 11 | Sabotage toxin/transmitter. | Sabotage | LOC_CH030_PREPARATION_CHAMBER | 1 | Main Quest objective 11. |
| OBJ_MQ030_12 | MQ_030 | 12 | Recover cult relay packet log. | Investigation | LOC_CH030_PREPARATION_CHAMBER | 1 | Main Quest objective 12. |
| OBJ_MQ030_13 | MQ_030 | 13 | Force Hoang confession. | Dialogue | comp_hoang | 1 | Main Quest objective 13. |
| OBJ_MQ030_14 | MQ_030 | 14 | Interrupt main ritual. | Combat | LOC_CH030_MAIN_TEMPLE | 1 | Main Quest objective 14. |
| OBJ_MQ030_15 | MQ_030 | 15 | Reject ascension naming. | Dialogue | comp_binh | 1 | Main Quest objective 15. |
| OBJ_MQ030_16 | MQ_030 | 16 | Escort children through lower canyon. | Escort | LOC_CH030_CANYON_ESCAPE_ROUTE | 1 | Main Quest objective 16. |
| OBJ_MQ030_17 | MQ_030 | 17 | Survive Blessed infected release. | Combat | LOC_CH030_CANYON_ESCAPE_ROUTE | 1 | Main Quest objective 17. |
| OBJ_MQ030_18 | MQ_030 | 18 | Return to convoy camp. | GoTo | LOC_CH030_CONVOY_CAMP_NIGHT | 1 | Main Quest objective 18. |
| OBJ_MQ030_19 | MQ_030 | 19 | Discover Hoang departure. | Investigation | LOC_CH030_CONVOY_CAMP_NIGHT | 1 | Main Quest objective 19. |
| OBJ_MQ030_20 | MQ_030 | 20 | Unlock Heartland Convoy route. | Unlock | MQ_031 | 1 | Main Quest objective 20. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ030_01_001 | SQ_030_01 | Help children reclaim real names from Cult labels. | ChildNameTokens improve rescue compliance. | SQ_Cult_01. |
| OBJ_SQ030_02_001 | SQ_030_02 | Collect doctrinal recordings for counter-broadcast. | Counter-broadcast material. | SQ_Cult_02. |
| OBJ_SQ030_03_001 | SQ_030_03 | Steal mask sample and disable toxin reservoir. | CultMaskAntidote. | SQ_Cult_03. |
| OBJ_SQ030_04_001 | SQ_030_04 | Recover relay log and confront Hoang. | HoangPacketLogRecovered. | SQ_Cult_04. |
| OBJ_SQ030_05_001 | SQ_030_05 | Find Elian's child memorial token and convince her to open exits. | MotherElianDefected. | SQ_Cult_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ030_BINH_ISOLATED | MQ_030 | Binh isolated by Cult during ritual. | Binh captured; ritual proceeds. | Metadata. |
| FAIL_MQ030_MASKS_ACTIVATED | MQ_030 | Ascension masks activated on children. | Children harmed. | Metadata. |
| FAIL_MQ030_NURSERY_LOCKED | MQ_030 | Nursery exits locked during Blessed release. | Children trapped. | Metadata. |
| FAIL_MQ030_CROWD_MASSACRE | MQ_030 | Cult crowd turns into massacre. | Civilian casualties. | Metadata. |
| FAIL_MQ030_HOANG_FLEES_EARLY | MQ_030 | Hoang flees before packet evidence recovered. | Evidence lost. | Metadata. |
| FAIL_MQ030_BROADCAST_SUCCESS | MQ_030 | Prophet successfully broadcasts Binh as Cult symbol. | Cult gains legitimacy. | Metadata. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ030_RESCUED_CHILDREN | MQ_030 | companion_group | Rescued children convoy group | Rewards section. |
| REW_MQ030_CULT_HOSTILITY | MQ_030 | faction_flag | CultHostility = true | Rewards section. |
| REW_MQ030_CANYON_TESTIMONIES | MQ_030 | lore_item | Red Canyon survivor testimonies | Rewards section. |
| REW_MQ030_PACKET_LOG | MQ_030 | evidence_item | Hoang packet log obtained | Rewards section. |
| REW_MQ030_HEARTLAND_ROUTE | MQ_030 | route_unlock | Heartland convoy route unlocked | Rewards section. |
| REW_MQ030_ELIAN_DEFECTOR | MQ_030 | npc_reward | Optional Mother Elian defector support | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH030_CULT_HOSTILITY | MQ_030 | Cult hostility | Ritual disrupted. |
| UNLOCK_CH030_RESCUED_CHILDREN | MQ_030 | Rescued children group | Nursery opened. |
| UNLOCK_CH030_HEARTLAND_ROUTE | MQ_030 | Heartland Convoy route | Children rescued and camp secured. |
| UNLOCK_CH030_MQ031 | MQ_030 | MQ_031 Protect Convoy | Heartland route unlocked. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH030_CULT_HOSTILITY | MQ_030 | Ritual disrupted. |
| FLAG_CH030_RESCUED_CHILDREN_CONVOY | MQ_030 | Children rescued from nursery. |
| FLAG_CH030_HEARTLAND_CONVOY_ROUTE_UNLOCKED | MQ_030 | Camp secured and route opened. |
| FLAG_CH030_HOANG_LEAVES_CONVVOY | MQ_030 | Hoang departs with note. |
| FLAG_CH030_HOANG_CONFESSION_PARTIAL | MQ_030 | Hoang confesses in cave. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_030_01 | Children Called Saints | npc_noah | Help nursery children reclaim real names. | Improves rescue compliance. | SQ_Cult_01. |
| SQ_030_02 | Prophet's Sermon | environmental | Listen to sermon, collect doctrinal recordings. | Counter-broadcast material. | SQ_Cult_02. |
| SQ_030_03 | Evolution Masks | npc_doctor | Steal mask sample, analyze, disable toxin. | CultMaskAntidote obtained. | SQ_Cult_03. |
| SQ_030_04 | Fourth Error In The Cave | environmental | Recover relay log, confront Hoang. | Packet evidence for confession arc. | SQ_Cult_04. |
| SQ_030_05 | Mother Believer's Choice | npc_mother_elian | Find Elian's memorial token, convince her to open exits. | Additional children saved. | SQ_Cult_05. |

# Quests - CH035

Metadata:

- chapterID: CH035
- sourceFilename: chapter_035_chau_au_dong_bang.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_035 | Enter Frozen Europe | main | npc_moreno | CH034 Europe route unlocked and Atlantic crossing prepared | Europe entry secured and Paris metro route unlocked | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ035_001 | MQ_035 | 1 | Rendezvous with Atlantic Fleet fragment. | TalkTo | LOC_CH035_ATLANTIC_RENDEZVOUS | 1 | Main Quest objective 1. |
| OBJ_MQ035_002 | MQ_035 | 2 | Trade NORAD star/nav data for Channel route. | Trade | LOC_CH035_ATLANTIC_RENDEZVOUS | 1 | Main Quest objective 2. |
| OBJ_MQ035_003 | MQ_035 | 3 | Prepare cold weather crossing. | Interact | LOC_CH035_ATLANTIC_RENDEZVOUS | 1 | Main Quest objective 3. |
| OBJ_MQ035_004 | MQ_035 | 4 | Keep engines warm through ice field. | Survival | LOC_CH035_CHANNEL_WATERS | 1 | Main Quest objective 4. |
| OBJ_MQ035_005 | MQ_035 | 5 | Land on frozen Europe coast. | GoTo | LOC_CH035_UK_COAST | 1 | Main Quest objective 5. |
| OBJ_MQ035_006 | MQ_035 | 6 | Salvage cold gear from evacuation zone. | Scavenge | LOC_CH035_UK_COAST | 1 | Main Quest objective 6. |
| OBJ_MQ035_007 | MQ_035 | 7 | Survive first Ice horde encounter. | Combat | LOC_CH035_MOTORWAY_PILEUP | 1 | Main Quest objective 7. |
| OBJ_MQ035_008 | MQ_035 | 8 | Learn heat/stem/shatter rules. | Tutorial | LOC_CH035_MOTORWAY_PILEUP | 1 | Main Quest objective 8. |
| OBJ_MQ035_009 | MQ_035 | 9 | Investigate humanitarian waystation. | Interact | LOC_CH035_SERVICE_STATION | 1 | Main Quest objective 9. |
| OBJ_MQ035_010 | MQ_035 | 10 | Expose fake relief operation. | SocialDetection | LOC_CH035_SERVICE_STATION | 1 | Main Quest objective 10. |
| OBJ_MQ035_011 | MQ_035 | 11 | Free Ingrid and secure shelter. | Rescue | LOC_CH035_SERVICE_STATION | 1 | Main Quest objective 11. |
| OBJ_MQ035_012 | MQ_035 | 12 | Build heat kits for team. | Craft | LOC_CH035_SERVICE_TUNNEL | 1 | Main Quest objective 12. |
| OBJ_MQ035_013 | MQ_035 | 13 | Verify Teacher Amelie Paris signal. | TalkTo | LOC_CH035_RADIO_SHELTER | 1 | Main Quest objective 13. |
| OBJ_MQ035_014 | MQ_035 | 14 | Survive major Ice horde assault. | Combat | LOC_CH035_EUROTUNNEL_ACCESS | 1 | Main Quest objective 14. |
| OBJ_MQ035_015 | MQ_035 | 15 | Unlock Paris metro route. | UnlockQuest | MQ_036 | 1 | Main Quest objective 15. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ035_01_001 | SQ_035_01 | Repair navigation array and share star data. | AtlanticFleetAlly. | SQ_EU_01. |
| OBJ_SQ035_02_001 | SQ_035_02 | Recover emergency ledger and mark family names. | EuropeEvacuationLedger. | SQ_EU_02. |
| OBJ_SQ035_03_001 | SQ_035_03 | Build portable heat kits and learn when to mask heat. | HeatKitBlueprint. | SQ_EU_03. |
| OBJ_SQ035_04_001 | SQ_035_04 | Observe delayed twitch and test fire/stem/shatter methods. | IceHordeCounterLearned. | SQ_EU_04. |
| OBJ_SQ035_05_001 | SQ_035_05 | Use child-safety phrase and confirm attendance code. | ParisMetroRouteUnlocked. | SQ_EU_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ035_ENGINES_FREEZE | MQ_035 | Channel crossing engines freeze. | Stranded in ice field. | Failure Conditions. |
| FAIL_MQ035_HYPOTHERMIA | MQ_035 | Landing party loses cold gear. | Hypothermia casualties. | Failure Conditions. |
| FAIL_MQ035_ICE_REANIMATION | MQ_035 | Ice horde reanimates behind child group. | Child casualties. | Failure Conditions. |
| FAIL_MQ035_RAIDER_CAPTURE | MQ_035 | Raiders capture radio/supply cache. | Lost equipment and contacts. | Failure Conditions. |
| FAIL_MQ035_PARIS_SIGNAL_LOST | MQ_035 | Paris signal not verified before relay closes. | Lost Paris contact. | Failure Conditions. |
| FAIL_MQ035_DOCTOR_DELAY | MQ_035 | Doctor delays escape too long for sample. | Survival risk. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ035_EUROPE_UNLOCK | MQ_035 | region_unlock | Europe region unlocked | Completion Rewards. |
| REW_MQ035_ICE_COUNTER | MQ_035 | system_unlock | Ice horde countermeasure | Completion Rewards. |
| REW_MQ035_FLEET_ALLY | MQ_035 | relationship_flag | Atlantic Fleet ally | Completion Rewards. |
| REW_MQ035_INGRID_CONTACT | MQ_035 | relationship_flag | Ingrid/waystation contact | Completion Rewards. |
| REW_MQ035_PARIS_ROUTE | MQ_035 | quest_unlock | Paris metro route | Completion Rewards. |
| REW_MQ035_COLD_GEAR | MQ_035 | item | Cold survival gear | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH035_EUROPE | MQ_035 | Europe region | Landing on frozen coast. |
| UNLOCK_CH035_ICE_HORDE | MQ_035 | Ice horde countermeasure | Heat/stem/shatter rules learned. |
| UNLOCK_CH035_PARIS_ROUTE | MQ_035 | Paris metro route | Amelie signal verified. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH035_EUROPE_REGION_UNLOCKED | MQ_035 | Landing on frozen coast. |
| FLAG_CH035_CRYOSTATIC_ENTRY_SURVIVED | MQ_035 | Entry survived. |
| FLAG_CH035_ICE_HORDE_COUNTER_LEARNED | MQ_035 | Heat/stem/shatter rules known. |
| FLAG_CH035_PARIS_METRO_ROUTE_UNLOCKED | MQ_035 | Amelie signal verified. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_035_01 | Ship Without Port | npc_moreno | Repair navigation array, share star data, decide fuel vs data trade. | AtlanticFleetAlly, future sea route support. | SQ_EU_01. |
| SQ_035_02 | City Frozen Mid-Rescue | environmental | Recover emergency ledger, mark family names, send archive to NORAD. | EuropeEvacuationLedger. | SQ_EU_02. |
| SQ_035_03 | Fire in Snow | npc_thu | Build portable heat kits, learn when to mask heat, create flare traps. | HeatKitBlueprint. | SQ_EU_03. |
| SQ_035_04 | Bodies That Won't Lie Down | npc_doctor | Observe delayed twitch, test fire/stem/shatter, codify team rules. | IceHordeCounterLearned. | SQ_EU_04. |
| SQ_035_05 | Promise to Paris | npc_amelie | Use child-safety phrase, confirm attendance code, decode metro route. | ParisMetroRouteUnlocked. | SQ_EU_05. |

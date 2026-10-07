# Quests - CH027

Metadata:

- chapterID: CH027
- sourceFilename: chapter_027_silicon_graveyard.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_027 | Recover AI Core | main | npc_mara | Group reaches Silicon Valley entrance following drone signal | Partial AI core extracted; Binh says no to VALE; walled enclave route unlocked | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ027_001 | MQ_027 | 1 | Follow Mara's rescue route into Silicon Valley | GoTo | LOC_CH027_FREEWAY | 1 | Main Quest objective 1. |
| OBJ_MQ027_002 | MQ_027 | 2 | Cross autonomous freeway without triggering road sensors | Stealth | LOC_CH027_FREEWAY | 1 | Main Quest objective 2. |
| OBJ_MQ027_003 | MQ_027 | 3 | Disable immune billboard tracking node | Interact | LOC_CH027_CAMPUS_ENTRANCE | 1 | Main Quest objective 3. |
| OBJ_MQ027_004 | MQ_027 | 4 | Enter abandoned tech campus | GoTo | LOC_CH027_CAMPUS_LOBBY | 1 | Main Quest objective 4. |
| OBJ_MQ027_005 | MQ_027 | 5 | Rescue scavenger children from locked lobby | Rescue | LOC_CH027_CAMPUS_LOBBY | 4 | Main Quest objective 5. |
| OBJ_MQ027_006 | MQ_027 | 6 | Survive first Phantom encounter | Combat | LOC_CH027_OFFICE_HALLS | 1 | Main Quest objective 6. |
| OBJ_MQ027_007 | MQ_027 | 7 | Reach data center basement | GoTo | LOC_CH027_DATA_CENTER | 1 | Main Quest objective 7. |
| OBJ_MQ027_008 | MQ_027 | 8 | Stabilize cooling system | Puzzle | LOC_CH027_DATA_CENTER | 1 | Main Quest objective 8. |
| OBJ_MQ027_009 | MQ_027 | 9 | Confront VALE-7's sampling demand | Dialogue | npc_vale7 | 1 | Main Quest objective 9. |
| OBJ_MQ027_010 | MQ_027 | 10 | Establish Binh consent protocol | Dialogue | LOC_CH027_MEDICAL_ROOM | 1 | Main Quest objective 10. |
| OBJ_MQ027_011 | MQ_027 | 11 | Locate AI core chamber | GoTo | LOC_CH027_CORE_CHAMBER | 1 | Main Quest objective 11. |
| OBJ_MQ027_012 | MQ_027 | 12 | Extract core while Hoang cuts active tracker | Extraction | LOC_CH027_CORE_CHAMBER | 1 | Main Quest objective 12. |
| OBJ_MQ027_013 | MQ_027 | 13 | Escape campus before satellite ping completes | Escape | LOC_CH027_PARKING_LOT | 1 | Main Quest objective 13. |
| OBJ_MQ027_014 | MQ_027 | 14 | Unlock route to walled enclave | UnlockRoute | LOC_CH027_PARKING_LOT | 1 | Main Quest objective 14. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ027_01_001 | SQ_Silicon_01 | Find manual override in self-driving car, retrieve family mementos | Car logs preserved | SQ_Silicon_01. |
| OBJ_SQ027_02_001 | SQ_Silicon_02 | Follow recruitment ads, rescue trapped scavengers from HR terminal | HR terminal contract broken | SQ_Silicon_02. |
| OBJ_SQ027_03_001 | SQ_Silicon_03 | Identify real vs generated children on billboard, save voice source child | VoiceSpoofDetector reward | SQ_Silicon_03. |
| OBJ_SQ027_04_001 | SQ_Silicon_04 | Compare VALE data models, consult Doctor/Mai, choose consent rule | EthicsProtocolCodex reward | SQ_Silicon_04. |
| OBJ_SQ027_05_001 | SQ_Silicon_05 | Salvage old medical scanner, retrieve optical sensor array | SafeScanResearch unlocked | SQ_Silicon_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ027_BINH_SCANNED | MQ_027 | Binh separated and scanned by VALE | Consent broken; trust loss | Failure Conditions. |
| FAIL_MQ027_KIDS_LOST | MQ_027 | Too many scavenger children lost before lobby extraction | Mara trust loss | Failure Conditions. |
| FAIL_MQ027_CORE_DESTROYED | MQ_027 | Cooling system overload destroys core | Mission failure | Failure Conditions. |
| FAIL_MQ027_SATELLITE_LOCK | MQ_027 | Drone uplink completes full satellite lock | Binh location compromised | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ027_AI_CORE | MQ_027 | item | Partial AI Core | Completion Rewards. |
| REW_MQ027_TECH_TREE | MQ_027 | system_unlock | TechUpgradeTree_ValePartial | Completion Rewards. |
| REW_MQ027_COUNTERMEASURE | MQ_027 | blueprint | Drone/satellite countermeasure blueprint | Completion Rewards. |
| REW_MQ027_PHANTOM_DETECT | MQ_027 | system_unlock | Phantom detection method | Completion Rewards. |
| REW_MQ027_MARA_TRUST | MQ_027 | relationship_flag | Mara trust increase | Completion Rewards. |
| REW_MQ027_ENCLAVE_COORDS | MQ_027 | unlock | Walled enclave coordinates | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH027_TECH_TREE | MQ_027 | Tech upgrade tree with ethical conditions | AI core extracted. |
| UNLOCK_CH027_PHANTOM_DETECTION | MQ_027 | Phantom detection via dust/water/reflection | Survived Phantom encounter. |
| UNLOCK_CH027_SAFE_SCAN | MQ_027 | Safe scan route for non-invasive study | SQ_Silicon_05 complete. |
| UNLOCK_CH027_WALLED_CITY | MQ_027 | Route to walled enclave | VALE ping accepted. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH027_AI_CORE_RECOVERED | MQ_027 | Core extracted from data center. |
| FLAG_CH027_BINH_CONSENT_PROTOCOL | MQ_027 | Consent protocol written by hand. |
| FLAG_CH027_BINH_REFUSED_BLOOD | MQ_027 | Binh says "No" to VALE. |
| FLAG_CH027_HOANG_PACKET_PRESERVED | MQ_027 | Hoang preserves packet log evidence. |
| FLAG_CH027_HOANG_MARKED_BY_VALE | MQ_027 | VALE marks Hoang as obstruction. |
| FLAG_CH027_WALLED_CITY_ROUTE | MQ_027 | VALE pings walled enclave. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Silicon_01 | Self-Driving Car Graveyard | environmental | Find manual override, retrieve family mementos, decide car AI fate | Car logs may contain pre-outbreak data | SQ_Silicon_01. |
| SQ_Silicon_02 | Dead Company Still Hiring | environmental | Follow recruitment ads, rescue trapped scavengers, break HR lock | Campus systems deactivated | SQ_Silicon_02. |
| SQ_Silicon_03 | Children on Billboard | environmental | Identify real vs generated children, locate projector node | VoiceSpoofDetector reward | SQ_Silicon_03. |
| SQ_Silicon_04 | Lies of Data | npc_vale7 | Compare data models, consult Doctor/Mai, choose consent rule | EthicsProtocolCodex reward | SQ_Silicon_04. |
| SQ_Silicon_05 | Blood Is Not A Password | npc_doctor | Salvage medical scanner, retrieve optical sensors, build safer rig | SafeScanResearch unlocked | SQ_Silicon_05. |

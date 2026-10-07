# Quests - CH029

Metadata:

- chapterID: CH029
- sourceFilename: chapter_029_neo_military.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_029 | Earn Military Trust | main | npc_graves | Neo-Military convoy detected at enclave | Conditional Army support earned; execution order refused; Red Canyon route unlocked | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ029_001 | MQ_029 | 1 | Detect Neo-Military convoy | Detection | LOC_CH029_OUTSIDE_WALL | 1 | Main Quest objective 1. |
| OBJ_MQ029_002 | MQ_029 | 2 | Prevent enclave/Army standoff | Dialogue | LOC_CH029_OUTSIDE_WALL | 1 | Main Quest objective 2. |
| OBJ_MQ029_003 | MQ_029 | 3 | Meet Colonel Graves with Mai present | Dialogue | npc_graves | 1 | Main Quest objective 3. |
| OBJ_MQ029_004 | MQ_029 | 4 | Refuse full command submission | Dialogue | npc_graves | 1 | Main Quest objective 4. |
| OBJ_MQ029_005 | MQ_029 | 5 | Inspect marked prisoner quarantine | Investigation | LOC_CH029_HOLDING_PEN | 1 | Main Quest objective 5. |
| OBJ_MQ029_006 | MQ_029 | 6 | Gather mark status evidence | Collect | LOC_CH029_HOLDING_PEN | 3 | Main Quest objective 6. |
| OBJ_MQ029_007 | MQ_029 | 7 | Travel to Fort Resolve | GoTo | LOC_CH029_FORT_RESOLVE | 1 | Main Quest objective 7. |
| OBJ_MQ029_008 | MQ_029 | 8 | Review Cult radar data | Investigation | LOC_CH029_FORT_RESOLVE | 1 | Main Quest objective 8. |
| OBJ_MQ029_009 | MQ_029 | 9 | Deploy to desert fuel depot | GoTo | LOC_CH029_FUEL_DEPOT | 1 | Main Quest objective 9. |
| OBJ_MQ029_010 | MQ_029 | 10 | Disable drone turrets | Combat | LOC_CH029_FUEL_DEPOT | 2 | Main Quest objective 10. |
| OBJ_MQ029_011 | MQ_029 | 11 | Rescue trapped engineer | Rescue | LOC_CH029_FUEL_DEPOT | 1 | Main Quest objective 11. |
| OBJ_MQ029_012 | MQ_029 | 12 | Preserve fuel tanks | Objective | LOC_CH029_FUEL_DEPOT | 3 | Main Quest objective 12. |
| OBJ_MQ029_013 | MQ_029 | 13 | Reject execution order | Dialogue | npc_sloane | 1 | Main Quest objective 13. |
| OBJ_MQ029_014 | MQ_029 | 14 | Protect marked prisoners | Combat | LOC_CH029_EXTRACTION_ZONE | 7 | Main Quest objective 14. |
| OBJ_MQ029_015 | MQ_029 | 15 | Restore Radar Dune relay | Repair | LOC_CH029_RADAR_DUNE | 1 | Main Quest objective 15. |
| OBJ_MQ029_016 | MQ_029 | 16 | Earn conditional Army support | Unlock | LOC_CH029_AFTER_ACTION | 1 | Main Quest objective 16. |
| OBJ_MQ029_017 | MQ_029 | 17 | Unlock Red Canyon route | UnlockRoute | LOC_CH029_AFTER_ACTION | 1 | Main Quest objective 17. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ029_01_001 | SQ_Mil_01 | Find original evacuation order, interview soldiers/refugees | Order amended or exposed | SQ_Mil_01. |
| OBJ_SQ029_02_001 | SQ_Mil_02 | Scan marks safely, identify active vs passive, protect marked teenager | VALEMarkClassifier reward | SQ_Mil_02. |
| OBJ_SQ029_03_001 | SQ_Mil_03 | Disable drone turret, seal leaking tank, rescue engineer, extract fuel trucks | Fuel depot secured | SQ_Mil_03. |
| OBJ_SQ029_04_001 | SQ_Mil_04 | Obtain written order, present medical counterproof, force Graves to suspend policy | ExecutionPolicySuspended reward | SQ_Mil_04. |
| OBJ_SQ029_05_001 | SQ_Mil_05 | Bring books/toys from enclave, let Binh speak with soldier children | Binh emotional payoff | SQ_Mil_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ029_STANDOFF | MQ_029 | Enclave/Army standoff turns into firefight | Military relationship destroyed | Failure Conditions. |
| FAIL_MQ029_FUEL_EXPLODES | MQ_029 | Fuel depot explodes | Fuel and convoy lost | Failure Conditions. |
| FAIL_MQ029_PRISONERS_EXECUTED | MQ_029 | Marked prisoners executed before player intervention | Moral failure; Hoang risk | Failure Conditions. |
| FAIL_MQ029_RADAR_LOST | MQ_029 | Radar relay lost to VALE drone swarm | Route intelligence lost | Failure Conditions. |
| FAIL_MQ029_BINH_SCANNED | MQ_029 | Binh caught in Army custody scan | Consent broken | Failure Conditions. |
| FAIL_MQ029_FULL_SUBMISSION | MQ_029 | Trung submits fully to command chain | Rebirth independence lost | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ029_ARMY_SUPPORT | MQ_029 | faction_support | ArmySupportPartial | Completion Rewards. |
| REW_MQ029_FUEL | MQ_029 | resource | Fuel allocation | Completion Rewards. |
| REW_MQ029_AMMO | MQ_029 | resource | Ammunition allocation | Completion Rewards. |
| REW_MQ029_RADAR_WINDOW | MQ_029 | intel | 48hr radar window toward Red Canyon | Completion Rewards. |
| REW_MQ029_ESCORT | MQ_029 | escort | Military escort token | Completion Rewards. |
| REW_MQ029_TESTIMONY | MQ_029 | clue | Marked prisoner testimony for Hoang hearing | Completion Rewards. |
| REW_MQ029_CULT_ROUTE | MQ_029 | unlock | CH030 route | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH029_ARMY_PARTIAL | MQ_029 | Partial Army support | Fuel depot mission complete; prisoners saved. |
| UNLOCK_CH029_RADAR_WINDOW | MQ_029 | 48hr radar window | Radar Dune relay restored. |
| UNLOCK_CH029_ESCORT_TEAM | MQ_029 | Military escort team | Conditional support earned. |
| UNLOCK_CH029_RED_CANYON | MQ_029 | Red Canyon route | Cult activity detected. |
| UNLOCK_CH029_EXECUTION_SUSPENDED | MQ_029 | Execution policy suspended | SQ_Mil_04 complete. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH029_REBIRTH_COMMAND_INDEPENDENT | MQ_029 | Trung rejects full submission. |
| FLAG_CH029_MARKED_STATUS_EVIDENCE | MQ_029 | Doctor scans prove marks differ. |
| FLAG_CH029_EXECUTION_ORDER_REFUSED | MQ_029 | Trung refuses execution order. |
| FLAG_CH029_MARKED_PRISONERS_SAVED | MQ_029 | All marked prisoners alive after mission. |
| FLAG_CH029_HOANG_MARK_EXPOSED | MQ_029 | Hoang's mark visible during radar hack. |
| FLAG_CH029_HOANG_TRUTH_CRITICAL | MQ_029 | Truth pressure at maximum. |
| FLAG_CH029_RADAR_RELAY_RESTORED | MQ_029 | Radar Dune relay restarted by marked engineer. |
| FLAG_CH029_LEGACY_COMMAND_FAILED | MQ_029 | Marked engineer saves entire unit. |
| FLAG_CH029_EXECUTION_POLICY_SUSPENDED | MQ_029 | Graves suspends policy. |
| FLAG_CH029_ARMY_SUPPORT_PARTIAL | MQ_029 | Conditional support earned. |
| FLAG_CH029_CULT_DETECTED | MQ_029 | Cult child cluster detected in Red Canyon. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Mil_01 | Old Orders | environmental | Find original evacuation order, interview soldiers/refugees | Order amended or exposed | SQ_Mil_01. |
| SQ_Mil_02 | The Marked | npc_doctor | Scan marks safely, identify active vs passive, protect marked teenager | VALEMarkClassifier reward | SQ_Mil_02. |
| SQ_Mil_03 | Desert Fuel Depot | npc_graves | Disable drone turret, seal leaking tank, rescue engineer, extract fuel trucks | Fuel depot secured for convoy | SQ_Mil_03. |
| SQ_Mil_04 | Execution Order | npc_sloane | Obtain written order, present medical counterproof, force Graves to suspend policy | ExecutionPolicySuspended | SQ_Mil_04. |
| SQ_Mil_05 | Flag Is Not Home | npc_graves | Bring books/toys from enclave, let Binh speak with soldier children | Binh learns other children also live under adult symbols they didn't choose | SQ_Mil_05. |

# Quests - CH028

Metadata:

- chapterID: CH028
- sourceFilename: chapter_028_thanh_pho_cua_nhung_buc_tuong.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_028 | Negotiate Entry | main | npc_mara | Group reaches Walled Civic Zone after VALE ping | Allied delegation status secured; Hoang public hearing agreed; Neo-Military detected | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ028_001 | MQ_028 | 1 | Scout Walled Civic Zone from ridge | GoTo | LOC_CH028_HILL | 1 | Main Quest objective 1. |
| OBJ_MQ028_002 | MQ_028 | 2 | Approach main gate with Mara as local witness | GoTo | LOC_CH028_GATE | 1 | Main Quest objective 2. |
| OBJ_MQ028_003 | MQ_028 | 3 | Refuse unsafe biometric scan for Binh | Dialogue | LOC_CH028_GATE | 1 | Main Quest objective 3. |
| OBJ_MQ028_004 | MQ_028 | 4 | Classify Edenrot Civic Filter | Lore | LOC_CH028_GATE | 1 | Main Quest objective 4. |
| OBJ_MQ028_005 | MQ_028 | 5 | Identify Hoang VALE mark | Investigation | comp_hoang | 1 | Main Quest objective 5. |
| OBJ_MQ028_006 | MQ_028 | 6 | Investigate refugee camp conditions | Investigation | LOC_CH028_REFUGEE_CAMP | 1 | Main Quest objective 6. |
| OBJ_MQ028_007 | MQ_028 | 7 | Collect testimonies about entry trade | Collect | LOC_CH028_REFUGEE_CAMP | 3 | Main Quest objective 7. |
| OBJ_MQ028_008 | MQ_028 | 8 | Meet Councilor Ada Price | Dialogue | npc_ada | 1 | Main Quest objective 8. |
| OBJ_MQ028_009 | MQ_028 | 9 | Enter outer district under temporary permit | GoTo | LOC_CH028_OUTER_DISTRICT | 1 | Main Quest objective 9. |
| OBJ_MQ028_010 | MQ_028 | 10 | Explore market/school/clinic | Explore | LOC_CH028_OUTER_DISTRICT | 3 | Main Quest objective 10. |
| OBJ_MQ028_011 | MQ_028 | 11 | Negotiate three entry conditions | Dialogue | npc_ada | 1 | Main Quest objective 11. |
| OBJ_MQ028_012 | MQ_028 | 12 | Prevent private detention of Hoang | Dialogue | LOC_CH028_COUNCIL_HALL | 1 | Main Quest objective 12. |
| OBJ_MQ028_013 | MQ_028 | 13 | Stop trader militia riot without mass casualties | Combat | LOC_CH028_GATE_MARKET | 1 | Main Quest objective 13. |
| OBJ_MQ028_014 | MQ_028 | 14 | Present evidence at Council platform | Dialogue | LOC_CH028_COUNCIL_PLATFORM | 1 | Main Quest objective 14. |
| OBJ_MQ028_015 | MQ_028 | 15 | Secure allied delegation status | Unlock | LOC_CH028_COUNCIL_PLATFORM | 1 | Main Quest objective 15. |
| OBJ_MQ028_016 | MQ_028 | 16 | Unlock Hoang public hearing | Unlock | LOC_CH028_COUNCIL_PLATFORM | 1 | Main Quest objective 16. |
| OBJ_MQ028_017 | MQ_028 | 17 | Detect Neo-Military convoy approach | Detection | LOC_CH028_COUNCIL_PLATFORM | 1 | Main Quest objective 17. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ028_01_001 | SQ_Wall_01 | Interview families, identify forged entry bands, protect sick child | Refugee trust | SQ_Wall_01. |
| OBJ_SQ028_02_001 | SQ_Wall_02 | Follow broker, record transaction, expose trader publicly | Entry band evidence | SQ_Wall_02. |
| OBJ_SQ028_03_001 | SQ_Wall_03 | Restore deleted names, return tokens to families | Registry audit data | SQ_Wall_03. |
| OBJ_SQ028_04_001 | SQ_Wall_04 | Maintain witness access, stop VALE terminal interrogation | Hoang hearing evidence | SQ_Wall_04. |
| OBJ_SQ028_05_001 | SQ_Wall_05 | Track money/medicine flow, protect families | Preacher exposed | SQ_Wall_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ028_BINH_SCANNED | MQ_028 | Binh forcibly scanned by gate system | Consent broken; trust loss | Failure Conditions. |
| FAIL_MQ028_HOANG_PRIVATE | MQ_028 | Hoang handed over privately without Rebirth witness | Hoang confession arc broken | Failure Conditions. |
| FAIL_MQ028_RIOT_MASSACRE | MQ_028 | Riot escalates into guard massacre | Enclave relationship destroyed | Failure Conditions. |
| FAIL_MQ028_CORE_CONNECTED | MQ_028 | AI core connected directly to enclave network | VALE access to enclave systems | Failure Conditions. |
| FAIL_MQ028_REFUGEES_HOSTILE | MQ_028 | Refugee camp turns hostile due to perceived abandonment | Refugee trust lost | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ028_ENCLAVE_ACCESS | MQ_028 | access | Limited enclave access | Completion Rewards. |
| REW_MQ028_DIPLOMACY_REP | MQ_028 | reputation | Diplomacy reputation | Completion Rewards. |
| REW_MQ028_PUBLIC_HEARING | MQ_028 | system_unlock | Public hearing system | Completion Rewards. |
| REW_MQ028_CLINIC_MARKET | MQ_028 | access | Clinic and market access | Completion Rewards. |
| REW_MQ028_REFUGEE_LIST | MQ_028 | item | Refugee medical priority list | Completion Rewards. |
| REW_MQ028_NEO_MILITARY_WARNING | MQ_028 | intel | Neo-Military contact warning | Completion Rewards. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH028_DIPLOMACY_REP | MQ_028 | Enclave diplomacy reputation | Mai leads gate negotiation. |
| UNLOCK_CH028_PUBLIC_HEARING | MQ_028 | Public tribunal mechanics | Hoang hearing agreed. |
| UNLOCK_CH028_ENCLAVE_HUB | MQ_028 | Enclave market and civic hub | Temporary permit granted. |
| UNLOCK_CH028_REFUGEE_CHAIN | MQ_028 | Refugee advocacy side chain | Refugee conditions witnessed. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH028_ALLIED_DELEGATION | MQ_028 | Council agrees to allied delegation status. |
| FLAG_CH028_MAI_DIPLOMACY | MQ_028 | Mai recognized as diplomatic lead at gate. |
| FLAG_CH028_PUBLIC_JUSTICE | MQ_028 | Public hearing system established. |
| FLAG_CH028_NO_GATE_MASSACRE | MQ_028 | Riot resolved without mass casualties. |
| FLAG_CH028_REFUGEE_MEDICAL_LIST | MQ_028 | Medical priority list created at negotiation. |
| FLAG_CH028_NEO_MILITARY_DETECTED | MQ_028 | VALE shows Neo-Military convoy approaching. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_Wall_01 | People Outside the Gate | npc_mara | Interview families, identify forged entry bands, protect sick child | Refugee trust earned | SQ_Wall_01. |
| SQ_Wall_02 | Price of an Open Door | environmental | Follow broker, record transaction, expose publicly or trade evidence | Entry band evidence preserved | SQ_Wall_02. |
| SQ_Wall_03 | Erased Names | environmental | Restore deleted names, return tokens, challenge Ada with evidence | Registry audit data for Council | SQ_Wall_03. |
| SQ_Wall_04 | Hoang's Cell | npc_rowan | Maintain witness access, stop VALE terminal interrogation | Hoang hearing evidence | SQ_Wall_04. |
| SQ_Wall_05 | Selling Faith | environmental | Track money/medicine flow, protect families, choose punishment or restorative deal | Preacher exposed | SQ_Wall_05. |

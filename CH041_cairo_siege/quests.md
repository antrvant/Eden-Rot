# Quests - CH041

Metadata:

- chapterID: CH041
- sourceFilename: chapter_041_cairo_siege.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_041 | Synthesize First Cure | main | narrative | Chapter 40 completed; ProperBioEnzymeSample in inventory; SeedCovenantRatified true; TribalAllianceActive true | First cure succeeds on Yusuf; batch failure documented; Juggernaut defeated or trapped; Architect beacon recovered; Ch42 hook active | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ041_001 | MQ_041 | 1 | Escort convoy into Cairo through market or canal route. | GoTo | LOC_CAIRO_QUARANTINE | 1 | Scene 01. |
| OBJ_MQ041_002 | MQ_041 | 2 | Locate and secure underground lab beneath bombed museum. | GoTo | LOC_MUSEUM_LAB | 1 | Scene 02. |
| OBJ_MQ041_003 | MQ_041 | 3 | Read checkpoint overlay labeling district as EDENROT CLASS: MIRACLE CLAIM SIEGE. | Interact | LOC_CAIRO_QUARANTINE | 1 | Scene 01. |
| OBJ_MQ041_004 | MQ_041 | 4 | Hand off enzyme to Doctor Samir in sterile tray. | Deliver | ITEM_PROPER_BIO_ENZYME | 1 | Scene 02. |
| OBJ_MQ041_005 | MQ_041 | 5 | Require Samir to attach covenant witness context to synthesis record. | Interact | ITEM_SEED_COVENANT_LEDGER | 1 | Scene 02. |
| OBJ_MQ041_006 | MQ_041 | 6 | Solve power reroute puzzle to restore lab electricity. | Puzzle | LOC_MUSEUM_LAB | 1 | Scene 02. |
| OBJ_MQ041_007 | MQ_041 | 7 | Help Mai organize fair triage queue outside museum. | TalkTo | LOC_REFUGEE_LINE | 1 | Scene 03. |
| OBJ_MQ041_008 | MQ_041 | 8 | Combine immune map, enzyme, stabilizer, and plasma base. | Craft | LOC_STERILE_FIELD | 1 | Scene 04. |
| OBJ_MQ041_009 | MQ_041 | 9 | Choose Yusuf, obtain informed consent. | TalkTo | npc_yusuf | 1 | Scene 05. |
| OBJ_MQ041_010 | MQ_041 | 10 | Hold lab during raider/infected breach. | Defend | LOC_MUSEUM_LAB | 1 | Scene 06. |
| OBJ_MQ041_011 | MQ_041 | 11 | Refuse Masud deal; do not reveal Binh data. | TalkTo | npc_masud | 1 | Scene 07. |
| OBJ_MQ041_012 | MQ_041 | 12 | Hold vitals for 90 seconds during cure injection. | Protect | npc_yusuf | 1 | Scene 08. |
| OBJ_MQ041_013 | MQ_041 | 13 | Log Yusuf as person, not product; encrypted ledger. | Interact | ITEM_FIRST_CURE_DOSE | 1 | Scene 08. |
| OBJ_MQ041_014 | MQ_041 | 14 | Analyze failed samples; discover resonance factor gap. | Investigate | LOC_STERILE_FIELD | 1 | Scene 09. |
| OBJ_MQ041_015 | MQ_041 | 15 | Explicitly protect Binh from being labeled material. | TalkTo | comp_binh | 1 | Scene 09. |
| OBJ_MQ041_016 | MQ_041 | 16 | Boss encounter; use resin, cooling vent, crane pin. | Combat | npc_juggernaut | 1 | Scene 10. |
| OBJ_MQ041_017 | MQ_041 | 17 | Retrieve Architect module from Juggernaut. | Loot | ITEM_ARCHITECT_BEACON_MODULE | 1 | Scene 10. |
| OBJ_MQ041_018 | MQ_041 | 18 | Pack lab under timer; escort Yusuf, enzyme, data, samples. | Evacuate | LOC_MOBILE_LAB | 1 | Scene 11. |
| OBJ_MQ041_019 | MQ_041 | 19 | Binh overhears Samir; Ch42 hook activates. | Trigger | comp_binh | 1 | Scene 12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ041_A_001 | SQ_041_A | Identify urgent cases in refugee line. | RefugeeTrust_Cairo medium or high. | SQ_041_A. |
| OBJ_SQ041_A_002 | SQ_041_A | Calm three panic clusters using dialogue. | RefugeeTrust_Cairo medium or high. | SQ_041_A. |
| OBJ_SQ041_A_003 | SQ_041_A | Stop militia guard from taking bribes. | RefugeeTrust_Cairo medium or high. | SQ_041_A. |
| OBJ_SQ041_A_004 | SQ_041_A | Record names, not numbers, on triage board. | Extra volunteers defend evacuation route in Scene 11. | SQ_041_A. |
| OBJ_SQ041_B_001 | SQ_041_B | Secure nephew legally in triage (Salma redeem branch). | MasudBeaconLocated true; SalmaRedeemed true; Salma creates false trail. | SQ_041_B. |
| OBJ_SQ041_C_001 | SQ_041_C | Recover Yusuf tool roll from ward C. | Stronger emotional weight for cure success scene. | SQ_041_C. |
| OBJ_SQ041_C_002 | SQ_041_C | Restart the pump so refugee ward has clean water. | YusufFamilyWitness true. | SQ_041_C. |
| OBJ_SQ041_C_003 | SQ_041_C | Let Yusuf speak to his sister Lina before injection. | YusufFamilyWitness true. | SQ_041_C. |
| OBJ_SQ041_D_001 | SQ_041_D | Choose sedation threshold with Samir. | HoangTrustRestraint true. | SQ_041_D. |
| OBJ_SQ041_D_002 | SQ_041_D | Assign release authority (Mai + Trung dual key). | HoangTrustRestraint true. | SQ_041_D. |
| OBJ_SQ041_D_003 | SQ_041_D | Let Hoang sign his own restraint order. | Hoang can assist in Juggernaut phase 3 without corruption spike. | SQ_041_D. |
| OBJ_SQ041_E_001 | SQ_041_E | Collect exhibit name tags from display cases. | ChildrenShelterMorale high. | SQ_041_E. |
| OBJ_SQ041_E_002 | SQ_041_E | Attach tags to refugee cots in shelter area. | Binh later remembers Yusuf as Yusuf, not first cure. | SQ_041_E. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ041_ENZYME_LOST | MQ_041 | Enzyme overheats or is stolen. | Quest fail; no cure possible. | Success Conditions. |
| FAIL_MQ041_POWER_COLLAPSE | MQ_041 | Lab power collapses before injection. | Quest fail; synthesis aborted. | Success Conditions. |
| FAIL_MQ041_YUSUF_DIES | MQ_041 | Yusuf dies before stabilizing. | Quest fail; first cure lost. | Success Conditions. |
| FAIL_MQ041_CROWD_MASSACRE | MQ_041 | Crowd panic reaches massacre threshold. | Civilian casualties; RefugeeTrust_Cairo broken. | Failure Conditions. |
| FAIL_MQ041_CORE_DESTROYED | MQ_041 | Juggernaut breaches sterile core. | Lab destroyed; data lost. | Failure Conditions. |
| FAIL_MQ041_MASUD_DATA | MQ_041 | Masud obtains viable cure profile. | Black market cure threat escalates. | Failure Conditions. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ041_FIRST_CURE | MQ_041 | narrative | Yusuf cured; first cure success logged as person not product | Scene 08. |
| REW_MQ041_BEACON | MQ_041 | item | Architect beacon fragment with partial Amazon coordinates | Scene 10. |
| REW_MQ041_MOBILE_LAB | MQ_041 | world_state | Mobile lab activated as primary cure space | Scene 11. |
| REW_MQ041_SAMIR_JOIN | MQ_041 | relationship | Doctor Samir joins Rebirth as mobile lab scientist | Scene 11. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH041_MOBILE_LAB | MQ_041 | Mobile Lab Access | Evacuation to mobile lab complete. |
| UNLOCK_CH041_BLOOD_PROTOCOL | MQ_041 | Chapter 42 Blood Protocol | Binh overhears Samir resonance bridge discussion. |
| UNLOCK_CH041_AMAZON_COORDS | MQ_041 | Partial Amazon Citadel Coordinates | Architect beacon recovered. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH041_FIRST_CURE_SUCCESS | MQ_041 | Yusuf cured successfully. |
| FLAG_CH041_BATCH_FAILED | MQ_041 | Micro-dose fails on other samples. |
| FLAG_CH041_JUGGERNAUT_DEFEATED | MQ_041 | Juggernaut defeated or trapped. |
| FLAG_CH041_ARCHITECT_BEACON_RECOVERED | MQ_041 | Architect beacon recovered from Juggernaut. |
| FLAG_CH041_LAB_COMPROMISED | MQ_041 | Cairo lab no longer secure. |
| FLAG_CH041_MOBILE_LAB_ACTIVATED | MQ_041 | Evacuation to mobile lab complete. |
| FLAG_CH041_BINH_UNDERSTANDS | MQ_041 | Binh realizes his blood may be key. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_041_A | No Miracle Without Queue | Mai | Establish fair triage queue; calm panic clusters; stop bribes; record names not numbers. | RefugeeTrust_Cairo medium or high; extra volunteers defend evacuation route. | SQ_041_A. |
| SQ_041_B | Salma Second Ledger | Salma | Expose Masud signals or sell information; redeem, threaten, or ignore branch. | MasudBeaconLocated if redeemed; Salma creates false trail during evacuation. | SQ_041_B. |
| SQ_041_C | The Water Mechanic | Yusuf | Recover tool roll from ward C; restart pump; let Yusuf speak to sister Lina. | YusufFamilyWitness true; stronger emotional weight for cure success. | SQ_041_C. |
| SQ_041_D | Hoang Lock | Hoang | Choose sedation threshold; assign release authority; let Hoang sign restraint order. | HoangTrustRestraint true; Hoang can assist in Juggernaut phase 3. | SQ_041_D. |
| SQ_041_E | Museum Of Names | Amelie | Collect exhibit name tags; attach to refugee cots. | ChildrenShelterMorale high; Binh remembers Yusuf as person. | SQ_041_E. |

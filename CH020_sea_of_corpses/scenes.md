# Scenes - CH020

Metadata:

- chapterID: CH020
- sourceFilename: chapter_020_bien_dong_day_xac.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH020_HOANG_JUDGMENT | Hoang's Trial | LOC_CH020_TEACHER_ROOM | Decide Hoang's temporary fate without forgiveness or execution. | After CH019; Hoang in custody, Architect drive obtained. | Hoang assigned as monitored companion; no authority, no weapons without order. | char_trung;char_mai;char_binh;comp_hoang;npc_worker_lead;npc_doctor | none | ITM_CH020_ARCHITECT_DRIVE | Scene 1 - Hoang's Trial. |
| SCN_CH020_LEAVING_HOME | Leaving Home | LOC_CH020_CLASSROOM_3B | Emotional farewell to first base; split travel team and caretakers. | Hoang judgment complete. | Base caretakers assigned; chalk fragment taken; name left on board. | char_trung;char_mai;char_binh;npc_worker_lead;npc_ba_sau;npc_so_4 | none | ITM_CH020_BLACKBOARD_RULES;ITM_CH020_CHALK_FRAGMENT_CLASSROOM_3B;ITM_CH020_HALF_CHALK_SO4;ITM_CH020_CONVOY_CLOTH | Scene 2 - Leaving Home. |
| SCN_CH020_CORPSE_RIVER | Corpse-Laden River | LOC_CH020_CANAL_SYSTEM | Travel through Edenrot-contaminated waterways; introduce drowned infected ecology. | Group departs base toward Mekong. | River crossing complete; Edenrot edge encountered. | char_trung;char_mai;char_binh;comp_hoang;npc_doctor | ENM_CH020_DROWNED_INFECTED_SWIMMER;ENM_CH020_BANDIT_PURSUERS | ITM_CH020_ARCHITECT_NAVAL_ROUTE;ITM_CH020_EDENROT_WATER_SAMPLE | Scene 3 - Corpse-Laden River. |
| SCN_CH020_FERRY_PILOT | The Ferry and the River Pilot | LOC_CH020_ABANDONED_FERRY_DOCK | Introduce Lam; negotiate passage; bandit pursuit forces decision. | Group reaches abandoned ferry dock. | Lam agrees to guide group to coast. | char_trung;char_mai;comp_hoang;npc_lam | ENM_CH020_BANDIT_PURSUERS | ITM_CH020_LAM_TIDE_MAP | Scene 4 - Ferry and River Pilot. |
| SCN_CH020_FISHING_PORT | The Fishing Port and the Nameless Ship | LOC_CH020_COASTAL_FISHING_PORT | Secure vessel; introduce Thu; defend against bandits and drowned infected. | Group reaches coast with Lam. | Ship repaired, fueled, and launched. | char_trung;char_mai;char_binh;comp_hoang;npc_doctor;npc_thu;npc_lam | ENM_CH020_DROWNED_INFECTED_BOARDERS;ENM_CH020_BANDIT_PURSUERS | ITM_CH020_SHIP_FILTER_FUEL;ITM_CH020_SHIP_NAVIGATION_DATA | Scene 5 - Fishing Port. |
| SCN_CH020_DEPARTURE | Leaving Vietnam | LOC_CH020_NEARSHORE_WATERS | Emotional departure; family processes leaving; Hoang isolated. | Ship launched from port. | Coast disappears; group at sea. | char_trung;char_mai;char_binh;comp_hoang;npc_ong_tu_nieu;npc_lam;npc_thu;npc_doctor;npc_radio_operator | none | none | Scene 6 - Leaving Vietnam. |
| SCN_CH020_BIO_STORM | Bio-Storm | LOC_CH020_OPEN_SEA_NIGHT | Cliffhanger; first bio-storm; radio picks up Eden signals; ship forced toward unknown island. | Night at sea. | Ship pushed toward unnamed island; CH021 hook. | char_trung;char_mai;char_binh;comp_hoang;npc_doctor;npc_thu;npc_lam;npc_radio_operator | ENM_CH020_MARITIME_EDENROT_BLOOM;ENM_CH020_BIO_STORM_HAZARD | ITM_CH020_BIO_STORM_DEBRIS;ITM_CH020_RADIO_SIGNAL_LOG | Scene 7 - Bio-Storm. |

## Scene Notes

- Scene 1 (Hoang's Trial) is a decision scene with no combat. Binh is present but can leave.
- Scene 2 (Leaving Home) is emotional setpiece. No enemies. Focus on farewell and symbol.
- Scene 3 (Corpse-River) introduces drowned infected as a river hazard. Stealth required.
- Scene 4 (Ferry Pilot) is negotiation plus forced decision when bandits arrive.
- Scene 5 (Fishing Port) is the action peak: repair, defend, escape.
- Scene 6 (Departure) is quiet emotional beat; Ong Tu Nieu cooks first meal.
- Scene 7 (Bio-Storm) is the cliffhanger; no win condition, only survival and forced movement.

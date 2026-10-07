# Dialogue - CH031

Metadata:

- chapterID: CH031
- sourceFilename: chapter_031_heartland_convoy.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH031_DT160_001 | comp_binh | STATE_EMPTY_SEAT | Is Uncle Hoang used to the seat? | none | none | morning_camp | DT_160. |
| DLG_CH031_DT160_002 | char_trung | STATE_EMPTY_SEAT | No. | none | none | morning_camp | DT_160. |
| DLG_CH031_DT160_003 | comp_binh | STATE_EMPTY_SEAT | Will he come back for it? | none | none | morning_camp | DT_160. |
| DLG_CH031_DT160_004 | comp_mai | STATE_EMPTY_SEAT | There are people who leave because they think they are protecting others. That does not mean the way they did it was right. | none | none | morning_camp | DT_160. |
| DLG_CH031_DT160_005 | comp_binh | STATE_EMPTY_SEAT | If he saved me but also hurt me, what is he? | none | none | morning_camp | DT_160. |
| DLG_CH031_DT160_006 | char_trung | STATE_EMPTY_SEAT | An adult who did something very wrong and is trying to do one right thing. Those two do not erase each other. | none | none | morning_camp | DT_160. |
| DLG_CH031_DT161_001 | npc_ong_tu_nieu | STATE_MOBILE_NATION | My truck is the kitchen. Anyone who calls it a cargo truck gets unsalted porridge. | none | none | convoy_setup | DT_161. |
| DLG_CH031_DT161_002 | npc_thu | STATE_MOBILE_NATION | My truck is a workshop, not a nursery. | none | none | convoy_setup | DT_161. |
| DLG_CH031_DT161_003 | npc_june | STATE_MOBILE_NATION | But it has a roof. | none | none | convoy_setup | DT_161. |
| DLG_CH031_DT161_004 | npc_thu | STATE_MOBILE_NATION | ...Fine. Workshop has a nursery corner. No one touches the wiring. | none | none | convoy_setup | DT_161. |
| DLG_CH031_DT161_005 | comp_mai | STATE_MOBILE_NATION | Every vehicle has a name, a person in charge, and a children's list. No one disappears without someone knowing. | none | set_flag:FLAG_CH031_CONVVOY_RULES_ESTABLISHED | convoy_setup | DT_161. |
| DLG_CH031_DT162_001 | npc_bandit_leader | STATE_FAKE_CHECKPOINT | We are state relief. Children first, then fuel inspection. | none | none | truck_stop | DT_162. |
| DLG_CH031_DT162_002 | npc_pike | STATE_FAKE_CHECKPOINT | State relief does not use three different uniforms and a hunting rifle with serial filed off. | none | none | truck_stop | DT_162. |
| DLG_CH031_DT162_003 | comp_mai | STATE_FAKE_CHECKPOINT | If children come first, why is the food behind the guns? | none | none | truck_stop | DT_162. |
| DLG_CH031_DT162_004 | npc_bandit_leader | STATE_FAKE_CHECKPOINT | Lady, you want safety or questions? | none | none | truck_stop | DT_162. |
| DLG_CH031_DT162_005 | char_trung | STATE_FAKE_CHECKPOINT | With us, the two go together. | none | set_flag:FLAG_CH031_TRUCK_STOP_BANDITS_EXPOSED | truck_stop | DT_162. |
| DLG_CH031_DT163_001 | npc_thu | STATE_DRONE_HESITATION | It locked onto Binh... wait. It's being pulled somewhere else. | none | none | drone_encounter | DT_163. |
| DLG_CH031_DT163_002 | npc_mara | STATE_DRONE_HESITATION | A decoy? | none | none | drone_encounter | DT_163. |
| DLG_CH031_DT163_003 | npc_thu | STATE_DRONE_HESITATION | No. That mark. It's Hoang's. | none | none | drone_encounter | DT_163. |
| DLG_CH031_DT163_004 | char_trung | STATE_DRONE_HESITATION | Is he nearby? | none | none | drone_encounter | DT_163. |
| DLG_CH031_DT163_005 | npc_thu | STATE_DRONE_HESITATION | Close enough to be bait. Far enough to not be seen. | none | set_flag:FLAG_CH031_HOANG_FALSE_PINGS_DETECTED | drone_encounter | DT_163. |
| DLG_CH031_DT163_006 | comp_binh | STATE_DRONE_HESITATION | Is he still helping? | none | none | drone_encounter | DT_163. |
| DLG_CH031_DT163_007 | comp_mai | STATE_DRONE_HESITATION | Maybe. | none | none | drone_encounter | DT_163. |
| DLG_CH031_DT164_001 | comp_mai | STATE_NAME_CIRCLE | If you remember your name, say it. If you don't remember yet, we won't force it. No one has to keep a name the Cult gave them. | none | none | name_circle | DT_164. |
| DLG_CH031_DT164_002 | npc_noah | STATE_NAME_CIRCLE | Noah. | none | none | name_circle | DT_164. |
| DLG_CH031_DT164_003 | npc_mother_elian | STATE_NAME_CIRCLE | Noah. | none | none | name_circle | DT_164. |
| DLG_CH031_DT164_004 | npc_noah | STATE_NAME_CIRCLE | You can't call me seed anymore. | none | none | name_circle | DT_164. |
| DLG_CH031_DT164_005 | npc_mother_elian | STATE_NAME_CIRCLE | No. If you allow me, I will call you Noah. | none | none | name_circle | DT_164. |
| DLG_CH031_DT164_006 | comp_binh | STATE_NAME_CIRCLE | I am Binh. Not a vector. Not a draft. Just Binh. | none | set_flag:FLAG_CH031_CHILD_NAME_CIRCLE_HELD | name_circle | DT_164. |
| DLG_CH031_DT165_001 | npc_radio_ping | STATE_HOANG_WARNING | Three short. One long. Road dead ahead is teeth. | none | none | radio_warning | DT_165. |
| DLG_CH031_DT165_002 | npc_pike | STATE_HOANG_WARNING | That is not Army code. | none | none | radio_warning | DT_165. |
| DLG_CH031_DT165_003 | npc_thu | STATE_HOANG_WARNING | It's not VALE either. | none | none | radio_warning | DT_165. |
| DLG_CH031_DT165_004 | char_trung | STATE_HOANG_WARNING | Hoang. | none | none | radio_warning | DT_165. |
| DLG_CH031_DT165_005 | comp_mai | STATE_HOANG_WARNING | Do you believe him? | none | none | radio_warning | DT_165. |
| DLG_CH031_DT165_006 | char_trung | STATE_HOANG_WARNING | I believe he knows what he owes. I don't know if I believe in him. | none | set_flag:FLAG_CH031_HOANG_WARNING_TRUSTED_PARTIAL | radio_warning | DT_165. |
| DLG_CH031_DT166_001 | npc_cult_scout | STATE_GRAIN_ELEVATOR | The children belong to tomorrow! | none | none | grain_elevator | DT_166. |
| DLG_CH031_DT166_002 | npc_mara | STATE_GRAIN_ELEVATOR | Tomorrow did not pack them snacks. We did. | none | none | grain_elevator | DT_166. |
| DLG_CH031_DT166_003 | npc_bandit | STATE_GRAIN_ELEVATOR | Fuel or kids, choose! | none | none | grain_elevator | DT_166. |
| DLG_CH031_DT166_004 | char_trung | STATE_GRAIN_ELEVATOR | I choose you first. | none | none | grain_elevator | DT_166. |
| DLG_CH031_DT166_005 | npc_pike | STATE_GRAIN_ELEVATOR | That order I can follow. | none | none | grain_elevator | DT_166. |
| DLG_CH031_DT167_001 | comp_binh | STATE_HOANG_SAVES | Uncle Hoang? | none | none | hoang_rescue | DT_167. |
| DLG_CH031_DT167_002 | comp_hoang | STATE_HOANG_SAVES | Don't run toward me. Run toward her. | none | none | hoang_rescue | DT_167. |
| DLG_CH031_DT167_003 | comp_binh | STATE_HOANG_SAVES | Are you coming back? | none | none | hoang_rescue | DT_167. |
| DLG_CH031_DT167_004 | comp_hoang | STATE_HOANG_SAVES | Not now. | none | none | hoang_rescue | DT_167. |
| DLG_CH031_DT167_005 | comp_binh | STATE_HOANG_SAVES | Dad is really angry. | none | none | hoang_rescue | DT_167. |
| DLG_CH031_DT167_006 | comp_hoang | STATE_HOANG_SAVES | Good. He should be. | none | set_flag:FLAG_CH031_BINH_SAVED_BY_HOANG | hoang_rescue | DT_167. |
| DLG_CH031_DT168_001 | char_trung | STATE_RAIL_LINE | Hoang! | none | none | rail_separation | DT_168. |
| DLG_CH031_DT168_002 | comp_hoang | STATE_RAIL_LINE | Get the convoy moving! | none | none | rail_separation | DT_168. |
| DLG_CH031_DT168_003 | char_trung | STATE_RAIL_LINE | You stop! | none | none | rail_separation | DT_168. |
| DLG_CH031_DT168_004 | comp_hoang | STATE_RAIL_LINE | This time I'm pulling them toward you! | none | none | rail_separation | DT_168. |
| DLG_CH031_DT168_005 | comp_mai | STATE_RAIL_LINE | Trung, the children! | none | none | rail_separation | DT_168. |
| DLG_CH031_DT168_006 | char_trung | STATE_RAIL_LINE | ...Get in the vehicle! | none | set_flag:FLAG_CH031_CONVOY_CHOSEN_OVER_HOANG | rail_separation | DT_168. |
| DLG_CH031_DT169_001 | npc_vale_core | STATE_NORAD_HOOK | Emergency broadcast node recovered. Mountain command facility detected. | none | none | norad_hook | DT_169. |
| DLG_CH031_DT169_002 | npc_pike | STATE_NORAD_HOOK | NORAD. | none | none | norad_hook | DT_169. |
| DLG_CH031_DT169_003 | comp_binh | STATE_NORAD_HOOK | Will that place have room for all of us? | none | none | norad_hook | DT_169. |
| DLG_CH031_DT169_004 | char_trung | STATE_NORAD_HOOK | We don't know yet. | none | none | norad_hook | DT_169. |
| DLG_CH031_DT169_005 | comp_mai | STATE_NORAD_HOOK | Then before we get there, we have to decide who we are when the answer is no. | none | set_flag:FLAG_CH031_NORAD_ROUTE_UNLOCKED | norad_hook | DT_169. |

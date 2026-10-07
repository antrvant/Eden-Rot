# Dialogue - CH043

Metadata:

- chapterID: CH043
- sourceFilename: chapter_043_amazon_ngap_mau_xanh.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH043_IARA_MAP_001 | char_trung | STATE_IARA_MAP | Satellite says channel is open. | none | none | arrival | DT_272. |
| DLG_CH043_IARA_MAP_002 | npc_iara | STATE_IARA_MAP | Satellite sees leaves. River sees teeth. | none | none | arrival | DT_272. |
| DLG_CH043_IARA_MAP_003 | comp_mai | STATE_IARA_MAP | Which one do we follow? | none | none | arrival | DT_272. |
| DLG_CH043_IARA_MAP_004 | npc_iara | STATE_IARA_MAP | The one that can kill us today. | none | set_flag:FLAG_CH043_IARA_GUIDE_MET | arrival | DT_272. |
| DLG_CH043_TREES_MOVING_001 | npc_scout | STATE_TREES_MOVING | Trees are moving behind us. | none | none | canopy_route | DT_273. |
| DLG_CH043_TREES_MOVING_002 | comp_samir | STATE_TREES_MOVING | Trees do not move like that. | none | none | canopy_route | DT_273. |
| DLG_CH043_TREES_MOVING_003 | npc_iara | STATE_TREES_MOVING | Then stop calling them trees for one minute. | none | set_flag:FLAG_CH043_MOVING_CANOPY_OBSERVED | canopy_route | DT_273. |
| DLG_CH043_BINH_NOT_SENSOR_001 | comp_samir | STATE_BINH_SENSOR | If Binh could listen just a little longer... | none | none | resonance_tension | DT_274. |
| DLG_CH043_BINH_NOT_SENSOR_002 | comp_binh | STATE_BINH_SENSOR | Den do. | none | none | resonance_tension | DT_274. |
| DLG_CH043_BINH_NOT_SENSOR_003 | comp_mai | STATE_BINH_SENSOR | You heard him. | none | none | resonance_tension | DT_274. |
| DLG_CH043_BINH_NOT_SENSOR_004 | comp_samir | STATE_BINH_SENSOR | I did. | none | none | resonance_tension | DT_274. |
| DLG_CH043_BINH_NOT_SENSOR_005 | char_trung | STATE_BINH_SENSOR | Then your sentence is over. | none | set_flag:FLAG_CH043_STOP_WORD_HONORED | resonance_tension | DT_274. |
| DLG_CH043_GREEN_WATER_001 | comp_yusuf | STATE_GREEN_WATER | It glows where we passed. | none | none | algae_river | DT_275. |
| DLG_CH043_GREEN_WATER_002 | npc_iara | STATE_GREEN_WATER | It remembers heat. | none | set_flag:FLAG_CH043_GREEN_WATER_DISCOVERED | algae_river | DT_275. |
| DLG_CH043_GREEN_WATER_003 | comp_hoang | STATE_GREEN_WATER | Great. Even water can hold a grudge now. | none | none | algae_river | DT_275. |
| DLG_CH043_FIRST_STALKER_001 | comp_amelie | STATE_FIRST_STALKER | I heard him call from the left. | none | none | stalker_encounter | DT_276. |
| DLG_CH043_FIRST_STALKER_002 | npc_iara | STATE_FIRST_STALKER | The body went right. | none | none | stalker_encounter | DT_276. |
| DLG_CH043_FIRST_STALKER_003 | char_trung | STATE_FIRST_STALKER | How do you know? | none | none | stalker_encounter | DT_276. |
| DLG_CH043_FIRST_STALKER_004 | npc_iara | STATE_FIRST_STALKER | Because the left wanted us to hear. | none | set_flag:FLAG_CH043_FIRST_STALKER_IDENTIFIED | stalker_encounter | DT_276. |
| DLG_CH043_ORISON_SCHOOL_001 | comp_mai | STATE_ORISON_SCHOOL | These are handwriting sheets. | none | none | schoolroom | DT_277. |
| DLG_CH043_ORISON_SCHOOL_002 | comp_samir | STATE_ORISON_SCHOOL | Orison labeled them harmonic subjects. | none | none | schoolroom | DT_277. |
| DLG_CH043_ORISON_SCHOOL_003 | comp_mai | STATE_ORISON_SCHOOL | No. Children. Start again. | none | set_flag:FLAG_CH043_ORISON_SCHOOLROOM_FOUND | schoolroom | DT_277. |
| DLG_CH043_SAVE_NAMES_001 | npc_fighter | STATE_SAVE_CHOICE | Fuel crate is going! | none | none | ambush_choice | DT_278. |
| DLG_CH043_SAVE_NAMES_002 | comp_amelie | STATE_SAVE_CHOICE | The names are in the other boat! | none | none | ambush_choice | DT_278. |
| DLG_CH043_SAVE_NAMES_003 | char_trung | STATE_SAVE_CHOICE | Fuel keeps us moving. | none | none | ambush_choice | DT_278. |
| DLG_CH043_SAVE_NAMES_004 | comp_mai | STATE_SAVE_CHOICE | Names tell us who we are moving for. | Choice A: Save fuel crate.; Choice B: Save child archive names. | open_choice | ambush_choice | DT_278. |
| DLG_CH043_SAVE_NAMES_005A | char_trung | STATE_SAVE_FUEL | We need to move. | none | set_flag:FLAG_CH043_FUEL_CRATE_SAVED;set_flag:FLAG_CH043_ORISON_NAMES_LOST | choice:DLG_CH043_SAVE_NAMES_004:A | DT_278 Choice A. |
| DLG_CH043_SAVE_NAMES_005B | char_trung | STATE_SAVE_NAMES | Save the names. | none | set_flag:FLAG_CH043_FUEL_CRATE_LOST;set_flag:FLAG_CH043_ORISON_NAMES_RECOVERED | choice:DLG_CH043_SAVE_NAMES_004:B | DT_278 Choice B. |
| DLG_CH043_HOANG_ECHO_001 | comp_hoang | STATE_HOANG_ECHO | The jungle is calling the sick part of me. | none | none | hoang_confession | DT_279. |
| DLG_CH043_HOANG_ECHO_002 | char_trung | STATE_HOANG_ECHO | Can you ignore it? | none | none | hoang_confession | DT_279. |
| DLG_CH043_HOANG_ECHO_003 | comp_hoang | STATE_HOANG_ECHO | I can lie and say yes. | none | none | hoang_confession | DT_279. |
| DLG_CH043_HOANG_ECHO_004 | char_trung | STATE_HOANG_ECHO | Then don't. | none | set_flag:FLAG_CH043_HOANG_SIGNAL_HONESTY | hoang_confession | DT_279. |
| DLG_CH043_FAMILY_CODE_001 | npc_voice_fake | STATE_FAMILY_CODE | Ba oi, con o day. | none | none | voice_trap | DT_280. |
| DLG_CH043_FAMILY_CODE_002 | char_trung | STATE_FAMILY_CODE | What color? | none | none | voice_trap | DT_280. |
| DLG_CH043_FAMILY_CODE_003 | npc_voice_fake | STATE_FAMILY_CODE | Ba oi... | none | none | voice_trap | DT_280. |
| DLG_CH043_FAMILY_CODE_004 | char_trung | STATE_FAMILY_CODE | Wrong. | none | set_flag:FLAG_CH043_FAMILY_CODE_VERIFIED | voice_trap | DT_280. |
| DLG_CH043_SPLIT_001 | comp_mai | STATE_SPLIT | We are alive. Binh is with me. Yusuf too. Do not run blind. | none | none | party_split | DT_281. |
| DLG_CH043_SPLIT_002 | char_trung | STATE_SPLIT | Say code. | none | none | party_split | DT_281. |
| DLG_CH043_SPLIT_003 | comp_mai | STATE_SPLIT | No one saves the world alone. | none | none | party_split | DT_281. |
| DLG_CH043_SPLIT_004 | char_trung | STATE_SPLIT | I am coming. | none | none | party_split | DT_281. |
| DLG_CH043_SPLIT_005 | comp_mai | STATE_SPLIT | Come right, not fast. | none | set_flag:FLAG_CH043_PARTY_SPLIT_ACTIVE | party_split | DT_281. |
| DLG_CH043_CITADEL_001 | npc_aster_relay | STATE_CITADEL | Welcome to the part of Earth that stopped asking permission. | none | none | citadel_edge | DT_282. |
| DLG_CH043_CITADEL_002 | npc_iara | STATE_CITADEL | That is not a welcome. | none | none | citadel_edge | DT_282. |
| DLG_CH043_CITADEL_003 | comp_binh | STATE_CITADEL | It sounds like a door locking. | none | set_flag:FLAG_CH043_OUTER_CITADEL_DOOR_SEEN;set_flag:FLAG_CH043_CH44_BREACH_UNLOCKED | citadel_edge | DT_282. |

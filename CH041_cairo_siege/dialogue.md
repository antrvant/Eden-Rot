# Dialogue - CH041

Metadata:

- chapterID: CH041
- sourceFilename: chapter_041_cairo_siege.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH041_252_01 | npc_kito | STATE_CAIRO_ARRIVAL | Route clean for twelve minutes. After that the wind shifts, blood smell will pull the infected back. | none | none | convoy_entering_cairo | DT_252. |
| DLG_CH041_252_02 | char_trung | STATE_CAIRO_ARRIVAL | Twelve minutes for a city with four thousand years of history. Sounds fair. | none | none | convoy_entering_cairo | DT_252. |
| DLG_CH041_252_03 | comp_mai | STATE_CAIRO_ARRIVAL | Let's go. History never gave anyone enough time. | none | set_flag:FLAG_CH041_CAIRO_ARRIVED | convoy_entering_cairo | DT_252. |
| DLG_CH041_253_01 | npc_samir | STATE_ENZYME_HANDOFF | This scanner is contaminated with living impurities. | none | none | enzyme_placed_in_tray | DT_253. |
| DLG_CH041_253_02 | npc_nia | STATE_ENZYME_HANDOFF | Your machine calls life a contaminant. The problem lies in the machine. | none | set_flag:FLAG_CH041_ENZYME_DELIVERED | enzyme_placed_in_tray | DT_253. |
| DLG_CH041_253_03 | npc_samir | STATE_ENZYME_HANDOFF | I will write that down. So every time the machine is overconfident, I read it to it. | none | set_flag:FLAG_CH041_SEED_COVENANT_LOGGED | enzyme_placed_in_tray | DT_253. |
| DLG_CH041_254_01 | npc_refugee_mother | STATE_REFUGEE_QUEUE | If there is one dose, give it to mine. I'll sign anything. | none | none | mother_holds_child | DT_254. |
| DLG_CH041_254_02 | comp_mai | STATE_REFUGEE_QUEUE | You sign when you understand. Here nobody trades a life for a signature. | none | set_flag:FLAG_CH041_REFUGEE_LINE_FORMED | mother_holds_child | DT_254. |
| DLG_CH041_254_03 | char_trung | STATE_REFUGEE_QUEUE | And nobody cuts the line with a gun. | none | none | mother_holds_child | DT_254. |
| DLG_CH041_255_01 | npc_yusuf | STATE_YUSUF_CONSENT | Will it hurt? | none | none | consent_form_presented | DT_255. |
| DLG_CH041_255_02 | comp_mai | STATE_YUSUF_CONSENT | Yes. | none | none | consent_form_presented | DT_255. |
| DLG_CH041_255_03 | npc_yusuf | STATE_YUSUF_CONSENT | Then why do you tell the truth? | none | none | consent_form_presented | DT_255. |
| DLG_CH041_255_04 | comp_mai | STATE_YUSUF_CONSENT | Because if this medicine starts with a lie, it does not deserve to save you. | none | set_flag:FLAG_CH041_CONSENT_GIVEN | consent_form_presented | DT_255. |
| DLG_CH041_256_01 | comp_hoang | STATE_HOANG_VOLUNTEER | Use me. I'm already infected. If it fails, the loss isn't as great as a child. | none | none | hoang_offers_self | DT_256. |
| DLG_CH041_256_02 | char_trung | STATE_HOANG_VOLUNTEER | Don't talk about yourself like damaged goods in storage. | none | none | hoang_offers_self | DT_256. |
| DLG_CH041_256_03 | comp_hoang | STATE_HOANG_VOLUNTEER | I'm talking as someone who knows he might explode. | none | set_flag:FLAG_CH041_HOANG_RESTRAINED | hoang_offers_self | DT_256. |
| DLG_CH041_257_01 | npc_masud | STATE_MASUD_BARGAIN | You keep the miracle in the basement while people die out here. I'm just putting it on the market. | none | none | masud_contacts_trung | DT_257. |
| DLG_CH041_257_02 | char_trung | STATE_MASUD_BARGAIN | Your market starts with hostages. | none | none | masud_contacts_trung | DT_257. |
| DLG_CH041_257_03 | npc_masud | STATE_MASUD_BARGAIN | Hostage is just an ugly word for collateral. | none | none | masud_contacts_trung | DT_257. |
| DLG_CH041_257_04 | comp_mai | STATE_MASUD_BARGAIN | Thank you. You just saved us a minute of hesitation. | none | set_flag:FLAG_CH041_RANSOM_REJECTED | masud_contacts_trung | DT_257. |
| DLG_CH041_258_01 | npc_samir | STATE_CURE_SUCCESS | Pulse dropping... no, skin changing... skin retreating. It's alive. My God, it's alive. | none | set_flag:FLAG_CH041_FIRST_CURE_SUCCESS | yusuf_injection | DT_258. |
| DLG_CH041_258_02 | comp_mai | STATE_CURE_SUCCESS | Yusuf. Can you hear me? Your name is Yusuf. | none | set_flag:FLAG_CH041_YUSUF_NAMED_LOGGED | yusuf_injection | DT_258. |
| DLG_CH041_258_03 | npc_yusuf | STATE_CURE_SUCCESS | Water... the pump... | none | none | yusuf_injection | DT_258. |
| DLG_CH041_258_04 | comp_binh | STATE_CURE_SUCCESS | He still remembers. | none | set_flag:FLAG_CH041_SAMIR_WHISPER | yusuf_injection | DT_258. |
| DLG_CH041_259_01 | npc_kareem | STATE_BATCH_FAILURE | Same formula. Same enzyme. Why? | none | set_flag:FLAG_CH041_BATCH_FAILED | micro_dose_tests | DT_259. |
| DLG_CH041_259_02 | npc_samir | STATE_BATCH_FAILURE | Not the same person. | none | set_flag:FLAG_CH041_RESONANCE_FACTOR_MISSING | micro_dose_tests | DT_259. |
| DLG_CH041_259_03 | comp_mai | STATE_BATCH_FAILURE | Don't turn that sentence into an excuse to take anyone. | none | set_flag:FLAG_CH041_BINH_NOT_FACTOR | micro_dose_tests | DT_259. |
| DLG_CH041_260_01 | comp_amelie | STATE_JUGGERNAUT_KNOCK | Is it breaking the door? | none | none | juggernaut_arrives | DT_260. |
| DLG_CH041_260_02 | char_trung | STATE_JUGGERNAUT_KNOCK | No. It's knocking. | none | set_flag:FLAG_CH041_JUGGERNAUT_ARRIVES | juggernaut_arrives | DT_260. |
| DLG_CH041_260_03 | comp_hoang | STATE_JUGGERNAUT_KNOCK | What kind of monster knocks before entering? | none | none | juggernaut_arrives | DT_260. |
| DLG_CH041_260_04 | char_trung | STATE_JUGGERNAUT_KNOCK | The kind that used to be human. | none | none | juggernaut_arrives | DT_260. |
| DLG_CH041_261_01 | npc_samir | STATE_BINH_UNDERSTANDS | Need a living resonance bridge. Not enzyme, not Elise. A person... | none | none | binh_overhears_samir | DT_261. |
| DLG_CH041_261_02 | comp_mai | STATE_BINH_UNDERSTANDS | Don't. | none | none | binh_overhears_samir | DT_261. |
| DLG_CH041_261_03 | comp_binh | STATE_BINH_UNDERSTANDS | Is it me? | none | set_flag:FLAG_CH041_BINH_UNDERSTANDS | binh_overhears_samir | DT_261. |
| DLG_CH041_261_04 | char_trung | STATE_BINH_UNDERSTANDS | Binh... | none | none | binh_overhears_samir | DT_261. |
| DLG_CH041_261_05 | comp_binh | STATE_BINH_UNDERSTANDS | If I can help, don't lie to me that I can't. | none | none | binh_overhears_samir | DT_261. |

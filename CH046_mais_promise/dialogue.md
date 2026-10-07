# Dialogue - CH046

Metadata:

- chapterID: CH046
- sourceFilename: chapter_046_loi_hua_cua_mai.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH046_DT304_001 | char_trung | STATE_PRISON_ENTRY | If the door opens, I can pull them out fast. | none | none | prison_entry | DT_304 - Mai's Rule. |
| DLG_CH046_DT304_002 | char_mai | STATE_PRISON_ENTRY | You can pull bodies out. I need them to also leave this place inside their heads. | none | none | prison_entry | DT_304. |
| DLG_CH046_DT305_001 | char_ana | STATE_CHILD_WARD | Adults know codes. Not names. | none | none | child_ward | DT_305 - Ana Tests Names. |
| DLG_CH046_DT305_002 | char_mai | STATE_CHILD_WARD | Ana. Mateo. Luz. Rafi. Nina. | none | set_flag:FLAG_CH046_ANA_MET | child_ward | DT_305. |
| DLG_CH046_DT305_003 | char_ana | STATE_CHILD_WARD | Who gave you those? | none | none | child_ward | DT_305. |
| DLG_CH046_DT305_004 | char_binh | STATE_CHILD_WARD | They left them themselves. | none | none | child_ward | DT_305. |
| DLG_CH046_DT306_001 | char_orison | STATE_CLASSROOM | Consent can be restored after survival. | none | none | classroom | DT_306 - Orison On Consent. |
| DLG_CH046_DT306_002 | char_mai | STATE_CLASSROOM | No. If you break it to save it, what you give back is only a shell. | none | none | classroom | DT_306. |
| DLG_CH046_DT307_001 | char_binh | STATE_NAME_CIRCLE | My stop word is Den do. Yours do not need to match mine. | none | none | name_circle | DT_307 - Name Circle. |
| DLG_CH046_DT307_002 | char_mateo | STATE_NAME_CIRCLE | *tap tap, pause, tap* | none | set_flag:FLAG_CH046_MATEO_TAP_CODE_LEARNED | name_circle | DT_307. |
| DLG_CH046_DT307_003 | char_amelie | STATE_NAME_CIRCLE | He says his is Knock. | none | none | name_circle | DT_307. |
| DLG_CH046_DT308_001 | char_orison | STATE_TRADE | One willing bridge for twenty-seven frightened children. | none | none | orison_trade | DT_308 - Orison Trade. |
| DLG_CH046_DT308_002 | char_ana | STATE_TRADE | No. | none | none | orison_trade | DT_308. |
| DLG_CH046_DT308_003 | char_mai | STATE_TRADE | You are not the adult here, Ana. You do not decide for anyone. | none | none | orison_trade | DT_308. |
| DLG_CH046_DT308_004 | char_ana | STATE_TRADE | I am not deciding for them. I am saying we do not sell friends. | none | set_flag:FLAG_CH046_NO_CHILD_AS_CURRENCY | orison_trade | DT_308. |
| DLG_CH046_DT309_001 | char_binh | STATE_GLUTTON_REVEAL | What does it eat? | none | none | glutton_below | DT_309 - Glutton Reveal. |
| DLG_CH046_DT309_002 | char_trung | STATE_GLUTTON_REVEAL | Not today. | none | none | glutton_below | DT_309. |
| DLG_CH046_DT309_003 | char_mai | STATE_GLUTTON_REVEAL | You did not answer. | none | none | glutton_below | DT_309. |
| DLG_CH046_DT309_004 | char_trung | STATE_GLUTTON_REVEAL | Because today the answer will not happen. | none | none | glutton_below | DT_309. |
| DLG_CH046_DT310_001 | char_luz | STATE_BREAKOUT | If I open the crawlspace, Orison knows I lied. | none | set_flag:FLAG_CH046_LUZ_INSIDER_ROUTE | ward_breakout | DT_310 - Luz Route. |
| DLG_CH046_DT310_002 | char_mai | STATE_BREAKOUT | Then we make your lie worth it. | none | none | ward_breakout | DT_310. |
| DLG_CH046_DT311_001 | npc_samir | STATE_ANTARCTICA | Terraforming core is leaving. | none | none | antarctica_transfer | DT_311 - Antarctica Transfer. |
| DLG_CH046_DT311_002 | char_iara | STATE_ANTARCTICA | Leaving where? | none | none | antarctica_transfer | DT_311. |
| DLG_CH046_DT311_003 | npc_samir | STATE_ANTARCTICA | Antarctica. | none | set_flag:FLAG_CH046_ANTARCTICA_TRANSFER_DISCOVERED | antarctica_transfer | DT_311. |
| DLG_CH046_DT311_004 | char_orison | STATE_ANTARCTICA | Children were one pathway. Source is the final one. | none | none | antarctica_transfer | DT_311. |
| DLG_CH046_DT312_001 | char_ana | STATE_COUNTING | How many did we save? | none | none | counting_names | DT_312 - Counting Names. |
| DLG_CH046_DT312_002 | char_mai | STATE_COUNTING | I will count by names. | none | none | counting_names | DT_312. |
| DLG_CH046_DT312_003 | char_binh | STATE_COUNTING | And the missing? | none | none | counting_names | DT_312. |
| DLG_CH046_DT312_004 | char_mai | STATE_COUNTING | Also by names. | none | set_flag:FLAG_CH046_CHILD_RECORD_PRIORITY | counting_names | DT_312. |
| DLG_CH046_DT313_001 | npc_radio_op | STATE_COLLAPSE_HOOK | Multiple factions converging. They know you have the children. | none | none | collapse_protocol | DT_313 - Chapter 47 Hook. |
| DLG_CH046_DT313_002 | char_mai | STATE_COLLAPSE_HOOK | We do not have children. We are going with children. | none | set_flag:FLAG_CH046_CH47_CITADEL_COLLAPSE_UNLOCKED | collapse_protocol | DT_313. |
| DLG_CH046_DT313_003 | char_trung | STATE_COLLAPSE_HOOK | Prepare to move. | none | none | collapse_protocol | DT_313. |
| DLG_CH046_char_binh_001 | char_binh | STATE_BASE | Mom promised me we would see the sun again. But it's always gray. | Choice 1: "She was speaking about the future." : STATE_BINH_CHAT_FUTURE \| Choice 2: "Do you believe her?" : STATE_BINH_CHAT_BELIEVE | none | none | none |
| DLG_CH046_char_binh_002 | char_binh | STATE_BINH_CHAT_FUTURE | The future is a long time. I want to play outside now. | none | none | none | none |
| DLG_CH046_char_binh_003 | char_binh | STATE_BINH_CHAT_BELIEVE | I do. She always keeps her promises, even when she has to go away. | none | none | none | none |
| DLG_CH046_char_mai_001 | char_mai | STATE_BASE | The research is complete. The cure is real, Trung. But the synthesis requires more power than this base can generate. | Choice 1: "Where can we get the power?" : STATE_MAI_CHAT_POWER \| Choice 2: "What is the risk?" : STATE_MAI_CHAT_RISK | none | none | none |
| DLG_CH046_char_mai_002 | char_mai | STATE_MAI_CHAT_POWER | The Edenrot core. We have to go to the prime sector. | none | none | none | none |
| DLG_CH046_char_mai_003 | char_mai | STATE_MAI_CHAT_RISK | The radiation level is lethal. Whoever goes there... won't be coming back. | none | none | none | none |
| DLG_CH046_char_amelie_001 | npc_amelie | STATE_BASE | The helicopters are prepped, but the weather is closing in. We have a narrow window. | Choice 1: "We need to wait for Mai." : STATE_AMELIE_CHAT_MAI \| Choice 2: "Are the children ready?" : STATE_AMELIE_CHAT_CHILDREN | none | none | none |
| DLG_CH046_char_amelie_002 | npc_amelie | STATE_AMELIE_CHAT_MAI | We can't wait. If the storm hits, the rotors will freeze. We leave in 30 minutes, with or without her. | none | none | none | none |
| DLG_CH046_char_amelie_003 | npc_amelie | STATE_AMELIE_CHAT_CHILDREN | They are on board. They are scared, but warm. | none | none | none | none |

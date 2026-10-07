# Dialogue - CH042

Metadata:

- chapterID: CH042
- sourceFilename: chapter_042_mau_cua_con.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH042_LAB_001 | char_binh | STATE_LAB_NIGHT | Everyone has been whispering since Uncle Yusuf woke up. Is it because of me? | none | none | Scene 01 start | Scene 01 - Binh asks why everyone whispers. |
| DLG_CH042_LAB_002 | char_trung | STATE_LAB_NIGHT | Not everything is your business. | none | set_flag:FLAG_CH042_TRUNG_SHUT_DOWN_HARD | Scene 01 | Scene 01 - Trung shuts down too hard. |
| DLG_CH042_LAB_003 | char_binh | STATE_LAB_NIGHT | But what if everything stops because of me? | none | none | Scene 01 | Scene 01 - Binh pushes back. |
| DLG_CH042_LAB_004 | char_mai | STATE_LAB_NIGHT | Then you have the right to hear the part that involves you. | none | none | Scene 01 | Scene 01 - Mai supports Binh. |
| DLG_CH042_TRUTH_001 | char_binh | STATE_TRUTH_MEETING | Everyone has been whispering since Uncle Yusuf woke up. Is it because of me? | none | none | Scene 02 | DT_262 - Binh asks for truth. |
| DLG_CH042_TRUTH_002 | char_trung | STATE_TRUTH_MEETING | Not everything is your business. | none | set_flag:FLAG_CH042_TRUNG_REFLEX | Scene 02 | DT_262 - Trung reflex response. |
| DLG_CH042_TRUTH_003 | char_binh | STATE_TRUTH_MEETING | But what if everything stops because of me? | none | none | Scene 02 | DT_262 - Binh challenge. |
| DLG_CH042_TRUTH_004 | char_mai | STATE_TRUTH_MEETING | Then you have the right to hear the part that involves you. | none | set_flag:FLAG_CH042_MAI_SUPPORTS_TRUTH | Scene 02 | DT_262 - Mai grants hearing right. |
| DLG_CH042_SAMIR_001 | char_samir | STATE_RESONANCE_EXPLAIN | There are bodies that help medicine find its way back to being human. Yusuf has a small part. You might have a stronger part. | none | none | Scene 02 | DT_263 - Samir explains resonance. |
| DLG_CH042_SAMIR_002 | char_binh | STATE_RESONANCE_EXPLAIN | My blood? | none | none | Scene 02 | DT_263 - Binh asks directly. |
| DLG_CH042_SAMIR_003 | char_samir | STATE_RESONANCE_EXPLAIN | Maybe. But maybe does not mean allowed. | none | none | Scene 02 | DT_263 - Samir corrects himself. |
| DLG_CH042_BINH_CONSENT_001 | char_binh | STATE_CONSENT_ASK | If I say no, will Mom and Dad be disappointed? | none | none | Scene 02 | DT_265 - Binh tests parental love. |
| DLG_CH042_BINH_CONSENT_002 | char_mai | STATE_CONSENT_ASK | No. | none | none | Scene 02 | DT_265 - Mai answer. |
| DLG_CH042_BINH_CONSENT_003 | char_trung | STATE_CONSENT_ASK | Never. | none | none | Scene 02 | DT_265 - Trung answer. |
| DLG_CH042_BINH_CONSENT_004 | char_binh | STATE_CONSENT_ASK | Even if people die out there? | none | none | Scene 02 | DT_265 - Binh pressure test. |
| DLG_CH042_BINH_CONSENT_005 | char_trung | STATE_CONSENT_ASK | The dead do not get to force you to live as a lock. | none | set_flag:FLAG_CH042_BINH_TRUTH_CONVERSATION_COMPLETE | Scene 02 | DT_265 - Trung answer. |
| DLG_CH042_GUARDIAN_001 | char_trung | STATE_GUARDIAN_FIGHT | I am not letting anyone touch our child. | none | none | Scene 03 | DT_264 - Trung opens argument. |
| DLG_CH042_GUARDIAN_002 | char_mai | STATE_GUARDIAN_FIGHT | Neither am I. But you are banning truth from reaching him too. | none | none | Scene 03 | DT_264 - Mai counters. |
| DLG_CH042_GUARDIAN_003 | char_trung | STATE_GUARDIAN_FIGHT | Truth does not hurt as much as a needle. | none | none | Scene 03 | DT_264 - Trung. |
| DLG_CH042_GUARDIAN_004 | char_mai | STATE_GUARDIAN_FIGHT | It hurts differently when he discovers he was lied to. | none | set_flag:FLAG_CH042_GUARDIAN_CONFLICT_RESOLVED | Scene 03 | DT_264 - Mai. |
| DLG_CH042_PROTOCOL_001 | npc_amelie | STATE_ETHICS_TABLE | Write it clearly: he is allowed to change his mind. | none | none | Scene 04 | DT_266 - Amelie clause. |
| DLG_CH042_PROTOCOL_002 | npc_kareem | STATE_ETHICS_TABLE | Even when the needle is already in? | none | none | Scene 04 | DT_266 - Kareem challenge. |
| DLG_CH042_PROTOCOL_003 | char_mai | STATE_ETHICS_TABLE | Especially when the needle is already in. | none | none | Scene 04 | DT_266 - Mai answer. |
| DLG_CH042_PROTOCOL_004 | npc_thu | STATE_ETHICS_TABLE | EDENROT CLASS: CHILD CONSENT FIREWALL. ACTIVE. | none | set_flag:FLAG_CH042_EDENROT_CHILD_CONSENT_FIREWALL_ESTABLISHED;set_flag:FLAG_CH042_CHILD_CONSENT_FIREWALL_ACTIVE | Scene 04 | Scene 04 - Thu writes firewall header. |
| DLG_CH042_STOP_WORD_001 | char_binh | STATE_STOP_WORD | Can I choose the word? | Choice A: "Red light"; Choice B: "Stop"; Choice C: "Home" | open_choice | Scene 04 | SQ_042_B - Stop word choice. |
| DLG_CH042_STOP_WORD_002A | char_binh | STATE_STOP_WORD_A | Red light. | none | set_flag:FLAG_CH042_BINH_STOP_WORD_CHOSEN;set_flag:FLAG_CH042_BINH_STOP_WORD | choice:DLG_CH042_STOP_WORD_001:A | SQ_042_B canon choice. |
| DLG_CH042_STOP_WORD_003 | char_samir | STATE_STOP_WORD_CONFIRM | Red light. When you say it, everything stops. | none | none | Scene 04 | Scene 04 - Samir confirms. |
| DLG_CH042_STOP_WORD_004 | char_binh | STATE_STOP_WORD_CONFIRM | Even if you are very close to the answer? | none | none | Scene 04 | Scene 04 - Binh tests commitment. |
| DLG_CH042_STOP_WORD_005 | char_samir | STATE_STOP_WORD_CONFIRM | Especially when I am very close to the answer. | none | set_flag:FLAG_CH042_BINH_TRUST_PLUS | Scene 04 | Scene 04 - Samir commits. |
| DLG_CH042_YUSUF_001 | npc_yusuf | STATE_YUSUF_WAKE | Pump number three... | none | none | Scene 05 | Scene 05 - Yusuf wakes. |
| DLG_CH042_YUSUF_002 | npc_yusuf | STATE_YUSUF_WAKE | Lina? | none | none | Scene 05 | Scene 05 - Yusuf asks for sister. |
| DLG_CH042_YUSUF_003 | char_mai | STATE_YUSUF_WAKE | We are searching for your sister through the relay. No confirmed news yet. | none | none | Scene 05 | Scene 05 - Mai honest answer. |
| DLG_CH042_YUSUF_004 | npc_yusuf | STATE_YUSUF_WAKE | Not dead? | none | none | Scene 05 | Scene 05 - Yusuf presses. |
| DLG_CH042_YUSUF_005 | char_mai | STATE_YUSUF_WAKE | No confirmed news. That means we do not know. Nothing more. I will not use that phrase to sell you false hope. | none | none | Scene 05 | Scene 05 - Mai refuses to lie. |
| DLG_CH042_YUSUF_006 | npc_yusuf | STATE_YUSUF_BINH | You are Binh. | none | none | Scene 05 | Scene 05 - Yusuf recognizes Binh. |
| DLG_CH042_YUSUF_007 | npc_yusuf | STATE_YUSUF_BINH | I heard you singing. | none | none | Scene 05 | Scene 05 - Yusuf warmth. |
| DLG_CH042_YUSUF_008 | npc_yusuf | STATE_YUSUF_BINH | Living does not mean you owe me the rest of you. | none | none | Scene 05 | DT_267 - Yusuf rejects debt logic. |
| DLG_CH042_YUSUF_009 | char_binh | STATE_YUSUF_BINH | But what if I can help? | none | none | Scene 05 | DT_267 - Binh asks. |
| DLG_CH042_YUSUF_010 | npc_yusuf | STATE_YUSUF_BINH | Then help as a person. Do not let anyone turn you into a blood warehouse. | none | set_flag:FLAG_CH042_YUSUF_DEBT_LOGIC_REJECTED | Scene 05 | DT_267 - Yusuf answer. |
| DLG_CH042_MASUD_001 | char_trung | STATE_MASUD_RUMOR | Shut down all comms. | none | none | Scene 06 | Scene 06 - Trung reaction. |
| DLG_CH042_MASUD_002 | npc_amelie | STATE_MASUD_RUMOR | If you shut down, Nia cannot warn about forest routes. NORAD cannot send Amazon data. Salma cannot tell us which direction Masud is chasing from. | none | none | Scene 06 | Scene 06 - Amelie counters blackout. |
| DLG_CH042_MASUD_003 | char_mai | STATE_MASUD_RUMOR | Trusted nodes only. Re-encrypt. No samples, no profiles, no names. | none | set_flag:FLAG_CH042_TRUSTED_ALLIES_BRIEFED | Scene 06 | Scene 06 - Mai solution. |
| DLG_CH042_MASUD_004 | char_mai | STATE_MASUD_RUMOR | Say that cure research continues. Say there is no child stock, no blood miracle, no shortcut. Say that anyone hunting children will be treated as an enemy of the alliance. | none | none | Scene 06 | Scene 06 - Mai message content. |
| DLG_CH042_NEEDLE_001 | char_samir | STATE_BLOOD_DRAW | Which arm? | none | none | Scene 07 | Scene 07 - Samir asks. |
| DLG_CH042_NEEDLE_002 | char_binh | STATE_BLOOD_DRAW | Left. | none | none | Scene 07 | Scene 07 - Binh chooses. |
| DLG_CH042_NEEDLE_003 | char_mai | STATE_BLOOD_DRAW | Cold. | none | none | Scene 07 | Scene 07 - Mai describes antiseptic. |
| DLG_CH042_NEEDLE_004 | char_mai | STATE_BLOOD_DRAW | The needle will hurt. | none | none | Scene 07 | Scene 07 - Mai prepares. |
| DLG_CH042_NEEDLE_005 | char_mai | STATE_BLOOD_DRAW | You can say red light any time. | none | none | Scene 07 | Scene 07 - Mai reminder. |
| DLG_CH042_STOP_001 | char_binh | STATE_STOP | Red light. | none | set_flag:FLAG_CH042_PROCEDURE_STOPPED_ON_COMMAND | Scene 07 stop word prompt | DT_268 - Binh uses stop word. |
| DLG_CH042_STOP_002 | char_samir | STATE_STOP | Stop. | none | none | Scene 07 | DT_268 - Samir stops. |
| DLG_CH042_STOP_003 | char_trung | STATE_STOP | Everyone stop. | none | none | Scene 07 | DT_268 - Trung repeats. |
| DLG_CH042_STOP_004 | char_mai | STATE_STOP | You do not need to explain. | none | set_flag:FLAG_CH042_STOP_WORD_HONORED_FIREWALL_VERIFIED | Scene 07 | DT_268 - Mai affirms. |
| DLG_CH042_STOP_005 | char_binh | STATE_AFTER_STOP | I thought I was ready. | none | none | Scene 07 | Scene 07 - Binh reflects. |
| DLG_CH042_STOP_006 | char_mai | STATE_AFTER_STOP | Ready does not mean no pain. | none | none | Scene 07 | Scene 07 - Mai response. |
| DLG_CH042_STOP_007 | char_binh | STATE_AFTER_STOP | What if I stop for good? | none | none | Scene 07 | Scene 07 - Binh tests. |
| DLG_CH042_STOP_008 | char_trung | STATE_AFTER_STOP | Then you stop for good. | none | none | Scene 07 | Scene 07 - Trung affirms. |
| DLG_CH042_STOP_009 | char_binh | STATE_RECONSENT | I want to try again. But slower. | none | set_flag:FLAG_CH042_BINH_CONSENT_RECONFIRMED | Scene 07 | Scene 07 - Binh re-consents. |
| DLG_CH042_STOP_010 | char_mai | STATE_RECONSENT | Are you sure? | none | none | Scene 07 | Scene 07 - Mai checks. |
| DLG_CH042_STOP_011 | char_binh | STATE_RECONSENT | No. But I want to. And I know I can say red light. | none | none | Scene 07 | Scene 07 - Binh honest answer. |
| DLG_CH042_BATCH_001 | char_samir | STATE_BATCH_RESULT | It is better. | none | none | Scene 08 | Scene 08 - Samir result. |
| DLG_CH042_BATCH_002 | char_mai | STATE_BATCH_RESULT | What is the cost to Binh? | none | none | Scene 08 | Scene 08 - Mai asks cost. |
| DLG_CH042_BATCH_003 | npc_kareem | STATE_BATCH_RESULT | Mild fever. | none | none | Scene 08 | Scene 08 - Kareem reports. |
| DLG_CH042_BATCH_004 | char_trung | STATE_BATCH_RESULT | Done. | none | none | Scene 08 | Scene 08 - Trung ends. |
| DLG_CH042_BATCH_005 | char_samir | STATE_BATCH_RESULT | One more micro-test could... | none | none | Scene 08 | Scene 08 - Samir pushes. |
| DLG_CH042_BATCH_006 | char_mai | STATE_BATCH_RESULT | Done. | none | set_flag:FLAG_CH042_EXTRA_EXTRACTION_REFUSED;set_flag:FLAG_CH042_MINIMAL_DRAW_ONLY_CHILD_NOT_SOURCE | Scene 08 | Scene 08 - Mai refuses. |
| DLG_CH042_BATCH_007 | char_binh | STATE_BATCH_RESULT | Did I break it? | none | none | Scene 08 | Scene 08 - Binh fears failure. |
| DLG_CH042_BATCH_008 | char_mai | STATE_BATCH_RESULT | No. You did enough. | none | none | Scene 08 | Scene 08 - Mai reassures. |
| DLG_CH042_BATCH_009 | char_trung | STATE_BATCH_RESULT | Adults want many things. Not all of them are allowed. | none | none | Scene 08 | Scene 08 - Trung teaches. |
| DLG_CH042_HOANG_001 | comp_hoang | STATE_HOANG_CONFESSION | There was a second where I hoped his blood could save me. Not millions of people. Me. Then I hated myself for hoping. | none | none | Scene 09 | DT_269 - Hoang confession. |
| DLG_CH042_HOANG_002 | char_trung | STATE_HOANG_CONFESSION | If it were me, I would hope too. | none | none | Scene 09 | DT_269 - Trung admits. |
| DLG_CH042_HOANG_003 | comp_hoang | STATE_HOANG_CONFESSION | Then remember to kill that hope before it turns me into someone else. | none | set_flag:FLAG_CH042_HOANG_SELF_AWARENESS | Scene 09 | DT_269 - Hoang request. |
| DLG_CH042_BEACON_001 | char_samir | STATE_BEACON_DECRYPT | Aster Node. Orison archive. Child resonance chamber. | none | none | Scene 10 | DT_370 - Samir reveals. |
| DLG_CH042_BEACON_002 | char_mai | STATE_BEACON_DECRYPT | Children. | none | none | Scene 10 | DT_370 - Mai reacts. |
| DLG_CH042_BEACON_003 | char_trung | STATE_BEACON_DECRYPT | Not keys. Children. | none | none | Scene 10 | DT_370 - Trung corrects. |
| DLG_CH042_BEACON_004 | char_mai | STATE_BEACON_DECRYPT | Then we go there before they find more children. | none | set_flag:FLAG_CH042_FLOODED_AMAZON_ROUTE_CHOSEN | Scene 10 | DT_370 - Mai decision. |
| DLG_CH042_FAMILY_001 | char_trung | STATE_FAMILY_VOW | I am sorry for sometimes wanting to answer for you. | none | none | Scene 11 | Scene 11 - Trung apology. |
| DLG_CH042_FAMILY_002 | char_binh | STATE_FAMILY_VOW | Because you were scared. | none | none | Scene 11 | Scene 11 - Binh understands. |
| DLG_CH042_FAMILY_003 | char_mai | STATE_FAMILY_VOW | I am sorry for not noticing sooner that you were listening through the door. | none | none | Scene 11 | Scene 11 - Mai apology. |
| DLG_CH042_FAMILY_004 | char_binh | STATE_FAMILY_VOW | I still want to help. But I want to be allowed to be scared. | none | none | Scene 11 | DT_271 - Binh request. |
| DLG_CH042_FAMILY_005 | char_trung | STATE_FAMILY_VOW | New family rule. No one saves the world alone. | none | set_flag:FLAG_CH042_FAMILY_RULE_ESTABLISHED | Scene 11 | DT_271 - Trung family rule. |
| DLG_CH042_GREEN_001 | npc_scout | STATE_GREEN_WATER | The trees are moving behind us. | none | set_flag:FLAG_CH042_CHAPTER_043_FLOODED_AMAZON_UNLOCKED | Scene 12 | Scene 12 - Scout warning. |
| DLG_CH042_npc_yusuf_001 | npc_yusuf | STATE_BASE | We need to lock the lab. People are starting to ask questions about the boy's blood. | Choice 1: "We must protect him." : STATE_YUSUF_CHAT_PROTECT \| Choice 2: "What are they saying?" : STATE_YUSUF_CHAT_SAY | none | none | none |
| DLG_CH042_npc_yusuf_002 | npc_yusuf | STATE_YUSUF_CHAT_PROTECT | I will stand by the door. No one enters without my permission. | none | none | none | none |
| DLG_CH042_npc_yusuf_003 | npc_yusuf | STATE_YUSUF_CHAT_SAY | They think his blood holds the cure. Some believe we are keeping it for ourselves. | none | none | none | none |
| DLG_CH042_npc_amelie_001 | npc_amelie | STATE_BASE | Binh is very weak today. The blood draws are taking a toll on him. | Choice 1: "We need to stop the tests." : STATE_AMELIE_CHAT_STOP \| Choice 2: "Can we give him something for the pain?" : STATE_AMELIE_CHAT_PAIN | none | none | none |
| DLG_CH042_npc_amelie_002 | npc_amelie | STATE_AMELIE_CHAT_STOP | The doctor says we are close. But what is the cure worth if we kill the child to get it? | none | none | none | none |
| DLG_CH042_npc_amelie_003 | npc_amelie | STATE_AMELIE_CHAT_PAIN | We are out of sedatives. I can only hold his hand. | none | none | none | none |
| DLG_CH042_npc_thu_001 | npc_thu | STATE_BASE | The radio says the Alliance is collapsing from within. Trust is a rare commodity now. | Choice 1: "We must hold our ground." : STATE_THU_CHAT_GROUND \| Choice 2: "Are there any updates from the capital?" : STATE_THU_CHAT_CAPITAL | none | none | none |
| DLG_CH042_npc_thu_002 | npc_thu | STATE_THU_CHAT_GROUND | As long as we have fuel, the generators will keep the heating on. That's our only priority. | none | none | none | none |
| DLG_CH042_npc_thu_003 | npc_thu | STATE_THU_CHAT_CAPITAL | Silence. Nothing but static and automated messages. | none | none | none | none |

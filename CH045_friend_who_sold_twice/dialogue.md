# Dialogue - CH045

Metadata:

- chapterID: CH045
- sourceFilename: chapter_045_ke_ban_minh_hai_lan.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH045_DT294_001 | char_hoang | STATE_HOANG_GATE | I don't want to kill you. I want you to lose to prove I'm right. | none | none | hoang_gate | DT_294 - Hoang At Gate. |
| DLG_CH045_DT294_002 | char_trung | STATE_HOANG_GATE | Right about what? | none | none | hoang_gate | DT_294. |
| DLG_CH045_DT294_003 | char_hoang | STATE_HOANG_GATE | That some people cannot be saved by love. | none | none | hoang_gate | DT_294. |
| DLG_CH045_DT295_001 | char_hoang | STATE_BINH_DEMAND | Just one pulse. No blood. No needle. | none | none | binh_demand | DT_295 - Binh And The Demand. |
| DLG_CH045_DT295_002 | char_mai | STATE_BINH_DEMAND | Guilt is not consent. | none | set_flag:FLAG_CH045_RELIEF_NOT_CONSENT | binh_demand | DT_295. |
| DLG_CH045_DT295_003 | char_binh | STATE_BINH_DEMAND | I love you, uncle. I still say no. | none | set_flag:FLAG_CH045_BINH_BOUNDARY_SET | binh_demand | DT_295. |
| DLG_CH045_DT296_001 | npc_aster | STATE_ASTER_WAGER | Kill him and prove love is conditional. Free him and prove ethics cannot guard children. Bind him and prove you prefer suffering to clarity. | none | none | aster_wager | DT_296 - Aster's Wager. |
| DLG_CH045_DT296_002 | char_trung | STATE_ASTER_WAGER | Or we stay in the part your math cuts away. | none | none | aster_wager | DT_296. |
| DLG_CH045_DT297_001 | char_hoang | STATE_SMOKE_DEBT | I pulled you from smoke and fire. Then I pushed your child into different fire. Does that balance? | none | none | smoke_memory | DT_297 - Smoke Debt. |
| DLG_CH045_DT297_002 | char_trung | STATE_SMOKE_DEBT | No. It does not balance. But you are still a person in both times. | none | set_flag:FLAG_CH045_SMOKE_DEBT_ACKNOWLEDGED | smoke_memory | DT_297. |
| DLG_CH045_DT298_001 | char_mai | STATE_BETRAYAL_MEM | You were afraid. I understand. But you gave my child's coordinates. | none | none | betrayal_memory | DT_298 - Betrayal Memory. |
| DLG_CH045_DT298_002 | char_hoang | STATE_BETRAYAL_MEM | Yes. | none | none | betrayal_memory | DT_298. |
| DLG_CH045_DT298_003 | char_mai | STATE_BETRAYAL_MEM | Then don't ask us to call it something else. | none | set_flag:FLAG_CH045_COORDINATE_BETRAYAL_ACKNOWLEDGED | betrayal_memory | DT_298. |
| DLG_CH045_DT299_001 | char_binh | STATE_BINH_BOUNDARY | I don't hate you, uncle. | none | none | binh_boundary | DT_299 - Binh Boundary. |
| DLG_CH045_DT299_002 | char_hoang | STATE_BINH_BOUNDARY | Then help me. | none | none | binh_boundary | DT_299. |
| DLG_CH045_DT299_003 | char_binh | STATE_BINH_BOUNDARY | My saying no doesn't mean I stopped caring. | none | none | binh_boundary | DT_299. |
| DLG_CH045_DT300_001 | char_hoang | STATE_CMD_OVERLAY | Left! It will hit left! | none | none | command_overlay | DT_300 - Command Overlay. |
| DLG_CH045_DT300_002 | char_trung | STATE_CMD_OVERLAY | You're still in there. | none | none | command_overlay | DT_300. |
| DLG_CH045_DT300_003 | char_hoang | STATE_CMD_OVERLAY | Not enough to come back. | none | none | command_overlay | DT_300. |
| DLG_CH045_DT301_001 | npc_aster | STATE_FATE_CHOICE | One door. Mercy, safety, or truth. | none | none | fate_choice | DT_301 - Fate Choice. |
| DLG_CH045_DT301_002 | char_mai | STATE_FATE_CHOICE | No. Kill, spare, or do the hard thing. | none | none | fate_choice | DT_301. |
| DLG_CH045_DT301_003 | char_trung | STATE_FATE_CHOICE | We take the hard one. | none | set_flag:FLAG_CH045_HOANG_FATE_CHOSEN | fate_choice | DT_301. |
| DLG_CH045_DT302_001 | char_hoang | STATE_CAPTURE | You took the screaming back. | none | none | capture | DT_302 - Capture. |
| DLG_CH045_DT302_002 | char_trung | STATE_CAPTURE | I know. | none | none | capture | DT_302. |
| DLG_CH045_DT302_003 | char_hoang | STATE_CAPTURE | I will hate you. | none | none | capture | DT_302. |
| DLG_CH045_DT302_004 | char_trung | STATE_CAPTURE | Live first. Then hate. | none | set_flag:FLAG_CH045_HOANG_CAPTURED_ALIVE | capture | DT_302. |
| DLG_CH045_DT303_001 | char_amelie | STATE_CHILD_TRANSFER | The children are moving. | none | none | orison_transfer | DT_303 - Chapter 46 Hook. |
| DLG_CH045_DT303_002 | char_mai | STATE_CHILD_TRANSFER | How many? | none | none | orison_transfer | DT_303. |
| DLG_CH045_DT303_003 | char_samir | STATE_CHILD_TRANSFER | Too many. | none | none | orison_transfer | DT_303. |
| DLG_CH045_DT303_004 | char_mai | STATE_CHILD_TRANSFER | No child is material. | none | set_flag:FLAG_CH045_CH046_UNLOCKED | orison_transfer | DT_303. |
| DLG_CH045_DT304_001 | char_hoang | STATE_PAIN_RETURN | If I ask you to give armor back... don't listen. | none | none | locked_fate | Scene 12. |
| DLG_CH045_DT304_002 | char_trung | STATE_PAIN_RETURN | If you say it's for Binh... | none | none | locked_fate | Scene 12. |
| DLG_CH045_DT304_003 | char_hoang | STATE_PAIN_RETURN | Even less. | none | none | locked_fate | Scene 12. |
| DLG_CH045_DT304_004 | char_trung | STATE_PAIN_RETURN | Good. | none | none | locked_fate | Scene 12. |
| DLG_CH045_DT305_001 | char_binh | STATE_CH46_HOOK | I still want you to live. | none | none | capture_resolution | Scene 10. |
| DLG_CH045_DT305_002 | char_hoang | STATE_CH46_HOOK | Don't look at me like that. | none | none | capture_resolution | Scene 10. |
| DLG_CH045_DT305_003 | char_binh | STATE_CH46_HOOK | Like what? | none | none | capture_resolution | Scene 10. |
| DLG_CH045_DT305_004 | char_hoang | STATE_CH46_HOOK | Like I'm not finished. | none | none | capture_resolution | Scene 10. |
| DLG_CH045_DT305_005 | char_binh | STATE_CH46_HOOK | I don't know how much is left. But not finished. | none | none | capture_resolution | Scene 10. |
| DLG_CH045_char_hoang_001 | comp_hoang | STATE_BASE | They offered us a way out, Trung. A clean city, warm food, safety. All they wanted was the boy. | Choice 1: "You sold us out, Hoang." : STATE_HOANG_CHAT_BETRAYAL \| Choice 2: "Why didn't you tell me?" : STATE_HOANG_CHAT_WHY | none | none | none |
| DLG_CH045_char_hoang_002 | comp_hoang | STATE_HOANG_CHAT_BETRAYAL | I did what I had to do so we could survive. Look at us. We are freezing to death in this forest! | Choice 1: "There are some lines we don't cross." : STATE_HOANG_CHAT_BETRAYAL_LINE \| Choice 2: "It's too late now." : STATE_BASE | none | none | none |
| DLG_CH045_char_hoang_003 | comp_hoang | STATE_HOANG_CHAT_BETRAYAL_LINE | Lines don't keep you warm, Trung. | none | none | none | none |
| DLG_CH045_char_hoang_004 | comp_hoang | STATE_HOANG_CHAT_WHY | Because you would have said no. You always say no when it comes to the boy, even if it kills the rest of us. | none | none | none | none |

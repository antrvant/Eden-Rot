# Dialogue - CH034

Metadata:

- chapterID: CH034
- sourceFilename: chapter_034_ban_do_cua_ngay_tan_the.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH034_BINH_001 | comp_binh | STATE_HUNGRY_STARS | This map looks like the night sky. | none | none | map_review | DT_189. |
| DLG_CH034_THU_001 | npc_thu | STATE_HUNGRY_STARS | What sky has every point hungry for food, medicine, and someone to fix a machine? | none | none | map_review | DT_189. |
| DLG_CH034_BINH_002 | comp_binh | STATE_HUNGRY_STARS | Why does every star need us? | none | none | map_review | DT_189. |
| DLG_CH034_MAI_001 | comp_mai | STATE_HUNGRY_STARS | It is not needing us alone. They are saying: we are still here. | none | none | map_review | DT_189. |
| DLG_CH034_TRUNG_001 | char_trung | STATE_HUNGRY_STARS | And we have to answer with a real road. | none | set_flag:FLAG_CH034_FRONT_SELECTION_OPENED | map_review | DT_189. |
| DLG_CH034_GRAVES_001 | npc_graves_radio | STATE_ROUTE_COUNCIL | Secure North America first. A relay you cannot hold is a liability. | none | none | route_council | DT_190. |
| DLG_CH034_ADA_001 | npc_ada | STATE_ROUTE_COUNCIL | Refugees will not pause because Europe has a clue. | none | none | route_council | DT_190. |
| DLG_CH034_DOCTOR_001 | npc_doctor | STATE_ROUTE_COUNCIL | Patient Zero trail may decay or be destroyed. Without origin, cure becomes guesswork. | none | none | route_council | DT_190. |
| DLG_CH034_LIRA_001 | npc_lira | STATE_ROUTE_COUNCIL | Weather machines are waking. We can hold, but not forever. | none | none | route_council | DT_190. |
| DLG_CH034_MAI_002 | comp_mai | STATE_ROUTE_COUNCIL | No one here gets to use "forever" to force others into silence. | none | none | route_council | DT_190. |
| DLG_CH034_DOCTOR_002 | npc_doctor | STATE_CURE_HISTORY | Cure is not in one blood sample. It is in the history of the virus. | none | none | cure_analysis | DT_191. |
| DLG_CH034_TRUNG_002 | char_trung | STATE_CURE_HISTORY | Then why is Binh's name in the warning? | none | none | cure_analysis | DT_191. |
| DLG_CH034_DOCTOR_003 | npc_doctor | STATE_CURE_HISTORY | Because the boy's blood can prove part of the path. Not the answer. A dangerous mirror. | none | none | cure_analysis | DT_191. |
| DLG_CH034_MAI_003 | comp_mai | STATE_CURE_HISTORY | A mirror can also cut. So no one touches it while the dark is still here and he has not agreed. | none | set_flag:FLAG_CH034_CURE_ETHICS_ADDENDUM | cure_analysis | DT_191. |
| DLG_CH034_THU_002 | npc_thu | STATE_HOANG_PING | Three short, one long. With "not north." | none | none | hoang_ping | DT_192. |
| DLG_CH034_TRUNG_003 | char_trung | STATE_HOANG_PING | Could be a trap. | none | none | hoang_ping | DT_192. |
| DLG_CH034_PIKE_001 | npc_pike | STATE_HOANG_PING | Could be him avoiding one. | none | none | hoang_ping | DT_192. |
| DLG_CH034_MAI_004 | comp_mai | STATE_HOANG_PING | You want to go. | none | none | hoang_ping | DT_192. |
| DLG_CH034_TRUNG_004 | char_trung | STATE_HOANG_PING | I want to finish a story that is keeping me awake. | none | none | hoang_ping | DT_192. |
| DLG_CH034_MAI_005 | comp_mai | STATE_HOANG_PING | And hundreds of other stories are waiting for us to not be able to sleep. | none | set_flag:FLAG_CH034_HOANG_SEARCH_DEFERRED | hoang_ping | DT_192. |
| DLG_CH034_BINH_003 | comp_binh | STATE_CHOOSE_ABANDON | If we go to Europe, does Cairo think we abandoned them? | none | none | binh_reflection | DT_193. |
| DLG_CH034_TRUNG_005 | char_trung | STATE_CHOOSE_ABANDON | Maybe. So we have to say why we go, what we send before we go, and how we come back. | none | none | binh_reflection | DT_193. |
| DLG_CH034_MAI_006 | comp_mai | STATE_CHOOSE_ABANDON | Choosing a direction and writing down the names of the other directions is not abandoning. Abandoning is silence. | none | none | binh_reflection | DT_193. |
| DLG_CH034_BINH_004 | comp_binh | STATE_CHOOSE_ABANDON | Then we do not use silence. | none | none | binh_reflection | DT_193. |
| DLG_CH034_HAYES_001 | npc_hayes | STATE_SHARED_NODE | Someone must command NORAD. | none | none | shared_node | DT_194. |
| DLG_CH034_SLOANE_001 | npc_sloane | STATE_SHARED_NODE | Shared authority fails under attack. | none | none | shared_node | DT_194. |
| DLG_CH034_ADA_002 | npc_ada | STATE_SHARED_NODE | Single authority fails quietly before anyone can object. | none | none | shared_node | DT_194. |
| DLG_CH034_PIKE_002 | npc_pike | STATE_SHARED_NODE | Then build a thing noisy enough to complain before it breaks. | none | none | shared_node | DT_194. |
| DLG_CH034_THU_003 | npc_thu | STATE_SHARED_NODE | First time I agree with a soldier on system design. | none | set_flag:FLAG_CH034_NA_SHARED_NODE | shared_node | DT_194. |
| DLG_CH034_AMELIE_001 | npc_amelie | STATE_PARIS_INVITE | We still take attendance. We still have archive keys. We cannot hold the metro forever. | none | none | paris_invitation | DT_195. |
| DLG_CH034_MAI_007 | comp_mai | STATE_PARIS_INVITE | We cannot come right away. | none | none | paris_invitation | DT_195. |
| DLG_CH034_AMELIE_002 | npc_amelie | STATE_PARIS_INVITE | Then tell us you are choosing us second, not forgetting us first. | none | none | paris_invitation | DT_195. |
| DLG_CH034_TRUNG_006 | char_trung | STATE_PARIS_INVITE | Europe first. Paris first landing if route holds. | none | set_flag:FLAG_CH034_PARIS_ARCHIVE_INVITATION | paris_invitation | DT_195. |
| DLG_CH034_MAI_008 | comp_mai | STATE_NIGHT_WARNING | This line says "immune child derivative risk." | none | none | night_warning | DT_196. |
| DLG_CH034_TRUNG_007 | char_trung | STATE_NIGHT_WARNING | Turn it off. | none | none | night_warning | DT_196. |
| DLG_CH034_DOCTOR_004 | npc_doctor | STATE_NIGHT_WARNING | Turning off the screen does not delete the data. | none | none | night_warning | DT_196. |
| DLG_CH034_TRUNG_008 | char_trung | STATE_NIGHT_WARNING | I do not want to hear anyone talk about my child's blood like a protocol. | none | none | night_warning | DT_196. |
| DLG_CH034_MAI_009 | comp_mai | STATE_NIGHT_WARNING | Neither do I. So we must be the first to set the rules for this conversation, before others set them for us. | none | set_flag:FLAG_CH034_BINH_TRUTH_DEBT | night_warning | DT_196. |
| DLG_CH034_VALE_001 | npc_vale_core | STATE_EUROPE_UNLOCKED | Europe vector acknowledged. | none | none | europe_decision | DT_197. |
| DLG_CH034_THU_004 | npc_thu | STATE_EUROPE_UNLOCKED | It just called us a vector again? | none | none | europe_decision | DT_197. |
| DLG_CH034_BINH_005 | comp_binh | STATE_EUROPE_UNLOCKED | We do not answer when called by the wrong name. | none | none | europe_decision | DT_197. |
| DLG_CH034_TRUNG_009 | char_trung | STATE_EUROPE_UNLOCKED | Right. But we still go. | none | none | europe_decision | DT_197. |
| DLG_CH034_MAI_010 | comp_mai | STATE_EUROPE_UNLOCKED | Go with our own names. | none | set_flag:FLAG_CH034_EUROPE_ROUTE_UNLOCKED | europe_decision | DT_197. |
| DLG_CH034_npc_doctor_001 | npc_doctor | STATE_BASE | The virus behaves differently in freezing temperatures. It is slower, but more stable. | Choice 1: "What does that mean for the vaccine?" : STATE_DOCTOR_CHAT_VACCINE \| Choice 2: "How are the patients?" : STATE_DOCTOR_CHAT_PATIENTS | none | none | none |
| DLG_CH034_npc_doctor_002 | npc_doctor | STATE_DOCTOR_CHAT_VACCINE | It gives us more time to isolate the proteins. But we need clean laboratory gear. | none | none | none | none |
| DLG_CH034_npc_doctor_003 | npc_doctor | STATE_DOCTOR_CHAT_PATIENTS | Stable means they don't decay. They just wait. Under the ice. | none | none | none | none |
| DLG_CH034_npc_thu_001 | npc_thu | STATE_BASE | I mapped three military checkpoints on the way to NORAD. They are likely overrun. | Choice 1: "Can we bypass them?" : STATE_THU_CHAT_BYPASS \| Choice 2: "Are there any supplies left there?" : STATE_THU_CHAT_SUPPLIES | none | none | none |
| DLG_CH034_npc_thu_002 | npc_thu | STATE_THU_CHAT_BYPASS | The mountain pass is blocked by snow. The only way is through the checkpoints. | none | none | none | none |
| DLG_CH034_npc_thu_003 | npc_thu | STATE_THU_CHAT_SUPPLIES | Possibly heavy weapons, but also heavy infected presence. Not worth it unless we are desperate. | none | none | none | none |

# Dialogue - CH033

Metadata:

- chapterID: CH033
- sourceFilename: chapter_033_tin_hieu_toan_cau.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH033_THU_001 | npc_thu | STATE_FOUR_HOURS | Four hours to talk to the whole planet. No pressure. | none | none | chapter_start | DT_180. |
| DLG_CH033_DOCTOR_001 | npc_doctor | STATE_FOUR_HOURS | If we send the medical packet first, maybe some lab... | none | none | chapter_start | DT_180. |
| DLG_CH033_SLOANE_001 | npc_sloane | STATE_FOUR_HOURS | Command identification first. Survivors need hierarchy. | none | none | chapter_start | DT_180. |
| DLG_CH033_MAI_001 | comp_mai | STATE_FOUR_HOURS | People alive need to know they are not alone before someone orders them around. | none | none | chapter_start | DT_180. |
| DLG_CH033_TRUNG_001 | char_trung | STATE_FOUR_HOURS | One message. Do not let it become anyone's flag. | none | set_flag:FLAG_CH033_BROADCAST_COUNCIL_STARTED | chapter_start | DT_180. |
| DLG_CH033_GRAVES_001 | npc_graves_radio | STATE_WHO_SPEAKS | Include military authentication. | none | none | broadcast_council | DT_181. |
| DLG_CH033_ADA_001 | npc_ada | STATE_WHO_SPEAKS | Include civic process. | none | none | broadcast_council | DT_181. |
| DLG_CH033_REFUGEE_001 | npc_refugee_father | STATE_WHO_SPEAKS | Include where to go. | none | none | broadcast_council | DT_181. |
| DLG_CH033_DOCTOR_002 | npc_doctor | STATE_WHO_SPEAKS | Include what not to inject. | none | none | broadcast_council | DT_181. |
| DLG_CH033_BINH_001 | comp_binh | STATE_WHO_SPEAKS | Include asking names. | none | none | broadcast_council | DT_181. |
| DLG_CH033_MAI_002 | comp_mai | STATE_WHO_SPEAKS | Right. First, we ask who is alive and what their name is. | none | set_flag:FLAG_CH033_NAMES_FIRST | broadcast_council | DT_181. |
| DLG_CH033_BINH_002 | comp_binh | STATE_PROMISE_OR_LIE | If you say we are coming, but we do not arrive in time, is that a lie? | none | none | promise_draft | DT_182. |
| DLG_CH033_TRUNG_002 | char_trung | STATE_PROMISE_OR_LIE | If you say it to make them quiet and then abandon them, that is a lie. | none | none | promise_draft | DT_182. |
| DLG_CH033_MAI_003 | comp_mai | STATE_PROMISE_OR_LIE | If we say it so they know there is a direction, and we accept the debt, that is a promise. | none | none | promise_draft | DT_182. |
| DLG_CH033_BINH_003 | comp_binh | STATE_PROMISE_OR_LIE | Does a promise have debt? | none | none | promise_draft | DT_182. |
| DLG_CH033_TRUNG_003 | char_trung | STATE_PROMISE_OR_LIE | Yes. And I will not say it if I will not carry it. | none | set_flag:FLAG_CH033_PROMISE_DEBT_ACCEPTED | promise_draft | DT_182. |
| DLG_CH033_JUNE_001 | npc_june | STATE_CHILD_WARNING | Say don't give kids to people who call them chosen. | none | none | child_safety | DT_183. |
| DLG_CH033_NOAH_001 | npc_noah | STATE_CHILD_WARNING | Or seed. | none | none | child_safety | DT_183. |
| DLG_CH033_BINH_004 | comp_binh | STATE_CHILD_WARNING | Or vector. | none | none | child_safety | DT_183. |
| DLG_CH033_MOTHER_ELIAN_001 | npc_mother_elian | STATE_CHILD_WARNING | Or saved if they obey. | none | none | child_safety | DT_183. |
| DLG_CH033_MAI_004 | comp_mai | STATE_CHILD_WARNING | We will say: no one may use the blood, name, or absence of children to buy safety. | none | set_flag:FLAG_CH033_CHILD_SAFETY_WARNING | child_safety | DT_183. |
| DLG_CH033_PARIS_001 | npc_amelie | STATE_PARIS_SIGNAL | Ici Paris... school shelter... we hear fragments... repeat name? | none | set_flag:FLAG_CH033_PARIS_SIGNAL_CONFIRMED | world_response | DT_184. |
| DLG_CH033_THU_002 | npc_thu | STATE_PARIS_SIGNAL | Paris is alive. | none | none | world_response | DT_184. |
| DLG_CH033_MAI_005 | comp_mai | STATE_PARIS_SIGNAL | Ask if they have children first. | none | none | world_response | DT_184. |
| DLG_CH033_PARIS_002 | npc_amelie | STATE_PARIS_SIGNAL | Children present. We still take attendance. | none | none | world_response | DT_184. |
| DLG_CH033_BINH_005 | comp_binh | STATE_PARIS_SIGNAL | They take attendance. | none | none | world_response | DT_184. |
| DLG_CH033_VALE_001 | npc_vale_core | STATE_ARCHITECT_LISTENER | Non-local listener detected. | none | none | architect_listener | DT_185. |
| DLG_CH033_SLOANE_002 | npc_sloane | STATE_ARCHITECT_LISTENER | Shut it down. | none | none | architect_listener | DT_185. |
| DLG_CH033_THU_003 | npc_thu | STATE_ARCHITECT_LISTENER | Stripping metadata. Do not touch my cables. | none | none | architect_listener | DT_185. |
| DLG_CH033_TRUNG_004 | char_trung | STATE_ARCHITECT_LISTENER | If we shut down now, we become a light in the mountain again. | none | none | architect_listener | DT_185. |
| DLG_CH033_MAI_006 | comp_mai | STATE_ARCHITECT_LISTENER | Send it. But do not send the address of our home. | none | set_flag:FLAG_CH033_METADATA_STRIPPED | architect_listener | DT_185. |
| DLG_CH033_TRUNG_005 | char_trung | STATE_BROADCAST | If anyone is still alive, we are Rebirth. | none | none | broadcast | DT_186. |
| DLG_CH033_TRUNG_006 | char_trung | STATE_BROADCAST | We are not a new government. Not a new army. Not a new church. | none | none | broadcast | DT_186. |
| DLG_CH033_TRUNG_007 | char_trung | STATE_BROADCAST | We are people who were pulled through one night by someone else, and now we pull back. | none | none | broadcast | DT_186. |
| DLG_CH033_TRUNG_008 | char_trung | STATE_BROADCAST | If you can hear us, say your name. If you cannot wait, live one more night. | none | set_flag:FLAG_CH033_REBIRTH_SIGNAL_TRANSMITTED | broadcast | DT_186. |
| DLG_CH033_CAIRO_001 | npc_samir | STATE_WORLD_ANSWERS | Rebirth, Cairo hears. Clinic standing. Need antibiotics. Can trade route data. | none | set_flag:FLAG_CH033_CAIRO_SIGNAL_CONFIRMED | world_response | DT_187. |
| DLG_CH033_AMAZON_001 | npc_lira | STATE_WORLD_ANSWERS | Weather wrong. Trees flowering in dead season. Machines in clouds. | none | set_flag:FLAG_CH033_AMAZON_SIGNAL_CONFIRMED | world_response | DT_187. |
| DLG_CH033_ATLANTIC_001 | npc_moreno | STATE_WORLD_ANSWERS | Fleet fragment alive. No port. Send stars. | none | set_flag:FLAG_CH033_ATLANTIC_SIGNAL_CONFIRMED | world_response | DT_187. |
| DLG_CH033_PARIS_003 | npc_amelie | STATE_WORLD_ANSWERS | We hear Rebirth. Children counted. | none | none | world_response | DT_187. |
| DLG_CH033_BINH_006 | comp_binh | STATE_WORLD_ANSWERS | The world is not silent. | none | none | world_response | DT_187. |
| DLG_CH033_ARCHITECT_MSG_001 | npc_architect | STATE_TERRAFORM_MAP | Human coordination confirmed. | none | none | terraforming_map | DT_188. |
| DLG_CH033_ARCHITECT_MSG_002 | npc_architect | STATE_TERRAFORM_MAP | Redesign schedule accelerated. | none | none | terraforming_map | DT_188. |
| DLG_CH033_DOCTOR_003 | npc_doctor | STATE_TERRAFORM_MAP | Redesign? | none | none | terraforming_map | DT_188. |
| DLG_CH033_THU_004 | npc_thu | STATE_TERRAFORM_MAP | This is not a weather map. | none | none | terraforming_map | DT_188. |
| DLG_CH033_MAI_007 | comp_mai | STATE_TERRAFORM_MAP | This is someone's demolition schedule. | none | none | terraforming_map | DT_188. |
| DLG_CH033_TRUNG_009 | char_trung | STATE_TERRAFORM_MAP | Then in the next chapter, we choose where to fight first. | none | set_flag:FLAG_CH033_CH34_FRONT_DECISION_UNLOCKED | terraforming_map | DT_188. |
| DLG_CH033_npc_samir_001 | npc_samir | STATE_BASE | The transmitter is functioning, but the signal is heavily distorted. | Choice 1: "Can you trace the origin?" : STATE_SAMIR_CHAT_TRACE \| Choice 2: "Is it a human message?" : STATE_SAMIR_CHAT_HUMAN | none | none | none |
| DLG_CH033_npc_samir_002 | npc_samir | STATE_SAMIR_CHAT_TRACE | It's coming from NORAD coordinates. But we need a booster to get a clear audio signal. | none | none | none | none |
| DLG_CH033_npc_samir_003 | npc_samir | STATE_SAMIR_CHAT_HUMAN | It repeats every 14 minutes. It's a distress beacon, not a live voice. | none | none | none | none |
| DLG_CH033_npc_amelie_001 | npc_amelie | STATE_BASE | The temperature is dropping fast. The sea is starting to freeze near the shore. | Choice 1: "Are we prepared for winter?" : STATE_AMELIE_CHAT_WINTER \| Choice 2: "Have you seen any scouts?" : STATE_AMELIE_CHAT_SCOUTS | none | none | none |
| DLG_CH033_npc_amelie_002 | npc_amelie | STATE_AMELIE_CHAT_WINTER | No. Our fuel is low. If the harbor freezes, we'll be trapped here. | none | none | none | none |
| DLG_CH033_npc_amelie_003 | npc_amelie | STATE_AMELIE_CHAT_SCOUTS | Some tracks on the snow. But they looked animal, not human. Big ones. | none | none | none | none |

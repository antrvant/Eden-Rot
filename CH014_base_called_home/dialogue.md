# Dialogue - CH014

Metadata:

- chapterID: CH014
- sourceFilename: chapter_014_can_cu_mang_ten_nha.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH014_BINH_HIDE_001 | char_trung | STATE_BINH_HIDES | Binh, come out to Dad. | none | none | Binh under truck | DT_052. |
| DLG_CH014_MAI_STOP_001 | char_mai | STATE_BINH_HIDES | Don't pull him out. | none | none | Binh under truck | DT_052. |
| DLG_CH014_TRUNG_SAFETY_001 | char_trung | STATE_BINH_HIDES | It's not safe out here. | none | none | Binh under truck | DT_052. |
| DLG_CH014_MAI_CHOICE_001 | char_mai | STATE_BINH_HIDES | For him, in there is the place he chose himself. | none | none | Binh under truck | DT_052. |
| DLG_CH014_TRUNG_ASK_001 | char_trung | STATE_BINH_HIDES | What should I do? | none | none | Binh under truck | DT_052. |
| DLG_CH014_MAI_ADVICE_001 | char_mai | STATE_BINH_HIDES | Sit down. Let him see you are not standing over him. | none | none | Binh under truck | DT_052. |
| DLG_CH014_BINH_QUESTION_001 | char_binh | STATE_BINH_HIDES | Is that vehicle coming back? | none | none | Binh under truck | DT_052. |
| DLG_CH014_TRUNG_HONEST_001 | char_trung | STATE_BINH_HIDES | I don't know. | none | set_flag:FLAG_CH014_TRUNG_HONEST_WITH_BINH | Binh under truck | DT_052. |
| DLG_CH014_BINH_PUSH_001 | char_binh | STATE_BINH_HIDES | If you don't know, why did you tell me to come out? | none | none | Binh under truck | DT_052. |
| DLG_CH014_TRUNG_ADMIT_001 | char_trung | STATE_BINH_HIDES | I was wrong. Can I sit here with you for a while? | none | none | Binh under truck | DT_052. |
| DLG_CH014_TRUNG_FENCE_001 | char_trung | STATE_FENCE_DEBATE | We need the fence first. If it breaks, no one sleeps tonight. | none | none | school courtyard | DT_053. |
| DLG_CH014_MAI_SLEEP_001 | char_mai | STATE_FENCE_DEBATE | The children need sleep. And the wounded need to lie down. | none | none | school courtyard | DT_053. |
| DLG_CH014_TRUNG_FENCE_002 | char_trung | STATE_FENCE_DEBATE | If the infected get in, no one sleeps. | none | none | school courtyard | DT_053. |
| DLG_CH014_MAI_SLEEP_002 | char_mai | STATE_FENCE_DEBATE | If the children don't sleep, they won't live either. | none | none | school courtyard | DT_053. |
| DLG_CH014_HOANG_FENCE_001 | comp_hoang | STATE_FENCE_DEBATE | Walls first, feet after. Basic principle. | none | none | school courtyard | DT_053. |
| DLG_CH014_MAI_FACTORY_001 | char_mai | STATE_FENCE_DEBATE | The factory had walls too. | none | set_flag:FLAG_CH014_MAI_FACTORY_REFERENCE | school courtyard | DT_053. |
| DLG_CH014_TRUNG_HURT_001 | char_trung | STATE_FENCE_DEBATE | Are you saying I'm like them? | none | none | school courtyard | DT_053. |
| DLG_CH014_MAI_FEAR_001 | char_mai | STATE_FENCE_DEBATE | I'm saying you are scared enough that you are starting to sound like them. | none | none | school courtyard | DT_053. |
| DLG_CH014_TRUNG_SPLIT_001 | char_trung | STATE_FENCE_DEBATE | Two teams. Fence and classroom at the same time. | none | set_flag:FLAG_CH014_ROLES_ASSIGNED | school courtyard | DT_053. |
| DLG_CH014_WORKER_ACCUSE_001 | npc_worker_lead | STATE_KITCHEN_CONFLICT | He cooked for the people who held us. | none | none | school kitchen | DT_054. |
| DLG_CH014_ONG_TU_NIEU_ADMIT_001 | npc_ong_tu_nieu | STATE_KITCHEN_CONFLICT | Yes. | none | none | school kitchen | DT_054. |
| DLG_CH014_WORKER_PUSH_001 | npc_worker_lead | STATE_KITCHEN_CONFLICT | You have nothing to say for yourself? | none | none | school kitchen | DT_054. |
| DLG_CH014_ONG_TU_NIEU_QUIET_001 | npc_ong_tu_nieu | STATE_KITCHEN_CONFLICT | If defending myself could fill your stomach, I would. But it cannot. | none | none | school kitchen | DT_054. |
| DLG_CH014_MAI_CHILDREN_001 | char_mai | STATE_KITCHEN_CONFLICT | The children need hot food. | none | none | school kitchen | DT_054. |
| DLG_CH014_WORKER_ALT_001 | npc_worker_lead | STATE_KITCHEN_CONFLICT | Then let someone else cook. | none | none | school kitchen | DT_054. |
| DLG_CH014_ONG_TU_NIEU_EXPERT_001 | npc_ong_tu_nieu | STATE_KITCHEN_CONFLICT | Someone else will divide it wrong. Small children will go hungry. Those with fever will eat what they should not. | none | none | school kitchen | DT_054. |
| DLG_CH014_TRUNG_RULE_001 | char_trung | STATE_KITCHEN_CONFLICT | You cook. The food store gets two locks. One key with Worker Lead, one with Mai. | none | set_flag:FLAG_CH014_ONG_TU_NIEU_KITCHEN | school kitchen | DT_054. |
| DLG_CH014_WORKER_THREAT_001 | npc_worker_lead | STATE_KITCHEN_CONFLICT | And if he hides supplies for some faction? | none | none | school kitchen | DT_054. |
| DLG_CH014_TRUNG_PENALTY_001 | char_trung | STATE_KITCHEN_CONFLICT | Then he loses the kitchen. Not his life. We are not inventing new hell here. | none | none | school kitchen | DT_054. |
| DLG_CH014_MAI_RULES_001 | char_mai | STATE_CLASSROOM_RULES | Here are three rules. | none | none | classroom 3B | DT_055. |
| DLG_CH014_LAN_PUNISH_001 | npc_child_lan | STATE_CLASSROOM_RULES | What if I break one? | none | none | classroom 3B | DT_055. |
| DLG_CH014_MAI_FIX_001 | char_mai | STATE_CLASSROOM_RULES | Then we fix it. No numbering. | none | none | classroom 3B | DT_055. |
| DLG_CH014_LAN_NUMBER_001 | npc_child_lan | STATE_CLASSROOM_RULES | No numbering? | none | none | classroom 3B | DT_055. |
| DLG_CH014_MAI_NAMES_001 | char_mai | STATE_CLASSROOM_RULES | No. Everyone has a name. If you don't want to say it yet, you don't have to. But no one gets turned into a number. | none | set_flag:FLAG_CH014_MAI_CHILD_SAFE_ROOM | classroom 3B | DT_055. |
| DLG_CH014_BINH_CRY_001 | char_binh | STATE_CLASSROOM_RULES | What if I cry? | none | none | classroom 3B | DT_055. |
| DLG_CH014_MAI_CURTAIN_001 | char_mai | STATE_CLASSROOM_RULES | If you cry, we close the curtain. | none | none | classroom 3B | DT_055. |
| DLG_CH014_LAN_HURT_001 | npc_child_lan | STATE_CLASSROOM_RULES | What if it hurts? | none | none | classroom 3B | DT_055. |
| DLG_CH014_MAI_STAY_001 | char_mai | STATE_CLASSROOM_RULES | If you say it hurts, someone stays with you. No one gets taken to a separate room for saying they hurt. | none | none | classroom 3B | DT_055. |
| DLG_CH014_HOANG_MOUTH_001 | comp_hoang | STATE_ADMISSION_DEBATE | Every person who comes in is one less meal for Binh. | none | none | teachers' room | DT_056. |
| DLG_CH014_MAI_KNIFE_001 | char_mai | STATE_ADMISSION_DEBATE | Every person turned away is someone who might come back with a knife. | none | none | teachers' room | DT_056. |
| DLG_CH014_HOANG_OPEN_001 | comp_hoang | STATE_ADMISSION_DEBATE | So we open the gate to everyone? | none | none | teachers' room | DT_056. |
| DLG_CH014_TRUNG_RULES_001 | char_trung | STATE_ADMISSION_DEBATE | No. We set rules. | none | none | teachers' room | DT_056. |
| DLG_CH014_HOANG_RULES_001 | comp_hoang | STATE_ADMISSION_DEBATE | Rules don't fill the pot. | none | none | teachers' room | DT_056. |
| DLG_CH014_DOCTOR_RULES_001 | npc_doctor | STATE_ADMISSION_DEBATE | But they let people know we are not arbitrary. | none | none | teachers' room | DT_056. |
| DLG_CH014_HOANG_APOCALYPSE_001 | comp_hoang | STATE_ADMISSION_DEBATE | The apocalypse does not care about fairness. | none | none | teachers' room | DT_056. |
| DLG_CH014_TRUNG_HOME_001 | char_trung | STATE_ADMISSION_DEBATE | Maybe. But if we abandon fairness at the very first gate, what we build is not a home. | none | set_flag:FLAG_CH014_ADMISSION_RULES_DRAFTED | teachers' room | DT_056. |
| DLG_CH014_HOANG_PACKAGE_001 | comp_hoang | STATE_PACKAGE_FOUND | Fever medicine. Canned food. Batteries. Everything we need. | none | none | gate at night | DT_057. |
| DLG_CH014_MAI_READ_001 | char_mai | STATE_PACKAGE_FOUND | Read the whole letter. | none | none | gate at night | DT_057. |
| DLG_CH014_TRUNG_READ_001 | char_trung | STATE_PACKAGE_FOUND | "Hand over B-07. EDENROT CLASS: SILENT BLOOD / EDEN NODE." | none | none | gate at night | DT_057. |
| DLG_CH014_HOANG_FILE_001 | comp_hoang | STATE_PACKAGE_FOUND | They still use the factory file name for the boy. | none | none | gate at night | DT_057. |
| DLG_CH014_MAI_NOT_NAME_001 | char_mai | STATE_PACKAGE_FOUND | That is not my child's name. | none | none | gate at night | DT_057. |
| DLG_CH014_TRUNG_CONFIRM_001 | char_trung | STATE_PACKAGE_FOUND | No, it is not. | none | none | gate at night | DT_057. |
| DLG_CH014_HOANG_MOVE_001 | comp_hoang | STATE_PACKAGE_FOUND | I'm not saying we should hand him over. | none | none | gate at night | DT_057. |
| DLG_CH014_MAI_THOUGHT_001 | char_mai | STATE_PACKAGE_FOUND | But you were thinking it. | none | none | gate at night | DT_057. |
| DLG_CH014_HOANG_THINKING_001 | comp_hoang | STATE_PACKAGE_FOUND | I was thinking about everything it took to keep that boy alive. | none | none | gate at night | DT_057. |
| DLG_CH014_MAI_HANDING_001 | char_mai | STATE_PACKAGE_FOUND | Handing him over does not keep him alive. | none | none | gate at night | DT_057. |
| DLG_CH014_HOANG_KILL_001 | comp_hoang | STATE_PACKAGE_FOUND | Keeping him here could kill the whole base. | none | none | gate at night | DT_057. |
| DLG_CH014_TRUNG_PRICE_001 | char_trung | STATE_PACKAGE_FOUND | Then the question is not what Binh is worth. | none | none | gate at night | DT_057. |
| DLG_CH014_HOANG_WHAT_001 | comp_hoang | STATE_PACKAGE_FOUND | Then what? | none | none | gate at night | DT_057. |
| DLG_CH014_TRUNG_HOME_QUESTION_001 | char_trung | STATE_PACKAGE_FOUND | Can we build a home if on the first day we call a child by the name of those who want to buy him? | none | set_flag:FLAG_CH014_EDEN_NODE_TRADE_REJECTED | gate at night | DT_057. |
| DLG_CH014_MAI_LAST_001 | char_mai | STATE_PACKAGE_FOUND | Today we just named this place home. Now let's see if we dare keep that name. | none | none | gate at night | DT_057. |
| DLG_CH014_TRUNG_PIN_001 | char_trung | STATE_PACKAGE_DECISION | Pin it on the council room board. Let everyone know the price they are offering. | none | set_flag:FLAG_CH014_EDENROT_EVIDENCE_BOARD | gate at night | Scene 9. |
| DLG_CH014_HOANG_PIN_001 | comp_hoang | STATE_PACKAGE_DECISION | You want to tell the whole base? | none | none | gate at night | Scene 9. |
| DLG_CH014_TRUNG_NO_SECRET_001 | char_trung | STATE_PACKAGE_DECISION | If we hide it, the day they find out, they will think we decided for them. A home does not start with a secret deal to sell a child. | none | none | gate at night | Scene 9. |
| DLG_CH014_char_binh_001 | char_binh | STATE_BASE | Dad, it's nice to have a home now, even if it's just this school. | Choice 1: "How is your new room?" : STATE_BINH_CHAT_ROOM \| Choice 2: "Are you hungry?" : STATE_BINH_CHAT_FOOD | none | none | none |
| DLG_CH014_char_binh_002 | char_binh | STATE_BINH_CHAT_ROOM | It's big! But the blackboard has some scary drawings from before. I tried to erase them. | Choice 1: "Good job. What did you draw instead?" : STATE_BINH_CHAT_ROOM_DRAW \| Choice 2: "Don't look at them. Go back." : STATE_BASE | none | none | none |
| DLG_CH014_char_binh_003 | char_binh | STATE_BINH_CHAT_ROOM_DRAW | I drew a huge tree with blue leaves! Like the one in mom's books. | none | none | none | none |
| DLG_CH014_char_binh_004 | char_binh | STATE_BINH_CHAT_FOOD | A bit. The soup uncle Cook made smells good, but some people were arguing in the kitchen. | none | none | none | none |
| DLG_CH014_char_mai_001 | char_mai | STATE_BASE | We managed to secure the school, but the fence is weak and food won't last more than a week. | Choice 1: "How are you holding up?" : STATE_MAI_CHAT_HEALTH \| Choice 2: "What's our next priority?" : STATE_MAI_CHAT_PRIORITY | none | none | none |
| DLG_CH014_char_mai_002 | char_mai | STATE_MAI_CHAT_HEALTH | I'm fine, but I'm worried about the children. They've seen too much. Binh is trying to look brave, but he woke up screaming twice last night. | Choice 1: "We will protect him. Together." : STATE_MAI_CHAT_HEALTH_PROM \| Choice 2: "We need to be stronger." : STATE_BASE | none | none | none |
| DLG_CH014_char_mai_003 | char_mai | STATE_MAI_CHAT_HEALTH_PROM | I know. I just wish we didn't have to build our home behind a fence. | none | none | none | none |
| DLG_CH014_char_mai_004 | char_mai | STATE_MAI_CHAT_PRIORITY | We need to reinforce the gate. Hoang wants to search the nearby pharmacy, but it's risky. | none | none | none | none |
| DLG_CH014_char_hoang_001 | comp_hoang | STATE_BASE | This place is a tactical nightmare. Too many entry points. We need ammo, and we need it yesterday. | Choice 1: "What do you suggest?" : STATE_HOANG_CHAT_SUGGEST \| Choice 2: "Do you trust the others?" : STATE_HOANG_CHAT_TRUST | none | none | none |
| DLG_CH014_char_hoang_002 | comp_hoang | STATE_HOANG_CHAT_SUGGEST | There is a police patrol car abandoned three blocks north. Might have some shells in the trunk. I'll go if you cover me. | Choice 1: "We go together." : STATE_HOANG_CHAT_SUGGEST_GO \| Choice 2: "Too dangerous for now." : STATE_BASE | none | none | none |
| DLG_CH014_char_hoang_003 | comp_hoang | STATE_HOANG_CHAT_SUGGEST_GO | Good. Meet me at the gate when you're ready. | none | none | none | none |
| DLG_CH014_char_hoang_004 | comp_hoang | STATE_HOANG_CHAT_TRUST | I trust people who can hold a gun and shoot straight. The rest are just mouth-breathers eating our food. | none | none | none | none |

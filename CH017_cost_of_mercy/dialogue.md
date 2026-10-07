# Dialogue - CH017

Metadata:

- chapterID: CH017
- sourceFilename: chapter_017_cai_gia_cua_long_thuong.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH017_RADIO_SIGNAL_001 | npc_hanh | STATE_DISTRESS_SIGNAL | That route is near the refugee path. The yellow jackets and bandits watch it. | none | none | Radio received | DT_070. |
| DLG_CH017_HOANG_BAIT_001 | comp_hoang | STATE_DISTRESS_SIGNAL | It could be bait. | none | none | Radio received | DT_070. |
| DLG_CH017_MAI_CHILDREN_001 | char_mai | STATE_DISTRESS_SIGNAL | And if it is bait with real children, then what? | none | none | Radio received | DT_070. |
| DLG_CH017_HOANG_BAIT_002 | comp_hoang | STATE_DISTRESS_SIGNAL | Then it is a better bait. | none | none | Radio received | DT_070. |
| DLG_CH017_BINH_TRIGGER_001 | char_binh | STATE_DISTRESS_SIGNAL | Does not remember the name. | none | set_flag:FLAG_CH017_BINH_TRIGGERED | Binh hears radio | Scene 1. |
| DLG_CH017_COUNCIL_DOCTOR_001 | npc_doctor | STATE_COUNCIL_VOTE | I can bring two bandage packs, some alcohol, three painkillers, one antibiotic dose. If I use them, the lab stops for at least two days. | none | none | Teachers' room | DT_070. |
| DLG_CH017_COUNCIL_HOANG_001 | comp_hoang | STATE_COUNCIL_VOTE | Lab for what if the base dies before the cure exists? | none | none | Teachers' room | DT_070. |
| DLG_CH017_COUNCIL_WORKER_001 | npc_worker_lead | STATE_COUNCIL_VOTE | If four people go, the back fence does not get finished today. If we bring refugees back, work increases, but they eat before they can work. | none | none | Teachers' room | DT_070. |
| DLG_CH017_COUNCIL_DOCTOR_002 | npc_doctor | STATE_COUNCIL_VOTE | If they crossed near Edenrot, we need serious quarantine. Serious does not mean treating them like contaminated cargo. | none | none | Teachers' room | DT_070. |
| DLG_CH017_COUNCIL_HOANG_002 | comp_hoang | STATE_COUNCIL_VOTE | Recon. Two people. No rescue commitment until we know what is there. | none | none | Teachers' room | DT_070. |
| DLG_CH017_MAI_RECON_001 | char_mai | STATE_COUNCIL_VOTE | And if we get there and find children dying? | none | none | Teachers' room | DT_070. |
| DLG_CH017_HOANG_RECON_002 | comp_hoang | STATE_COUNCIL_VOTE | Then we decide there. | none | none | Teachers' room | DT_070. |
| DLG_CH017_MAI_RECON_002 | char_mai | STATE_COUNCIL_VOTE | With who? | none | none | Teachers' room | DT_070. |
| DLG_CH017_HOANG_RECON_003 | comp_hoang | STATE_COUNCIL_VOTE | With the people who are there and take the bullets. | none | none | Teachers' room | DT_070. |
| DLG_CH017_TRUNG_LIMITED_001 | char_trung | STATE_COUNCIL_VOTE | Limited rescue. Small team. Children and movable wounded first. Bandit and EDEN intel second. No promise to bring everyone home if the base cannot hold them. | none | set_flag:FLAG_CH017_LIMITED_RESCUE_APPROVED | Teachers' room | DT_070. |
| DLG_CH017_HOANG_LINE_001 | comp_hoang | STATE_COUNCIL_VOTE | Goodness that needs votes and conditions should at least not call itself beautiful. | none | set_flag:FLAG_CH017_HOANG_DISSENT_RESCUE | Teachers' room | DT_070. |
| DLG_CH017_TRUNG_LINE_001 | char_trung | STATE_COUNCIL_VOTE | Beauty is not the goal. Living without becoming monsters is the goal. | none | none | Teachers' room | DT_070. |
| DLG_CH017_BA_SAU_MEET_001 | npc_ba_sau | STATE_CONVOY_ARRIVAL | Where are you from? | none | none | Bridge site | DT_071. |
| DLG_CH017_TRUNG_MEET_001 | char_trung | STATE_CONVOY_ARRIVAL | From a place not safe enough to brag about. | none | none | Bridge site | DT_071. |
| DLG_CH017_BA_SAU_MEET_002 | npc_ba_sau | STATE_CONVOY_ARRIVAL | Then why come? | none | none | Bridge site | DT_071. |
| DLG_CH017_TRUNG_MEET_002 | char_trung | STATE_CONVOY_ARRIVAL | Because the signal said there are children. | none | none | Bridge site | DT_071. |
| DLG_CH017_BA_SAU_MEET_003 | npc_ba_sau | STATE_CONVOY_ARRIVAL | Children are always there. Adults only listen when they still have enough strength to be good. | none | none | Bridge site | DT_071. |
| DLG_CH017_HOANG_TIME_001 | comp_hoang | STATE_CONVOY_ARRIVAL | We do not have much time. | none | none | Bridge site | DT_071. |
| DLG_CH017_BA_SAU_TIME_001 | npc_ba_sau | STATE_CONVOY_ARRIVAL | I do not have many people to lose either. | none | none | Bridge site | DT_071. |
| DLG_CH017_MAI_NAME_001 | char_mai | STATE_NAMELESS_CHILD | What is your name? | none | none | Under bus | DT_072. |
| DLG_CH017_SO4_NAME_001 | npc_so4 | STATE_NAMELESS_CHILD | Number 4. | none | none | Under bus | DT_072. |
| DLG_CH017_MAI_NAME_002 | char_mai | STATE_NAMELESS_CHILD | That is how adults count. It is not a name if you do not want it to be. | none | none | Under bus | DT_072. |
| DLG_CH017_SO4_NAME_002 | npc_so4 | STATE_NAMELESS_CHILD | If you have a name, they call you. | none | none | Under bus | DT_072. |
| DLG_CH017_MAI_NAME_003 | char_mai | STATE_NAMELESS_CHILD | Where I am, having a name also means you can say "I am not ready to come out yet." | none | none | Under bus | DT_072. |
| DLG_CH017_SO4_NAME_003 | npc_so4 | STATE_NAMELESS_CHILD | What if I forget the name? | none | none | Under bus | DT_072. |
| DLG_CH017_MAI_NAME_004 | char_mai | STATE_NAMELESS_CHILD | Then we keep an empty space on the blackboard until you remember, or until you choose a new name. | none | none | Under bus | DT_072. |
| DLG_CH017_HOANG_BRIDGE_001 | comp_hoang | STATE_BRIDGE_DECISION | Cut the bridge. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_TRUNG_BRIDGE_001 | char_trung | STATE_BRIDGE_DECISION | There are still children on the other side. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_HOANG_BRIDGE_002 | comp_hoang | STATE_BRIDGE_DECISION | And thirty people on this side. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_MAI_BRIDGE_001 | char_mai | STATE_BRIDGE_DECISION | Give me two minutes. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_HOANG_BRIDGE_003 | comp_hoang | STATE_BRIDGE_DECISION | Two minutes is the price of someone dead or alive. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_TRUNG_BRIDGE_002 | char_trung | STATE_BRIDGE_DECISION | I hold the bridge with you. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_HOANG_BRIDGE_004 | comp_hoang | STATE_BRIDGE_DECISION | I do not need a hero. I need a stop order. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_TRUNG_BRIDGE_003 | char_trung | STATE_BRIDGE_DECISION | The stop order is to hold a little longer. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_HOANG_BRIDGE_005 | comp_hoang | STATE_BRIDGE_DECISION | A little longer becomes a grave. | none | none | Bridge during retreat | DT_073. |
| DLG_CH017_BINH_PORRIDGE_001 | char_binh | STATE_RATION_SCENE | Today the porridge is less. | none | none | Base evening | DT_074. |
| DLG_CH017_TRUNG_PORRIDGE_001 | char_trung | STATE_RATION_SCENE | Mm. | none | none | Base evening | DT_074. |
| DLG_CH017_BINH_PORRIDGE_002 | char_binh | STATE_RATION_SCENE | Because of the new people? | none | none | Base evening | DT_074. |
| DLG_CH017_TRUNG_PORRIDGE_002 | char_trung | STATE_RATION_SCENE | Because today there are more people who need to live. | none | none | Base evening | DT_074. |
| DLG_CH017_BINH_PORRIDGE_003 | char_binh | STATE_RATION_SCENE | What if tomorrow there are more? | none | none | Base evening | DT_074. |
| DLG_CH017_TRUNG_PORRIDGE_003 | char_trung | STATE_RATION_SCENE | Then we have to find more. And it might still be less. | none | none | Base evening | DT_074. |
| DLG_CH017_BINH_SHARE_001 | char_binh | STATE_RATION_SCENE | Can I share half my bowl? | none | none | Base evening | DT_074. |
| DLG_CH017_MAI_SHARE_001 | char_mai | STATE_RATION_SCENE | You can, if you want. But you do not have to pay for the mercy of adults. | none | none | Base evening | DT_074. |
| DLG_CH017_BINH_SHARE_002 | char_binh | STATE_RATION_SCENE | I just do not want that kid to be hungry. | none | none | Base evening | DT_074. |
| DLG_CH017_MAI_SHARE_002 | char_mai | STATE_RATION_SCENE | Then you are sharing as Binh, not as a debt. | none | none | Base evening | DT_074. |
| DLG_CH017_HOANG_CORE_001 | comp_hoang | STATE_SUPPLY_AFTERMATH | The well is not stable, the fence lacks sheet metal, the generator is almost out of fuel, the lab lacks alcohol. | none | none | Base evening | DT_075. |
| DLG_CH017_TRUNG_CORE_001 | char_trung | STATE_SUPPLY_AFTERMATH | I know. | none | none | Base evening | DT_075. |
| DLG_CH017_HOANG_CORE_002 | comp_hoang | STATE_SUPPLY_AFTERMATH | No. You feel. I am counting. | none | none | Base evening | DT_075. |
| DLG_CH017_TRUNG_CORE_002 | char_trung | STATE_SUPPLY_AFTERMATH | But people out there will die. | none | none | Base evening | DT_075. |
| DLG_CH017_HOANG_CORE_003 | comp_hoang | STATE_SUPPLY_AFTERMATH | A few will still die. | none | none | Base evening | DT_075. |
| DLG_CH017_TRUNG_CORE_003 | char_trung | STATE_SUPPLY_AFTERMATH | But not all of them. | none | none | Base evening | DT_075. |
| DLG_CH017_HOANG_CORE_004 | comp_hoang | STATE_SUPPLY_AFTERMATH | Save everyone, Trung. Then tonight give your child mercy to drink. | none | none | Base evening | DT_075. |
| DLG_CH017_TRUNG_CORE_004 | char_trung | STATE_SUPPLY_AFTERMATH | You think I do not know Binh's bowl is smaller? | none | none | Base evening | DT_075. |
| DLG_CH017_HOANG_CORE_005 | comp_hoang | STATE_SUPPLY_AFTERMATH | I think you know and still choose. That is what scares me. | none | set_flag:FLAG_CH017_HOANG_SUPPLY_RESENTMENT | Base evening | DT_075. |
| DLG_CH017_THEFT_HOANG_001 | comp_hoang | STATE_SUPPLY_THEFT | I said it. Bring too many people in, this is the result. | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_MAI_001 | char_mai | STATE_SUPPLY_THEFT | It could be someone old. | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_HOANG_002 | comp_hoang | STATE_SUPPLY_THEFT | Great. So we were already broken before. Even better. | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_HANH_001 | npc_hanh | STATE_SUPPLY_THEFT | Checkpoint. The bandits use this mark to point to fuel drop sites. | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_MAI_002 | char_mai | STATE_SUPPLY_THEFT | If we investigate with fear, the base will break. | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_HOANG_003 | comp_hoang | STATE_SUPPLY_THEFT | If we investigate with trust, the base gets robbed clean. | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_TRUNG_001 | char_trung | STATE_SUPPLY_THEFT | Lock the gate. No one in or out until morning. Hoang, make a list of everyone who knows the supply room. Worker Lead, check the mud traces against the quarantine area. Mai, keep the children calm. No one gets convicted without evidence. | none | set_flag:FLAG_CH017_SUPPLY_THEFT_TRIGGERED | Supply room night | Scene 8. |
| DLG_CH017_THEFT_HOANG_004 | comp_hoang | STATE_SUPPLY_THEFT | And if the evidence points to one of the people you just saved? | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_TRUNG_002 | char_trung | STATE_SUPPLY_THEFT | Then that person still gets heard before being judged. | none | none | Supply room night | Scene 8. |
| DLG_CH017_THEFT_HOANG_005 | comp_hoang | STATE_SUPPLY_THEFT | That line will look good on a tombstone. | none | set_flag:FLAG_CH017_BANDIT_CHECKPOINT_LEAD | Supply room night | Scene 8. |
| DLG_CH017_npc_ba_sau_001 | npc_ba_sau | STATE_BASE | The rations are getting smaller. Some of the young ones are talking about leaving. | Choice 1: "We must stay together." : STATE_BASAU_CHAT_STAY \| Choice 2: "I will find more supplies." : STATE_BASAU_CHAT_SUPPLIES | none | none | none |
| DLG_CH017_npc_ba_sau_002 | npc_ba_sau | STATE_BASAU_CHAT_STAY | Easy to say when you have a gun. People are hungry, Trung. | none | none | none | none |
| DLG_CH017_npc_ba_sau_003 | npc_ba_sau | STATE_BASAU_CHAT_SUPPLIES | Be careful. The city belongs to the dead now. | none | none | none | none |
| DLG_CH017_npc_so4_001 | npc_so4 | STATE_BASE | Just tell me who to shoot. I don't care about the council votes. | Choice 1: "We need order, not violence." : STATE_SO4_CHAT_ORDER \| Choice 2: "Keep your weapon ready." : STATE_SO4_CHAT_READY | none | none | none |
| DLG_CH017_npc_so4_002 | npc_so4 | STATE_SO4_CHAT_ORDER | Order is what we had before the walls fell. Now, it's just steel and blood. | none | none | none | none |
| DLG_CH017_npc_so4_003 | npc_so4 | STATE_SO4_CHAT_READY | Locked and loaded. Nobody gets past my post. | none | none | none | none |
| DLG_CH017_npc_lan_001 | npc_lan | STATE_BASE | I found a flower growing in the concrete near the courtyard. Can I keep it? | Choice 1: "Of course. Take care of it." : STATE_LAN_CHAT_FLOWER \| Choice 2: "We have more important things to worry about." : STATE_BASE | none | none | none |
| DLG_CH017_npc_lan_002 | npc_lan | STATE_LAN_CHAT_FLOWER | I will water it every day. It's yellow, like the sun. | none | none | none | none |

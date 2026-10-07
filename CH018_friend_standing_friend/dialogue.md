# Dialogue - CH018

Metadata:

- chapterID: CH018
- sourceFilename: chapter_018_ban_than_ban_dung.md
- language: English

## Required Dialogue

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH018_SCENE1_001 | char_worker_lead | STATE_THEFT_INVESTIGATION | If we say the refugees did it, the base breaks. | none | none | supply_storage_inspection | Scene 1 - Worker Lead warns against false accusation. |
| DLG_CH018_SCENE1_002 | char_hoang | STATE_THEFT_INVESTIGATION | If we pretend nobody did it, the base gets eaten clean. | none | none | supply_storage_inspection | Scene 1 - Hoang pushes for action. |
| DLG_CH018_SCENE1_003 | char_worker_lead | STATE_THEFT_INVESTIGATION | I am not saying ignore it. I am saying evidence first. | none | none | supply_storage_inspection | Scene 1 - Worker Lead demands evidence. |
| DLG_CH018_SCENE1_004 | char_hoang | STATE_THEFT_INVESTIGATION | The evidence is on the floor. | none | none | supply_storage_inspection | Scene 1 - Hoang points at mud. |
| DLG_CH018_SCENE1_005 | char_worker_lead | STATE_THEFT_INVESTIGATION | The evidence says bandit marker. It does not say who carried it in. | none | none | supply_storage_inspection | Scene 1 - Worker Lead logic. |
| DLG_CH018_SCENE1_006 | char_trung | STATE_HOANG_QUESTION | Where were you last night at six? | none | none | hoang_present_at_storage | Scene 1 - Trung questions Hoang. |
| DLG_CH018_SCENE1_007 | char_hoang | STATE_HOANG_ANSWER | Guarding the back gate. | none | none | hoang_question_asked | Scene 1 - Hoang answers too quickly. |
| DLG_CH018_SCENE1_008 | char_trung | STATE_HOANG_QUESTION | The back gate is Tuan's. | none | none | hoang_answer_given | Scene 1 - Trung catches inconsistency. |
| DLG_CH018_SCENE1_009 | char_hoang | STATE_HOANG_ANSWER | I swapped shifts because he was falling asleep. | none | none | trung_catches_inconsistency | Scene 1 - Hoang covers. |
| DLG_CH018_SCENE1_010 | char_trung | STATE_HOANG_QUESTION | Who logged it? | none | none | hoang_shift_claim | Scene 1 - Trung presses. |
| DLG_CH018_SCENE1_011 | char_hoang | STATE_HOANG_DEFLECT | Now guarding needs paperwork? | none | none | trung_presses | Scene 1 - Hoang deflects. |
| DLG_CH018_SCENE1_012 | char_trung | STATE_HOANG_WARNING | Now everything needs to be logged. | none | none | hoang_deflects | Scene 1 - Trung sets the rule. |
| DLG_CH018_SCENE1_013 | char_binh | STATE_BINH_WHISPER | I heard Uncle Hoang walking past the classroom very late. | none | set_flag:FLAG_CH018_BINH_HOANG_CLUE | binh_with_mai_private | Scene 1 - Binh tells Mai. |
| DLG_CH018_SCENE2_001 | char_hoang | STATE_HOANG_RATIONALIZE | One can of gas. Two pills. A generator that still runs. | none | none | hoang_leaving_base | DT_076 - Hoang rationalizes. |
| DLG_CH018_SCENE2_002 | char_hoang | STATE_HOANG_RATIONALIZE | Nobody dies from the coordinates of a side road. | none | none | hoang_walking | DT_076 - Hoang rationalizes. |
| DLG_CH018_SCENE2_003 | char_hoang | STATE_HOANG_RATIONALIZE | Nobody dies from knowing a base has children. Everyone has children. | none | none | hoang_walking | DT_076 - Hoang rationalizes. |
| DLG_CH018_SCENE2_004 | char_hoang | STATE_HOANG_RATIONALIZE | Trung will say no. The council will say wait. When the generator dies, they will all look at me. | none | none | hoang_walking | DT_076 - Hoang rationalizes. |
| DLG_CH018_SCENE2_005 | char_hoang | STATE_HOANG_RATIONALIZE | So I go first. | none | none | hoang_arrives_checkpoint | DT_076 - Hoang decides. |
| DLG_CH018_SCENE3_001 | npc_bandit_trader | STATE_TRADE_OPEN | Information has value. The question is whether you know what you are selling. | none | none | trade_begins | DT_077 - Bandit Trader opens. |
| DLG_CH018_SCENE3_002 | char_hoang | STATE_TRADE_OFFER | Refugee route. Old guard gap. Fuel needs. No names. No children. | none | none | trade_offer | DT_077 - Hoang offers. |
| DLG_CH018_SCENE3_003 | npc_bandit_trader | STATE_TRADE_COUNTER | Names are the last thing you need to know. | none | none | hoang_offers | DT_077 - Trader responds. |
| DLG_CH018_SCENE3_004 | char_hoang | STATE_TRADE_CONDITION | Nobody touches the children. | none | none | trader_mentions_children | DT_077 - Hoang sets condition. |
| DLG_CH018_SCENE3_005 | npc_bandit_trader | STATE_TRADE_COUNTER | You are making demands with the person who has gas? | none | none | hoang_sets_condition | DT_077 - Trader challenges. |
| DLG_CH018_SCENE3_006 | char_hoang | STATE_TRADE_THREAT | I am making demands with the person who wants to live until the next trade. | none | none | trader_challenges | DT_077 - Hoang counters. |
| DLG_CH018_SCENE3_007 | npc_bandit_trader | STATE_TRADE_LAUGH | Good. I like customers who think they still hold the knife. | none | none | hoang_counters | DT_077 - Trader laughs. |
| DLG_CH018_SCENE3_008 | npc_bandit_trader | STATE_TRADE_QUESTION | Is there anyone there who walked through Edenrot? | none | none | trade_continues | Scene 3 - Trader asks about Edenrot. |
| DLG_CH018_SCENE3_009 | npc_bandit_trader | STATE_TRADE_JUSTIFY | I am asking because children make noise. If we want to keep trading, I do not want my people walking past a classroom. | none | none | hoang_reacts_to_question | Scene 3 - Trader justifies question. |
| DLG_CH018_SCENE3_010 | npc_bandit_trader | STATE_TRADE_HINT | If you want more, next time bring proof of a child who does not fever. Or a child who walked through Edenrot and still breathes. | none | none | trade_ends | Scene 3 - Trader sets future price. |
| DLG_CH018_SCENE3_011 | npc_bandit_trader | STATE_TRADE_WARNING | You sold coordinates. Do not go home and comfort yourself by calling it a road. | none | none | hoang_leaves | Scene 3 - Trader's parting shot. |
| DLG_CH018_SCENE4_001 | char_mai | STATE_BINH_REPORT | Binh heard Hoang walk past the classroom last night. | none | none | mai_tells_trung | Scene 4 - Mai reports Binh's clue. |
| DLG_CH018_SCENE4_002 | char_mai | STATE_BINH_REPORT | I am not saying he did it. I am saying something does not fit. | none | none | mai_reports | Scene 4 - Mai clarifies. |
| DLG_CH018_SCENE4_003 | char_trung | STATE_INVESTIGATE | Where did you get the gas? | none | none | hoang_returns_with_fuel | DT_078 - Trung confronts. |
| DLG_CH018_SCENE4_004 | char_hoang | STATE_HOANG_LIE | Found it. | none | none | trung_asks_fuel | DT_078 - Hoang lies. |
| DLG_CH018_SCENE4_005 | char_trung | STATE_INVESTIGATE | Gas with checkpoint seals that you "found"? | none | none | hoang_claims_found | DT_078 - Trung catches lie. |
| DLG_CH018_SCENE4_006 | char_hoang | STATE_HOANG_ADMIT | I traded. | none | none | trung_catches_lie | DT_078 - Hoang admits trade. |
| DLG_CH018_SCENE4_007 | char_trung | STATE_INVESTIGATE | Traded for what? | none | none | hoang_admits_trade | DT_078 - Trung presses. |
| DLG_CH018_SCENE4_008 | char_hoang | STATE_HOANG_DEFEND | Harmless information. | none | none | trung_asks_what | DT_078 - Hoang defends. |
| DLG_CH018_SCENE5_001 | char_trung | STATE_CONFRONTATION | What did you give them? | none | none | confrontation_begins | DT_078 - Trung demands details. |
| DLG_CH018_SCENE5_002 | char_hoang | STATE_CONFRONTATION_DEFEND | Refugee route. Fuel needs. One old guard gap. | none | none | trung_demands | DT_078 - Hoang lists. |
| DLG_CH018_SCENE5_003 | char_trung | STATE_CONFRONTATION | Which gate? | none | none | hoang_lists_info | DT_078 - Trung presses. |
| DLG_CH018_SCENE5_004 | char_hoang | STATE_CONFRONTATION_DEFEND | The back gate. | none | none | trung_asks_gate | DT_078 - Hoang answers. |
| DLG_CH018_SCENE5_005 | char_hoang | STATE_CONFRONTATION_DEFEND | I said we were weak after convoy. I said we needed fuel. I said... | none | none | hoang_continues | DT_078 - Hoang trails off. |
| DLG_CH018_SCENE5_006 | char_mai | STATE_CONFRONTATION | You said there is a classroom. | none | none | hoang_trails_off | DT_078 - Mai finishes. |
| DLG_CH018_SCENE5_007 | char_hoang | STATE_CONFRONTATION_DEFEND | I said there are children. Not which classroom. | none | none | mai_finishes | DT_078 - Hoang splits hairs. |
| DLG_CH018_SCENE5_008 | char_mai | STATE_CONFRONTATION | But you just said the back gate. | none | none | hoang_splits_hairs | DT_078 - Mai catches the link. |
| DLG_CH018_SCENE5_009 | char_trung | STATE_CONFRONTATION | You gave them the road into my home. | none | none | mai_catches_link | DT_078 - Trung says the wound. |
| DLG_CH018_SCENE5_010 | char_hoang | STATE_CONFRONTATION_DEFEND | I gave them the road into a base that is dying because you will not count. | none | none | trung_says_wound | DT_078 - Hoang retaliates. |
| DLG_CH018_SCENE5_011 | char_hoang | STATE_BETRAYAL_LINE | I sold coordinates, not a soul. | none | none | confrontation_climax | DT_079 - Core betrayal line. |
| DLG_CH018_SCENE5_012 | char_trung | STATE_CONFRONTATION | You think those two things can be separated? | none | none | hoang_core_line | DT_079 - Trung challenges. |
| DLG_CH018_SCENE5_013 | char_hoang | STATE_BETRAYAL_LINE | A soul is worth less than gas. | none | none | trung_challenges | DT_079 - Hoang's coldest line. |
| DLG_CH018_SCENE5_014 | char_mai | STATE_CONFRONTATION | No. A soul is the reason gas is not bought with children. | none | none | hoang_coldest_line | DT_079 - Mai corrects. |
| DLG_CH018_SCENE5_015 | char_hoang | STATE_CONFRONTATION_DEFEND | Say that when the generator dies and the boy fevers again. | none | none | mai_corrects | DT_079 - Hoang uses Binh. |
| DLG_CH018_SCENE5_016 | char_trung | STATE_CONFRONTATION | Do not bring Binh into this. | none | none | hoang_uses_binh | DT_079 - Trung warns. |
| DLG_CH018_SCENE5_017 | char_hoang | STATE_CONFRONTATION_DEFEND | I am bringing in the truth. You rescued convoy, lost fuel. You built lab, need fuel. You keep Binh, need fences. Everything you call morality needs what you refuse to take. | none | none | trung_warns | DT_079 - Hoang's argument. |
| DLG_CH018_SCENE5_018 | char_trung | STATE_CONFRONTATION | Taking by selling the road to children's classroom? | none | none | hoang_argument | DT_079 - Trung exposes. |
| DLG_CH018_SCENE5_019 | char_hoang | STATE_CONFRONTATION_ADMIT | I did not know they would go there! | none | none | trung_exposes | DT_079 - Hoang's accidental truth. |
| DLG_CH018_SCENE5_020 | char_worker_lead | STATE_CONFRONTATION | Conditions with someone who buys information with gas are not locks. | none | none | hoang_accidental_truth | DT_079 - Worker Lead corrects. |
| DLG_CH018_SCENE6_001 | char_hoang | STATE_RAID_REALIZE | The classroom. | none | none | raid_begins | Scene 6 - Hoang understands first. |
| DLG_CH018_SCENE6_002 | char_mai | STATE_CHILDREN_EVAC | Push, push. Second route. | none | none | mai_enters_classroom | Scene 6 - Mai evacuates children. |
| DLG_CH018_SCENE6_003 | char_mai | STATE_CHILDREN_EVAC | Binh. The tool cabinet. With So 4. Remember to count to ten. | none | none | mai_assigns_binh | Scene 6 - Mai hides Binh. |
| DLG_CH018_SCENE6_004 | char_binh | STATE_CHILDREN_EVAC | Mom? | none | none | mai_assigns | Scene 6 - Binh asks. |
| DLG_CH018_SCENE6_005 | char_mai | STATE_CHILDREN_LIE | Mom will come after you. | none | none | binh_asks | Scene 6 - Mai's half-truth. |
| DLG_CH018_SCENE6_006 | npc_bandit_lieutenant | STATE_RAID_THREAT | Trade the woman for the child or gas. Choose which one, husband. | none | none | mai_captured | Scene 6 - Lieutenant's ultimatum. |
| DLG_CH018_SCENE6_007 | char_hoang | STATE_RAID_FIGHT | Let her go. | none | none | lieutenant_ultimatum | Scene 6 - Hoang demands release. |
| DLG_CH018_SCENE6_008 | npc_bandit_lieutenant | STATE_RAID_RECOGNIZE | Ah. The customer. | none | none | hoang_demands | Scene 6 - Lieutenant recognizes Hoang. |
| DLG_CH018_SCENE7_001 | npc_bandit_lieutenant | STATE_RAID_MESSAGE | Trade the woman for the child or fuel. | none | none | raid_ends | Scene 7 - Bandit withdrawal message. |
| DLG_CH018_SCENE7_002 | char_hoang | STATE_POST_RAID | I did not know they would take Mai. | none | none | post_raid_begins | Scene 7 - Hoang's defense. |
| DLG_CH018_SCENE7_003 | char_trung | STATE_POST_RAID | But you knew they were the kind of people who would use what you gave. | none | none | hoang_defends | Scene 7 - Trung's response. |
| DLG_CH018_SCENE7_004 | char_binh | STATE_BINH_QUESTION | Did Uncle Hoang sell Mom? | none | set_flag:FLAG_CH018_BINH_TRUST_SHAKEN | post_raid_silence | DT_080 - Binh asks. |
| DLG_CH018_SCENE7_005 | char_trung | STATE_BINH_ANSWER | Dad is looking for words that will not hurt you more but are still true. | none | none | binh_asks | DT_080 - Trung tries. |
| DLG_CH018_SCENE7_006 | char_binh | STATE_BINH_QUESTION | Are there such words? | none | none | trung_tries | DT_080 - Binh presses. |
| DLG_CH018_SCENE7_007 | char_trung | STATE_BINH_ANSWER | Dad has not found them yet. | none | none | binh_presses | DT_080 - Trung admits. |
| DLG_CH018_SCENE7_008 | char_hoang | STATE_POST_RAID | Binh, I did not- | none | none | trung_admits | DT_080 - Hoang tries. |
| DLG_CH018_SCENE7_009 | char_trung | STATE_POST_RAID | Stop. | none | none | hoang_tries | DT_080 - Trung stops Hoang. |
| DLG_CH018_SCENE7_010 | char_binh | STATE_BINH_QUESTION | Did you lie? | none | none | trung_stops | DT_080 - Binh asks Hoang. |
| DLG_CH018_SCENE7_011 | char_hoang | STATE_POST_RAID | Yes. | none | none | binh_asks_lie | DT_080 - Hoang admits. |
| DLG_CH018_SCENE7_012 | char_binh | STATE_BINH_QUESTION | Then which part was true? | none | none | hoang_admits_lie | DT_080 - Binh asks. |
| DLG_CH018_SCENE7_013 | char_hoang | STATE_POST_RAID | I wanted to save our home. | none | none | binh_asks_what_true | DT_080 - Hoang answers. |
| DLG_CH018_SCENE7_014 | char_binh | STATE_BINH_REPLY | But Mom is not at home anymore. | none | none | hoang_answers | DT_080 - Binh's devastating reply. |
| DLG_CH018_SCENE7_015 | char_hoang | STATE_POST_RAID | I will go with you. | none | none | trung_prepares_rescue | Scene 7 - Hoang offers. |
| DLG_CH018_SCENE7_016 | char_trung | STATE_POST_RAID | I do not know if I can let you walk behind me. | none | none | hoang_offers | Scene 7 - Trung's trust wound. |
| DLG_CH018_SCENE7_017 | char_hoang | STATE_POST_RAID | Then let me walk in front. | none | none | trung_refuses | Scene 7 - Hoang's offer. |
| DLG_CH018_SCENE7_018 | char_trung | STATE_POST_RAID | We are going to get Mai. Your story comes after. | none | none | chapter_ends | Scene 7 - Trung delays judgment. |
| DLG_CH018_npc_bandit_trader_001 | npc_bandit_trader | STATE_BASE | I sell, you buy. Simple. No politics, no questions. | Choice 1: "What do you have today?" : STATE_TRADER_CHAT_SELL \| Choice 2: "Where do you get your goods?" : STATE_TRADER_CHAT_SOURCE | none | none | none |
| DLG_CH018_npc_bandit_trader_002 | npc_bandit_trader | STATE_TRADER_CHAT_SELL | Just some scraps and old food. Take it or leave it. | none | none | none | none |
| DLG_CH018_npc_bandit_trader_003 | npc_bandit_trader | STATE_TRADER_CHAT_SOURCE | Let's just say some people don't need their things anymore. | none | none | none | none |
| DLG_CH018_npc_bandit_lieutenant_001 | npc_bandit_lieutenant | STATE_BASE | Keep your hands where I can see them, stranger. | Choice 1: "Just looking around." : STATE_BASE \| Choice 2: "Who's in charge here?" : STATE_LIEUT_CHAT_BOSS | none | none | none |
| DLG_CH018_npc_bandit_lieutenant_002 | npc_bandit_lieutenant | STATE_LIEUT_CHAT_BOSS | The boss doesn't like visitors. Don't make me ask you to leave. | none | none | none | none |

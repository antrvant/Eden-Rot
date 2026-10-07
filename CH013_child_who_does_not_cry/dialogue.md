# Dialogue - CH013

Metadata:

- chapterID: CH013
- sourceFilename: chapter_013_dua_tre_khong_khoc.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH013_MAI_MARK_001 | char_mai | STATE_FACTORY_PERIMETER | Look. That mark on the pole. A circle with a line through it. Binh drew that when he was angry at adults. It means the sun being told to be quiet. | none | set_flag:FLAG_CH013_BINH_MARK_FOUND | perimeter_scout | Scene 1. |
| DLG_CH013_TRUNG_HEAR_001 | char_trung | STATE_FACTORY_PERIMETER | I hear children. | none | none | children_singing | Scene 1. |
| DLG_CH013_MAI_HOLD_001 | char_mai | STATE_FACTORY_PERIMETER | If you go in like a terrified father, they will use your son to break you. | none | set_flag:FLAG_CH013_MAI_LEADS_APPROACH | trung_wants_to_rush | DT_046. |
| DLG_CH013_MAI_HOLD_002 | char_mai | STATE_FACTORY_PERIMETER | Hold my hand. I will hold it until you find him. | none | none | trung_wants_to_rush | DT_046. |
| DLG_CH013_ONG_001 | npc_ong_tu_nieu | STATE_CAFETERIA_INTRO | I am not stealing. I just... saved a spoonful. The porridge is so thin the children vomit. | none | none | group_finds_ong | DT_047. |
| DLG_CH013_HOANG_ONG_001 | comp_hoang | STATE_CAFETERIA_INTRO | Hidden rice in your coat and you call it saving a spoonful? | none | none | rice_discovered | DT_047. |
| DLG_CH013_MAI_ONG_001 | char_mai | STATE_CAFETERIA_INTRO | Who is that rice for? | none | none | rice_discovered | DT_047. |
| DLG_CH013_ONG_002 | npc_ong_tu_nieu | STATE_CAFETERIA_INTRO | The little ones. | none | set_flag:FLAG_CH013_ONG_SOFT_DIALOGUE | rice_for_children | DT_047. |
| DLG_CH013_TRUNG_BINH_001 | char_trung | STATE_CAFETERIA_INTRO | Is there a child named Binh? | none | none | asks_about_binh | DT_047. |
| DLG_CH013_ONG_003 | npc_ong_tu_nieu | STATE_CAFETERIA_INTRO | Here they do not call children by name. | none | none | asks_about_binh | DT_047. |
| DLG_CH013_TRUNG_BINH_002 | char_trung | STATE_CAFETERIA_INTRO | But you do. | none | none | ong_knows_name | DT_047. |
| DLG_CH013_ONG_004 | npc_ong_tu_nieu | STATE_CAFETERIA_INTRO | The one who does not cry. | none | set_flag:FLAG_CH013_BINH_IDENTITY_CONFIRMED | ong_reveals_binh | DT_047. |
| DLG_CH013_MAI_BINH_001 | char_mai | STATE_CAFETERIA_INTRO | Is he alive? | none | none | ong_reveals_binh | DT_047. |
| DLG_CH013_ONG_005 | npc_ong_tu_nieu | STATE_CAFETERIA_INTRO | Alive. But do not ask me if he is still himself. That question I have no right to answer. | none | none | ong_reveals_binh | DT_047. |
| DLG_CH013_WORKER_WARN_001 | npc_worker_lead | STATE_WORKER_FLOOR | If the alarm sounds, the children's room locks and they release the infected from cold storage. | none | set_flag:FLAG_CH013_WORKER_WARNING_RECEIVED | worker_floor_crossed | Scene 3. |
| DLG_CH013_MAI_DRAWING_001 | char_mai | STATE_WORKER_FLOOR | This is a person with a limp. Binh is mapping the guard route. | none | set_flag:FLAG_CH013_BINH_DRAWINGS_FOUND | sees_drawing | Scene 3. |
| DLG_CH013_BINH_REUNION_001 | char_binh | STATE_MEDICAL_ROOM | Are you really my father? | none | set_flag:FLAG_CH013_BINH_FOUND | family_enters_medical | DT_048, Scene 6. |
| DLG_CH013_TRUNG_REUNION_001 | char_trung | STATE_MEDICAL_ROOM | I am here. | none | none | binh_asks_father | DT_048. |
| DLG_CH013_BINH_REUNION_002 | char_binh | STATE_MEDICAL_ROOM | Someone else said that too. | none | none | binh_asks_father | DT_048. |
| DLG_CH013_TRUNG_REUNION_002 | char_trung | STATE_MEDICAL_ROOM | I know. | none | none | binh_says_others_lied | DT_048. |
| DLG_CH013_BINH_REUNION_003 | char_binh | STATE_MEDICAL_ROOM | They said if I was good, my parents would come. | none | none | binh_says_others_lied | DT_048. |
| DLG_CH013_MAI_REUNION_001 | char_mai | STATE_MEDICAL_ROOM | Mom came late. I am sorry. | none | none | mai_apologizes | DT_048. |
| DLG_CH013_BINH_REUNION_004 | char_binh | STATE_MEDICAL_ROOM | Did you lie? | none | none | mai_apologizes | DT_048. |
| DLG_CH013_MAI_REUNION_002 | char_mai | STATE_MEDICAL_ROOM | Yes. I once said you would always be safe if you had me. I wanted that to be true. But I could not make it happen. | none | set_flag:FLAG_CH013_MAI_HONEST_WITH_BINH | binh_asks_lie | DT_048. |
| DLG_CH013_TRUNG_REUNION_003 | char_trung | STATE_MEDICAL_ROOM | We promise you will not have to be afraid alone anymore. | none | set_flag:FLAG_CH013_FAMILY_PROMISE | after_mai_honest | DT_048. |
| DLG_CH013_BINH_EXPOSURE_001 | char_binh | STATE_MEDICAL_ROOM | A sick person scratched me. | none | set_flag:FLAG_CH013_BINH_EXPOSURE_FLAG | binh_reveals_scratch | Scene 6. |
| DLG_CH013_BINH_EXPOSURE_002 | char_binh | STATE_MEDICAL_ROOM | The man in the white coat said I do not have a fever. Then he told the guards to watch me carefully. | none | none | binh_reveals_scratch | Scene 6. |
| DLG_CH013_FACTORY_BOSS_001 | npc_factory_boss | STATE_BOSS_CONFRONTATION | That child is no longer only yours. | none | none | boss_appears | DT_049, Scene 7. |
| DLG_CH013_MAI_BOSS_001 | char_mai | STATE_BOSS_CONFRONTATION | He was never yours. | none | none | boss_claims_binh | DT_049. |
| DLG_CH013_FACTORY_BOSS_002 | npc_factory_boss | STATE_BOSS_CONFRONTATION | Out there people call it Edenrot because they only see the rot. I see an unmanaged garden. | none | none | boss_justifies | DT_049. |
| DLG_CH013_FACTORY_BOSS_003 | npc_factory_boss | STATE_BOSS_CONFRONTATION | If his blood could save thousands? | none | none | boss_justifies | DT_049. |
| DLG_CH013_TRUNG_BOSS_001 | char_trung | STATE_BOSS_CONFRONTATION | Then you will ask his permission when he is old enough to understand. | none | none | boss_asks_what_if | DT_049. |
| DLG_CH013_FACTORY_BOSS_004 | npc_factory_boss | STATE_BOSS_CONFRONTATION | The world is dying and you still talk about permission. | none | none | boss_dismisses | DT_049. |
| DLG_CH013_MAI_BOSS_002 | char_mai | STATE_BOSS_CONFRONTATION | No. The world died because people thought rules only mattered when there were enough young people left to follow them. | none | none | boss_dismisses | DT_049. |
| DLG_CH013_FACTORY_BOSS_005 | npc_factory_boss | STATE_BOSS_CONFRONTATION | I will release the other children. Leave him. | Choice A: Refuse.; Choice B: Consider the trade.; Choice C: Let Mai decide. | open_choice | boss_offers_trade | DT_049. |
| DLG_CH013_TRUNG_BOSS_002 | char_trung | STATE_BOSS_CONFRONTATION | You use children to bargain with parents, and you call that saving the world? | none | set_flag:FLAG_CH013_REFUSED_TRADE | choice:DLG_CH013_FACTORY_BOSS_005:A | DT_049. |
| DLG_CH013_HOANG_BOSS_001 | comp_hoang | STATE_BOSS_CONFRONTATION | Everyone says that before they make someone else pay the price. | none | none | boss_justifies | DT_049. |
| DLG_CH013_BINH_COUNT_001 | char_binh | STATE_COLD_STORAGE | Count to ten. | none | set_flag:FLAG_CH013_BINH_COUNTING_COPING | spitter_appears | Scene 8. |
| DLG_CH013_BINH_COUNT_002 | char_binh | STATE_COLD_STORAGE | One. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_003 | char_binh | STATE_COLD_STORAGE | Two. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_004 | char_binh | STATE_COLD_STORAGE | Three. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_005 | char_binh | STATE_COLD_STORAGE | Four. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_006 | char_binh | STATE_COLD_STORAGE | Five. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_007 | char_binh | STATE_COLD_STORAGE | Six. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_008 | char_binh | STATE_COLD_STORAGE | Seven. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_009 | char_binh | STATE_COLD_STORAGE | Eight. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_010 | char_binh | STATE_COLD_STORAGE | Nine. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_COUNT_011 | char_binh | STATE_COLD_STORAGE | Ten. | none | none | counting | Scene 8. |
| DLG_CH013_BINH_LAN_001 | char_binh | STATE_LOADING_YARD | Lan is in there. | none | set_flag:FLAG_CH013_BINH_IDENTIFIES_LAN | hears_locked_children | Scene 9. |
| DLG_CH013_TRUNG_CHOICE_001 | char_trung | STATE_LOADING_YARD | Hoang. Take my son out the gate. | none | set_flag:FLAG_CH013_TRUNG_GOES_BACK | decides_to_rescue_locked | Scene 9. |
| DLG_CH013_HOANG_CHOICE_001 | comp_hoang | STATE_LOADING_YARD | Trung. | none | none | trung_asks_hoang | Scene 9. |
| DLG_CH013_TRUNG_CHOICE_002 | char_trung | STATE_LOADING_YARD | Please. | none | none | trung_says_please | Scene 9. |
| DLG_CH013_BINH_HOANG_001 | char_binh | STATE_LOADING_YARD | Do you lie? | none | none | binh_to_hoang | Scene 9. |
| DLG_CH013_HOANG_CHOICE_002 | comp_hoang | STATE_LOADING_YARD | Sometimes. Not right now. | none | set_flag:FLAG_CH013_HOANG_PROMISE | binh_asks_hoang | Scene 9. |
| DLG_CH013_MAI_PAIN_001 | char_mai | STATE_OUTSIDE_FENCE | Does it hurt? | none | none | mai_checks_wound | DT_051. |
| DLG_CH013_BINH_PAIN_001 | char_binh | STATE_OUTSIDE_FENCE | No. | none | none | mai_asks_pain | DT_051. |
| DLG_CH013_MAI_PAIN_002 | char_mai | STATE_OUTSIDE_FENCE | Binh. | none | none | binh_says_no | DT_051. |
| DLG_CH013_BINH_PAIN_002 | char_binh | STATE_OUTSIDE_FENCE | I am not allowed to say it hurts. | none | set_flag:FLAG_CH013_BINH_PAIN_SUPPRESSED | mai_presses | DT_051. |
| DLG_CH013_MAI_PAIN_003 | char_mai | STATE_OUTSIDE_FENCE | Who said that? | none | none | binh_not_allowed | DT_051. |
| DLG_CH013_BINH_PAIN_003 | char_binh | STATE_OUTSIDE_FENCE | If I say it hurts, they take me to a separate room. | none | none | mai_asks_who | DT_051. |
| DLG_CH013_TRUNG_PAIN_001 | char_trung | STATE_OUTSIDE_FENCE | Here you are allowed to speak. | none | none | binh_separate_room | DT_051. |
| DLG_CH013_BINH_PAIN_004 | char_binh | STATE_OUTSIDE_FENCE | If I say it, will you take me away? | none | none | trung_allows | DT_051. |
| DLG_CH013_TRUNG_PAIN_002 | char_trung | STATE_OUTSIDE_FENCE | No. | none | none | binh_asks_taken_away | DT_051. |
| DLG_CH013_MAI_PAIN_004 | char_mai | STATE_OUTSIDE_FENCE | If you say it, I will sit with you longer. | none | none | binh_asks_taken_away | DT_051. |
| DLG_CH013_BINH_PAIN_005 | char_binh | STATE_OUTSIDE_FENCE | Then... ask me if it hurts. | none | set_flag:FLAG_CH013_BINH_FIRST_TRUST | mai_sits_longer | DT_051. |
| DLG_CH013_HOANG_END_001 | comp_hoang | STATE_OUTSIDE_FENCE | Do not. | none | none | trung_thanks_hoang | DT_050. |
| DLG_CH013_TRUNG_END_001 | char_trung | STATE_OUTSIDE_FENCE | Hoang- | none | none | trung_thanks_hoang | DT_050. |
| DLG_CH013_HOANG_END_002 | comp_hoang | STATE_OUTSIDE_FENCE | I said don't. | none | none | trung_tries_again | DT_050. |
| DLG_CH013_TRUNG_END_002 | char_trung | STATE_OUTSIDE_FENCE | Without you... | none | none | trung_tries_again | DT_050. |
| DLG_CH013_HOANG_END_003 | comp_hoang | STATE_OUTSIDE_FENCE | You would still have charged in. The difference is you would have died sooner. | none | none | trung_without_you | DT_050. |
| DLG_CH013_TRUNG_END_003 | char_trung | STATE_OUTSIDE_FENCE | I do not know how to repay you. | none | none | hoang_died_sooner | DT_050. |
| DLG_CH013_HOANG_END_004 | comp_hoang | STATE_OUTSIDE_FENCE | Live. Do not make that boy ask that question again. | none | set_flag:FLAG_CH013_HOANG_OUTSIDE_FAMILY_SEED | trung_repays | DT_050. |
| DLG_CH013_TRUNG_END_004 | char_trung | STATE_OUTSIDE_FENCE | What question? | none | none | hoang_live | DT_050. |
| DLG_CH013_HOANG_END_005 | comp_hoang | STATE_OUTSIDE_FENCE | Are you really my father? | none | none | trung_what_question | DT_050. |
| DLG_CH013_ONG_NOTE_001 | npc_ong_tu_nieu | STATE_OUTSIDE_FENCE | I took this from his desk. I do not know if it is important. | none | set_flag:FLAG_CH013_SILENT_BLOOD_LORE;grant_item:ITM_CH013_EDEN_NODE_NOTE | ong_delivers_note | Scene 10. |
| DLG_CH013_HOANG_LORE_001 | comp_hoang | STATE_OUTSIDE_FENCE | Out there they call it Edenrot. They call your son a node. | none | none | note_read | Scene 10. |
| DLG_CH013_MAI_LORE_001 | char_mai | STATE_OUTSIDE_FENCE | One side sees rot. The other side sees a sample. | none | none | hoang_says_node | Scene 10. |
| DLG_CH013_TRUNG_LORE_001 | char_trung | STATE_OUTSIDE_FENCE | Our son is not anyone's name for him. | none | set_flag:FLAG_CH013_FAMILY_REJECTS_LABELS | mai_rot_sample | Scene 10. |
| DLG_CH013_TRUNG_END_005 | char_trung | STATE_OUTSIDE_FENCE | Then we build a place. | none | none | chapter_ending | Scene 10. |
| DLG_CH013_MAI_END_001 | char_mai | STATE_OUTSIDE_FENCE | Where? | none | none | trung_builds | Scene 10. |
| DLG_CH013_TRUNG_END_006 | char_trung | STATE_OUTSIDE_FENCE | A place where when a child says it hurts, no one takes them to a separate room. | none | set_flag:FLAG_CH013_BASE_BUILDING_MOTIVATION | mai_where | Scene 10. |
| DLG_CH013_FACTORY_BOSS_END_001 | npc_factory_boss | STATE_LOADING_YARD | You are killing hope! | none | none | group_escapes | Scene 7. |

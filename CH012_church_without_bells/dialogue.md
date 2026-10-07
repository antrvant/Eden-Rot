# Dialogue - CH012

Metadata:

- chapterID: CH012
- sourceFilename: chapter_012_nha_tho_khong_chuong.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH012_HOANG_ROUTE_001 | comp_hoang | STATE_ROUTE_DECISION | Shortest path goes straight through that block. | none | none | retreat_route | Scene 1. |
| DLG_CH012_TRUNG_ROUTE_001 | char_trung | STATE_ROUTE_DECISION | We go around. | none | none | retreat_route | Scene 1. |
| DLG_CH012_HOANG_ROUTE_002 | comp_hoang | STATE_ROUTE_DECISION | That costs twenty more minutes. | none | none | retreat_route | Scene 1. |
| DLG_CH012_TRUNG_ROUTE_002 | char_trung | STATE_ROUTE_DECISION | Better than losing everyone. | none | set_flag:FLAG_CH012_ROUTE_CHOSEN | retreat_route | Scene 1. |
| DLG_CH012_HOANG_ORDER_001 | comp_hoang | STATE_ROUTE_DECISION | You just gave orders like the old Mentor. | none | none | retreat_route | Scene 1. |
| DLG_CH012_TRUNG_ORDER_001 | char_trung | STATE_ROUTE_DECISION | Don't say that. | none | set_flag:FLAG_CH012_MENTOR_WOUND_TOUCHED | retreat_route | Scene 1. |
| DLG_CH012_PRIEST_GATE_001 | npc_priest | STATE_CHURCH_GATE | If you are looking for family, why do you carry more guns than medicine? | Choice A: "Because outside here, medicine does not stop zombies."; Choice B: "We have wounded and children."; Choice C: Let Hoang speak.; Choice D: "What is Edenrot street?" | open_choice | church_arrival | DT_042. |
| DLG_CH012_PRIEST_GATE_002A | npc_priest | STATE_CHURCH_GATE_A | But guns do not cure fear either. | none | set_flag:FLAG_CH012_TENSION_PLUS | choice:DLG_CH012_PRIEST_GATE_001:A | DT_042 Choice A. |
| DLG_CH012_PRIEST_GATE_002B | npc_priest | STATE_CHURCH_GATE_B | Then enter through the side door. No one raises a gun in the prayer hall. | none | set_flag:FLAG_CH012_CHURCH_TRUST_GAINED | choice:DLG_CH012_PRIEST_GATE_001:B | DT_042 Choice B. |
| DLG_CH012_PRIEST_GATE_002C | comp_hoang | STATE_CHURCH_GATE_C | Because every time someone says 'safe,' we almost die. | none | set_flag:FLAG_CH012_HOANGRESPECT_PLUS | choice:DLG_CH012_PRIEST_GATE_001:C | DT_042 Choice C. |
| DLG_CH012_PRIEST_GATE_003C | npc_priest | STATE_CHURCH_GATE_C2 | Then you have learned half the lesson. The other half is trying not to become what you fear. | none | none | choice:DLG_CH012_PRIEST_GATE_001:C | DT_042 Choice C. |
| DLG_CH012_PRIEST_GATE_002D | npc_priest | STATE_CHURCH_GATE_D | It is the street where people no longer die properly. Trees grow inside houses. Corpses stand as if listening to a sermon. We sealed that road and prayed it does not learn to open doors. | none | set_flag:FLAG_CH012_EDENROT_STREET_KNOWN | choice:DLG_CH012_PRIEST_GATE_001:D | DT_042 Choice D. |
| DLG_CH012_PRIEST_RULE_001 | npc_priest | STATE_CHURCH_RULE | No one carries guns in the prayer hall. Enter through the side door. Two at a time. Children and wounded first. | none | none | church_entry | Scene 2. |
| DLG_CH012_HOANG_PRIEST_001 | comp_hoang | STATE_CHURCH_ENTRY | There is something wrong with him. | none | none | church_entry | Scene 2. |
| DLG_CH012_TRUNG_PRIEST_001 | char_trung | STATE_CHURCH_ENTRY | I know. | none | none | church_entry | Scene 2. |
| DLG_CH012_TRUNG_PRIEST_002 | char_trung | STATE_CHURCH_ENTRY | But I trust Mai was here. | none | none | church_entry | Scene 2. |
| DLG_CH012_GIRL_CHALK_001 | npc_girl | STATE_GIRL_MEET | Where did you get that? | none | none | catechism_room | Scene 3. |
| DLG_CH012_TRUNG_GIRL_001 | char_trung | STATE_GIRL_MEET | Mai left it for me. | none | none | catechism_room | Scene 3. |
| DLG_CH012_GIRL_CHALK_002 | npc_girl | STATE_GIRL_MEET | Teacher Mai? | none | none | catechism_room | Scene 3. |
| DLG_CH012_GIRL_STORY_001 | npc_girl | STATE_GIRL_STORY | She saved me. The yellow coats wanted to put me on a truck because I was small. Teacher Mai said I was her student and students follow their teacher. | none | set_flag:FLAG_CH012_GIRL_SAVED_BY_MAI_CONFIRMED | girl_story | Scene 3. |
| DLG_CH012_GIRL_WARNING_001 | npc_girl | STATE_GIRL_WARNING | Teacher Mai does not want anyone to say Binh's name out loud. | none | none | girl_story | Scene 3. |
| DLG_CH012_GIRL_QUESTION_001 | npc_girl | STATE_GIRL_TEST | Do you remember the song? | none | none | girl_test | Scene 3. |
| DLG_CH012_TRUNG_QUESTION_001 | char_trung | STATE_GIRL_TEST | I remember. You haven't heard it yet. | none | set_flag:FLAG_CH012_GIRL_TRUST_GAINED | girl_test | Scene 3. |
| DLG_CH012_GIRL_CONFIRM_001 | npc_girl | STATE_GIRL_TEST | Teacher Mai said if you answer like that, you are really Trung. | none | none | girl_test | Scene 3. |
| DLG_CH012_HOANG_PRIVACY_001 | comp_hoang | STATE_PRIVACY | I'll wait outside. | none | none | before_reunion | DT_045. |
| DLG_CH012_TRUNG_PRIVACY_001 | char_trung | STATE_PRIVACY | Hoang, you... | none | none | before_reunion | DT_045. |
| DLG_CH012_HOANG_PRIVACY_002 | comp_hoang | STATE_PRIVACY | You two need to talk like husband and wife, not like teammates with a close friend standing nearby. | none | set_flag:FLAG_CH012_HOANGRESPECT_PLUS | before_reunion | DT_045. |
| DLG_CH012_MAI_REUNION_001 | char_mai | STATE_REUNION | You are late. But you came. | none | none | reunion | DT_043. |
| DLG_CH012_TRUNG_REUNION_001 | char_trung | STATE_REUNION | I'm sorry. | none | none | reunion | DT_043. |
| DLG_CH012_MAI_REUNION_002 | char_mai | STATE_REUNION | Binh... | none | none | reunion | DT_043. |
| DLG_CH012_TRUNG_REUNION_002 | char_trung | STATE_REUNION | Don't apologize. Tell me where our child is. | none | none | reunion | DT_043. |
| DLG_CH012_MAI_REUNION_003 | char_mai | STATE_REUNION | I lost him. | none | none | reunion | DT_043. |
| DLG_CH012_TRUNG_REUNION_003 | char_trung | STATE_REUNION | No. They took him. That is different. | none | set_flag:FLAG_CH012_FAMILYTRUST_PLUS | reunion | DT_043. |
| DLG_CH012_MAI_HURT_001 | char_mai | STATE_REUNION | You're hurt. | none | none | reunion | Scene 4. |
| DLG_CH012_TRUNG_HURT_001 | char_trung | STATE_REUNION | Shoulder. Arm. Not bad. You're hurt too... | none | none | reunion | Scene 4. |
| DLG_CH012_TRUNG_BINH_001 | char_trung | STATE_REUNION | Where is Binh right now? | none | none | reunion | Scene 4. |
| DLG_CH012_MAI_BINH_001 | char_mai | STATE_TESTIMONY | They did not ask if I was bitten. They asked if Binh had a fever. | none | none | testimony | DT_044. |
| DLG_CH012_TRUNG_BINH_002 | char_trung | STATE_TESTIMONY | Why? | none | none | testimony | DT_044. |
| DLG_CH012_MAI_BINH_002 | char_mai | STATE_TESTIMONY | I don't know. But when he was scratched on the arm, he did not develop a fever. Someone saw that and their attitude changed immediately. | none | none | testimony | DT_044. |
| DLG_CH012_TRUNG_BINH_003 | char_trung | STATE_TESTIMONY | Who? | none | none | testimony | DT_044. |
| DLG_CH012_MAI_BINH_003 | char_mai | STATE_TESTIMONY | Yellow coats. And someone standing behind them writing notes. Not wearing a rescue jacket. Not looking like a refugee. | none | none | testimony | DT_044. |
| DLG_CH012_MAI_EDENROT_001 | char_mai | STATE_TESTIMONY | One of them said: Edenrot does not eat him. | none | none | testimony | DT_044. |
| DLG_CH012_TRUNG_EDENROT_001 | char_trung | STATE_TESTIMONY | He is not food for anything. | none | set_flag:FLAG_CH012_EDENROT_PHRASE_HEARD | testimony | DT_044. |
| DLG_CH012_MAI_JOURNEY_001 | char_mai | STATE_TESTIMONY | They said children were being taken to a separate safe area. I refused. There was a struggle. During the chaos, an old cook pulled Binh behind the kitchen. | none | none | testimony | Scene 5. |
| DLG_CH012_MAI_NOTE_001 | char_mai | STATE_TESTIMONY | He called himself Tu Nieu. I don't know his real name. | none | none | testimony | Scene 5. |
| DLG_CH012_TRUNG_NOTE_001 | char_trung | STATE_TESTIMONY | Which industrial zone? | none | none | testimony | Scene 5. |
| DLG_CH012_MAI_NOTE_002 | char_mai | STATE_TESTIMONY | East. Where the Factory Boss forces people to work. I was going to go, but the church is being watched. If I leave, I lead them to our child. | none | set_flag:FLAG_CH012_BINH_LOCATION_KNOWN | testimony | Scene 5. |
| DLG_CH012_TRUNG_TOGETHER_001 | char_trung | STATE_TESTIMONY | This time we go together. | none | none | testimony | Scene 5. |
| DLG_CH012_MAI_CHOICE_001 | char_mai | STATE_TESTIMONY | If you have to choose between me and Binh? | Choice A: "Don't ask me that."; Choice B: "Both. Always both."; Choice C: "I will not choose." | open_choice | testimony | Scene 5. |
| DLG_CH012_MAI_CHOICE_002A | char_mai | STATE_TESTIMONY_A | Then don't answer. Just go. | none | set_flag:FLAG_CH012_FAMILY_HONEST | choice:DLG_CH012_MAI_CHOICE_001:A | Scene 5. |
| DLG_CH012_MAI_CHOICE_002B | char_mai | STATE_TESTIMONY_B | That is what a father says. | none | set_flag:FLAG_CH012_FAMILY_PROMISE | choice:DLG_CH012_MAI_CHOICE_001:B | Scene 5. |
| DLG_CH012_MAI_CHOICE_002C | char_mai | STATE_TESTIMONY_C | The end of the world likes to make people choose. | none | set_flag:FLAG_CH012_FAMILY_DEFIANCE | choice:DLG_CH012_MAI_CHOICE_001:C | Scene 5. |
| DLG_CH012_HOANG_WATCHER_001 | comp_hoang | STATE_WATCHER | Yellow coat. Across the street. Second floor. | none | set_flag:FLAG_CH012_WATCHER_DETECTED | watcher_scene | Scene 6. |
| DLG_CH012_PRIEST_WATCHER_001 | npc_priest | STATE_WATCHER | They came once before. Asked about a boy in a blue shirt. Said they were taking him to a medical area. I told them there was no child like that here. | none | none | watcher_scene | Scene 6. |
| DLG_CH012_PRIEST_WATCHER_002 | npc_priest | STATE_WATCHER | They also asked which roads avoid Edenrot street. They know the fear map of this area. | none | none | watcher_scene | Scene 6. |
| DLG_CH012_TRUNG_LIE_001 | char_trung | STATE_WATCHER | You lied to them too? | none | none | watcher_scene | Scene 6. |
| DLG_CH012_PRIEST_LIE_001 | npc_priest | STATE_WATCHER | I lied because for the first time in my life, I saw that telling the truth would smell like blood. | none | none | watcher_scene | Scene 6. |
| DLG_CH012_PRIEST_BELL_001 | npc_priest | STATE_BELL_OFFER | If they come back, we can ring the bell. The zombies nearby will come. We can escape through the back gate. | none | none | watcher_scene | Scene 6. |
| DLG_CH012_HOANG_BELL_001 | comp_hoang | STATE_BELL_OFFER | A selective suicide plan. I respect that. | none | none | watcher_scene | Scene 6. |
| DLG_CH012_PRIEST_BELL_002 | npc_priest | STATE_BELL_OFFER | I call it the last resort. | none | none | watcher_scene | Scene 6. |
| DLG_CH012_MAI_READY_001 | char_mai | STATE_DEPARTURE | I lost my child once because I waited too long. I don't want to make that mistake again. | none | set_flag:FLAG_CH012_MAI_READY | departure | Scene 6. |
| DLG_CH012_MAI_RECORDER_001 | char_mai | STATE_DEPARTURE | That voice sounds so fake. | none | none | departure | Scene 7. |
| DLG_CH012_TRUNG_RECORDER_001 | char_trung | STATE_DEPARTURE | I hear you are alive. | none | none | departure | Scene 7. |
| DLG_CH012_HOANG_FACTORY_001 | comp_hoang | STATE_DEPARTURE | The industrial zone is Bandit territory. Going in there is not a rescue. It is a war. | none | none | departure | Scene 7. |
| DLG_CH012_MAI_FACTORY_001 | char_mai | STATE_DEPARTURE | Then we go in as parents looking for their child, not as rescuers. | none | set_flag:FLAG_CH012_INDUSTRIAL_ZONE_UNLOCKED | departure | Scene 7. |
| DLG_CH012_PRIEST_GOODBYE_001 | npc_priest | STATE_DEPARTURE | Go with God. Or go without Him. Either way, go. | none | none | departure | Scene 7. |
| DLG_CH012_BARK_CHALK_001 | char_trung | STATE_BARK | Another chalk mark. She was here. | none | none | exploring_church | Implementation Notes. |
| DLG_CH012_BARK_BELL_001 | npc_priest | STATE_BARK | The bell is silent so we can stay alive. | none | none | bell_tower | Implementation Notes. |
| DLG_CH012_BARK_EDENROT_001 | npc_survivor_refugee | STATE_BARK | Don't look at Edenrot street. It looks back. | none | none | neighboring_streets | Implementation Notes. |
| DLG_CH012_BARK_MAI_STILL_001 | char_mai | STATE_BARK | I kept teaching. Even without a classroom. | none | none | catechism_room | Implementation Notes. |
| DLG_CH012_BARK_BINH_ABSENT_001 | char_mai | STATE_BARK | The space where Binh should be is between us. | none | none | departure | Implementation Notes. |

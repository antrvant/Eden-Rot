# Dialogue - CH011

Metadata:

- chapterID: CH011
- sourceFilename: chapter_011_su_sup_do_cua_can_cu.md
- language: English

## Dialogue Table

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH011_GATE_001 | comp_hoang | ST_SIDE_GATE | Report to Mentor. | null | null | null | Scene 1 |
| DLG_CH011_FALSE_ORDER_001 | npc_speaker | ST_YARD | All civilians move to East Gate. Repeat, East Gate. | null | null | null | Scene 2 - false loudspeaker |
| DLG_CH011_FALSE_ORDER_002 | npc_speaker | ST_YARD | Zombies attacking from west. East Gate is the only escape. | null | null | null | Scene 2 - false loudspeaker |
| DLG_CH011_MENTOR_001 | npc_mentor | ST_YARD | Fake! East Gate has been locked since afternoon! | null | null | null | Scene 2 |
| DLG_CH011_TRUNG_001 | char_trung | ST_YARD | They hear the speaker, not us! | null | null | null | Scene 2 |
| DLG_CH011_HOANG_001 | comp_hoang | ST_YARD | Then stop whispering! | null | null | null | Scene 2 |
| DLG_CH011_TRUNG_COMMAND_001 | char_trung | ST_YARD | Everyone together! Children in the middle! Wounded follow! Armed on both sides! | null | FLAG_CH011_FIRST_COMMAND_GIVEN | null | Scene 2 |
| DLG_CH011_RADIO_CALL_001 | npc_radio_operator | ST_RADIO | Radio tent under attack! I need help getting equipment out! | null | null | null | Scene 3 |
| DLG_CH011_DOCTOR_CALL_001 | npc_doctor | ST_MEDICAL | Medical tent has people trapped! I will not leave if there are patients! | null | null | null | Scene 3 |
| DLG_CH011_ENGINEER_CALL_001 | npc_engineer | ST_AMMO | Ammo storage burning! If it blows, West Gate breaks! | null | null | null | Scene 3 |
| DLG_CH011_HOANG_CHOOSE_001 | comp_hoang | ST_YARD | Choose fast! | null | null | null | Scene 3 |
| DLG_CH011_TRUNG_CHOOSE_001 | char_trung | ST_YARD | Hoang, help engineer with ammo. Phuc, help doctor. I help radio operator then refugees. Meet at West Gate. | null | null | null | Scene 3 - priority choice |
| DLG_CH011_HOANG_TIME_001 | comp_hoang | ST_YARD | Five minutes. After five, I drag you out. | null | null | null | Scene 3 |
| DLG_CH011_TRUNG_TIME_001 | char_trung | ST_YARD | Three minutes. | null | null | null | Scene 3 |
| DLG_CH011_HOANG_LEARN_001 | comp_hoang | ST_YARD | You learn fast. | null | null | null | Scene 3 |
| DLG_CH011_SABOTEUR_001 | npc_bandit_saboteur | ST_KITCHEN | This outpost died the moment it started sharing rations. | null | null | null | Scene 4 |
| DLG_CH011_TRUNG_002 | char_trung | ST_KITCHEN | Drop him. | null | null | null | Scene 4 |
| DLG_CH011_SABOTEUR_002 | npc_bandit_saboteur | ST_KITCHEN | Money? You still think money has value? | null | null | null | Scene 4 |
| DLG_CH011_HOANG_002 | comp_hoang | ST_KITCHEN | Food, gas, family. Pick one. | null | null | null | Scene 4 |
| DLG_CH011_SABOTEUR_003 | npc_bandit_saboteur | ST_KITCHEN | See, your friend understands life better than you. | null | null | null | Scene 4 |
| DLG_CH011_TRUNG_003 | char_trung | ST_KITCHEN | Why say Edenrot is in the west? | null | null | null | Scene 4 |
| DLG_CH011_SABOTEUR_004 | npc_bandit_saboteur | ST_KITCHEN | Because just saying that word makes people run. Fear is the cheapest gate. | null | null | null | Scene 4 |
| DLG_CH011_HOANG_003 | comp_hoang | ST_KITCHEN | Enough intel. | null | null | null | Scene 4 |
| DLG_CH011_OLD_COOK_001 | npc_old_cook | ST_KITCHEN | It came into my kitchen. Said it wanted to help wash pots. | null | null | null | Scene 4 |
| DLG_CH011_MENTOR_WOUND_001 | npc_mentor | ST_WEST_GATE | Pull back! Retreat! | null | null | null | Scene 5 |
| DLG_CH011_TRUNG_004 | char_trung | ST_WEST_GATE | I will help you! | null | null | null | Scene 5 |
| DLG_CH011_MENTOR_002 | npc_mentor | ST_WEST_GATE | Get them out! | null | null | null | Scene 5 |
| DLG_CH011_MENTOR_HANDOFF_001 | npc_mentor | ST_WEST_GATE | Drainage behind medical tent. Take them. | null | FLAG_CH011_MENTOR_DOG_TAG_OBTAINED | null | Scene 5 |
| DLG_CH011_TRUNG_005 | char_trung | ST_WEST_GATE | Come with me! | null | null | null | Scene 5 |
| DLG_CH011_MENTOR_LAST_001 | npc_mentor | ST_WEST_GATE | I hold the gate. | null | FLAG_CH011_MENTOR_DEAD | null | Scene 5 |
| DLG_CH011_TRUNG_006 | char_trung | ST_WEST_GATE | I will not leave you! | null | null | null | Scene 5 |
| DLG_CH011_MENTOR_LAST_002 | npc_mentor | ST_WEST_GATE | You do not leave me. You carry my lessons out of here. | null | null | null | Scene 5 |
| DLG_CH011_TRUNG_007 | char_trung | ST_WEST_GATE | Come with me! | null | null | null | Scene 5 |
| DLG_CH011_MENTOR_ORDER_001 | npc_mentor | ST_WEST_GATE | Go now. That is an order. | null | null | null | Scene 5 |
| DLG_CH011_HOANG_PULL_001 | comp_hoang | ST_WEST_GATE | If you go back, his death is pointless! | null | FLAG_CH011_HOANG_PULLED_TRUNG_AGAIN | null | Scene 5 |
| DLG_CH011_TRUNG_FROZEN_001 | char_trung | ST_YARD | Mentor is still in there. | null | null | null | Scene 6 |
| DLG_CH011_HOANG_PUSH_001 | comp_hoang | ST_YARD | And all these people are looking at you. | null | null | null | Scene 6 |
| DLG_CH011_TRUNG_008 | char_trung | ST_YARD | I am not him. | null | null | null | Scene 6 |
| DLG_CH011_HOANG_PUSH_002 | comp_hoang | ST_YARD | No. But command your way. Command now. | null | null | null | Scene 6 |
| DLG_CH011_TRUNG_COMMAND_002 | char_trung | ST_YARD | Children in the middle. Wounded right after. Doctor and radio in center. Armed on both sides. No one breaks line. If someone falls, the person behind pulls them up. Silent when entering the channel. | null | null | null | Scene 6 |
| DLG_CH011_OLD_COOK_002 | npc_old_cook | ST_ESCAPE | Cook porridge... | null | null | null | Scene 7 |
| DLG_CH011_HOANG_004 | comp_hoang | ST_ESCAPE | Faster. | null | null | null | Scene 7 |
| DLG_CH011_TRUNG_009 | char_trung | ST_ESCAPE | The wounded cannot go faster. | null | null | null | Scene 7 |
| DLG_CH011_HOANG_005 | comp_hoang | ST_ESCAPE | Zombies do not wait for anyone. | null | null | null | Scene 7 |
| DLG_CH011_HOANG_FINAL_001 | comp_hoang | ST_ESCAPE | Mai and Binh. | null | null | null | Scene 7 - Hoang stops Trung |

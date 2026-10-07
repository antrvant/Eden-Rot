# Flags - CH011

Metadata:

- chapterID: CH011
- sourceFilename: chapter_011_su_sup_do_cua_can_cu.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH011_GATE_OPENED | progression | false | Side gate opened by saboteur | MQ_011 trigger | Scene 1 |
| FLAG_CH011_GUARD_DOWN | world_state | false | Guard at side gate silenced | Scene 1 | Scene 1 |
| FLAG_CH011_ALARM_SOUNDED | progression | false | Trung pulls alarm | MQ_011 | Scene 1 |
| FLAG_CH011_FALSE_ORDER_BROADCAST | world_state | false | False loudspeaker orders play | Scene 2 | Scene 2 |
| FLAG_CH011_MENTOR_IDENTIFIES_FAKE | progression | false | Mentor recognizes false orders | Scene 2 | Scene 2 |
| FLAG_CH011_EDENROT_FEAR_USED | world_state | false | Edenrot used as fear weapon | Scene 2 | Scene 2 - "Edenrot is spreading from west" |
| FLAG_CH011_FIRST_COMMAND_GIVEN | progression | false | Trung issues first command | Scene 2 | Scene 2 - "Children in the middle!" |
| FLAG_CH011_RADIO_TENT_CHOSEN | choice | false | Player prioritizes radio tent | Scene 3 | Choice |
| FLAG_CH011_MEDICAL_TENT_CHOSEN | choice | false | Player prioritizes medical tent | Scene 3 | Choice |
| FLAG_CH011_AMMO_CHOSEN | choice | false | Player prioritizes ammo storage | Scene 3 | Choice |
| FLAG_CH011_REFUGEES_CHOSEN | choice | false | Player prioritizes refugee tent | Scene 3 | Choice |
| FLAG_CH011_RADIO_OPERATOR_SAVED | outcome | false | Radio operator rescued | Depends on choice | Scene 3 |
| FLAG_CH011_DOCTOR_SAVED | outcome | false | Doctor rescued | Depends on choice | Scene 3 |
| FLAG_CH011_ENGINEER_SAVED | outcome | false | Engineer rescued | Depends on choice | Scene 3 |
| FLAG_CH011_EDENROT_MAP_SAVED | outcome | false | Edenrot risk map rescued | If radio tent chosen | Scene 3 |
| FLAG_CH011_SABOTEUR_ENCOUNTERED | progression | false | Trung confronts saboteur | Scene 4 | Scene 4 |
| FLAG_CH011_SABOTEUR_ESCAPED | outcome | false | Saboteur escapes | Trung shows mercy | Scene 4 |
| FLAG_CH011_SABOTEUR_KILLED | outcome | false | Saboteur killed | Alternate choice | Scene 4 alternate |
| FLAG_CH011_MENTOR_INJURED | world_state | false | Mentor injured by falling metal | Scene 5 | Scene 5 |
| FLAG_CH011_MENTOR_DOG_TAG_OBTAINED | progression | false | Trung receives dog tag | Scene 5 | Scene 5 |
| FLAG_CH011_MENTOR_MAP_OBTAINED | progression | false | Trung receives map | Scene 5 | Scene 5 |
| FLAG_CH011_MENTOR_DEAD | world_state | false | Mentor dies holding West Gate | Scene 5 | Scene 5 |
| FLAG_CH011_HOANG_PULLED_TRUNG_AGAIN | relationship | false | Hoang stops Trung from returning | Scene 5 | Scene 5 |
| FLAG_CH011_TRUNG_FROZEN | emotional | false | Trung nearly freezes when Mentor is down | Scene 6 | Scene 6 |
| FLAG_CH011_SECOND_COMMAND_GIVEN | progression | false | Trung issues detailed retreat command | Scene 6 | Scene 6 |
| FLAG_CH011_DRAINAGE_ENTERED | progression | false | Group enters drainage tunnel | Scene 7 | Scene 7 |
| FLAG_CH011_AMMO_EXPLOSION | world_state | false | Ammo storage explodes | Scene 7 | Scene 7 |
| FLAG_CH011_LAST_GUNSHOT_HEARD | world_state | false | Mentor's last gunshot heard | Scene 7 | Scene 7 |
| FLAG_CH011_OUTPOST_DESTROYED | world_state | false | Outpost fully burned | Scene 7 | Scene 7 |
| FLAG_CH011_OUTPOST_ESCAPE_COMPLETE | progression | false | Group exits drainage tunnel | Scene 7 | Scene 7 |
| FLAG_CH011_BANDIT_NETWORK_REVEALED | lore | false | Saboteur reveals bandit organization | Scene 4 | Scene 4 |
| FLAG_CH011_FEAR_IS_GATE | lore | false | Saboteur says "Fear is the cheapest gate" | Scene 4 | Scene 4 |

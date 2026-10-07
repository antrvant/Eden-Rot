# Scenes - CH011

Metadata:

- chapterID: CH011
- sourceFilename: chapter_011_su_sup_do_cua_can_cu.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH011_GATE_OPEN | Side Gate Opens at Night | LOC_CH011_SIDE_GATE | Collapse trigger; connects CH010 | Night patrol signs | Gate open; guard down | char_trung, comp_hoang, npc_infected_guard | ENM_CH011_HORDE_INITIAL | Side gate, guard body | Scene 1 - Cổng phụ mở trong đêm |
| SCN_CH011_FALSE_ORDER | False Loudspeaker Orders | LOC_CH011_OUTPOST_YARD | Information warfare attack | Alarm sounds | Real orders spread | char_trung, npc_mentor, comp_hoang | None | Loudspeakers | Scene 2 - Loa giả lệnh |
| SCN_CH011_MULTI_CRISIS | Multiple Burning Points | LOC_CH011_RADIO_TENT | Priority rescue gameplay | False orders spread | Rescue choices made | char_trung, comp_hoang, npc_doctor, npc_radio_operator, npc_engineer, npc_phuc | ENM_CH011_INFECTED_SOLDIER | Multiple crisis points | Scene 3 - Những điểm đang cháy |
| SCN_CH011_BANDIT_REVEAL | Bandit in Yellow Fire Jacket | LOC_CH011_KITCHEN | Human betrayal reveal | Trung moving between points | Saboteur escapes | char_trung, npc_bandit_saboteur, npc_old_cook, comp_hoang | None | Kitchen, fire jacket | Scene 4 - Bandit trong áo cứu hỏa |
| SCN_CH011_MENTOR_GATE | Mentor Holds the Gate | LOC_CH011_WEST_GATE | Mentor sacrifice | Horde pressing gate | Mentor dead; Trung has dog tag | char_trung, npc_mentor, comp_hoang | ENM_CH011_ARMORED_INFECTED | West gate, truck barrier | Scene 5 - Mentor giữ cổng |
| SCN_CH011_FIRST_COMMAND | Trung's First Command | LOC_CH011_MEDICAL_YARD | Commander moment | Mentor down | Survivors assembled | char_trung, comp_hoang, npc_doctor, npc_radio_operator, npc_old_cook, npc_phuc, npc_nam | None | Map, survivors | Scene 6 - Lệnh đầu tiên của Trung |
| SCN_CH011_DRAIN_ESCAPE | Drainage Tunnel Escape | LOC_CH011_DRAINAGE_TUNNEL | Escape and aftermath | Group assembled | Outpost burned; survivors out | char_trung, comp_hoang, all survivors | ENM_CH011_SCREAMER_OUTSIDE | Drainage tunnel, water | Scene 7 - Kênh thoát nước |

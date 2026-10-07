# Dialogue - CH036

Metadata:

- chapterID: CH036
- sourceFilename: chapter_036_paris_khong_anh_den.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH036_DT207_001 | char_binh | STATE_PARIS_ARRIVAL | Is that the Eiffel Tower? | none | none | arrival_at_paris | DT_207 - Paris Without Light. |
| DLG_CH036_DT207_002 | char_mai | STATE_PARIS_ARRIVAL | Yes. | none | none | arrival_at_paris | DT_207. |
| DLG_CH036_DT207_003 | char_binh | STATE_PARIS_ARRIVAL | Why is it not lit? | none | none | arrival_at_paris | DT_207. |
| DLG_CH036_DT207_004 | char_trung | STATE_PARIS_ARRIVAL | Because the city is hiding in the dark. | none | none | arrival_at_paris | DT_207. |
| DLG_CH036_DT207_005 | char_mai | STATE_PARIS_ARRIVAL | Not all darkness is death. Sometimes it is how you survive longer. | none | none | arrival_at_paris | DT_207. |
| DLG_CH036_DT208_001 | char_teacher_amelie | STATE_ATTENDANCE_GATE | Phrase. | none | none | metro_entrance | DT_208 - Attendance Password. |
| DLG_CH036_DT208_002 | char_mai | STATE_ATTENDANCE_GATE | No one may demand blood, names, or the silence of children in exchange for safety. | none | none | metro_entrance | DT_208. |
| DLG_CH036_DT208_003 | char_teacher_amelie | STATE_ATTENDANCE_GATE | Counterphrase: What do we ask first? | none | none | metro_entrance | DT_208. |
| DLG_CH036_DT208_004 | char_binh | STATE_ATTENDANCE_GATE | Name. | none | set_flag:FLAG_CH036_GATE_OPENED | metro_entrance | DT_208. |
| DLG_CH036_DT208_005 | char_teacher_amelie | STATE_ATTENDANCE_GATE | Gate one opens. | none | none | metro_entrance | DT_208. |
| DLG_CH036_DT209_001 | char_teacher_amelie | STATE_ROLL_CALL | June? | none | none | roll_call_morning | DT_209 - Roll Call. |
| DLG_CH036_DT209_002 | char_june | STATE_ROLL_CALL | Present. | none | none | roll_call_morning | DT_209. |
| DLG_CH036_DT209_003 | char_teacher_amelie | STATE_ROLL_CALL | Binh? | none | none | roll_call_morning | DT_209. |
| DLG_CH036_DT209_004 | char_binh | STATE_ROLL_CALL | I... am present. | none | set_flag:FLAG_CH036_BINH_SCHOOL_MOMENT | roll_call_morning | DT_209. |
| DLG_CH036_DT209_005 | char_teacher_amelie | STATE_ROLL_CALL | Here, "present" is enough. No one asks why you survived before breakfast. | none | none | roll_call_morning | DT_209. |
| DLG_CH036_DT209_006 | char_mai | STATE_ROLL_CALL_THANKS | Thank you, teacher. | none | none | roll_call_morning | DT_209. |
| DLG_CH036_DT210_001 | char_mai | STATE_TEACHER_MIRROR | You still teach? | none | none | after_roll_call | DT_210 - Teacher Mirror. |
| DLG_CH036_DT210_002 | char_teacher_amelie | STATE_TEACHER_MIRROR | If we stop, the tunnel becomes only a tunnel. | none | none | after_roll_call | DT_210. |
| DLG_CH036_DT210_003 | char_mai | STATE_TEACHER_MIRROR | I once opened a class in a base that was about to collapse. | none | none | after_roll_call | DT_210. |
| DLG_CH036_DT210_004 | char_teacher_amelie | STATE_TEACHER_MIRROR | Then you know. A lesson is a candle that does not admit it is a weapon. | none | none | after_roll_call | DT_210. |
| DLG_CH036_DT211_001 | npc_mimic | STATE_MIMIC_LURE | Amelie, present. | none | none | service_tunnel | DT_211 - Mimic Rule. |
| DLG_CH036_DT211_002 | npc_mathis | STATE_MIMIC_LURE | That is Lucie! | none | none | service_tunnel | DT_211. |
| DLG_CH036_DT211_003 | char_teacher_amelie | STATE_MIMIC_LURE | Lucie is on the wall. We do not follow voices the teacher cannot see. | none | none | service_tunnel | DT_211. |
| DLG_CH036_DT211_004 | char_mai | STATE_MIMIC_LURE | Everyone say your name to the person on your left. | none | none | service_tunnel | DT_211. |
| DLG_CH036_DT211_005 | char_binh | STATE_MIMIC_LURE | Binh. | none | none | service_tunnel | DT_211. |
| DLG_CH036_DT211_006 | char_june | STATE_MIMIC_LURE | June. | none | none | service_tunnel | DT_211. |
| DLG_CH036_DT212_001 | char_celine | STATE_ARCHIVE | Books first hid food. Then medicine. Then sins. | none | none | station_library | DT_212 - Archive. |
| DLG_CH036_DT212_002 | char_doctor | STATE_ARCHIVE | Patient Zero transfer logs? | none | none | station_library | DT_212. |
| DLG_CH036_DT212_003 | char_celine | STATE_ARCHIVE | Behind children's astronomy. Adults rarely look there after the world ends. | none | none | station_library | DT_212. |
| DLG_CH036_DT212_004 | char_thu | STATE_ARCHIVE | That is insulting and accurate. | none | none | station_library | DT_212. |
| DLG_CH036_DT213_001 | npc_mimic | STATE_MIMIC_BINH | Mom, I am here. | none | none | mimic_imitates_binh | DT_213 - Mimic Imitates Binh. |
| DLG_CH036_DT213_002 | char_mai | STATE_MIMIC_BINH | Binh is holding my hand. | none | none | mimic_imitates_binh | DT_213. |
| DLG_CH036_DT213_003 | npc_mimic | STATE_MIMIC_BINH_REPEAT | Mom... | none | none | mimic_imitates_binh | DT_213. |
| DLG_CH036_DT213_004 | char_trung | STATE_MIMIC_BINH | Do not listen with your heart. Check with your eyes, your hands, your name. | none | none | mimic_imitates_binh | DT_213. |
| DLG_CH036_DT213_005 | char_binh | STATE_MIMIC_BINH | It speaks my voice but it does not know when I am real. | none | none | mimic_imitates_binh | DT_213. |
| DLG_CH036_DT214_001 | char_doctor | STATE_ARCHIVE_RUN | Archive case! | none | none | flooded_tunnel | DT_214 - Data Follows People. |
| DLG_CH036_DT214_002 | char_trung | STATE_ARCHIVE_RUN | Catch! | none | none | flooded_tunnel | DT_214. |
| DLG_CH036_DT214_003 | char_doctor | STATE_ARCHIVE_RUN | What about the child? | none | none | flooded_tunnel | DT_214. |
| DLG_CH036_DT214_004 | char_trung | STATE_ARCHIVE_RUN | I am already carrying her. Data follows the living, not the other way around. | none | set_flag:FLAG_CH036_DATA_FOLLOWS_PEOPLE | flooded_tunnel | DT_214. |
| DLG_CH036_DT215_001 | char_doctor | STATE_ALPS_HOOK | Paris transfer, Geneva corridor, Alpine Lab. Patient Zero went to the mountains. | none | none | shelter_after_battle | DT_215 - Alps Hook. |
| DLG_CH036_DT215_002 | char_binh | STATE_ALPS_HOOK | I hear it calling. | none | none | shelter_after_battle | DT_215. |
| DLG_CH036_DT215_003 | char_mai | STATE_ALPS_HOOK | Which radio? | none | none | shelter_after_battle | DT_215. |
| DLG_CH036_DT215_004 | char_binh | STATE_ALPS_HOOK | Not through my ears. | none | set_flag:FLAG_CH036_BINH_ALPS_SIGNAL | shelter_after_battle | DT_215. |
| DLG_CH036_DT215_005 | char_trung | STATE_ALPS_HOOK | Binh? | none | none | shelter_after_battle | DT_215. |
| DLG_CH036_DT215_006 | char_binh | STATE_ALPS_HOOK | It is in the mountains. | none | none | shelter_after_battle | DT_215. |

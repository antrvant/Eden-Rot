# Dialogue - CH007

Metadata:

- chapterID: CH007
- sourceFilename: chapter_007_dem_dau_ngoai_tuong_rao.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH007_MENTOR_ASSIGN_001 | npc_mentor | STATE_GUARD_ASSIGNMENT | West Gate. Midnight until dawn. | none | set_flag:FLAG_CH007_GUARD_DUTY_ASSIGNED | chapter_start | Scene 1. |
| DLG_CH007_TRUNG_ASSIGN_001 | char_trung | STATE_GUARD_ASSIGNMENT | I need to find my wife and child. | none | none | chapter_start | DT_022. |
| DLG_CH007_MENTOR_ASSIGN_002 | npc_mentor | STATE_GUARD_ASSIGNMENT | With those shaking hands? | none | none | chapter_start | DT_022. |
| DLG_CH007_TRUNG_ASSIGN_002 | char_trung | STATE_GUARD_ASSIGNMENT | You want me to guard a wall for strangers? | Choice A: "I am not your soldier."; Choice B: "If there is news about Mai, I go."; Choice C: "I need a weapon and a position." | open_choice | chapter_start | DT_022. |
| DLG_CH007_MENTOR_ASSIGN_003A | npc_mentor | STATE_ASSIGN_A | Tonight the dead will not care what uniform you wear. | none | set_flag:FLAG_CH007_TENSION_PLUS | choice:DLG_CH007_TRUNG_ASSIGN_002:A | DT_022 Choice A. |
| DLG_CH007_MENTOR_ASSIGN_003B | npc_mentor | STATE_ASSIGN_B | If the gate falls, every signal becomes meaningless. | none | set_flag:FLAG_CH007_FAMILY_PANIC_PLUS | choice:DLG_CH007_TRUNG_ASSIGN_002:B | DT_022 Choice B. |
| DLG_CH007_MENTOR_ASSIGN_003C | npc_mentor | STATE_ASSIGN_C | Finally, something useful. | none | set_flag:FLAG_CH007_MENTOR_RESPECT_PLUS | choice:DLG_CH007_TRUNG_ASSIGN_002:C | DT_022 Choice C. |
| DLG_CH007_HOANG_ASSIGN_001 | comp_hoang | STATE_HOANG_WARNING | Your circle is getting bigger, Trung. Be careful. | none | set_flag:FLAG_CH007_INNER_CIRCLE_PRESSURE | after_assignment | Scene 1. |
| DLG_CH007_NAM_001 | npc_nam_child | STATE_REFUGEE_TENT | Are you a soldier? | none | none | refugee_tent | Scene 2. |
| DLG_CH007_TRUNG_NAM_001 | char_trung | STATE_REFUGEE_TENT | No. | none | none | refugee_tent | Scene 2. |
| DLG_CH007_NAM_002 | npc_nam_child | STATE_REFUGEE_TENT | Then do not let them trick you into opening the gate. | none | set_flag:FLAG_CH007_REFUGEE_TENT_VISITED | refugee_tent | Scene 2. |
| DLG_CH007_LOST_MOTHER_001 | npc_lost_mother | STATE_REFUGEE_TENT | If you go outside, help me find my daughter. They said children were prioritized. | none | set_flag:FLAG_CH007_NHI_THREAD_CONTINUES | refugee_tent | Scene 2. |
| DLG_CH007_ENGINEER_001 | npc_engineer | STATE_DEFENSE_PREP | I have enough material to reinforce two points, not three. The fence does not wait for emotional stability. | none | set_flag:FLAG_CH007_DEFENSE_PREP_STARTED | defense_prep | Scene 3 and implementation bark. |
| DLG_CH007_HOANG_DEFENSE_001 | comp_hoang | STATE_DEFENSE_PRIORITY | Fix the section near the ammo shed first. | none | none | defense_prep | DT_023. |
| DLG_CH007_TRUNG_DEFENSE_001 | char_trung | STATE_DEFENSE_PRIORITY | The children's tent is on the other side. | none | none | defense_prep | DT_023. |
| DLG_CH007_HOANG_DEFENSE_002 | comp_hoang | STATE_DEFENSE_PRIORITY | If the ammo is gone, the children die too. | none | none | defense_prep | DT_023. |
| DLG_CH007_TRUNG_DEFENSE_002 | char_trung | STATE_DEFENSE_PRIORITY | If the children die, what are we saving the ammo for? | none | none | defense_prep | DT_023. |
| DLG_CH007_SCREAMER_001 | ENM_CH007_FIRST_SCREAMER | STATE_FIRST_SCREAM | [distorted childlike cry] | none | set_flag:FLAG_CH007_FIRST_SCREAMER_HEARD;set_flag:FLAG_CH007_CROWD_PANIC_UNLOCKED | first_scream | Implementation Notes. |
| DLG_CH007_RADIO_OPERATOR_001 | npc_radio_operator | STATE_SCREAM_INTERFERENCE | Every time that thing screams, the radio floods with noise. | none | set_flag:FLAG_CH007_SCREAMER_RADIO_INTERFERENCE_SEEN | first_scream | Scene 4. |
| DLG_CH007_TRUNG_COMMAND_001 | char_trung | STATE_DEFENSE_COMMAND | Children down! Adults cover their ears! Bring wood, water, and ammo! | none | set_flag:FLAG_CH007_COMMANDER_SEED | wave_active | Scene 5 and implementation bark. |
| DLG_CH007_LOST_MOTHER_GATE_001 | npc_lost_mother | STATE_MOTHER_GATE | That is my child! I hear her calling! | Choice A: "Because I have a child, I will not let you die."; Choice B: "Hoang, hold her back."; Choice C: "Open one small gap." | open_choice | mother_at_gate | DT_024. |
| DLG_CH007_TRUNG_GATE_001A | char_trung | STATE_MOTHER_GATE_A | Because I have a child, I will not let you die. | none | set_flag:FLAG_CH007_MOTHER_GATE_PERSUADED;set_flag:FLAG_CH007_FAMILY_MIRROR_PLUS | choice:DLG_CH007_LOST_MOTHER_GATE_001:A | DT_024 Choice A. |
| DLG_CH007_TRUNG_GATE_001B | char_trung | STATE_MOTHER_GATE_B | Hoang, hold her back. | none | set_flag:FLAG_CH007_MOTHER_GATE_RESTRAINED;set_flag:FLAG_CH007_PRAGMATISM_PLUS;set_flag:FLAG_CH007_REFUGEE_TRUST_DOWN | choice:DLG_CH007_LOST_MOTHER_GATE_001:B | DT_024 Choice B. |
| DLG_CH007_TRUNG_GATE_001C | char_trung | STATE_MOTHER_GATE_C | Open one small gap. No wider. | none | set_flag:FLAG_CH007_MOTHER_GATE_OPENED;set_flag:FLAG_CH007_RISK_PLUS | choice:DLG_CH007_LOST_MOTHER_GATE_001:C | DT_024 Choice C. |
| DLG_CH007_TRUNG_NHI_001 | char_trung | STATE_NHI_NAME | Nhi. I will remember. Help me keep this gate closed so the children inside still have mothers. | none | set_flag:FLAG_CH007_NHI_NAME_REMEMBERED | mother_persuaded | Scene 6. |
| DLG_CH007_MENTOR_SCREAMER_001 | npc_mentor | STATE_SCREAMER_SHOT | Mark it! Hold the gate! | none | set_flag:FLAG_CH007_FIRST_SCREAMER_SEEN | screamer_visible | Scene 6. |
| DLG_CH007_RADIO_FRAGMENT_001 | char_mai | STATE_DAWN_FRAGMENT | ...Binh... no... | none | set_flag:FLAG_CH007_MAI_FRAGMENT_BLOCKED | dawn_radio | Scene 7. |
| DLG_CH007_MENTOR_AFTER_001 | npc_mentor | STATE_AFTER_WAVE | Tomorrow morning, you learn how not to let a scream control your hands. | none | set_flag:FLAG_CH007_TRAINING_DAY_UNLOCKED | dawn_aftermath | Scene 7. |
| DLG_CH007_HOANG_AFTER_001 | comp_hoang | STATE_AFTER_WAVE | You are expanding the circle. | none | none | dawn_aftermath | DT_025. |
| DLG_CH007_TRUNG_AFTER_001 | char_trung | STATE_AFTER_WAVE | What do you mean? | none | none | dawn_aftermath | DT_025. |
| DLG_CH007_HOANG_AFTER_002 | comp_hoang | STATE_AFTER_WAVE | Yesterday your circle had two people. Tonight you almost died for thirty strangers. | none | set_flag:FLAG_CH007_INNER_CIRCLE_PRESSURE | dawn_aftermath | DT_025. |
| DLG_CH007_TRUNG_AFTER_002 | char_trung | STATE_AFTER_WAVE | There were children in there. | none | none | dawn_aftermath | DT_025. |
| DLG_CH007_HOANG_AFTER_003 | comp_hoang | STATE_AFTER_WAVE | There will always be children in there, Trung. | none | set_flag:FLAG_CH007_HOANG_PRAGMATISM_PLUS | dawn_aftermath | DT_025. |

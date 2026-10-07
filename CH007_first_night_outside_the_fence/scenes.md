# Scenes - CH007

Metadata:

- chapterID: CH007
- sourceFilename: chapter_007_dem_dau_ngoai_tuong_rao.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH007_NIGHT_ASSIGNMENT | Night Assignment | LOC_CH007_OUTPOST_YARD | Establish conflict between chasing Mai and guarding strangers. | Chapter begins after CH006 fence test and training acceptance. | Trung is assigned West Gate duty and Hoang offers possible escape later. | char_trung;comp_hoang;npc_mentor | none | ITM_CH007_GUARD_ASSIGNMENT | Scene 1 - Phan cong dem. |
| SCN_CH007_REFUGEE_TENT | Refugee Tent | LOC_CH007_REFUGEE_TENT | Humanize refugees and connect child protection to Binh/Mai. | Trung checks tent near weak fence. | Trung promises to seek news after the night if they survive. | char_trung;comp_hoang;npc_nam_child;npc_lost_mother;npc_refugee_child_group | none | ITM_CH007_CHILD_EAR_CLOTH;ITM_CH007_REFUGEE_NAME_LIST | Scene 2 - Leu dan ti nan. |
| SCN_CH007_REINFORCE_FENCE | Reinforce the Fence | LOC_CH007_MATERIAL_DEPOT | Base defense prep and moral resource allocation. | Engineer presents limited materials and three vulnerable points. | Player locks allocation plan for night wave. | char_trung;comp_hoang;npc_engineer;npc_mentor;npc_phuc | none | ITM_CH007_REPAIR_PLAN;ITM_CH007_SANDBAG;ITM_CH007_WIRE;ITM_CH007_SHEET_METAL;ITM_CH007_BROKEN_VEHICLE_BARRIER;ITM_CH007_AMMO_CRATE | Scene 3 - Gia co hang rao. |
| SCN_CH007_FIRST_SCREAM | First Scream | LOC_CH007_WATCH_TOWER | Introduce Screamer audio, radio interference, and crowd panic. | Night falls and Trung watches West Gate. | Horde begins approaching and crowd wants the gate opened. | char_trung;comp_hoang;npc_radio_operator;npc_lost_mother;npc_refugee_child_group | ENM_CH007_FIRST_SCREAMER;ENM_CH007_HORDE_STANDARD | ITM_CH007_SCREAMER_AUDIO_SAMPLE;ITM_CH007_GATE_LATCH | Scene 4 - Tieng het dau tien. |
| SCN_CH007_NIGHT_WAVE | Night Wave | LOC_CH007_WEST_GATE | Multi-point defense setpiece. | Screamer calls horde from multiple directions. | Player survives waves and prevents critical breach. | char_trung;comp_hoang;npc_mentor;npc_phuc;npc_engineer;npc_refugee_old_man | ENM_CH007_HORDE_STANDARD;ENM_CH007_INFECTED_CLIMBER_FORESHADOW;ENM_CH007_GATE_PRESSURE_INFECTED | ITM_CH007_AMMO_CRATE;ITM_CH007_SANDBAG;ITM_CH007_WIRE;ITM_CH007_SHEET_METAL | Scene 5 - Wave dem. |
| SCN_CH007_MOTHER_GATE | Mother at the Gate | LOC_CH007_WEST_GATE | Moral crisis under Screamer manipulation. | Mother hears what she believes is Nhi outside the fence. | Mother is persuaded, restrained, or gate is risked; Screamer is revealed. | char_trung;comp_hoang;npc_lost_mother;npc_nhi;npc_phuc | ENM_CH007_FIRST_SCREAMER;ENM_CH007_CROWD_PANIC_HAZARD | ITM_CH007_GATE_LATCH;ITM_CH007_FLARE | Scene 6 - Nguoi me va canh cong. |
| SCN_CH007_DAWN_AFTERMATH | Dawn Aftermath | LOC_CH007_WEST_GATE | Consequence review, blocked Mai signal, training unlock, leadership seed. | Outpost survives the wave near dawn. | Mentor schedules training day and Trung helps repair the tent/fence. | char_trung;comp_hoang;npc_mentor;npc_radio_operator;npc_doctor;npc_nam_child;npc_lost_mother | none | ITM_CH007_CHILD_EAR_CLOTH;ITM_CH007_POST_WAVE_DAMAGE_REPORT;ITM_CH007_SCREAMER_AUDIO_SAMPLE | Scene 7 - Sau wave. |

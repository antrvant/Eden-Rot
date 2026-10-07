# Scenes - CH008

Metadata:

- chapterID: CH008
- sourceFilename: chapter_008_bai_hoc_cua_dai_uy.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH008_MORNING_AFTER | Morning After the Scream | LOC_CH008_OUTPOST_MORNING | Establish fatigue, Screamer echo, radio need, and training obstacle. | Chapter starts morning after CH007 wave. | Mentor redirects Trung from radio rush to training. | char_trung;comp_hoang;npc_mentor;npc_radio_operator | none | ITM_CH008_RADIO_FILTER_PARTS;ITM_CH008_BATTERY_PACK | Scene 1 - Sang sau tieng het. |
| SCN_CH008_BREATHING_DRILL | Lesson One: Breathe | LOC_CH008_TRAINING_YARD | Teach aim stability and emotional fire discipline. | Trung meets Mentor at training yard. | Firearm tier 1 unlocks if living target is not hit. | char_trung;comp_hoang;npc_mentor | none | ITM_CH008_TRAINING_RIFLE;ITM_CH008_EMPTY_MAGAZINE;ITM_CH008_LIVING_TARGET_PLATE;ITM_CH008_FIRST_CORRECT_CARTRIDGE;ITM_CH008_SPENT_CORRECT_SHELL | Scene 2 - Bai hoc so 1: Tho. |
| SCN_CH008_STEALTH_HOUSE | Lesson Two: Silence | LOC_CH008_ABANDONED_HOUSES | Teach stealth, sound discipline, and emotional interruption from child toy. | Scout leads team outside fence for parts. | Stealth tier 1 unlocks and parts route continues. | char_trung;comp_hoang;npc_mentor;npc_scout | ENM_CH008_GUNSHOT_ATTRACTED_ZOMBIES | ITM_CH008_RADIO_FILTER_PARTS;ITM_CH008_BATTERY_PACK;ITM_CH008_PUMP_STATION_PARTS | Scene 3 - Bai hoc so 2: Im lang. |
| SCN_CH008_TARGET_PRIORITY | Lesson Three: Choose the Target | LOC_CH008_ABANDONED_BUS_YARD | Teach target priority in a real encounter. | Team searches buses for ammo. | Priority targeting unlocks; Phuc/recruit outcome resolved. | char_trung;comp_hoang;npc_mentor;npc_phuc;npc_lam_recruit;npc_scout | ENM_CH008_BUS_YARD_INFECTED;ENM_CH008_PANIC_FIRE_HAZARD | ITM_CH008_AMMO_CRATE;ITM_CH008_MISSING_AMMO_NOTE | Scene 4 - Bai hoc so 3: Chon muc tieu. |
| SCN_CH008_MENTOR_TOKEN | Mentor's Keepsake | LOC_CH008_COMMAND_ROOM | Reveal a small crack in Mentor's grief. | Team returns with ammo/parts. | Mentor child backstory seed is recorded quietly. | char_trung;npc_mentor | none | ITM_CH008_TOY_CAR;ITM_CH008_AMMO_CRATE | Scene 5 - Mon do cua Mentor. |
| SCN_CH008_ARMORY_LOCKED | The Locked Armory | LOC_CH008_OLD_ARMORY | Test risk assessment and foreshadow Tank/armored infected. | Smith wants the armory opened for ammo. | Tank foreshadow appears; Mentor orders retreat. | char_trung;comp_hoang;npc_mentor;npc_smith;npc_lam_recruit;npc_scout | ENM_CH008_TANK_FORESHADOW;ENM_CH008_ARMORED_INFECTED | ITM_CH008_LOCKED_ARMORY_DOOR;ITM_CH008_ARMORY_INSPECTION_CLUE;ITM_CH008_AMMO_CRATE | Scene 6 - Kho vu khi bi khoa. |
| SCN_CH008_RETREAT_LESSON | Final Lesson: Retreat | LOC_CH008_ARMORY_RETREAT_ROUTE | Define survival as knowing which fights not to win. | Tank/armored infected threatens to break through. | Player retreats and MQ_009 Restore Radio unlocks. | char_trung;comp_hoang;npc_mentor;npc_smith;npc_scout | ENM_CH008_TANK_FORESHADOW | ITM_CH008_RADIO_FILTER_PARTS;ITM_CH008_BATTERY_PACK | Scene 7 - Bai hoc cuoi: Rut lui. |

# Scenes - CH012

Metadata:

- chapterID: CH012
- sourceFilename: chapter_012_nha_tho_khong_chuong.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH012_ROAD_TO_CHURCH | Road to the Church | LOC_CH012_RETREAT_ROUTE;LOC_CH012_SUBURBAN_STREETS | Transition from outpost collapse to church objective. Establish group state, route choice, and Mentor wound. | Group hides in abandoned house after outpost collapse. | Group arrives at church perimeter. | char_trung;comp_hoang;npc_doctor;npc_radio_operator;npc_old_cook;npc_nam | ENM_CH012_EDENROT_STREET_HAZARD | ITM_CH012_EDENROT_RISK_MAP;ITM_CH012_MENTOR_DOG_TAG | Scene 1 - Duong den nha tho. |
| SCN_CH012_SILENT_BELL | Church Without Bells | LOC_CH012_OLD_CHURCH;LOC_CH012_CHURCHYARD | Establish setting and symbol. Negotiate with Priest for entry. | Group reaches church gate. | Priest allows entry through side door. | char_trung;comp_hoang;npc_priest | ENM_CH012_CHURCH_PERIMETER_INFECTED | ITM_CH012_MAI_CHALK;ITM_CH012_CANDLE_SET | Scene 2 - Nha tho khong chuong. |
| SCN_CH012_GIRL_WITNESS | Girl Saved by Mai | LOC_CH012_CATECHISM_ROOM | Lead Trung to Mai through girl witness. Show Mai saved others. | Trung enters catechism room. | Girl leads Trung to prayer shelter basement. | char_trung;comp_hoang;npc_girl | none | ITM_CH012_MAI_CHALK_BROKEN;ITM_CH012_NOAH_MURAL | Scene 3 - Co be duoc Mai cuu. |
| SCN_CH012_REUNION | Reunion | LOC_CH012_PRAYER_SHELTER | Emotional center. Husband and wife reunite; Binh truth emerges. | Trung descends to basement alone. | Couple decides to find Binh together. | char_trung;char_mai | none | ITM_CH012_MAI_CHALK | Scene 4 - Doan tu. |
| SCN_CH012_MAI_TESTIMONY | Mai's Testimony | LOC_CH012_PRAYER_SHELTER | Exposition about Binh's capture and industrial zone location. | Mai begins telling story. | Industrial zone objective unlocks. | char_trung;char_mai;npc_survivor_refugee | none | ITM_CH012_O_TU_NIEU_NOTE | Scene 5 - Loi ke cua Mai. |
| SCN_CH012_WATCHER | Church Under Watch | LOC_CH012_OLD_CHURCH;LOC_CH012_BELL_TOWER;LOC_CH012_NEIGHBORING_STREETS | External threat and urgency. Yellow coat watcher detected. | Hoang spots movement across street. | Group decides to leave immediately. | char_trung;comp_hoang;char_mai;npc_priest | ENM_CH012_YELLOW_COAT_WATCHER | ITM_CH012_YELLOW_CLOTH_FRAGMENT;ITM_CH012_TOBACCO_MARK;ITM_CH012_CHURCH_BELL_ROPE | Scene 6 - Nha tho bi quan sat. |
| SCN_CH012_DEPARTURE | Leaving the Church | LOC_CH012_OLD_CHURCH | Setup Chapter 13. Mai rejoins; group heads to industrial zone. | Group prepares to leave. | Group exits through back gate toward industrial zone. | char_trung;char_mai;comp_hoang;npc_priest | none | ITM_CH012_BINH_SCARF;ITM_CH012_MAI_RECORDING;ITM_CH012_CHURCH_SURVIVOR_LIST | Scene 7 - Roi nha tho. |

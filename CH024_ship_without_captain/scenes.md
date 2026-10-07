# Scenes - CH024

Metadata:

- chapterID: CH024
- sourceFilename: chapter_024_tau_chien_khong_thuyen_truong.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH024_WARSHIP_SHADOW | Warship Shadow | LOC_CH024_NAVAL_BASE | Establish scale of warship and automated threat | Group approaches naval base | Aiko warning replay; Doctor catches EDENROT classification | char_trung;comp_binh;comp_mai;npc_doctor | ENM_CH024_DROWNED_HORDE | none | Scene 1 - Bong Tau Chien. |
| SCN_CH024_MILITARY_PIER | Military Pier | LOC_CH024_MILITARY_PIER | Boarding challenge under automated defense | Codes from Aiko open partial access | Nha Di docks in blind spot; team boards | char_trung;comp_hoang;comp_thu;comp_lam | ENM_CH024_CWS_TURRET;ENM_CH024_CYBER_INFECTED_SAILOR | none | Scene 2 - Cau Tau Quan Su. |
| SCN_CH024_CAPTAIN_QUARTERS | Locked Captain's Quarters | LOC_CH024_CAPTAIN_QUARTERS | Learn tragedy and recover captain authority | Team enters locked quarters | Captain authority token and log recovered; Binh sees photo | char_trung;comp_binh;npc_dead_captain | none | ITM_CH024_CAPTAIN_AUTHORITY_TOKEN;ITM_CH024_CAPTAIN_FAMILY_PHOTO;ITM_CH024_CAPTAIN_FINAL_LOG | Scene 3 - Phong Thuyen Truong Dong Khoa. |
| SCN_CH024_CIC_UNMANNED | Unmanned CIC | LOC_CH024_CIC | Main hack/command sequence | Naval codes + captain token insufficient | Ship AI accepts provisional command; Aster probes system | char_trung;comp_hoang;comp_mai;npc_ship_ai | ENM_CH024_SHIP_AI_DEFENSE | ITM_CH024_NAVAL_CODE_FRAGMENT;ITM_CH024_CAPTAIN_AUTHORITY_TOKEN | Scene 4 - CIC Khong Nguoi. |
| SCN_CH024_AUTOMATED_WEAPONS | Automated Weapons | LOC_CH024_DECK_CWS | Action pressure from turret targeting Nha Di | Turret starts tracking Nha Di | Manual override achieved; cyber-infected cleared | char_trung;comp_hoang;comp_thu;comp_mai;comp_binh | ENM_CH024_CWS_TURRET;ENM_CH024_CYBER_INFECTED_SAILOR | none | Scene 5 - Sung Tu Dong. |
| SCN_CH024_COORDINATES_SENT | Coordinates Sent | LOC_CH024_SIGNAL_CORE | Hoang second betrayal/cliffhanger | Hoang cannot get admin window | Admin window opens; coordinates sent; Hoang hides evidence | comp_hoang | ENM_CH024_ASTER_SIGNAL | ITM_CH024_HOANG_COORDINATE_PACKET | Scene 6 - Toa Do Bi Gui. |
| SCN_CH024_TRUNG_ACCEPTS_WAR | Trung Accepts War | LOC_CH024_CIC | Warship secured with rules | Turret neutralized | Trung assumes provisional command; weapons-safe doctrine; Nha Di docked | char_trung;comp_mai;comp_binh;comp_hoang;npc_ship_ai | none | ITM_CH024_AI_COMPLIANCE_RECORD | Scene 7 - Trung Chap Nhan Chien Tranh. |

# Scenes - CH022

Metadata:

- chapterID: CH022
- sourceFilename: chapter_022_thanh_pho_nguoi_may_chet.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH022_PORT_STILL_RUNNING | Port Still Running | LOC_CH022_APPROACH | Establish dead automated city with cranes still operating | Nha Di follows port array signal | Container drops corpses; Thu needs parts; Hoang needs control center | char_trung;comp_thu;comp_hoang;comp_lam;comp_mai;comp_binh | ENM_CH022_AUTOMATED_CRANE | ITM_CH022_NAVIGATION_MODULE;ITM_CH022_MARINE_BATTERY;ITM_CH022_MARINE_FUEL_FILTER | Scene 1 - Cang Van Chay. |
| SCN_CH022_CAMERA_WATCHING_BINH | Camera Eyes Watching Binh | LOC_CH022_DOCK_GATE | Binh targeted by automated biometric scan | Cameras auto-track group and linger on Binh | Hoang bypasses gate; Binh data flagged but not confirmed | char_trung;comp_mai;comp_binh;comp_hoang | ENM_CH022_BIOMETRIC_SCAN | ITM_CH022_BINH_BIOMETRIC_FLAG | Scene 2 - Mat Camera Nhin Binh. |
| SCN_CH022_ROBOTS_DONT_KNOW | Robots Don't Know The Dead | LOC_CH022_CONTAINER_YARD | Environmental horror and gameplay hazard | Automated forklifts/cranes loading containers | Team crosses yard; manual override used | char_trung;comp_thu;comp_hoang;comp_lam;comp_doctor | ENM_CH022_AUTOMATED_FORKLIFT;ENM_CH022_CONTAINER_DROWNED | ITM_CH022_NAVIGATION_MODULE;ITM_CH022_MARINE_BATTERY;ITM_CH022_MARINE_FUEL_FILTER;ITM_CH022_HULL_PATCH_KIT | Scene 3 - Robot Khong Biet Nguoi Chet. |
| SCN_CH022_ENGINEER_OATH | Engineer Housing And Oath | LOC_CH022_ENGINEER_HOUSING | Humanize dead port through engineer's story | Group finds dead engineer's keycard and logs | Daycare checked; Binh leaves chalk dot on names board | char_trung;comp_mai;comp_binh;comp_hoang | none | ITM_CH022_ENGINEER_KEYCARD;ITM_CH022_ENGINEER_VOICE_LOG | Scene 4 - Khu Ky Su Va Mieng The. |
| SCN_CH022_FLOODED_SERVER | Flooded Server Hall | LOC_CH022_SERVER_HALL | Decode Architect signal and block Binh data | Server hall flooded to ankles; electricity intermittent | Architect signal decoded; Binh data blocked; Aster named | char_trung;comp_hoang;comp_thu;comp_doctor | ENM_CH022_BIOMETRIC_SCAN | ITM_CH022_PORT_ARRAY_DATA;ITM_CH022_BINH_BIOMETRIC_FLAG | Scene 5 - Server Hall Ngap Nuoc. |
| SCN_CH022_CYBERNETIC_INFECTED | Cybernetic Infected | LOC_CH022_EXOSUIT_BAY | First cyber zombie encounter | Infected worker trapped in industrial exosuit | Cybernetic infected defeated by disabling joints and power | char_trung;comp_thu;comp_hoang;comp_binh;comp_doctor | ENM_CH022_CYBERNETIC_INFECTED | none | Scene 6 - Cybernetic Infected. |
| SCN_CH022_TOKYO_SIGNAL | Signal From Japan | LOC_CH022_DEPARTURE | Chapter cliffhanger to Chapter 23 | Group escapes port with parts and data | Tokyo relay signal received; port lights turn on behind them | char_trung;comp_mai;comp_binh;comp_hoang;comp_thu;comp_lam | none | ITM_CH022_PORT_ARRAY_DATA | Scene 7 - Tin Hieu Tu Nhat Ban. |

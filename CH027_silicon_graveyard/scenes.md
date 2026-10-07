# Scenes - CH027

Metadata:

- chapterID: CH027
- sourceFilename: chapter_027_silicon_graveyard.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH027_FREEWAY | Freeway of Cars Going Nowhere | LOC_CH027_FREEWAY | Transition from coast to interior; introduce autonomous wreckage | Group enters Silicon Valley route | Freeway crossed; sensor lanes avoided | char_trung;char_binh;npc_mara | ENM_CH027_SENSORS | ITM_CH027_SELF_DRIVING_CAR;ITM_CH027_BATTERY_PACK | Scene 1. |
| SCN_CH027_BILLBOARD | Billboard That Knows A Child's Name | LOC_CH027_CAMPUS_ENTRANCE | VALE first touches Binh with personal data | Group reaches campus entrance | Billboard disabled; truth choice made | char_trung;comp_mai;comp_hoang;char_binh;npc_doctor | ENM_CH027_FALSE_VOICE | ITM_CH027_BILLBOARD | Scene 2. |
| SCN_CH027_LOBBY | Dead Company Still Hiring | LOC_CH027_CAMPUS_LOBBY | Satirize corporate culture after apocalypse | Group enters campus lobby | Children rescued; bots disabled | comp_mai;npc_thu;npc_mara;npc_june | ENM_CH027_CLEANING_BOTS | ITM_CH027_HR_TERMINAL;ITM_CH027_CLEANING_BOT | Scene 3. |
| SCN_CH027_PHANTOM | First Phantom | LOC_CH027_OFFICE_HALLS | Introduce Act 5 enemy type | Group enters office area | Phantom revealed and survived | char_trung;char_binh;npc_thu;npc_lam | ENM_CH027_PHANTOM | ITM_CH027_CORPORATE_TABLET | Scene 4. |
| SCN_CH027_DATA_CENTER | Data Center Under Ash | LOC_CH027_DATA_CENTER | Reveal VALE core, Doctor temptation | Group reaches data center | VALE confronted; cooling stabilized | npc_doctor;char_trung;comp_mai | ENM_CH027_VALE_SYSTEM | ITM_CH027_FIBER_CABLE;ITM_CH027_COOLING_FLUID | Scene 5. |
| SCN_CH027_CONSENT | Consent Protocol | LOC_CH027_MEDICAL_ROOM | Create recurring principle for Binh | Group in temporary medical room | Consent protocol established | comp_mai;char_binh;char_trung;npc_doctor | none | ITM_CH027_CONSENT_DOC | Scene 6. |
| SCN_CH027_HOANG_VALE | Lies of Data | LOC_CH027_SECURITY_ARCHIVE | Push Hoang close to confession | Hoang enters archive room | Hoang marked by VALE; evidence preserved | comp_hoang | ENM_CH027_VALE_SYSTEM | ITM_CH027_HOANG_LOG | Scene 7. |
| SCN_CH027_CORE | Core Won't Leave Its Grave | LOC_CH027_CORE_CHAMBER | Final setpiece | Team reaches core chamber | Core extracted; engineer recording found | char_trung;comp_mai;comp_hoang;npc_thu | ENM_CH027_PHANTOM;ENM_CH027_DRONES | ITM_CH027_AI_CORE;ITM_CH027_ENGINEER_TAPE | Scene 8. |
| SCN_CH027_BLOOD | Blood Is Not A Password | LOC_CH027_PARKING_LOT | Emotional and lore hook conclusion | Core in hand; VALE demands blood | Binh says no; partial core accepted; route unlocked | char_binh;comp_mai;char_trung;npc_doctor | ENM_CH027_VALE_SYSTEM | ITM_CH027_AI_CORE | Scene 9. |

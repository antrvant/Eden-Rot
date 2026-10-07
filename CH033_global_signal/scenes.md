# Scenes - CH033

Metadata:

- chapterID: CH033
- sourceFilename: chapter_033_tin_hieu_toan_cau.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH033_FOUR_HOURS | Four Hours | LOC_CH033_NORAD_CONTROL | Establish broadcast countdown and 4-hour window. | NORAD satellite window opens. | Broadcast council convenes. | char_trung;comp_mai;comp_binh;npc_thu;npc_doctor;npc_sloane | none | ITM_CH033_SIGNAL_MAP | Scene 1. |
| SCN_CH033_WHO_SPEAKS | Who Speaks | LOC_CH033_INTAKE_TUNNEL | Decide voice and content legitimacy. | Council convenes. | Message priorities built. | char_trung;comp_mai;comp_binh;npc_doctor;npc_ada;npc_eli | none | ITM_CH033_BROADCAST_DRAFT | Scene 2. |
| SCN_CH033_PROMISE_DEBT | Promise Has Debt | LOC_CH033_QUIET_ROOM | Trung/Mai/Binh emotional core on promise vs lie. | Trung drafts message. | Promise accepted with debt. | char_trung;comp_mai;comp_binh | none | ITM_CH033_BROADCAST_DRAFT | Scene 3. |
| SCN_CH033_TRANSLATE | Translate the Promise | LOC_CH033_TRANSLATION_CORNER | Make broadcast multilingual and inclusive. | Survivors contribute languages. | Child safety warning added. | comp_mai;npc_doctor;npc_june;npc_noah;npc_mother_elian | none | ITM_CH033_MULTILINGUAL_PACKET;ITM_CH033_CHILD_SAFETY_WARNING | Scene 4. |
| SCN_CH033_WEAK_SIGNALS | Weak Signals | LOC_CH033_LISTEN_DECK | Hear world alive and classify signals. | Incoming signals detected. | Map populated with markers. | npc_thu;comp_mai;npc_doctor | ENM_CH033_FALSE_DISTRESS | ITM_CH033_SIGNAL_MAP | Scene 5. |
| SCN_CH033_LISTENER | The Listener | LOC_CH033_SATELLITE_RELAY | Architect listener escalates. | VALE detects non-human listener. | Metadata stripped, broadcast continues. | npc_thu;npc_sloane;char_trung;comp_mai | ENM_CH033_VALE_LISTENER;ENM_CH033_VALE_METADATA | ITM_CH033_PROMISE_METADATA | Scene 6. |
| SCN_CH033_BROADCAST | Rebirth Calls | LOC_CH033_BROADCAST_ROOM | Main emotional climax. | Message assembled. | Signal transmitted. | char_trung;comp_mai;comp_binh | ENM_CH033_TIME_PRESSURE | ITM_CH033_BROADCAST_DRAFT;ITM_CH033_PROMISE_METADATA | Scene 7. |
| SCN_CH033_WORLD_ANSWERS | World Answers | LOC_CH033_NORAD_CONTROL | Hope payoff. | Broadcast sent. | Responses archived. | char_trung;comp_mai;comp_binh;npc_thu;npc_doctor | none | ITM_CH033_RESPONSE_ARCHIVE;ITM_CH033_SIGNAL_MAP | Scene 8. |
| SCN_CH033_TERRAFORM_MAP | Terraforming Map | LOC_CH033_NORAD_CONTROL | Cliffhanger to Chapter 34. | Responses received. | Next front decision unlocked. | npc_doctor;comp_mai;char_trung | ENM_CH033_ARCHITECT_LISTENER | ITM_CH033_TERRAFORM_MAP_FRAGMENT | Scene 9. |

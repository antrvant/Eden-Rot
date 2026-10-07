# Scenes - CH036

Metadata:

- chapterID: CH036
- sourceFilename: chapter_036_paris_khong_anh_den.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH036_FROZEN_PARIS | City Without Light | LOC_CH036_FROZEN_RAIL | Establish Paris aboveground as dark landmark. | Group arrives at frozen Paris outskirts. | Metro entrance located; Amelie radio contact. | char_mai;char_trung;char_binh;char_thu | ENM_CH036_ICE_HORDE_PATROL | ITM_CH036_AMBER_FLARE | Scene 1 - Thanh Pho Khong Anh Den. |
| SCN_CH036_ATTENDANCE_GATE | Attendance Password | LOC_CH036_METRO_ENTRANCE | Verify trust with Amelie using child-safety phrase. | Group reaches metro entrance. | Gate opens; group enters metro. | char_mai;char_binh;char_teacher_amelie | none | ITM_CH036_CHILD_SAFETY_PHRASE | Scene 2 - Mat Khau Diem Danh. |
| SCN_CH036_METRO_CLASSROOM | Classroom Under the Platform | LOC_CH036_METRO_SCHOOL | Emotional center: Mai/Amelie connection; Binh attends class. | Group enters metro school shelter. | Roll call complete; Mai sees education as resistance. | char_mai;char_binh;char_trung;char_teacher_amelie;char_june | none | ITM_CH036_ATTENDANCE_LEDGER | Scene 3 - Lop Hoc Duoi Ham. |
| SCN_CH036_SHELTER_LIMITS | Limits of the Classroom | LOC_CH036_SHELTER_STORAGE | Show cost of keeping school alive; archive vault revealed. | After roll call. | Archive location known; Mimic warning given. | char_mai;char_teacher_amelie;char_celine | none | ITM_CH036_RESEARCH_COURIER_CACHE | Scene 4 - Gioi Han Cua Lop Hoc. |
| SCN_CH036_MIMIC_LURE | Voice in the Tunnel | LOC_CH036_SERVICE_TUNNEL | Introduce Mimic encounter with sound lure. | Group traverses service tunnel. | Mimic revealed and retreats; voice rule learned. | char_mai;char_binh;char_trung;char_teacher_amelie;npc_mathis;npc_mimic | ENM_CH036_MIMIC | ITM_CH036_SCARF_YELLOW;ITM_CH036_AMBER_FLARE | Scene 5 - Giong Noi Trong Ham. |
| SCN_CH036_ARCHIVE_VAULT | Library Under the Station | LOC_CH036_STATION_LIBRARY | Retrieve Patient Zero archive from courier cache. | Group reaches station library. | Archive recovered; flood begins. | char_doctor;char_celine;char_binh;char_june | none | ITM_CH036_PATIENT_ZERO_ARCHIVE;ITM_CH036_CATALOG_CARD_ORION;ITM_CH036_CATALOG_CARD_ANDROMEDA | Scene 6 - Thu Vien Duoi Ga. |
| SCN_CH036_FALSE_ATTENDANCE | False Attendance | LOC_CH036_PLATFORM_CORRIDOR | Mimic escalates using attendance names. | Mimic uses station speakers. | Group call-and-response breaks trap. | char_mai;char_trung;char_binh;char_teacher_amelie;npc_mimic | ENM_CH036_MIMIC | none | Scene 7 - Diem Danh Sai. |
| SCN_CH036_ARCHIVE_RUN | Archive Run | LOC_CH036_FLOODED_TUNNEL | Action climax: ice horde breach, archive extraction. | Ice horde enters metro. | Archive and children evacuated. | char_trung;char_doctor;char_mai;char_binh | ENM_CH036_ICE_HORDE_REMNANTS;ENM_CH036_MIMIC | ITM_CH036_PATIENT_ZERO_ARCHIVE | Scene 8 - Archive Run. |
| SCN_CH036_ALPS_HOOK | Patient Zero Goes to the Mountains | LOC_CH036_SHELTER_AFTER | Resolution and Chapter 37 hook. | Battle ends. | Swiss route confirmed; Binh senses Alps call. | char_mai;char_trung;char_binh;char_doctor;char_teacher_amelie | none | ITM_CH036_ARCHIVE_KEY_COPY;ITM_CH036_ALPINE_ROUTE_MAP | Scene 9 - Patient Zero Di Ve Nui. |

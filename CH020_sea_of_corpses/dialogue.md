# Dialogue - CH020

Metadata:

- chapterID: CH020
- sourceFilename: chapter_020_bien_dong_day_xac.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH020_WORKER_LEAD_JUDGMENT_001 | npc_worker_lead | STATE_HOANG_JUDGMENT | Kill him, we lose the skill. Spare him, we lose trust. | none | none | council_meeting | DT_087. |
| DLG_CH020_HOANG_JUDGMENT_001 | comp_hoang | STATE_HOANG_JUDGMENT | Sounds like I still have value then. | none | none | council_meeting | DT_087. |
| DLG_CH020_MAI_JUDGMENT_001 | char_mai | STATE_HOANG_JUDGMENT | Value is not forgiveness. | none | none | council_meeting | DT_087. |
| DLG_CH020_TRUNG_JUDGMENT_001 | char_trung | STATE_HOANG_JUDGMENT | Hoang comes with us. Monitored. No command authority. No weapons without direct order. Not near children alone. | none | set_flag:FLAG_CH020_HOANG_MONITORED_COMPANION | council_meeting | DT_087. |
| DLG_CH020_BINH_JUDGMENT_001 | char_binh | STATE_HOANG_JUDGMENT | Is this forgiveness? | none | none | council_meeting | DT_087. |
| DLG_CH020_TRUNG_JUDGMENT_002 | char_trung | STATE_HOANG_JUDGMENT | No. This is not finished yet. | none | none | council_meeting | DT_087. |
| DLG_CH020_HOANG_JUDGMENT_002 | comp_hoang | STATE_HOANG_JUDGMENT | That is worse than being shot. | none | none | council_meeting | DT_087. |
| DLG_CH020_TRUNG_JUDGMENT_003 | char_trung | STATE_HOANG_JUDGMENT | Good. | none | none | council_meeting | DT_087. |
| DLG_CH020_BINH_BOARD_001 | char_binh | STATE_CLASSROOM_GOODBYE | If I leave my name here, will it get lost? | none | none | classroom_farewell | DT_088. |
| DLG_CH020_MAI_BOARD_001 | char_mai | STATE_CLASSROOM_GOODBYE | Rain might wash it away. Someone else might write over it. | none | none | classroom_farewell | DT_088. |
| DLG_CH020_BINH_BOARD_002 | char_binh | STATE_CLASSROOM_GOODBYE | Then should I erase it? | none | none | classroom_farewell | DT_088. |
| DLG_CH020_TRUNG_BOARD_001 | char_trung | STATE_CLASSROOM_GOODBYE | You can leave it and still carry it with you. | none | none | classroom_farewell | DT_088. |
| DLG_CH020_BINH_BOARD_003 | char_binh | STATE_CLASSROOM_GOODBYE | Can one name be in two places? | none | none | classroom_farewell | DT_088. |
| DLG_CH020_MAI_BOARD_002 | char_mai | STATE_CLASSROOM_GOODBYE | Yes. One place to remember you lived. One place to remember you are still alive. | none | set_flag:FLAG_CH020_BINH_LEFT_NAME_ON_BOARD | classroom_farewell | DT_088. |
| DLG_CH020_SO4_BOARD_001 | npc_so_4 | STATE_CLASSROOM_GOODBYE | What if I do not have a name yet? | none | none | classroom_farewell | DT_088. |
| DLG_CH020_BINH_BOARD_004 | char_binh | STATE_CLASSROOM_GOODBYE | Leave a dot. When you remember, write more. | none | none | classroom_farewell | DT_088. |
| DLG_CH020_LAM_RIVER_001 | npc_lam | STATE_RIVER_NEGOTIATION | Children, hunted people, a man in chains. You are a whole storm. | none | none | ferry_dock | DT_089. |
| DLG_CH020_MAI_RIVER_001 | char_mai | STATE_RIVER_NEGOTIATION | We do not sell ourselves as heavy cargo. | none | none | ferry_dock | DT_089. |
| DLG_CH020_LAM_RIVER_002 | npc_lam | STATE_RIVER_NEGOTIATION | At least you tell the truth. | none | none | ferry_dock | DT_089. |
| DLG_CH020_TRUNG_RIVER_001 | char_trung | STATE_RIVER_NEGOTIATION | We need to cross. What is the price? | none | none | ferry_dock | DT_089. |
| DLG_CH020_LAM_RIVER_003 | npc_lam | STATE_RIVER_NEGOTIATION | A promise. If you reach the sea and see a ship named Mê Linh, ask if anyone named Lam is still alive. | none | set_flag:FLAG_CH020_LAM_PROMISE_MADE | ferry_dock | DT_089. |
| DLG_CH020_HOANG_RIVER_001 | comp_hoang | STATE_RIVER_NEGOTIATION | Promises do not run engines. | none | none | ferry_dock | DT_089. |
| DLG_CH020_LAM_RIVER_004 | npc_lam | STATE_RIVER_NEGOTIATION | No. But they decide whether the river pilot throws you overboard. | none | none | ferry_dock | DT_089. |
| DLG_CH020_BINH_SEA_001 | char_binh | STATE_SEA_FIRST_VIEW | The sea is bigger than every place I was ever scared of. | none | none | coast_departure | DT_090. |
| DLG_CH020_TRUNG_SEA_001 | char_trung | STATE_SEA_FIRST_VIEW | Mm-hmm. | none | none | coast_departure | DT_090. |
| DLG_CH020_BINH_SEA_002 | char_binh | STATE_SEA_FIRST_VIEW | You are not going to say I do not need to be scared? | none | none | coast_departure | DT_090. |
| DLG_CH020_TRUNG_SEA_002 | char_trung | STATE_SEA_FIRST_VIEW | No. I am scared too. | none | none | coast_departure | DT_090. |
| DLG_CH020_MAI_SEA_001 | char_mai | STATE_SEA_FIRST_VIEW | The difference is this time we are scared on the same ship. | none | none | coast_departure | DT_090. |
| DLG_CH020_BINH_SEA_003 | char_binh | STATE_SEA_FIRST_VIEW | Is the ship home? | none | none | coast_departure | DT_090. |
| DLG_CH020_TRUNG_SEA_003 | char_trung | STATE_SEA_FIRST_VIEW | Not yet. But we can practice. | none | set_flag:FLAG_CH020_VIETNAM_COAST_DEPARTED | coast_departure | DT_090. |
| DLG_CH020_THU_STORM_001 | npc_thu | STATE_BIO_STORM | Kill the lights! Do not let it see the waves! | none | set_flag:FLAG_CH020_BIO_STORM_ENCOUNTERED | bio_storm | DT_091. |
| DLG_CH020_DOCTOR_STORM_001 | npc_doctor | STATE_BIO_STORM | What is "it"? | none | none | bio_storm | DT_091. |
| DLG_CH020_LAM_STORM_001 | npc_lam | STATE_BIO_STORM | The sea when it runs a fever. | none | none | bio_storm | DT_091. |
| DLG_CH020_HOANG_STORM_001 | comp_hoang | STATE_BIO_STORM | Seas do not run fevers. | none | none | bio_storm | DT_091. |
| DLG_CH020_LAM_STORM_002 | npc_lam | STATE_BIO_STORM | This one does. | none | set_flag:FLAG_CH020_MARITIME_EDENROT_ZONE_ENTERED | bio_storm | DT_091. |
| DLG_CH020_THU_STORM_002 | npc_thu | STATE_BIO_STORM | Living Edenrot. Not stains. It is listening. | none | set_flag:FLAG_CH020_EDENROT_COASTAL_BLOOM_CLASSIFIED | bio_storm | DT_091. |
| DLG_CH020_BINH_STORM_001 | char_binh | STATE_BIO_STORM | Is that voice in my blood? | none | none | bio_storm | DT_091. |
| DLG_CH020_DOCTOR_STORM_002 | npc_doctor | STATE_BIO_STORM | Possibly the same language. | none | set_flag:FLAG_CH020_EDEN_NODE_ACTIVE_SIGNAL | bio_storm | DT_091. |
| DLG_CH020_TRUNG_STORM_001 | char_trung | STATE_BIO_STORM | Hold the ship. Talk language later. | none | set_flag:FLAG_CH020_UNKNOWN_ISLAND_FORCED | bio_storm | DT_091. |

# Dialogue - CH022

Metadata:

- chapterID: CH022
- sourceFilename: chapter_022_thanh_pho_nguoi_may_chet.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH022_097_PORT_AI_001 | npc_port_ai | STATE_CAMERA_FLAG | Biometric anomaly detected. Child profile flagged. | none | set_flag:FLAG_CH022_BINH_DATA_FLAGGED | camera_scan | DT_097. |
| DLG_CH022_097_BINH_001 | comp_binh | STATE_CAMERA_FLAG | Why is it calling me? | none | none | camera_scan | DT_097. |
| DLG_CH022_097_MAI_001 | comp_mai | STATE_CAMERA_FLAG | It sees a part of you. It does not know you. | none | none | camera_scan | DT_097. |
| DLG_CH022_097_PORT_AI_002 | npc_port_ai | STATE_CAMERA_FLAG | Confirm asset category. | none | none | camera_scan | DT_097. |
| DLG_CH022_097_HOANG_001 | comp_hoang | STATE_CAMERA_FLAG | Not pressing. | none | set_flag:FLAG_CH022_HOANG_HACK_TRANSPARENCY | camera_scan | DT_097. |
| DLG_CH022_097_TRUNG_001 | char_trung | STATE_CAMERA_FLAG | Say it clearly. | none | none | camera_scan | DT_097. |
| DLG_CH022_097_HOANG_002 | comp_hoang | STATE_CAMERA_FLAG | I am not pressing confirm. I am redirecting camera to a wide profile. | none | none | camera_scan | DT_097. |
| DLG_CH022_097_BINH_002 | comp_binh | STATE_CAMERA_FLAG | Can machines lie? | none | none | camera_scan | DT_097. |
| DLG_CH022_097_MAI_002 | comp_mai | STATE_CAMERA_FLAG | Machines only read what they are taught. People lie. | none | none | camera_scan | DT_097. |
| DLG_CH022_097_HOANG_003 | comp_hoang | STATE_CAMERA_FLAG | And people choose not to follow orders. | none | none | camera_scan | DT_097. |
| DLG_CH022_098_THU_001 | comp_thu | STATE_ROBOT_BODIES | It is loading corpses like cargo. | none | none | forklift_encounter | DT_098. |
| DLG_CH022_098_LAM_001 | comp_lam | STATE_ROBOT_BODIES | Machines do not know souls are heavier than containers. | none | none | forklift_encounter | DT_098. |
| DLG_CH022_098_HOANG_001 | comp_hoang | STATE_ROBOT_BODIES | It knows orders. Orders say cargo. | none | none | forklift_encounter | DT_098. |
| DLG_CH022_098_MAI_001 | comp_mai | STATE_ROBOT_BODIES | Who wrote the orders? | none | none | forklift_encounter | DT_098. |
| DLG_CH022_098_HOANG_002 | comp_hoang | STATE_ROBOT_BODIES | The people who died. | none | none | forklift_encounter | DT_098. |
| DLG_CH022_098_TRUNG_001 | char_trung | STATE_ROBOT_BODIES | Then the living fix it. | none | none | forklift_encounter | DT_098. |
| DLG_CH022_099_HOANG_001 | comp_hoang | STATE_HACK_TRANSPARENCY | I need admin access. | none | none | server_hack | DT_099. |
| DLG_CH022_099_TRUNG_001 | char_trung | STATE_HACK_TRANSPARENCY | Say every step. | none | none | server_hack | DT_099. |
| DLG_CH022_099_HOANG_002 | comp_hoang | STATE_HACK_TRANSPARENCY | Opening shell. Reading log. Copying route. Blocking outbound queue. | none | set_flag:FLAG_CH022_HOANG_HACK_TRANSPARENCY | server_hack | DT_099. |
| DLG_CH022_099_DOCTOR_001 | comp_doctor | STATE_HACK_TRANSPARENCY | Which queue? | none | none | server_hack | DT_099. |
| DLG_CH022_099_HOANG_003 | comp_hoang | STATE_HACK_TRANSPARENCY | Sending child anomaly data. Binh. | none | none | server_hack | DT_099. |
| DLG_CH022_099_MAI_001 | comp_mai | STATE_HACK_TRANSPARENCY | Delete it. | none | none | server_hack | DT_099. |
| DLG_CH022_099_HOANG_004 | comp_hoang | STATE_HACK_TRANSPARENCY | Deleting may lose evidence of who received it. | none | none | server_hack | DT_099. |
| DLG_CH022_099_TRUNG_002 | char_trung | STATE_HACK_TRANSPARENCY | Block first. Copy evidence. Do not send more. | none | set_flag:FLAG_CH022_BINH_DATA_OUTBOUND_BLOCKED | server_hack | DT_099. |
| DLG_CH022_099_HOANG_005 | comp_hoang | STATE_HACK_TRANSPARENCY | Understood. Block first. Copy. No sending. | none | none | server_hack | DT_099. |
| DLG_CH022_100_BINH_001 | comp_binh | STATE_CYBER_FIGHT | It was made to work after dying. | none | none | cybernetic_combat | DT_100. |
| DLG_CH022_100_THU_001 | comp_thu | STATE_CYBER_FIGHT | Exosuit keeps it standing. | none | none | cybernetic_combat | DT_100. |
| DLG_CH022_100_TRUNG_001 | char_trung | STATE_CYBER_FIGHT | Headshot? | none | none | cybernetic_combat | DT_100. |
| DLG_CH022_100_HOANG_001 | comp_hoang | STATE_CYBER_FIGHT | Not enough. Suit auto-balances. | none | none | cybernetic_combat | DT_100. |
| DLG_CH022_100_THU_002 | comp_thu | STATE_CYBER_FIGHT | Knee joints, back battery, shoulder control cables. | none | none | cybernetic_combat | DT_100. |
| DLG_CH022_100_MAI_001 | comp_mai | STATE_CYBER_FIGHT | Do not let it reach Binh. | none | none | cybernetic_combat | DT_100. |
| DLG_CH022_100_HOANG_002 | comp_hoang | STATE_CYBER_FIGHT | This time I know. | none | none | cybernetic_combat | DT_100. |
| DLG_CH022_101_RADIO_001 | npc_radio_operator | STATE_TOKYO_SIGNAL | Tokyo relay requesting naval codes... | none | set_flag:FLAG_CH022_TOKYO_RELAY_SIGNAL_RECEIVED | departure | DT_101. |
| DLG_CH022_101_VOICE_001 | npc_radio_operator | STATE_TOKYO_SIGNAL | If anyone human hears this... do not come in black rain... | none | none | departure | DT_101. |
| DLG_CH022_101_MAI_001 | comp_mai | STATE_TOKYO_SIGNAL | If they say do not come, maybe they are warning. | none | none | departure | DT_101. |
| DLG_CH022_101_HOANG_001 | comp_hoang | STATE_TOKYO_SIGNAL | In this world, warning and trap often share the same frequency. | none | none | departure | DT_101. |
| DLG_CH022_101_TRUNG_001 | char_trung | STATE_TOKYO_SIGNAL | Keep listening. | none | none | departure | DT_101. |
| DLG_CH022_101_BINH_001 | comp_binh | STATE_TOKYO_SIGNAL | Is Tokyo far? | none | none | departure | DT_101. |
| DLG_CH022_101_LAM_001 | comp_lam | STATE_TOKYO_SIGNAL | Farther than where you were just scared. Closer than what comes next. | none | none | departure | DT_101. |

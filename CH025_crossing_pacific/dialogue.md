# Dialogue - CH025

Metadata:

- chapterID: CH025
- sourceFilename: chapter_025_vuot_thai_binh_duong.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH025_AI_VESSEL_001 | npc_ship_ai | STATE_VESSEL_HIERARCHY | Designate civilian vessel status. | none | none | ship_organization | DT_112. |
| DLG_CH025_TRUNG_VESSEL_001 | char_trung | STATE_VESSEL_HIERARCHY | Protected. | none | none | ship_organization | DT_112. |
| DLG_CH025_AI_VESSEL_002 | npc_ship_ai | STATE_VESSEL_HIERARCHY | Cargo? | none | none | ship_organization | DT_112. |
| DLG_CH025_MAI_VESSEL_001 | comp_mai | STATE_VESSEL_HIERARCHY | Home. | none | none | ship_organization | DT_112. |
| DLG_CH025_AI_VESSEL_003 | npc_ship_ai | STATE_VESSEL_HIERARCHY | Category unknown. | none | none | ship_organization | DT_112. |
| DLG_CH025_HOANG_VESSEL_001 | comp_hoang | STATE_VESSEL_HIERARCHY | We can create a new category. | none | none | ship_organization | DT_112. |
| DLG_CH025_TRUNG_VESSEL_002 | char_trung | STATE_VESSEL_HIERARCHY | New category. Nha Di: protected home vessel. Not cargo. | none | set_flag:FLAG_CH025_NHA_DI_PROTECTED_HOME | ship_organization | DT_112. |
| DLG_CH025_BINH_VESSEL_001 | comp_binh | STATE_VESSEL_HIERARCHY | Do you understand home? | none | none | ship_organization | DT_112. |
| DLG_CH025_AI_VESSEL_004 | npc_ship_ai | STATE_VESSEL_HIERARCHY | Definition required. | none | none | ship_organization | DT_112. |
| DLG_CH025_MAI_VESSEL_002 | comp_mai | STATE_VESSEL_HIERARCHY | Something that people do not get turned into things to store. | none | set_flag:FLAG_CH025_NHA_DI_DEFINITION_STORED | ship_organization | DT_112. |
| DLG_CH025_AI_VESSEL_005 | npc_ship_ai | STATE_VESSEL_HIERARCHY | Definition stored. | none | none | ship_organization | DT_112. |
| DLG_CH025_HOANG_WEAPONS_001 | comp_hoang | STATE_WEAPONS_DOCTRINE | Manual-only is too slow. | none | none | weapons_ethics | DT_113. |
| DLG_CH025_MAI_WEAPONS_001 | comp_mai | STATE_WEAPONS_DOCTRINE | Slow is the price of conscience. | none | none | weapons_ethics | DT_113. |
| DLG_CH025_HOANG_WEAPONS_002 | comp_hoang | STATE_WEAPONS_DOCTRINE | The horde will not wait for conscience to boot. | none | none | weapons_ethics | DT_113. |
| DLG_CH025_TRUNG_WEAPONS_001 | char_trung | STATE_WEAPONS_DOCTRINE | Automated weapons do not fire on people. Do not fire near Nha Di. Do not fire without human witness. | none | set_flag:FLAG_CH025_DOCTRINE_RULE_1 | weapons_ethics | DT_113. |
| DLG_CH025_DOCTOR_WEAPONS_001 | npc_doctor | STATE_WEAPONS_DOCTRINE | And when AI asks about edge cases? | none | none | weapons_ethics | DT_113. |
| DLG_CH025_TRUNG_WEAPONS_002 | char_trung | STATE_WEAPONS_DOCTRINE | It asks. We answer. We do not let it write ethics on its own. | none | set_flag:FLAG_CH025_DOCTRINE_RULE_2 | weapons_ethics | DT_113. |
| DLG_CH025_BINH_WEAPONS_001 | comp_binh | STATE_WEAPONS_DOCTRINE | Can guns say sorry? | none | none | weapons_ethics | DT_113. |
| DLG_CH025_THU_WEAPONS_001 | comp_thu | STATE_WEAPONS_DOCTRINE | No. | none | none | weapons_ethics | DT_113. |
| DLG_CH025_BINH_WEAPONS_002 | comp_binh | STATE_WEAPONS_DOCTRINE | Then the person pressing the button must speak before pressing. | none | set_flag:FLAG_CH025_BINH_BUTTON_RULE | weapons_ethics | DT_113. |
| DLG_CH025_BINH_NIGHT_001 | comp_binh | STATE_CALM_NIGHT | Can tomorrow wait? | none | none | calm_night | DT_114. |
| DLG_CH025_TRUNG_NIGHT_001 | char_trung | STATE_CALM_NIGHT | I want to say yes. | none | none | calm_night | DT_114. |
| DLG_CH025_MAI_NIGHT_001 | comp_mai | STATE_CALM_NIGHT | Tonight does. | none | none | calm_night | DT_114. |
| DLG_CH025_BINH_NIGHT_002 | comp_binh | STATE_CALM_NIGHT | How long is tonight? | none | none | calm_night | DT_114. |
| DLG_CH025_MAI_NIGHT_002 | comp_mai | STATE_CALM_NIGHT | As long as one warm bowl of porridge and three more questions. | none | none | calm_night | DT_114. |
| DLG_CH025_TRUNG_NIGHT_002 | char_trung | STATE_CALM_NIGHT | Only three? | none | none | calm_night | DT_114. |
| DLG_CH025_BINH_NIGHT_003 | comp_binh | STATE_CALM_NIGHT | Four. I am saving one for when I am scared. | none | set_flag:FLAG_CH025_FAMILY_CALM_NIGHT | calm_night | DT_114. |
| DLG_CH025_SYSTEM_PING_001 | npc_ship_ai | STATE_SATELLITE_PING | Correction coordinate refinement received. | none | set_flag:FLAG_CH025_SATELLITE_THREAT_UNLOCKED | satellite_detection | DT_115. |
| DLG_CH025_HOANG_PING_001 | comp_hoang | STATE_SATELLITE_PING | No... | none | none | satellite_detection | DT_115. |
| DLG_CH025_THU_PING_001 | comp_thu | STATE_SATELLITE_PING | What? | none | none | satellite_detection | DT_115. |
| DLG_CH025_HOANG_PING_002 | comp_hoang | STATE_SATELLITE_PING | Satellite signal. It is refining route. | none | none | satellite_detection | DT_115. |
| DLG_CH025_THU_PING_002 | comp_thu | STATE_SATELLITE_PING | From where? | none | none | satellite_detection | DT_115. |
| DLG_CH025_HOANG_PING_003 | comp_hoang | STATE_SATELLITE_PING | From... yesterday's admin window. | none | set_flag:FLAG_CH025_HOANG_SEES_CONSEQUENCE | satellite_detection | DT_115. |
| DLG_CH025_THU_PING_003 | comp_thu | STATE_SATELLITE_PING | Window or price? | none | none | satellite_detection | DT_115. |
| DLG_CH025_HOANG_PING_004 | comp_hoang | STATE_SATELLITE_PING | Now is not the time. | none | none | satellite_detection | DT_115. |
| DLG_CH025_THU_PING_004 | comp_thu | STATE_SATELLITE_PING | With you it is never the time until it explodes. | none | none | satellite_detection | DT_115. |
| DLG_CH025_ASTER_HORDE_001 | npc_aster | STATE_SEA_HORDE | Correction vector converging. | none | set_flag:FLAG_CH025_SEA_HORDE_SUMMONED | sea_horde | DT_116. |
| DLG_CH025_TRUNG_HORDE_001 | char_trung | STATE_SEA_HORDE | Kill channel. | none | none | sea_horde | DT_116. |
| DLG_CH025_HOANG_HORDE_001 | comp_hoang | STATE_SEA_HORDE | Cannot kill underwater signal. | none | none | sea_horde | DT_116. |
| DLG_CH025_DOCTOR_HORDE_001 | npc_doctor | STATE_SEA_HORDE | They are responding to the pulse. | none | none | sea_horde | DT_116. |
| DLG_CH025_AI_HORDE_001 | npc_ship_ai | STATE_SEA_HORDE | Recommend autonomous lethal defense. | none | none | sea_horde | DT_116. |
| DLG_CH025_MAI_HORDE_001 | comp_mai | STATE_SEA_HORDE | Denied. | none | none | sea_horde | DT_116. |
| DLG_CH025_AI_HORDE_002 | npc_ship_ai | STATE_SEA_HORDE | Survival probability reduced. | none | none | sea_horde | DT_116. |
| DLG_CH025_TRUNG_HORDE_002 | char_trung | STATE_SEA_HORDE | Conscience probability increased. | none | set_flag:FLAG_CH025_AUTONOMOUS_DEFENSE_REJECTED | sea_horde | DT_116. |
| DLG_CH025_HOANG_HORDE_002 | comp_hoang | STATE_SEA_HORDE | That is not a real metric. | none | none | sea_horde | DT_116. |
| DLG_CH025_TRUNG_HORDE_003 | char_trung | STATE_SEA_HORDE | Then we make it one. | none | none | sea_horde | DT_116. |

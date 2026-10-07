# Dialogue - CH026

Metadata:

- chapterID: CH026
- sourceFilename: chapter_026_bo_tay_khong_con_mat_troi.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH026_BINH_COAST_001 | comp_binh | STATE_WEST_COAST | Is this morning or still night? | none | none | landfall | DT_117. |
| DLG_CH026_LAM_COAST_001 | comp_lam | STATE_WEST_COAST | This is smoke. | none | none | landfall | DT_117. |
| DLG_CH026_BINH_COAST_002 | comp_binh | STATE_WEST_COAST | Where is the sun? | none | none | landfall | DT_117. |
| DLG_CH026_MAI_COAST_001 | comp_mai | STATE_WEST_COAST | It is behind everything that people and Eden burned. | none | none | landfall | DT_117. |
| DLG_CH026_TRUNG_COAST_001 | char_trung | STATE_WEST_COAST | We will find a way through. | none | none | landfall | DT_117. |
| DLG_CH026_BINH_COAST_003 | comp_binh | STATE_WEST_COAST | What if everywhere has no sun? | none | none | landfall | DT_117. |
| DLG_CH026_MAI_COAST_002 | comp_mai | STATE_WEST_COAST | Then we bring our own light. Not enough, but it is a start. | none | set_flag:FLAG_CH026_MAI_LIGHT_ANCHOR | landfall | DT_117. |
| DLG_CH026_MARA_CONTACT_001 | npc_mara | STATE_FIRST_CONTACT | Warship, foreign guns, kids on board. You occupying, trading, or running? | none | none | first_contact | DT_118. |
| DLG_CH026_MAI_CONTACT_001 | comp_mai | STATE_FIRST_CONTACT | Maybe all three if we are not careful. So we start with names. | none | none | first_contact | DT_118. |
| DLG_CH026_MARA_CONTACT_002 | npc_mara | STATE_FIRST_CONTACT | Names do not lower guns. | none | none | first_contact | DT_118. |
| DLG_CH026_TRUNG_CONTACT_001 | char_trung | STATE_FIRST_CONTACT | We can. | none | none | first_contact | DT_118. |
| DLG_CH026_MARA_CONTACT_003 | npc_mara | STATE_FIRST_CONTACT | Why should I believe you? | none | none | first_contact | DT_118. |
| DLG_CH026_MAI_CONTACT_002 | comp_mai | STATE_FIRST_CONTACT | You should not yet. Trust that we know we have to earn it. | none | set_flag:FLAG_CH026_MARA_CONTACT | first_contact | DT_118. |
| DLG_CH026_MARA_NAME_001 | npc_mara | STATE_REBIRTH_NAME | What are you people? | none | none | rebirth_name | DT_119. |
| DLG_CH026_MAI_NAME_001 | comp_mai | STATE_REBIRTH_NAME | Survivors who got tired of only surviving. | none | none | rebirth_name | DT_119. |
| DLG_CH026_HOANG_NAME_001 | comp_hoang | STATE_REBIRTH_NAME | That sounds like a poster. | none | none | rebirth_name | DT_119. |
| DLG_CH026_MAI_NAME_002 | comp_mai | STATE_REBIRTH_NAME | Rebirth Alliance. | none | set_flag:FLAG_CH026_REBIRTH_ALLIANCE_NAMED | rebirth_name | DT_119. |
| DLG_CH026_MARA_NAME_002 | npc_mara | STATE_REBIRTH_NAME | Alliance with who? | none | none | rebirth_name | DT_119. |
| DLG_CH026_TRUNG_NAME_001 | char_trung | STATE_REBIRTH_NAME | Anyone who can follow rules before taking power. | none | none | rebirth_name | DT_119. |
| DLG_CH026_MARA_NAME_003 | npc_mara | STATE_REBIRTH_NAME | Good luck finding Americans like that. | none | none | rebirth_name | DT_119. |
| DLG_CH026_BINH_DRONE_001 | comp_binh | STATE_DRONE_TRACKING | Does it know my name? | none | none | drone_tracking | DT_120. |
| DLG_CH026_HOANG_DRONE_001 | comp_hoang | STATE_DRONE_TRACKING | It knows direction. | none | none | drone_tracking | DT_120. |
| DLG_CH026_TRUNG_DRONE_001 | char_trung | STATE_DRONE_TRACKING | Direction? | none | none | drone_tracking | DT_120. |
| DLG_CH026_HOANG_DRONE_002 | comp_hoang | STATE_DRONE_TRACKING | Signal. Pattern. | none | none | drone_tracking | DT_120. |
| DLG_CH026_MAI_DRONE_001 | comp_mai | STATE_DRONE_TRACKING | Hoang. | none | none | drone_tracking | DT_120. |
| DLG_CH026_HOANG_DRONE_003 | comp_hoang | STATE_DRONE_TRACKING | ... | none | none | drone_tracking | DT_120. |
| DLG_CH026_BINH_DRONE_002 | comp_binh | STATE_DRONE_TRACKING | Who showed it direction? | none | none | drone_tracking | DT_120. |
| DLG_CH026_HOANG_DRONE_004 | comp_hoang | STATE_DRONE_TRACKING | Do not know yet. | none | set_flag:FLAG_CH026_DRONE_TRACKED_BINH | drone_tracking | DT_120. |
| DLG_CH026_HOANG_CONFESS_001 | comp_hoang | STATE_CONFESSION | Trung, the satellite signal did not find us naturally. | none | none | confession_attempt | DT_121. |
| DLG_CH026_TRUNG_CONFESS_001 | char_trung | STATE_CONFESSION | Keep talking. | none | none | confession_attempt | DT_121. |
| DLG_CH026_HOANG_CONFESS_002 | comp_hoang | STATE_CONFESSION | Yesterday, when the turret was about to fire on Nha Di, I- | none | none | confession_attempt | DT_121. |
| DLG_CH026_ALARM_001 | npc_drone | STATE_ALARM | IMMUNE VECTOR LANDED. | none | set_flag:FLAG_CH026_IMMUNE_VECTOR_LANDED | confession_attempt | DT_121. |
| DLG_CH026_TRUNG_CONFESS_002 | char_trung | STATE_CONFESSION | What? | none | none | confession_attempt | DT_121. |
| DLG_CH026_HOANG_CONFESS_003 | comp_hoang | STATE_CONFESSION | ... | none | none | confession_attempt | DT_121. |
| DLG_CH026_TRUNG_CONFESS_003 | char_trung | STATE_CONFESSION | Hoang? | none | none | confession_attempt | DT_121. |
| DLG_CH026_HOANG_CONFESS_004 | comp_hoang | STATE_CONFESSION | The drone is transmitting. We need to block it first. | none | set_flag:FLAG_CH026_HOANG_CONFESSION_INTERRUPTED_AGAIN | confession_attempt | DT_121. |

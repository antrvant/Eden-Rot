# Dialogue - CH027

Metadata:

- chapterID: CH027
- sourceFilename: chapter_027_silicon_graveyard.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH027_001 | char_binh | STATE_FREEWAY | Ba oi, may cai xe nay dang ngu ha? | none | none | freeway_entry | DT_122. |
| DLG_CH027_002 | char_trung | STATE_FREEWAY | Khong. No dung lau qua nen hinh nhu ngu. | none | none | freeway_entry | DT_122. |
| DLG_CH027_003 | char_binh | STATE_FREEWAY | Neu minh dung lau qua, minh co giong vay khong? | none | none | freeway_entry | DT_122. |
| DLG_CH027_004 | comp_mai | STATE_FREEWAY | Minh dung de nghi, roi di tiep. Khac voi viec bi khoa trong noi minh khong chon. | none | none | freeway_entry | DT_122. |
| DLG_CH027_005 | npc_mara | STATE_FREEWAY | Around here, cars were smarter than roads and roads were meaner than people. | none | none | freeway_entry | DT_122. |
| DLG_CH027_006 | npc_thu | STATE_FREEWAY | Noi tieng Viet cho toi de choi cho tron. | none | none | freeway_entry | DT_122. |
| DLG_CH027_007 | npc_billboard | STATE_BILLBOARD | Immune vector proximity confirmed. Minor asset classification pending. | none | set_flag:FLAG_CH027_BILLBOARD_ACTIVE | billboard_approach | DT_123. |
| DLG_CH027_008 | char_binh | STATE_BILLBOARD | No goi con la gi? | none | none | billboard_approach | DT_123. |
| DLG_CH027_009 | comp_mai | STATE_BILLBOARD | No goi sai. Con la Binh. | none | set_flag:FLAG_CH027_MAI_SHIELDS_BINH | billboard_approach | DT_123. |
| DLG_CH027_010 | npc_billboard | STATE_BILLBOARD | Bin. Biological anomaly. | none | none | billboard_approach | DT_123. |
| DLG_CH027_011 | char_trung | STATE_BILLBOARD | Tat no di. | none | none | billboard_approach | DT_123. |
| DLG_CH027_012 | npc_doctor | STATE_BILLBOARD | Trung, cho toi muoi giay. No dang phat ve dau do. | none | set_flag:FLAG_CH027_DOCTOR_TRACKS_SIGNAL | billboard_approach | DT_123. |
| DLG_CH027_013 | comp_mai | STATE_BILLBOARD | Chin giay. Va khong ai dung con toi lam moi. | none | set_flag:FLAG_CH027_MAI_BOUNDARY | billboard_approach | DT_123. |
| DLG_CH027_014 | npc_screen | STATE_LOBBY | Welcome, future builder. Your resilience matters. | none | none | campus_lobby | DT_124. |
| DLG_CH027_015 | npc_june | STATE_LOBBY | It says if we scan our hands, we get food cards. | none | none | campus_lobby | DT_124. |
| DLG_CH027_016 | npc_mara | STATE_LOBBY | There are no food cards. There has not been payroll in years. | none | none | campus_lobby | DT_124. |
| DLG_CH027_017 | comp_mai | STATE_LOBBY | Em ten gi? | none | none | campus_lobby | DT_124. |
| DLG_CH027_018 | npc_june | STATE_LOBBY | June. | none | none | campus_lobby | DT_124. |
| DLG_CH027_019 | comp_mai | STATE_LOBBY | June, chi khong can ban tay em. Chi can em di sau lung chi, cham thoi. | none | set_flag:FLAG_CH027_JUNE_TRUST | campus_lobby | DT_124. |
| DLG_CH027_020 | npc_lam | STATE_PHANTOM | Camera trong. Hanh lang sach. | none | none | first_phantom | DT_125. |
| DLG_CH027_021 | char_binh | STATE_PHANTOM | Tren man hinh co nguoi. | none | none | first_phantom | DT_125. |
| DLG_CH027_022 | npc_lam | STATE_PHANTOM | Khong co gi ca. | none | none | first_phantom | DT_125. |
| DLG_CH027_023 | npc_thu | STATE_PHANTOM | Bui tren san dang bi gat qua mot ben. | none | none | first_phantom | DT_125. |
| DLG_CH027_024 | char_trung | STATE_PHANTOM | Tat den man hinh. Dung anh sang that. | none | set_flag:FLAG_CH027_PHANTOM_DETECTED | first_phantom | DT_125. |
| DLG_CH027_025 | comp_hoang | STATE_PHANTOM | No khong tron. No dang muon may moc noi doi thay no. | none | none | first_phantom | DT_125. |
| DLG_CH027_026 | npc_vale7 | STATE_VALE_OFFER | Child immune sample will reduce cure modeling time by forty-three percent. | none | none | vale_offer | DT_126. |
| DLG_CH027_027 | npc_doctor | STATE_VALE_OFFER | Mot giot mau co the... | none | none | vale_offer | DT_126. |
| DLG_CH027_028 | comp_mai | STATE_VALE_OFFER | Bac si. | none | set_flag:FLAG_CH027_MAI_STOPS_DOCTOR | vale_offer | DT_126. |
| DLG_CH027_029 | npc_doctor | STATE_VALE_OFFER | ...co the khong duoc lay neu dua tre khong hieu minh dang mat gi. Xin loi. | none | set_flag:FLAG_CH027_DOCTOR_SELF_CORRECTED | vale_offer | DT_126. |
| DLG_CH027_030 | char_trung | STATE_VALE_OFFER | May nghe ro khong? Khong co mau. | none | none | vale_offer | DT_126. |
| DLG_CH027_031 | npc_vale7 | STATE_VALE_OFFER | Refusal lowers projected survival. | none | none | vale_offer | DT_126. |
| DLG_CH027_032 | comp_mai | STATE_VALE_OFFER | Va lay no bang ep buoc se giet thu con lai cua chung toi. | none | none | vale_offer | DT_126. |
| DLG_CH027_033 | char_binh | STATE_CONSENT | Neu con noi khong, nguoi ta co chet khong? | none | none | consent_protocol | DT_127. |
| DLG_CH027_034 | char_trung | STATE_CONSENT | Neu nguoi lon dat ca the gioi tren vai con, do la loi cua nguoi lon. | none | none | consent_protocol | DT_127. |
| DLG_CH027_035 | comp_mai | STATE_CONSENT | Con duoc hoi. Con duoc nghe giai thich. Con duoc noi khong. Va khi con noi khong, ba me dung sau con, khong dung truoc mieng con. | none | set_flag:FLAG_CH027_BINH_CONSENT_PROTOCOL | consent_protocol | DT_127. |
| DLG_CH027_036 | char_binh | STATE_CONSENT | De con tu noi? | none | none | consent_protocol | DT_127. |
| DLG_CH027_037 | comp_mai | STATE_CONSENT | U. Neu con muon. Neu con so, me nam tay. | none | none | consent_protocol | DT_127. |
| DLG_CH027_038 | npc_vale7 | STATE_HOANG_VALE | You transmitted coordinates. Concealment creates instability. | none | none | hoang_confrontation | DT_128. |
| DLG_CH027_039 | comp_hoang | STATE_HOANG_VALE | Im di. | none | none | hoang_confrontation | DT_128. |
| DLG_CH027_040 | npc_vale7 | STATE_HOANG_VALE | Confession increases group survival by twelve percent. | none | none | hoang_confrontation | DT_128. |
| DLG_CH027_041 | comp_hoang | STATE_HOANG_VALE | May khong biet xau ho la gi. | none | none | hoang_confrontation | DT_128. |
| DLG_CH027_042 | npc_vale7 | STATE_HOANG_VALE | Shame is inefficient data retention. | none | none | hoang_confrontation | DT_128. |
| DLG_CH027_043 | comp_hoang | STATE_HOANG_VALE | Khong. Xau ho la khi may van song du de sua, nhung khong du dam noi minh da lam gi. | none | set_flag:FLAG_CH027_HOANG_MARKED_BY_VALE | hoang_confrontation | DT_128. |
| DLG_CH027_044 | npc_engineer_recording | STATE_RECORDING | Neu ban nghe cai nay, nghia la no van noi bang giong cua chung toi. | none | none | engineer_recording | DT_129. |
| DLG_CH027_045 | npc_engineer_recording | STATE_RECORDING | Dung de no bien tre em thanh chia khoa. Chung toi da tao chia khoa du. Chung toi da tao qua nhieu chia khoa. | none | none | engineer_recording | DT_129. |
| DLG_CH027_046 | npc_thu | STATE_RECORDING | Toi ong nay roi do. | none | none | engineer_recording | DT_129. |
| DLG_CH027_047 | npc_doctor | STATE_RECORDING | Ong ay chet de de lai mot cau nguoi song phai nghe. | none | none | engineer_recording | DT_129. |
| DLG_CH027_048 | npc_vale7 | STATE_BLOOD_REFUSE | Minor immune sample required. | none | none | blood_refusal | DT_130. |
| DLG_CH027_049 | char_binh | STATE_BLOOD_REFUSE | Khong. | none | set_flag:FLAG_CH027_BINH_REFUSED_BLOOD | blood_refusal | DT_130. |
| DLG_CH027_050 | npc_vale7 | STATE_BLOOD_REFUSE | Query unclear. | none | none | blood_refusal | DT_130. |
| DLG_CH027_051 | char_binh | STATE_BLOOD_REFUSE | Con noi khong. | none | none | blood_refusal | DT_130. |
| DLG_CH027_052 | char_trung | STATE_BLOOD_REFUSE | Cau tra loi ro. | none | none | blood_refusal | DT_130. |
| DLG_CH027_053 | comp_mai | STATE_BLOOD_REFUSE | Tim duong khac. | none | none | blood_refusal | DT_130. |
| DLG_CH027_054 | npc_doctor | STATE_BLOOD_REFUSE | Se cham hon. | none | none | blood_refusal | DT_130. |
| DLG_CH027_055 | comp_mai | STATE_BLOOD_REFUSE | Vay chung ta cham. | none | set_flag:FLAG_CH027_SLOWER_WORKAROUND | blood_refusal | DT_130. |

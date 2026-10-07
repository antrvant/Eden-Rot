# Dialogue - CH028

Metadata:

- chapterID: CH028
- sourceFilename: chapter_028_thanh_pho_cua_nhung_buc_tuong.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH028_001 | char_binh | STATE_WALL_SIGHT | Trong do co den. | none | none | wall_approach | DT_131. |
| DLG_CH028_002 | char_trung | STATE_WALL_SIGHT | Co. | none | none | wall_approach | DT_131. |
| DLG_CH028_003 | char_binh | STATE_WALL_SIGHT | Vay trong do la nha ha ba? | none | none | wall_approach | DT_131. |
| DLG_CH028_004 | comp_mai | STATE_WALL_SIGHT | Chua chac. Noi co den chua chac co nguoi doi minh. | none | none | wall_approach | DT_131. |
| DLG_CH028_005 | npc_mara | STATE_WALL_SIGHT | Walls keep things out. They also teach people not to look over. | none | none | wall_approach | DT_131. |
| DLG_CH028_006 | npc_thu | STATE_WALL_SIGHT | Tuong cao ma long thap thi toi thich ham thoat nuoc hon. | none | none | wall_approach | DT_131. |
| DLG_CH028_007 | npc_rowan | STATE_GATE_SCAN | Weapons down. Blood screen, retinal scan, child registry. | none | none | gate_scan | DT_132. |
| DLG_CH028_008 | char_trung | STATE_GATE_SCAN | Khong ai lay mau con toi. | none | none | gate_scan | DT_132. |
| DLG_CH028_009 | npc_rowan | STATE_GATE_SCAN | Then no one enters. | none | none | gate_scan | DT_132. |
| DLG_CH028_010 | comp_mai | STATE_GATE_SCAN | Chung toi co the cho ong kiem tra sot, vet can, trieu chung. Khong co mau tre em. Khong co scan ket noi voi he thong VALE. | none | set_flag:FLAG_CH028_MAI_GATE_TERMS | gate_scan | DT_132. |
| DLG_CH028_011 | npc_rowan | STATE_GATE_SCAN | You do not set terms at my gate. | none | none | gate_scan | DT_132. |
| DLG_CH028_012 | comp_mai | STATE_GATE_SCAN | Neu cong cua ong can tre em mat quyen noi khong moi mo, thi no khong khac gi cai bay ngoai kia. | none | set_flag:FLAG_CH028_MAI_BOUNDARY | gate_scan | DT_132. |
| DLG_CH028_013 | npc_june | STATE_REFUGEE | They said my friend is low skill household. | none | none | refugee_camp | DT_133. |
| DLG_CH028_014 | char_binh | STATE_REFUGEE | Nghia la gi? | none | none | refugee_camp | DT_133. |
| DLG_CH028_015 | npc_june | STATE_REFUGEE | Means they don't need her parents. | none | none | refugee_camp | DT_133. |
| DLG_CH028_016 | char_binh | STATE_REFUGEE | Nhung tre em dau co nghe. | none | none | refugee_camp | DT_133. |
| DLG_CH028_017 | npc_mara | STATE_REFUGEE | That is why adults invented softer words. | none | none | refugee_camp | DT_133. |
| DLG_CH028_018 | comp_mai | STATE_REFUGEE | Khong. Do la ly do nguoi lon phai bi bat noi dung tu. | none | set_flag:FLAG_CH028_MAI_LANGUAGE_STAND | refugee_camp | DT_133. |
| DLG_CH028_019 | npc_ada | STATE_ADA_INTRO | I have buried children because I opened the gate too wide. | none | none | ada_meeting | DT_134. |
| DLG_CH028_020 | comp_mai | STATE_ADA_INTRO | Toi tin ba. | none | none | ada_meeting | DT_134. |
| DLG_CH028_021 | npc_ada | STATE_ADA_INTRO | Then you understand why I cannot open it for everyone. | none | none | ada_meeting | DT_134. |
| DLG_CH028_022 | comp_mai | STATE_ADA_INTRO | Toi hieu cong khong the mo vo dieu kien. Toi khong hieu viec bien nguoi thanh gia ve. | none | none | ada_meeting | DT_134. |
| DLG_CH028_023 | npc_ada | STATE_ADA_INTRO | Idealism is cheaper outside the wall. | none | none | ada_meeting | DT_134. |
| DLG_CH028_024 | comp_mai | STATE_ADA_INTRO | Khong. Ngoai tuong, ly tuong dat hon. Vi minh tra bang mang song ngay lap tuc. | none | none | ada_meeting | DT_134. |
| DLG_CH028_025 | npc_ada | STATE_ENTRY_PRICE | One core access window. One non-invasive child scan. One security hold: Hoang. | none | none | entry_negotiation | DT_135. |
| DLG_CH028_026 | npc_vale_core | STATE_ENTRY_PRICE | Civic filter entry terms available. | none | set_flag:FLAG_CH028_CIVIC_FILTER_TERMS | entry_negotiation | DT_135. |
| DLG_CH028_027 | char_trung | STATE_ENTRY_PRICE | Thu lai ten anh ay bang giong do lan nua xem. | none | none | entry_negotiation | DT_135. |
| DLG_CH028_028 | comp_hoang | STATE_ENTRY_PRICE | Trung. | none | none | entry_negotiation | DT_135. |
| DLG_CH028_029 | comp_mai | STATE_ENTRY_PRICE | Khong ai bi giao rieng. Neu co nghi van, co phien cong khai, co nhan chung, co bang chung. | none | set_flag:FLAG_CH028_MAI_PUBLIC_PROCESS | entry_negotiation | DT_135. |
| DLG_CH028_030 | npc_ada | STATE_ENTRY_PRICE | You ask us to trust an armed stranger marked by hostile AI. | none | none | entry_negotiation | DT_135. |
| DLG_CH028_031 | comp_mai | STATE_ENTRY_PRICE | Toi yeu cau ba dung luoc de tim su that, khong dung so hai de thay luoc. | none | none | entry_negotiation | DT_135. |
| DLG_CH028_032 | comp_hoang | STATE_HOANG_OFFER | Neu giao tao doi lay hai muoi nguoi ngoai cong duoc vao phong y te, tao di. | none | none | hoang_offer | DT_136. |
| DLG_CH028_033 | char_trung | STATE_HOANG_OFFER | May khong phai tien le. | none | none | hoang_offer | DT_136. |
| DLG_CH028_034 | comp_hoang | STATE_HOANG_OFFER | Co luc tao da tu bien minh thanh tien le roi. | none | none | hoang_offer | DT_136. |
| DLG_CH028_035 | char_trung | STATE_HOANG_OFFER | Cau do nghia la gi? | none | none | hoang_offer | DT_136. |
| DLG_CH028_036 | comp_hoang | STATE_HOANG_OFFER | Nghia la... tao no may mot cau chuyen. | none | set_flag:FLAG_CH028_HOANG_ALMOST_CONFESSED | hoang_offer | DT_136. |
| DLG_CH028_037 | npc_alarm | STATE_RIOT | Crowd breach at south market. | none | set_flag:FLAG_CH028_RIOT_STARTED | hoang_offer | DT_136. |
| DLG_CH028_038 | npc_guard | STATE_RIOT | Step back or we fire! | none | none | market_riot | DT_137. |
| DLG_CH028_039 | comp_mai | STATE_RIOT | Khong ai ban vao dong co tre em. | none | set_flag:FLAG_CH028_MAI_RIOT_STAND | market_riot | DT_137. |
| DLG_CH028_040 | npc_trader | STATE_RIOT | They are storming your wall! | none | none | market_riot | DT_137. |
| DLG_CH028_041 | comp_mai | STATE_RIOT | Khong. Ong ban cho ho loi noi doi, roi dung sau lung linh khi loi noi doi vo. | none | none | market_riot | DT_137. |
| DLG_CH028_042 | char_binh | STATE_RIOT | Me oi! | none | none | market_riot | DT_137. |
| DLG_CH028_043 | comp_mai | STATE_RIOT | Binh, dua em nho kia qua ben trai. Nhin June. | none | none | market_riot | DT_137. |
| DLG_CH028_044 | npc_ada | STATE_COUNCIL | You could have let the riot prove my point. | none | none | council_platform | DT_138. |
| DLG_CH028_045 | comp_mai | STATE_COUNCIL | Toi khong can nguoi vo toi de minh dung. | none | none | council_platform | DT_138. |
| DLG_CH028_046 | npc_ada | STATE_COUNCIL | And what do you want? | none | none | council_platform | DT_138. |
| DLG_CH028_047 | comp_mai | STATE_COUNCIL | Mot cong mo co nguoi ghi lai ai vao, vi sao vao, ai bi tu choi, va ai chiu trach nhiem. Mot phien cong khai cho Hoang. Mot ket noi AI core bi cach ly. Mot danh sach y te cho tre em ngoai cong. | none | set_flag:FLAG_CH028_MAI_DEMANDS | council_platform | DT_138. |
| DLG_CH028_048 | npc_ada | STATE_COUNCIL | That is not a small ask. | none | none | council_platform | DT_138. |
| DLG_CH028_049 | comp_mai | STATE_COUNCIL | Khong. Nhung no nho hon mot thanh pho mat linh hon. | none | set_flag:FLAG_CH028_ALLIED_DELEGATION | council_platform | DT_138. |
| DLG_CH028_050 | npc_vale_core | STATE_NEO_MILITARY | Armed convoy approaching. Legacy command authority detected. | none | none | neo_military_hook | DT_139. |
| DLG_CH028_051 | npc_vale_core | STATE_NEO_MILITARY | Civic filter status: disputed by public witness. | none | none | neo_military_hook | DT_139. |
| DLG_CH028_052 | npc_rowan | STATE_NEO_MILITARY | Army Remnants. | none | none | neo_military_hook | DT_139. |
| DLG_CH028_053 | char_trung | STATE_NEO_MILITARY | Ban cua cac ong? | none | none | neo_military_hook | DT_139. |
| DLG_CH028_054 | npc_ada | STATE_NEO_MILITARY | Depends who they decide we are today. | none | none | neo_military_hook | DT_139. |
| DLG_CH028_055 | npc_vale_core | STATE_NEO_MILITARY | Query: Rebirth command legitimacy disputed. | none | set_flag:FLAG_CH028_NEO_MILITARY_DETECTED | neo_military_hook | DT_139. |
| DLG_CH028_056 | comp_mai | STATE_NEO_MILITARY | Lai mot nua muon dat ten cho chung ta. | none | none | neo_military_hook | DT_139. |

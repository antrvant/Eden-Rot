# Dialogue - CH029

Metadata:

- chapterID: CH029
- sourceFilename: chapter_029_neo_military.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH029_001 | npc_graves | STATE_ARMY_ARRIVAL | I requested the commander. | none | none | army_arrival | DT_140. |
| DLG_CH029_002 | comp_mai | STATE_ARMY_ARRIVAL | Ong dang gap hai nguoi dai dien. | none | none | army_arrival | DT_140. |
| DLG_CH029_003 | npc_graves | STATE_ARMY_ARRIVAL | I see one armed commander and one civilian. | none | none | army_arrival | DT_140. |
| DLG_CH029_004 | char_trung | STATE_ARMY_ARRIVAL | Vay ong thieu. | none | none | army_arrival | DT_140. |
| DLG_CH029_005 | npc_ada | STATE_ARMY_ARRIVAL | Colonel, this city is not under your command. | none | none | army_arrival | DT_140. |
| DLG_CH029_006 | npc_graves | STATE_ARMY_ARRIVAL | Not yet under anyone's protection either. | none | none | army_arrival | DT_140. |
| DLG_CH029_007 | npc_vale_core | STATE_ARMY_ARRIVAL | Civic filter dispute received. Edenrot class: legacy command. | none | set_flag:FLAG_CH029_EDENROT_LEGACY_COMMAND | army_arrival | DT_140. |
| DLG_CH029_008 | npc_graves | STATE_COMMAND_CHAIN | Councils debate. Command moves. | none | none | command_negotiation | DT_141. |
| DLG_CH029_009 | char_trung | STATE_COMMAND_CHAIN | Command cung co the di sai huong rat nhanh. | none | none | command_negotiation | DT_141. |
| DLG_CH029_010 | npc_graves | STATE_COMMAND_CHAIN | You took a warship. You understand force. | none | none | command_negotiation | DT_141. |
| DLG_CH029_011 | char_trung | STATE_COMMAND_CHAIN | Toi hieu force can day xich. Council la mot trong nhung day xich do. | none | none | command_negotiation | DT_141. |
| DLG_CH029_012 | comp_mai | STATE_COMMAND_CHAIN | Neu ong muon phoi hop, chung toi nghe. Neu ong muon so huu chung toi, cong kia vang day toi cach noi khong. | none | set_flag:FLAG_CH029_REBIRTH_COMMAND_INDEPENDENT | command_negotiation | DT_141. |
| DLG_CH029_013 | npc_sloane | STATE_MARKED | Marked individuals are compromised assets. | none | none | marked_prisoners | DT_142. |
| DLG_CH029_014 | npc_doctor | STATE_MARKED | Chua co bang chung ho bi dieu khien. | none | none | marked_prisoners | DT_142. |
| DLG_CH029_015 | npc_sloane | STATE_MARKED | I do not need certainty. I need risk reduction. | none | none | marked_prisoners | DT_142. |
| DLG_CH029_016 | char_binh | STATE_MARKED | Neu may goi sai ten, minh khong tra loi. | none | none | marked_prisoners | DT_142. |
| DLG_CH029_017 | npc_marked_teen | STATE_MARKED | Wish it worked for guns. | none | none | marked_prisoners | DT_142. |
| DLG_CH029_018 | comp_hoang | STATE_MARKED | Doi khi phai co nguoi dung giua. | none | none | marked_prisoners | DT_142. |
| DLG_CH029_019 | char_binh | STATE_FORT_CHILDREN | Cac ban hoc ban do chien tranh moi ngay ha? | none | none | fort_children | DT_143. |
| DLG_CH029_020 | npc_soldier_child | STATE_FORT_CHILDREN | We learn sectors. Sectors keep people alive. | none | none | fort_children | DT_143. |
| DLG_CH029_021 | char_binh | STATE_FORT_CHILDREN | Con hoc ve bien. Bien cung lam nguoi ta song. | none | none | fort_children | DT_143. |
| DLG_CH029_022 | npc_soldier_child | STATE_FORT_CHILDREN | Does the sea have orders? | none | none | fort_children | DT_143. |
| DLG_CH029_023 | char_binh | STATE_FORT_CHILDREN | Co. Me bao di gan lan can khi song lon. | none | none | fort_children | DT_143. |
| DLG_CH029_024 | npc_graves | STATE_FUEL_DEPOT | Shell the tank row if containment fails. | none | none | fuel_depot | DT_144. |
| DLG_CH029_025 | char_trung | STATE_FUEL_DEPOT | Neu ban vao do, chung ta mat fuel va engineer. | none | none | fuel_depot | DT_144. |
| DLG_CH029_026 | npc_graves | STATE_FUEL_DEPOT | If we hesitate, we lose the convoy. | none | none | fuel_depot | DT_144. |
| DLG_CH029_027 | comp_mai | STATE_FUEL_DEPOT | Trung, co hai phut. | none | none | fuel_depot | DT_144. |
| DLG_CH029_028 | char_trung | STATE_FUEL_DEPOT | Vay cho toi mot phut ruoi de khong phai giet nguoi minh chua thu cuu. | none | set_flag:FLAG_CH029_ENGINEER_RESCUE_CHOSEN | fuel_depot | DT_144. |
| DLG_CH029_029 | npc_sloane | STATE_EXECUTION | Transport capacity is exceeded. Marked prisoners do not ride. | none | none | execution_order | DT_145. |
| DLG_CH029_030 | char_trung | STATE_EXECUTION | Thi ho di bo giua vong bao ve. | none | none | execution_order | DT_145. |
| DLG_CH029_031 | npc_sloane | STATE_EXECUTION | They are compromised. | none | none | execution_order | DT_145. |
| DLG_CH029_032 | comp_mai | STATE_EXECUTION | Scan cho thay passive mark. | none | none | execution_order | DT_145. |
| DLG_CH029_033 | npc_sloane | STATE_EXECUTION | Field policy says terminate. | none | none | execution_order | DT_145. |
| DLG_CH029_034 | npc_vale_core | STATE_EXECUTION | Legacy command execution path available. | none | none | execution_order | DT_145. |
| DLG_CH029_035 | char_trung | STATE_EXECUTION | Field policy sai. | none | none | execution_order | DT_145. |
| DLG_CH029_036 | npc_graves | STATE_EXECUTION | In my operation, refusal is mutiny. | none | none | execution_order | DT_145. |
| DLG_CH029_037 | char_trung | STATE_EXECUTION | Toi se nghe lenh nao cuu nguoi. Lenh con lai, tu ong lam. | none | set_flag:FLAG_CH029_EXECUTION_ORDER_REFUSED | execution_order | DT_145. |
| DLG_CH029_038 | comp_hoang | STATE_HOANG_FORWARD | Neu marked la ly do de chet, thi... | none | none | hoang_almost_confesses | DT_146. |
| DLG_CH029_039 | char_trung | STATE_HOANG_FORWARD | Hoang. | none | none | hoang_almost_confesses | DT_146. |
| DLG_CH029_040 | comp_hoang | STATE_HOANG_FORWARD | Thi may can biet... | none | none | hoang_almost_confesses | DT_146. |
| DLG_CH029_041 | npc_vale_drone | STATE_HOANG_FORWARD | Lock reacquired. | none | set_flag:FLAG_CH029_DRONE_INTERRUPT | hoang_almost_confesses | DT_146. |
| DLG_CH029_042 | npc_pike | STATE_HOANG_FORWARD | Incoming! | none | none | hoang_almost_confesses | DT_146. |
| DLG_CH029_043 | npc_marked_engineer | STATE_RADAR_DUNE | I built this relay before I was marked. | none | none | radar_dune | DT_147. |
| DLG_CH029_044 | npc_sloane | STATE_RADAR_DUNE | You touch that console, I shoot. | none | none | radar_dune | DT_147. |
| DLG_CH029_045 | char_trung | STATE_RADAR_DUNE | Neu anh ta khong cham, tat ca chung ta chet. Chon muc tieu cho dung. | none | none | radar_dune | DT_147. |
| DLG_CH029_046 | npc_graves | STATE_RADAR_DUNE | Stand down, Major. | none | set_flag:FLAG_CH029_SLOANE_STAND_DOWN | radar_dune | DT_147. |
| DLG_CH029_047 | npc_marked_engineer | STATE_RADAR_DUNE | Never thought I would miss being yelled at by management. | none | set_flag:FLAG_CH029_RADAR_RELAY_RESTORED | radar_dune | DT_147. |
| DLG_CH029_048 | npc_thu | STATE_RADAR_DUNE | Sua may di roi toi choi sau. | none | none | radar_dune | DT_147. |
| DLG_CH029_049 | npc_graves | STATE_CONDITIONAL | You disobeyed a field order. | none | none | conditional_ally | DT_148. |
| DLG_CH029_050 | char_trung | STATE_CONDITIONAL | Toi cuu fuel, radar, soldiers cua ong, va prisoners. | none | none | conditional_ally | DT_148. |
| DLG_CH029_051 | npc_graves | STATE_CONDITIONAL | You created precedent. | none | none | conditional_ally | DT_148. |
| DLG_CH029_052 | comp_mai | STATE_CONDITIONAL | Tot. Co vai tien le nen duoc tao lai. | none | none | conditional_ally | DT_148. |
| DLG_CH029_053 | npc_graves | STATE_CONDITIONAL | Conditional support. Fuel, one radar window, one escort team. Your friend still faces hearing. | none | set_flag:FLAG_CH029_ARMY_SUPPORT_PARTIAL | conditional_ally | DT_148. |
| DLG_CH029_054 | comp_hoang | STATE_CONDITIONAL | Anh ay khong can ong nhac. | none | none | conditional_ally | DT_148. |
| DLG_CH029_055 | npc_vale_core | STATE_CULT_HOOK | Child movement cluster detected. Red Canyon. Non-state religious command. | none | none | cult_hook | DT_149. |
| DLG_CH029_056 | npc_vale_core | STATE_CULT_HOOK | Legacy command assumption failed. Marked unit retained operational value. | none | set_flag:FLAG_CH029_LEGACY_COMMAND_FAILED | cult_hook | DT_149. |
| DLG_CH029_057 | char_binh | STATE_CULT_HOOK | Tre em do duoc noi khong khong? | none | none | cult_hook | DT_149. |
| DLG_CH029_058 | comp_mai | STATE_CULT_HOOK | Minh se hoi cac em. | none | none | cult_hook | DT_149. |
| DLG_CH029_059 | char_trung | STATE_CULT_HOOK | Va neu ai khong cho cac em tra loi? | none | none | cult_hook | DT_149. |
| DLG_CH029_060 | npc_mara | STATE_CULT_HOOK | Then we ask louder. | none | set_flag:FLAG_CH029_CULT_DETECTED | cult_hook | DT_149. |

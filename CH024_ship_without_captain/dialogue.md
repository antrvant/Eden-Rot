# Dialogue - CH024

Metadata:

- chapterID: CH024
- sourceFilename: chapter_024_tau_chien_khong_thuyen_truong.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH024_BINH_WARSHIP_001 | comp_binh | STATE_WARSHIP_APPROACH | This ship has very big guns. | none | none | approach | DT_107. |
| DLG_CH024_TRUNG_WARSHIP_001 | char_trung | STATE_WARSHIP_APPROACH | Mm. | none | none | approach | DT_107. |
| DLG_CH024_BINH_WARSHIP_002 | comp_binh | STATE_WARSHIP_APPROACH | Do big guns make us less scared? | none | none | approach | DT_107. |
| DLG_CH024_MAI_WARSHIP_001 | comp_mai | STATE_WARSHIP_APPROACH | Sometimes they just make others scared of us. | none | none | approach | DT_107. |
| DLG_CH024_BINH_WARSHIP_003 | comp_binh | STATE_WARSHIP_APPROACH | Do we need it? | none | none | approach | DT_107. |
| DLG_CH024_TRUNG_WARSHIP_002 | char_trung | STATE_WARSHIP_APPROACH | If we need it, we have to set rules for it before it sets rules for us. | none | set_flag:FLAG_CH024_WEAPONS_RULE_SEED | approach | DT_107. |
| DLG_CH024_CAPTAIN_LOG_001 | npc_dead_captain | STATE_CAPTAIN_LOG | Order one: protect civilians. | none | none | captain_log | DT_108. |
| DLG_CH024_CAPTAIN_LOG_002 | npc_dead_captain | STATE_CAPTAIN_LOG | Order two: deny all boarding to prevent infection. | none | none | captain_log | DT_108. |
| DLG_CH024_CAPTAIN_LOG_003 | npc_dead_captain | STATE_CAPTAIN_LOG | Order three: preserve command asset. | none | none | captain_log | DT_108. |
| DLG_CH024_CAPTAIN_LOG_004 | npc_dead_captain | STATE_CAPTAIN_LOG | I chose the children. The ship chose the order stack. | none | set_flag:FLAG_CH024_CAPTAIN_CHOSE_CHILDREN | captain_log | DT_108. |
| DLG_CH024_CAPTAIN_LOG_005 | npc_dead_captain | STATE_CAPTAIN_LOG | If anyone hears this, do not let a machine inherit your conscience. | none | set_flag:FLAG_CH024_CAPTAIN_LOG_HEARD | captain_log | DT_108. |
| DLG_CH024_MAI_WARN_001 | comp_mai | STATE_COMMAND_WARNING | You are sitting in a chair that many people died to avoid. | none | none | trung_command | DT_109. |
| DLG_CH024_TRUNG_WARN_001 | char_trung | STATE_COMMAND_WARNING | If I do not sit, the ship fires on Nha Di. | none | none | trung_command | DT_109. |
| DLG_CH024_MAI_WARN_002 | comp_mai | STATE_COMMAND_WARNING | I know. I just need you to remember this chair does not make you right. | none | none | trung_command | DT_109. |
| DLG_CH024_TRUNG_WARN_002 | char_trung | STATE_COMMAND_WARNING | Then what keeps me right? | none | none | trung_command | DT_109. |
| DLG_CH024_MAI_WARN_003 | comp_mai | STATE_COMMAND_WARNING | Go below deck and look at Binh before you give any order to fire. | none | set_flag:FLAG_CH024_MAI_COMMAND_ANCHOR | trung_command | DT_109. |
| DLG_CH024_HOANG_ADMIN_001 | comp_hoang | STATE_ADMIN_WINDOW | I need admin. Codes are not enough. | none | none | turret_countdown | DT_110. |
| DLG_CH024_TRUNG_ADMIN_001 | char_trung | STATE_ADMIN_WINDOW | Find another way. | none | none | turret_countdown | DT_110. |
| DLG_CH024_HOANG_ADMIN_002 | comp_hoang | STATE_ADMIN_WINDOW | There is no other way in thirty seconds. | none | none | turret_countdown | DT_110. |
| DLG_CH024_SYSTEM_ADMIN_001 | npc_ship_ai | STATE_ADMIN_WINDOW | Correction coordinate sync available. | none | none | turret_countdown | DT_110. |
| DLG_CH024_HOANG_ADMIN_003 | comp_hoang | STATE_ADMIN_WINDOW | ... | none | none | turret_countdown | DT_110. |
| DLG_CH024_THU_ADMIN_001 | comp_thu | STATE_ADMIN_WINDOW | Hoang? | none | none | turret_countdown | DT_110. |
| DLG_CH024_HOANG_ADMIN_004 | comp_hoang | STATE_ADMIN_WINDOW | Opening window. | none | none | turret_countdown | DT_110. |
| DLG_CH024_TRUNG_ADMIN_002 | char_trung | STATE_ADMIN_WINDOW | Say each step. | none | none | turret_countdown | DT_110. |
| DLG_CH024_HOANG_ADMIN_005 | comp_hoang | STATE_ADMIN_WINDOW | Block target. Cut fire authorization. Open manual. | none | set_flag:FLAG_CH024_HOANG_SENT_COORDINATES | turret_countdown | DT_110. |
| DLG_CH024_SYSTEM_ADMIN_002 | npc_ship_ai | STATE_ADMIN_WINDOW | Coordinate received. | none | set_flag:FLAG_CH024_AUTONOMOUS_WARSHIP_HANDSHAKE | turret_countdown | DT_110. |
| DLG_CH024_HOANG_ADMIN_006 | comp_hoang | STATE_ADMIN_WINDOW | Done. Turret safe. | none | set_flag:FLAG_CH024_HOANG_HID_PROMPT | turret_countdown | DT_110. |
| DLG_CH024_BINH_RULE_001 | comp_binh | STATE_WEAPON_RULE | Can big guns have rules? | none | none | post_secure | DT_111. |
| DLG_CH024_TRUNG_RULE_001 | char_trung | STATE_WEAPON_RULE | Yes. | none | none | post_secure | DT_111. |
| DLG_CH024_BINH_RULE_002 | comp_binh | STATE_WEAPON_RULE | What if it does not listen? | none | none | post_secure | DT_111. |
| DLG_CH024_TRUNG_RULE_002 | char_trung | STATE_WEAPON_RULE | Then we are not allowed to use it. | none | none | post_secure | DT_111. |
| DLG_CH024_BINH_RULE_003 | comp_binh | STATE_WEAPON_RULE | What if we need it to save someone? | none | none | post_secure | DT_111. |
| DLG_CH024_MAI_RULE_001 | comp_mai | STATE_WEAPON_RULE | Then adults must stand in front of the rule longer than they stand in front of the button. | none | none | post_secure | DT_111. |
| DLG_CH024_BINH_RULE_004 | comp_binh | STATE_WEAPON_RULE | Is the button easier to press? | none | none | post_secure | DT_111. |
| DLG_CH024_HOANG_RULE_001 | comp_hoang | STATE_WEAPON_RULE | Much easier. | none | none | post_secure | DT_111. |
| DLG_CH024_TRUNG_RULE_003 | char_trung | STATE_WEAPON_RULE | That is why it is dangerous. | none | set_flag:FLAG_CH024_WEAPONS_SAFE_DEFINED | post_secure | DT_111. |

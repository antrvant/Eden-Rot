# Dialogue - CH047

Metadata:

- chapterID: CH047
- sourceFilename: chapter_047_lien_minh_tan_vo.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH047_DT314_001 | npc_norad_officer | STATE_CUSTODY_CLAIM | We need temporary custody for secure transport. | none | none | root_column_exit | DT_314 - Custody Language. |
| DLG_CH047_DT314_002 | char_mai | STATE_CUSTODY_CLAIM | Say guardianship. | none | none | root_column_exit | DT_314. |
| DLG_CH047_DT314_003 | npc_norad_officer | STATE_CUSTODY_CLAIM | This is not a school. | none | none | root_column_exit | DT_314. |
| DLG_CH047_DT314_004 | char_ana | STATE_CUSTODY_CLAIM | No. It was a prison when they used words like yours. | none | set_flag:FLAG_CH047_CUSTODY_LANGUAGE_CORRECTED | root_column_exit | DT_314. |
| DLG_CH047_DT315_001 | npc_heartland_soldier | STATE_HUNTER_SHOT | That shot came from your line! | none | none | battlefield | DT_315 - Hunter Shot. |
| DLG_CH047_DT315_002 | char_trung | STATE_HUNTER_SHOT | No one fires until we know what wants us firing. | none | set_flag:FLAG_CH047_FRIENDLY_FIRE_PREVENTED | battlefield | DT_315. |
| DLG_CH047_DT315_003 | char_iara | STATE_HUNTER_SHOT | Canopy bent wrong. Shooter is above both of you. | none | none | battlefield | DT_315. |
| DLG_CH047_DT316_001 | char_binh | STATE_PROTECTION | If the adults guard me to protect me without asking me, it is like that room. | none | none | command_raft | DT_316 - Binh On Protection. |
| DLG_CH047_DT316_002 | char_mai | STATE_PROTECTION | Listen to him. | none | none | command_raft | DT_316. |
| DLG_CH047_DT317_001 | npc_fighter | STATE_MERCY | They tried to take the records. Leave them. | none | none | trapped_squad | DT_317 - Theme Line. |
| DLG_CH047_DT317_002 | char_trung | STATE_MERCY | An alliance does not shatter because people argue. It shatters when people stop turning back to save each other. | none | set_flag:FLAG_CH047_ALLIANCE_MERCY_DEBT | trapped_squad | DT_317. |
| DLG_CH047_DT318_001 | char_ana | STATE_HUNTER_TAG | Down! | none | none | hunter_tag | DT_318 - Hunter Tag. |
| DLG_CH047_DT318_002 | char_binh | STATE_HUNTER_TAG | You saved me. | none | none | hunter_tag | DT_318. |
| DLG_CH047_DT318_003 | char_ana | STATE_HUNTER_TAG | You are not the only bridge they want. | none | none | hunter_tag | DT_318. |
| DLG_CH047_DT319_001 | npc_faction_rep | STATE_HOANG_POD | That man is Architect-compromised. | none | none | hoang_pod | DT_319 - Hoang Pod. |
| DLG_CH047_DT319_002 | char_trung | STATE_HOANG_POD | He is also under our guard and our promise. | none | none | hoang_pod | DT_319. |
| DLG_CH047_DT319_003 | char_mai | STATE_HOANG_POD | Both things are true. We act like both are true. | none | set_flag:FLAG_CH047_HOANG_STASIS_MAINTAINED_ACT7 | hoang_pod | DT_319. |
| DLG_CH047_DT320_001 | char_architect_broadcast | STATE_ANTARCTICA | Thirty days to Source rewrite. Resistance is weather before winter. | none | set_flag:FLAG_CH047_ANTARCTICA_COUNTDOWN_BROADCAST | alliance_broadcast | DT_320 - Antarctica Broadcast. |
| DLG_CH047_DT320_002 | npc_samir | STATE_ANTARCTICA | They are not threatening us. | none | none | alliance_broadcast | DT_320. |
| DLG_CH047_DT320_003 | char_iara | STATE_ANTARCTICA | No. They are scheduling us. | none | none | alliance_broadcast | DT_320. |
| DLG_CH047_DT321_001 | char_mai | STATE_GUARDIAN_CIRCLE | No faction owns children. | none | set_flag:FLAG_CH047_GUARDIAN_CIRCLE_ACTIVE | guardian_circle | DT_321 - Guardian Circle. |
| DLG_CH047_DT321_002 | char_ana | STATE_GUARDIAN_CIRCLE | Including Rebirth. | none | none | guardian_circle | DT_321. |
| DLG_CH047_DT321_003 | char_mai | STATE_GUARDIAN_CIRCLE | Including Rebirth. | none | set_flag:FLAG_CH047_GUARDIAN_CHARTER_SIGNED | guardian_circle | DT_321. |
| DLG_CH047_DT322_001 | npc_radio_op | STATE_SOUTHWARD | Southern route is murder. | none | none | fleet_departure | DT_322 - Southward. |
| DLG_CH047_DT322_002 | char_trung | STATE_SOUTHWARD | So was every route that brought us here. | none | none | fleet_departure | DT_322. |
| DLG_CH047_DT322_003 | char_binh | STATE_SOUTHWARD | But this time everyone knows where we are going. | none | set_flag:FLAG_CH047_ACT7_COMPLETED | fleet_departure | DT_322. |
| DLG_CH047_char_trung_001 | char_trung | STATE_BASE | The Alliance is gone. Everyone is fighting for their own group now. | Choice 1: "We can rebuild it." : STATE_TRUNG_CHAT_REBUILD \| Choice 2: "We need to focus on ourselves." : STATE_TRUNG_CHAT_SELF | none | none | none |
| DLG_CH047_char_trung_002 | char_trung | STATE_TRUNG_CHAT_REBUILD | There are no foundations left to build on. Just ashes. | none | none | none | none |
| DLG_CH047_char_trung_003 | char_trung | STATE_TRUNG_CHAT_SELF | That's what Hoang said. And look what it made him. | none | none | none | none |

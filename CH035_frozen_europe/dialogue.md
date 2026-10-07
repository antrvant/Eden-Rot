# Dialogue - CH035

Metadata:

- chapterID: CH035
- sourceFilename: chapter_035_chau_au_dong_bang.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH035_MORENO_001 | npc_moreno | STATE_ATLANTIC_FLEET | No port. No flag worth dying for. Just hulls that still float. | none | none | fleet_rendezvous | DT_198. |
| DLG_CH035_TRUNG_001 | char_trung | STATE_ATLANTIC_FLEET | We have star data and a route. | none | none | fleet_rendezvous | DT_198. |
| DLG_CH035_MORENO_002 | npc_moreno | STATE_ATLANTIC_FLEET | Stars I trust. Ports lie. | none | none | fleet_rendezvous | DT_198. |
| DLG_CH035_MAI_001 | comp_mai | STATE_ATLANTIC_FLEET | We do not buy a road with people. | none | none | fleet_rendezvous | DT_198. |
| DLG_CH035_MORENO_003 | npc_moreno | STATE_ATLANTIC_FLEET | Then maybe you are the first honest buyers this ocean has seen in years. | none | set_flag:FLAG_CH035_ATLANTIC_FLEET_ALLY | fleet_rendezvous | DT_198. |
| DLG_CH035_THU_001 | npc_thu | STATE_WRONG_COLD | Water freezing in this pattern is not natural. | none | none | channel_crossing | DT_199. |
| DLG_CH035_DOCTOR_001 | npc_doctor | STATE_WRONG_COLD | Atmospheric seeding. Maybe reflective aerosols, maybe something biological. | none | none | channel_crossing | DT_199. |
| DLG_CH035_BINH_001 | comp_binh | STATE_WRONG_COLD | Can cold also be forced to do bad work? | none | none | channel_crossing | DT_199. |
| DLG_CH035_MAI_002 | comp_mai | STATE_WRONG_COLD | Yes. But cold can also keep people alive if we learn to respect it. | none | set_flag:FLAG_CH035_CRYOSTATIC_FRONTIER_CONFIRMED | channel_crossing | DT_199. |
| DLG_CH035_BINH_002 | comp_binh | STATE_FROZEN_CITY | Snow is beautiful. | none | none | uk_landing | DT_200. |
| DLG_CH035_TRUNG_002 | char_trung | STATE_FROZEN_CITY | Beautiful does not mean safe. | none | none | uk_landing | DT_200. |
| DLG_CH035_MAI_003 | comp_mai | STATE_FROZEN_CITY | This city froze while it was calling for help. | none | none | uk_landing | DT_200. |
| DLG_CH035_PIKE_001 | npc_pike | STATE_FROZEN_CITY | That may be the saddest field report I have ever heard. | none | none | uk_landing | DT_200. |
| DLG_CH035_THU_002 | npc_thu | STATE_FROZEN_CITY | Write it down. Do not let anyone call this weather. | none | set_flag:FLAG_CH035_CRYOSTATIC_FRONTIER_CONFIRMED | uk_landing | DT_200. |
| DLG_CH035_LAM_001 | npc_lam | STATE_ICE_HORDE | Down! | none | none | ice_horde_encounter | DT_201. |
| DLG_CH035_BINH_003 | comp_binh | STATE_ICE_HORDE | Its hand is still moving. | none | none | ice_horde_encounter | DT_201. |
| DLG_CH035_LAM_002 | npc_lam | STATE_ICE_HORDE | It is dead. | none | none | ice_horde_encounter | DT_201. |
| DLG_CH035_BINH_004 | comp_binh | STATE_ICE_HORDE | No. The finger just moved. | none | none | ice_horde_encounter | DT_201. |
| DLG_CH035_THU_003 | npc_thu | STATE_ICE_HORDE | Fire! Not bullets, fire! | none | none | ice_horde_encounter | DT_201. |
| DLG_CH035_DOCTOR_002 | npc_doctor | STATE_ICE_HORDE | Brain stem preserved by cold. God help us. | none | set_flag:FLAG_CH035_ICE_HORDE_INTRODUCED | ice_horde_encounter | DT_201. |
| DLG_CH035_RAIDER_001 | npc_raider | STATE_FALSE_RELIEF | Warm beds. Children first. | none | none | false_relief | DT_202. |
| DLG_CH035_MAI_004 | comp_mai | STATE_FALSE_RELIEF | Where are the names of the children who entered yesterday? | none | none | false_relief | DT_202. |
| DLG_CH035_RAIDER_002 | npc_raider | STATE_FALSE_RELIEF | Records burned. | none | none | false_relief | DT_202. |
| DLG_CH035_MAI_005 | comp_mai | STATE_FALSE_RELIEF | Kitchen still hot, flags still new, but ledger spotless? That is too poor a lie. | none | none | false_relief | DT_202. |
| DLG_CH035_INGRID_001 | npc_ingrid | STATE_FALSE_RELIEF | They make me keep the flag up. | none | set_flag:FLAG_CH035_FALSE_RELIEF_EXPOSED | false_relief | DT_202. |
| DLG_CH035_BINH_005 | comp_binh | STATE_SNOW_QUESTION | Is snow bad? | none | none | night_camp | DT_203. |
| DLG_CH035_TRUNG_003 | char_trung | STATE_SNOW_QUESTION | No. Snow is snow. | none | none | night_camp | DT_203. |
| DLG_CH035_BINH_006 | comp_binh | STATE_SNOW_QUESTION | But it hides bodies. | none | none | night_camp | DT_203. |
| DLG_CH035_MAI_006 | comp_mai | STATE_SNOW_QUESTION | Some beautiful things can hide pain. Our job is to not let beauty make us stop looking. | none | none | night_camp | DT_203. |
| DLG_CH035_AMELIE_001 | npc_amelie | STATE_PARIS_SIGNAL | Attendance phrase? | none | none | paris_verification | DT_204. |
| DLG_CH035_MAI_007 | comp_mai | STATE_PARIS_SIGNAL | No one may use the blood, name, or absence of children to buy safety. | none | none | paris_verification | DT_204. |
| DLG_CH035_AMELIE_002 | npc_amelie | STATE_PARIS_SIGNAL | Rebirth confirmed. We still take attendance every morning. | none | set_flag:FLAG_CH035_AMELIE_SIGNAL_VERIFIED | paris_verification | DT_204. |
| DLG_CH035_BINH_007 | comp_binh | STATE_PARIS_SIGNAL | How many friends does she have? | none | none | paris_verification | DT_204. |
| DLG_CH035_AMELIE_003 | npc_amelie | STATE_PARIS_SIGNAL | Fewer than yesterday. More than zero. | none | none | paris_verification | DT_204. |
| DLG_CH035_AMELIE_004 | npc_amelie | STATE_MIMIC_WARNING | Something in the tunnel has begun using voices. | none | none | mimic_warning | DT_205. |
| DLG_CH035_DOCTOR_003 | npc_doctor | STATE_MIMIC_WARNING | Infected? | none | none | mimic_warning | DT_205. |
| DLG_CH035_AMELIE_005 | npc_amelie | STATE_MIMIC_WARNING | Maybe. It calls absent children "present." | none | none | mimic_warning | DT_205. |
| DLG_CH035_BINH_008 | comp_binh | STATE_MIMIC_WARNING | It takes wrong attendance. | none | none | mimic_warning | DT_205. |
| DLG_CH035_MAI_008 | comp_mai | STATE_MIMIC_WARNING | Then we go fix the list. | none | set_flag:FLAG_CH035_MIMIC_VOICE_WARNING | mimic_warning | DT_205. |
| DLG_CH035_THU_004 | npc_thu | STATE_ICE_HORDE_RULE | New rule: shooting down does not count as dead. | none | none | ice_horde_rule | DT_206. |
| DLG_CH035_PIKE_002 | npc_pike | STATE_ICE_HORDE_RULE | Burn, shatter, or stem. | none | none | ice_horde_rule | DT_206. |
| DLG_CH035_ONG_TU_001 | npc_ong_tu_nieu | STATE_ICE_HORDE_RULE | I have cooking oil. | none | none | ice_horde_rule | DT_206. |
| DLG_CH035_THU_005 | npc_thu | STATE_ICE_HORDE_RULE | You plan to cook zombies? | none | none | ice_horde_rule | DT_206. |
| DLG_CH035_ONG_TU_002 | npc_ong_tu_nieu | STATE_ICE_HORDE_RULE | I plan to survive with what I have. | none | set_flag:FLAG_CH035_ICE_HORDE_COUNTER_LEARNED | ice_horde_rule | DT_206. |

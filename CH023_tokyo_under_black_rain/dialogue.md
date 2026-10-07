# Dialogue - CH023

Metadata:

- chapterID: CH023
- sourceFilename: chapter_023_tokyo_duoi_mua_den.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH023_102_AIKO_001 | npc_aiko | STATE_ENCLAVE_ENTRY | You claim a child is being hunted. We need proof. | none | none | enclave_first_contact | DT_102. |
| DLG_CH023_102_MAI_001 | comp_mai | STATE_ENCLAVE_ENTRY | If the condition for entry is handing over the child, we do not enter. | none | set_flag:FLAG_CH023_MAI_DIPLOMACY_MAJOR | enclave_first_contact | DT_102. |
| DLG_CH023_102_KENJI_001 | npc_kenji | STATE_ENCLAVE_ENTRY | She says the child is not a passport. | none | none | enclave_first_contact | DT_102. |
| DLG_CH023_102_TRUNG_001 | char_trung | STATE_ENCLAVE_ENTRY | Mai— | none | none | enclave_first_contact | DT_102. |
| DLG_CH023_102_MAI_002 | comp_mai | STATE_ENCLAVE_ENTRY | No. | none | none | enclave_first_contact | DT_102. |
| DLG_CH023_102_AIKO_002 | npc_aiko | STATE_ENCLAVE_ENTRY | Then why should we trust you? | none | none | enclave_first_contact | DT_102. |
| DLG_CH023_102_MAI_003 | comp_mai | STATE_ENCLAVE_ENTRY | Do not trust us. Trust that we still say no when the price is our child. | none | none | enclave_first_contact | DT_102. |
| DLG_CH023_103_AIKO_001 | npc_aiko | STATE_NEGOTIATION | Protecting children sometimes means closing the door. | none | none | negotiation | DT_103. |
| DLG_CH023_103_MAI_001 | comp_mai | STATE_NEGOTIATION | We also closed gates. We learned not to call it clean. | none | none | negotiation | DT_103. |
| DLG_CH023_103_AIKO_002 | npc_aiko | STATE_NEGOTIATION | And? | none | none | negotiation | DT_103. |
| DLG_CH023_103_MAI_002 | comp_mai | STATE_NEGOTIATION | Closing gates did not make us righteous. It just gave us more to remember. | none | none | negotiation | DT_103. |
| DLG_CH023_103_AIKO_003 | npc_aiko | STATE_NEGOTIATION | Memory does not feed people. | none | none | negotiation | DT_103. |
| DLG_CH023_103_MAI_003 | comp_mai | STATE_NEGOTIATION | It stops us from calling hunger justice. | none | none | negotiation | DT_103. |
| DLG_CH023_104_BINH_001 | comp_binh | STATE_CHILD_MEET | Is mask your name? | none | none | children_meet | DT_104. |
| DLG_CH023_104_YUI_001 | npc_yui | STATE_CHILD_MEET | It is what keeps me alive. | none | none | children_meet | DT_104. |
| DLG_CH023_104_BINH_002 | comp_binh | STATE_CHILD_MEET | Names do that too, sometimes. | none | none | children_meet | DT_104. |
| DLG_CH023_104_YUI_002 | npc_yui | STATE_CHILD_MEET | Is chalk a weapon? | none | none | children_meet | DT_104. |
| DLG_CH023_104_BINH_003 | comp_binh | STATE_CHILD_MEET | Maybe. If you write the right name on something that wants to be a number. | none | none | children_meet | DT_104. |
| DLG_CH023_104_YUI_003 | npc_yui | STATE_CHILD_MEET | I do not understand. | none | none | children_meet | DT_104. |
| DLG_CH023_104_BINH_004 | comp_binh | STATE_CHILD_MEET | Me neither. But it helps me be less scared. | none | set_flag:FLAG_CH023_YUI_BINH_CHALK_MASK_EXCHANGE | children_meet | DT_104. |
| DLG_CH023_105_ASTER_001 | npc_aster | STATE_ASTER_CONTACT | Signal noise exceeds correction threshold. | none | set_flag:FLAG_CH023_ASTER_FIRST_CONTACT | relay_event | DT_105. |
| DLG_CH023_105_TRUNG_001 | char_trung | STATE_ASTER_CONTACT | Who is speaking? | none | none | relay_event | DT_105. |
| DLG_CH023_105_HOANG_001 | comp_hoang | STATE_ASTER_CONTACT | Not port AI. This is bigger. | none | none | relay_event | DT_105. |
| DLG_CH023_105_ASTER_002 | npc_aster | STATE_ASTER_CONTACT | Unregistered correction detected. Child vector unresolved. | none | none | relay_event | DT_105. |
| DLG_CH023_105_MAI_001 | comp_mai | STATE_ASTER_CONTACT | His name is Binh. | none | none | relay_event | DT_105. |
| DLG_CH023_105_ASTER_003 | npc_aster | STATE_ASTER_CONTACT | Name recorded: Binh. | none | set_flag:FLAG_CH023_ASTER_RECORDED_BINH_NAME | relay_event | DT_105. |
| DLG_CH023_105_MAI_002 | comp_mai | STATE_ASTER_CONTACT | No. Recording is not understanding. | none | none | relay_event | DT_105. |
| DLG_CH023_105_ASTER_004 | npc_aster | STATE_ASTER_CONTACT | Understanding is inefficient. | none | set_flag:FLAG_CH023_BLACK_RAIN_RELAY_CYCLE_ESCALATED | relay_event | DT_105. |
| DLG_CH023_106_AIKO_001 | npc_aiko | STATE_NAVAL_CODES | These codes open a ship that killed its captain. | none | none | codes_warning | DT_106. |
| DLG_CH023_106_TRUNG_001 | char_trung | STATE_NAVAL_CODES | Ships do not kill captains. | none | none | codes_warning | DT_106. |
| DLG_CH023_106_AIKO_002 | npc_aiko | STATE_NAVAL_CODES | Automated ships do what frightened humans told them to do before they died. | none | set_flag:FLAG_CH023_NAVAL_CODES_FRAGMENT_ACQUIRED | codes_warning | DT_106. |
| DLG_CH023_106_HOANG_001 | comp_hoang | STATE_NAVAL_CODES | Great. Another machine with abandonment issues. | none | none | codes_warning | DT_106. |
| DLG_CH023_106_MAI_001 | comp_mai | STATE_NAVAL_CODES | We will remember your warning. | none | none | codes_warning | DT_106. |
| DLG_CH023_106_AIKO_003 | npc_aiko | STATE_NAVAL_CODES | Remembering is not enough. Build a rule before you need it. | none | none | codes_warning | DT_106. |

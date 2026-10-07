# Dialogue - CH005

Metadata:

- chapterID: CH005
- sourceFilename: chapter_005_khu_an_toan_gia.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH005_LOUDSPEAKER_001 | speaker_false_safe_zone | STATE_GATE_BROADCAST | Children and the injured will be prioritized. Please remain calm. | none | set_flag:FLAG_CH005_CHILD_PRIORITY_SCAM_SEEN | gate_queue | Scene 1 and implementation barks. |
| DLG_CH005_HOANG_SUSPICION_001 | comp_hoang | STATE_FENCE_SUSPICION | Real soldiers do not point barbed wire inward. | none | set_flag:FLAG_CH005_INWARD_BARBED_WIRE_NOTICED | false_gate | DT_015. |
| DLG_CH005_TRUNG_SUSPICION_001 | char_trung | STATE_FENCE_SUSPICION | What do you mean? | none | none | false_gate | DT_015. |
| DLG_CH005_HOANG_SUSPICION_002 | comp_hoang | STATE_FENCE_SUSPICION | I mean this place is not keeping infected out. It is keeping people in. | none | set_flag:FLAG_CH005_TRUST_HOANG_PLUS | false_gate | DT_015. |
| DLG_CH005_TRUNG_SUSPICION_002 | char_trung | STATE_FENCE_SUSPICION | Mai could be inside. | none | set_flag:FLAG_CH005_FAMILY_DRIVE_PLUS | false_gate | DT_015. |
| DLG_CH005_HOANG_SUSPICION_003 | comp_hoang | STATE_FENCE_SUSPICION | Then we go in like we are entering a trap, not like we are coming home. | none | set_flag:FLAG_CH005_TRUST_HOANG_PLUS | false_gate | DT_015. |
| DLG_CH005_MANAGER_001 | npc_false_safe_manager | STATE_PROCESSING_FEE | Everyone has family, friend. If you want to search quickly, there is a processing fee. | Choice A: Give medicine or fuel.; Choice B: "Real soldiers do not charge refugees."; Choice C: Let Hoang talk. | open_choice | registry_table | DT_014. |
| DLG_CH005_MANAGER_002A | npc_false_safe_manager | STATE_PROCESSING_FEE_A | Good. Now we can move your request forward. | none | set_flag:FLAG_CH005_PRAGMATISM_PLUS;set_flag:FLAG_CH005_REGISTRY_ACCESSED | choice:DLG_CH005_MANAGER_001:A | DT_014 Choice A. |
| DLG_CH005_MANAGER_002B | npc_false_safe_manager | STATE_PROCESSING_FEE_B | Careful. Accusing the checkpoint staff during an emergency is a security issue. | none | set_flag:FLAG_CH005_INTEGRITY_PLUS;set_flag:FLAG_CH005_CONFLICT_PLUS | choice:DLG_CH005_MANAGER_001:B | DT_014 Choice B. |
| DLG_CH005_HOANG_FEE_001 | comp_hoang | STATE_PROCESSING_FEE_C | Does the processing fee come with a receipt, or should I write one for you? | none | set_flag:FLAG_CH005_TRUST_HOANG_PLUS;set_flag:FLAG_CH005_REGISTRY_ACCESS_DISTRACTION | choice:DLG_CH005_MANAGER_001:C | DT_014 Choice C. |
| DLG_CH005_TRUNG_REGISTRY_001 | char_trung | STATE_REGISTRY_FIND | My wife and child are not a procedure. | none | set_flag:FLAG_CH005_MAI_BINH_TRANSFER_LIST_FOUND | registry_line_seen | Scene 2 and implementation barks. |
| DLG_CH005_MOTHER_001 | npc_separated_mother | STATE_CHILD_TAKEN | They said children were prioritized. I handed my child through the gate, then they locked it. | Choice A: "I will find your child."; Choice B: "I am looking for my child too."; Choice C: "I cannot stop." | open_choice | separated_mother_event | DT_016. |
| DLG_CH005_MOTHER_002A | char_trung | STATE_CHILD_TAKEN_A | I will find your child. | none | set_flag:FLAG_CH005_COMPASSION_PLUS;set_flag:FLAG_CH005_CHILD_PRIORITY_ROUTE_UNLOCKED | choice:DLG_CH005_MOTHER_001:A | DT_016 Choice A. |
| DLG_CH005_MOTHER_002B | char_trung | STATE_CHILD_TAKEN_B | I am looking for my child too. | none | set_flag:FLAG_CH005_FAMILY_MIRROR_PLUS | choice:DLG_CH005_MOTHER_001:B | DT_016 Choice B. |
| DLG_CH005_MOTHER_002C | char_trung | STATE_CHILD_TAKEN_C | I cannot stop. | none | set_flag:FLAG_CH005_FAMILY_FIRST_PLUS;set_flag:FLAG_CH005_GUILT_PLUS | choice:DLG_CH005_MOTHER_001:C | DT_016 Choice C. |
| DLG_CH005_QUARANTINE_001 | npc_quarantine_survivor | STATE_TENT_PLEA | Please... we are not all infected. | none | set_flag:FLAG_CH005_QUARANTINE_SURVIVORS_HEARD | quarantine_tent | Scene 4. |
| DLG_CH005_MAI_NOTE_001 | char_mai | STATE_TENT_CHALK_NOTE | NOT HERE. | none | set_flag:FLAG_CH005_MAI_NOT_HERE_NOTE_FOUND | inspect:ITM_CH005_MAI_NOT_HERE_CHALK | Scene 4. |
| DLG_CH005_HOANG_LURKER_001 | comp_hoang | STATE_LURKER_WARNING | It waits for the light. Keep your back off the dark. | none | set_flag:FLAG_CH005_LURKER_KNOWLEDGE_UNLOCKED | lurker_seen | Scene 4 Lurker behavior. |
| DLG_CH005_RECORDS_001 | char_trung | STATE_TRANSFER_LIST | "Mai plus boy in blue shirt." That is them. | none | set_flag:FLAG_CH005_MAI_BINH_TRANSFER_LIST_FOUND | inspect:ITM_CH005_RIPPED_TRANSFER_LIST | DT_017. |
| DLG_CH005_RECORDS_002 | comp_hoang | STATE_TRANSFER_LIST | The next column says transfer. | none | none | inspect:ITM_CH005_RIPPED_TRANSFER_LIST | DT_017. |
| DLG_CH005_RECORDS_003 | char_trung | STATE_TRANSFER_LIST | Transferred where? | none | none | inspect:ITM_CH005_RIPPED_TRANSFER_LIST | DT_017. |
| DLG_CH005_RECORDS_004 | comp_hoang | STATE_TRANSFER_LIST | Two columns. Skilled adults to the outpost. Children have a separate column. | none | none | inspect:ITM_CH005_RIPPED_TRANSFER_LIST | DT_017. |
| DLG_CH005_RECORDS_005 | char_trung | STATE_TRANSFER_LIST | Read it. | none | none | inspect:ITM_CH005_RIPPED_TRANSFER_LIST | DT_017. |
| DLG_CH005_RECORDS_006 | comp_hoang | STATE_TRANSFER_LIST | Monitor. There is also an E mark. I do not know what it means. | none | set_flag:FLAG_CH005_EDEN_MARK_SEEN | inspect:ITM_CH005_RIPPED_TRANSFER_LIST | DT_017 and Continuity Notes. |
| DLG_CH005_MAI_NOTE_002 | char_mai | STATE_BACK_ROOM_CHALK_NOTE | GET OUT. | none | set_flag:FLAG_CH005_GET_OUT_NOTE_FOUND | inspect:ITM_CH005_GET_OUT_CHALK | Scene 5. |
| DLG_CH005_MANAGER_COLLAPSE_001 | npc_false_safe_manager | STATE_GATE_COLLAPSE | Close the gate! Close it now! | none | set_flag:FLAG_CH005_GATE_COLLAPSE_STARTED | gate_collapse | Scene 6. |
| DLG_CH005_RETIRED_SOLDIER_001 | npc_retired_soldier | STATE_GATE_HOLD | Go! I asked for a rifle. I got a gate. | none | set_flag:FLAG_CH005_RETIRED_SOLDIER_HOLDS_GATE | gate_collapse | Scene 6. |
| DLG_CH005_HOANG_END_001 | comp_hoang | STATE_AFTER_FENCE | Next time, listen to me sooner. | none | none | drainage_retreat | Scene 7. |
| DLG_CH005_TRUNG_END_001 | char_trung | STATE_AFTER_FENCE | Next time, do not let me become someone who no longer wants to trust anyone. | none | set_flag:FLAG_CH005_TRUST_WOUND_WITH_HOANG | drainage_retreat | Scene 7. |

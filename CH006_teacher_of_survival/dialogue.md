# Dialogue - CH006

Metadata:

- chapterID: CH006
- sourceFilename: chapter_006_nguoi_day_cach_song_sot.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH006_GUARD_001 | npc_young_guard | STATE_GATE_RULE | Line up. Bite check. Anyone who lies gets the whole line killed. | none | set_flag:FLAG_CH006_BITE_CHECK_STARTED | outpost_gate | Scene 1 and implementation bark. |
| DLG_CH006_HOANG_001 | comp_hoang | STATE_REAL_OUTPOST | This place looks like it wants to survive tomorrow. That is a better sign than a welcome banner. | none | none | outpost_approach | Scene 1. |
| DLG_CH006_MENTOR_BITE_001 | npc_mentor | STATE_HIDDEN_BITE | Left wrist. Open it. | none | set_flag:FLAG_CH006_HIDDEN_BITE_FOUND | hidden_bite_suspected | Scene 1-2. |
| DLG_CH006_MENTOR_BITE_002 | npc_mentor | STATE_HIDDEN_BITE | Isolation. If she has not turned, no one shoots. If she turns, no one gets close. | none | set_flag:FLAG_CH006_DISCIPLINE_SEED | hidden_bite_revealed | Scene 1-2. |
| DLG_CH006_MENTOR_EVIDENCE_001 | npc_mentor | STATE_FALSE_STAMP | Who took this? | none | none | evidence_present | Scene 2. |
| DLG_CH006_TRUNG_EVIDENCE_001 | char_trung | STATE_FALSE_STAMP | I did. From the false checkpoint. My wife and son passed through there. | none | set_flag:FLAG_CH006_FAKE_STAMP_DELIVERED | evidence_present | Scene 2. |
| DLG_CH006_MENTOR_MEET_001 | npc_mentor | STATE_MEET_MENTOR | Name? | none | none | mentor_first_meeting | DT_018. |
| DLG_CH006_TRUNG_MEET_001 | char_trung | STATE_MEET_MENTOR | Trung. I need to find my wife and child. | none | none | mentor_first_meeting | DT_018. |
| DLG_CH006_MENTOR_MEET_002 | npc_mentor | STATE_MEET_MENTOR | Everyone outside needs to find someone. Can you load a magazine? | Choice A: "No. But I can learn."; Choice B: "I do not need a gun. I need a road."; Choice C: "Are you helping or not?" | open_choice | mentor_first_meeting | DT_018. |
| DLG_CH006_MENTOR_MEET_003A | npc_mentor | STATE_MEET_A | You are alive because you can tell the truth. Good. | none | set_flag:FLAG_CH006_MENTOR_RESPECT_PLUS | choice:DLG_CH006_MENTOR_MEET_002:A | DT_018 Choice A. |
| DLG_CH006_MENTOR_MEET_003B | npc_mentor | STATE_MEET_B | Roads are full of bodies. You need a gun. | none | set_flag:FLAG_CH006_URGENCY_PLUS | choice:DLG_CH006_MENTOR_MEET_002:B | DT_018 Choice B. |
| DLG_CH006_MENTOR_MEET_003C | npc_mentor | STATE_MEET_C | I help people who can survive until morning. | none | set_flag:FLAG_CH006_TENSION_PLUS | choice:DLG_CH006_MENTOR_MEET_002:C | DT_018 Choice C. |
| DLG_CH006_DOCTOR_001 | npc_doctor | STATE_TRIAGE | I have eight doses and twenty people who need them. You tell me who lives. | Choice A: "Children first."; Choice B: "People who can protect more people first."; Choice C: "No one has the right to choose." | open_choice | triage_tent | DT_021. |
| DLG_CH006_DOCTOR_002A | npc_doctor | STATE_TRIAGE_A | And if the guard dies, who holds the gate for those children? | none | set_flag:FLAG_CH006_COMPASSION_PLUS | choice:DLG_CH006_DOCTOR_001:A | DT_021 Choice A. |
| DLG_CH006_DOCTOR_002B | npc_doctor | STATE_TRIAGE_B | You sound like a soldier now. Can you look at the people left behind? | none | set_flag:FLAG_CH006_PRAGMATISM_PLUS | choice:DLG_CH006_DOCTOR_001:B | DT_021 Choice B. |
| DLG_CH006_DOCTOR_002C | npc_doctor | STATE_TRIAGE_C | Then the virus chooses for us. | none | set_flag:FLAG_CH006_MORAL_CONFLICT_PLUS | choice:DLG_CH006_DOCTOR_001:C | DT_021 Choice C. |
| DLG_CH006_RADIO_001 | npc_radio_operator | STATE_RADIO_FRAGMENT | The signal is short. It may be live, old, or reflected off a tower. | none | none | radio_tent | Scene 4. |
| DLG_CH006_RADIO_FRAGMENT_001 | char_mai | STATE_RADIO_FRAGMENT | ...Binh, lie down... | none | set_flag:FLAG_CH006_RADIO_FRAGMENT_MAI_HEARD | radio_signal_played | DT_019. |
| DLG_CH006_TRUNG_RADIO_001 | char_trung | STATE_RADIO_PANIC | That is my wife. | none | set_flag:FLAG_CH006_FAMILY_PANIC_PLUS | radio_signal_played | DT_019. |
| DLG_CH006_MENTOR_RADIO_001 | npc_mentor | STATE_RADIO_WARNING | It could be an old signal. | none | none | radio_signal_played | DT_019. |
| DLG_CH006_TRUNG_RADIO_002 | char_trung | STATE_RADIO_WARNING | You do not know that. | none | none | radio_signal_played | DT_019. |
| DLG_CH006_MENTOR_RADIO_002 | npc_mentor | STATE_RADIO_WARNING | I know chasing the voices of the dead has killed many living people. | none | none | radio_signal_played | DT_019. |
| DLG_CH006_TRUNG_RADIO_003 | char_trung | STATE_RADIO_WARNING | She is not dead. | none | none | radio_signal_played | DT_019. |
| DLG_CH006_MENTOR_RADIO_003 | npc_mentor | STATE_RADIO_WARNING | Then do not make her lose a husband to static. | none | set_flag:FLAG_CH006_DISCIPLINE_SEED | radio_signal_played | DT_019. |
| DLG_CH006_MENTOR_LOST_CHILD_001 | npc_mentor | STATE_LOST_CHILD_SEED | I had a child. | none | set_flag:FLAG_CH006_MENTOR_LOST_CHILD_SEED | radio_argument | Scene 4. |
| DLG_CH006_HOANG_MENTOR_001 | comp_hoang | STATE_HOANG_ON_MENTOR | The old man is terrifying, but he is right. | none | none | training_yard | DT_020. |
| DLG_CH006_TRUNG_MENTOR_001 | char_trung | STATE_HOANG_ON_MENTOR | I do not have time to train. | none | none | training_yard | DT_020. |
| DLG_CH006_HOANG_MENTOR_002 | comp_hoang | STATE_HOANG_ON_MENTOR | You do not have time to die. More accurate. | none | none | training_yard | DT_020. |
| DLG_CH006_TRUNG_MENTOR_002 | char_trung | STATE_HOANG_ON_MENTOR | Since when are you on the side of people giving orders? | none | none | training_yard | DT_020. |
| DLG_CH006_HOANG_MENTOR_003 | comp_hoang | STATE_HOANG_ON_MENTOR | Since the person giving orders sounds like he might keep you alive. | none | set_flag:FLAG_CH006_HOANG_POSITION_SHIFT | training_yard | DT_020. |
| DLG_CH006_PHUC_001 | npc_phuc | STATE_FENCE_RESCUE | Pull me! Please! | none | none | west_fence_attack | Scene 6. |
| DLG_CH006_MENTOR_PHUC_001 | npc_mentor | STATE_AFTER_RESCUE | His name is Phuc. Remember the names of the living, not only the names of the missing. | none | set_flag:FLAG_CH006_PHUC_RESCUED;set_flag:FLAG_CH006_MENTOR_RESPECT_PLUS | phuc_rescued | Scene 6. |
| DLG_CH006_MENTOR_FINAL_001 | npc_mentor | STATE_FIRST_ORDER | If you want to find your family, first stop dying like an amateur. | none | set_flag:FLAG_CH006_MENTOR_TRAINING_ACCEPTED;set_flag:FLAG_CH006_DISCIPLINE_SEED | chapter_end | Scene 7 and implementation bark. |

# Scenes - CH006

Metadata:

- chapterID: CH006
- sourceFilename: chapter_006_nguoi_day_cach_song_sot.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH006_REAL_OUTPOST | No Sign That Says Safe | LOC_CH006_OUTPOST_ROAD | Contrast real outpost with false safe zone. | Trung and Hoang retreat from CH005 with evidence. | Player approaches gate and sees real defensive discipline. | char_trung;comp_hoang;npc_young_guard;npc_mentor | ENM_CH006_OUTPOST_APPROACH_INFECTED | ITM_CH006_FALSE_SAFE_EVIDENCE_BUNDLE | Scene 1 - Noi khong co bang an toan. |
| SCN_CH006_BITE_CHECK | Bite Check | LOC_CH006_DECONTAMINATION_LINE | Show real discipline and hidden bite danger. | Player enters inspection queue. | Hidden bite is isolated and Trung understands procedure has value. | char_trung;comp_hoang;npc_mentor;npc_refugee_hidden_bite;npc_young_guard | ENM_CH006_HIDDEN_BITE_TURNING | ITM_CH006_BITE_INSPECTION_TAG;ITM_CH006_HIDDEN_BITE_BANDAGE;ITM_CH005_RIPPED_TRANSFER_LIST;ITM_CH005_FAKE_MILITARY_STAMP | Scene 2 - Kiem tra vet can. |
| SCN_CH006_TRIAGE | Triage Without Enough Medicine | LOC_CH006_TRIAGE_TENT | Force resource morality through doctor choice. | Player passes inspection and enters medical area. | Player helps, argues, or observes triage scarcity. | char_trung;comp_hoang;npc_doctor;npc_refugee_mother;npc_sick_child_triage;npc_phuc | none | ITM_CH006_ANTIBIOTIC_DOSE;ITM_CH006_SMALL_MEDKIT;ITM_CH006_SUPPLY_LEDGER | Scene 3 - Triage khong co du thuoc. |
| SCN_CH006_RADIO_NOISE | Radio Noise | LOC_CH006_RADIO_TENT | Pull Mai back as uncertain sound and trigger Trung's panic. | Radio operator may have a fragment tied to Mai/Binh. | Trung is stopped from rushing out after uncertain signal. | char_trung;comp_hoang;npc_radio_operator;npc_mentor;char_mai;char_binh | none | ITM_CH006_NOISY_MAI_SIGNAL;ITM_CH006_RADIO_HEADSET;ITM_CH006_RADIO_FILTER_PARTS | Scene 4 - Radio nhieu. |
| SCN_CH006_MEET_MENTOR | Mentor | LOC_CH006_TRAINING_YARD | Introduce Mentor as skill gate and trainer. | Trung confronts Mentor after radio argument. | Player completes first truth/skill check and receives training challenge. | char_trung;comp_hoang;npc_mentor | none | ITM_CH006_EMPTY_MAGAZINE;ITM_CH006_TRAINING_RIFLE;ITM_CH006_CHILD_TOKEN_MENTOR | Scene 5 - Mentor. |
| SCN_CH006_FENCE_TEST | Fence Test | LOC_CH006_WEST_FENCE | Test action under pressure: rescue Phuc or chase radio. | Infected scout group approaches while radio signal returns. | Canon route: Phuc rescued, radio signal lost, Mentor respect gained. | char_trung;comp_hoang;npc_mentor;npc_phuc;npc_radio_operator | ENM_CH006_INFECTED_SCOUT_GROUP;ENM_CH006_GATE_PRESSURE_INFECTED | ITM_CH006_WEST_GATE_BARRIER;ITM_CH006_NOISY_MAI_SIGNAL | Scene 6 - Bai test hang rao. |
| SCN_CH006_FIRST_ORDER | First Order | LOC_CH006_WEST_FENCE | Mentor accepts training Trung and sets survival rule. | Fence attack ends and Phuc survives. | Mentor training arc unlocks. | char_trung;comp_hoang;npc_mentor;npc_phuc | none | ITM_CH006_EMPTY_MAGAZINE;ITM_CH006_TRAINING_RIFLE | Scene 7 - Lenh dau tien. |

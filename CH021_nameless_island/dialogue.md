# Dialogue - CH021

Metadata:

- chapterID: CH021
- sourceFilename: chapter_021_dao_khong_ten.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH021_092_THU_001 | comp_thu | STATE_BOAT_ASSESS | Bad news: this boat is dying. Good news? It dies slower than us if I get filter, belt, sealant, and battery. | none | none | after_bio_storm | DT_092. |
| DLG_CH021_092_HOANG_001 | comp_hoang | STATE_BOAT_ASSESS | I can fix the radio panel. | none | none | after_bio_storm | DT_092. |
| DLG_CH021_092_THU_002 | comp_thu | STATE_BOAT_ASSESS | Stay where I can hear you. | none | none | after_bio_storm | DT_092. |
| DLG_CH021_092_HOANG_002 | comp_hoang | STATE_BOAT_ASSESS | Still in the warm trust phase? | none | none | after_bio_storm | DT_092. |
| DLG_CH021_092_THU_003 | comp_thu | STATE_BOAT_ASSESS | I just met you and heard you sell coordinates. You are getting preferential treatment for not being thrown overboard yet. | none | none | after_bio_storm | DT_092. |
| DLG_CH021_093_TRUNG_001 | char_trung | STATE_CLASSROOM_DEBATE | Mai, the engine is not running. Can this wait? | none | none | classroom_setup | DT_093. |
| DLG_CH021_093_MAI_001 | comp_mai | STATE_CLASSROOM_DEBATE | If we wait until it is safe to teach children how to live, they will only learn fear. | none | set_flag:FLAG_CH021_BOAT_CLASSROOM_CREATED | classroom_setup | DT_093. |
| DLG_CH021_093_TRUNG_002 | char_trung | STATE_CLASSROOM_DEBATE | I am not saying it is not important. | none | none | classroom_setup | DT_093. |
| DLG_CH021_093_MAI_002 | comp_mai | STATE_CLASSROOM_DEBATE | I know. You are saying it is not urgent. For children, every new place is urgent. | none | none | classroom_setup | DT_093. |
| DLG_CH021_093_BINH_001 | comp_binh | STATE_CLASSROOM_DEBATE | The writing is crooked. | none | none | classroom_setup | DT_093. |
| DLG_CH021_093_MAI_003 | comp_mai | STATE_CLASSROOM_DEBATE | The boat is rocking. | none | none | classroom_setup | DT_093. |
| DLG_CH021_093_BINH_002 | comp_binh | STATE_CLASSROOM_DEBATE | So crooked letters are okay? | none | none | classroom_setup | DT_093. |
| DLG_CH021_093_MAI_004 | comp_mai | STATE_CLASSROOM_DEBATE | Yes. Crooked letters are still a name. | none | none | classroom_setup | DT_093. |
| DLG_CH021_094_HOANG_001 | comp_hoang | STATE_HOANG_APOLOGY | Binh. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_BINH_001 | comp_binh | STATE_HOANG_APOLOGY | There are adults here. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_HOANG_002 | comp_hoang | STATE_HOANG_APOLOGY | I know. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_BINH_002 | comp_binh | STATE_HOANG_APOLOGY | Then you can speak. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_HOANG_003 | comp_hoang | STATE_HOANG_APOLOGY | I am fixing this so the boat runs. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_BINH_003 | comp_binh | STATE_HOANG_APOLOGY | That is not an apology. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_HOANG_004 | comp_hoang | STATE_HOANG_APOLOGY | No. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_BINH_004 | comp_binh | STATE_HOANG_APOLOGY | When you know which words are real, then say them. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_HOANG_005 | comp_hoang | STATE_HOANG_APOLOGY | I am learning. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_094_BINH_005 | comp_binh | STATE_HOANG_APOLOGY | Me too. | none | none | hoang_near_binh | DT_094. |
| DLG_CH021_095_LAM_001 | comp_lam | STATE_BOAT_NAMING | A boat without a name sails like a person without a shadow. | none | none | boat_naming | DT_095. |
| DLG_CH021_095_THU_001 | comp_thu | STATE_BOAT_NAMING | A name does not fix an engine. | none | none | boat_naming | DT_095. |
| DLG_CH021_095_ONG_001 | npc_ong_tu_nieu | STATE_BOAT_NAMING | But it lets the cook know what to call it when it leaks. | none | none | boat_naming | DT_095. |
| DLG_CH021_095_MAI_001 | comp_mai | STATE_BOAT_NAMING | We should not call it Nha. The first Nha is still there. | none | none | boat_naming | DT_095. |
| DLG_CH021_095_BINH_001 | comp_binh | STATE_BOAT_NAMING | Then call it Nha Di. | none | set_flag:FLAG_CH021_VESSEL_NAMED | boat_naming | DT_095. |
| DLG_CH021_095_TRUNG_001 | char_trung | STATE_BOAT_NAMING | Nha Di? | none | none | boat_naming | DT_095. |
| DLG_CH021_095_BINH_002 | comp_binh | STATE_BOAT_NAMING | Because it moves. We move too. If the rain washes it off, we write it again. | none | none | boat_naming | DT_095. |
| DLG_CH021_095_THU_002 | comp_thu | STATE_BOAT_NAMING | The name sounds like a reminder that engine repair never ends. | none | none | boat_naming | DT_095. |
| DLG_CH021_095_LAM_002 | comp_lam | STATE_BOAT_NAMING | Good name. | none | none | boat_naming | DT_095. |
| DLG_CH021_096_DOCTOR_001 | comp_doctor | STATE_DROWNED_FIGHT | It does not react like a Runner. | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_THU_001 | comp_thu | STATE_DROWNED_FIGHT | It reacts like something that was underwater too long and is angry about being pulled up. | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_HOANG_001 | comp_hoang | STATE_DROWNED_FIGHT | Shoot for the head? | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_LAM_001 | comp_lam | STATE_DROWNED_FIGHT | Shoot for the head and the whole sea hears. | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_TRUNG_001 | char_trung | STATE_DROWNED_FIGHT | Weak points? | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_THU_002 | comp_thu | STATE_DROWNED_FIGHT | Joints. Knock it down. Do not let it get a crawling position. | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_BINH_001 | comp_binh | STATE_DROWNED_FIGHT | Does it remember who it used to be? | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_MAI_001 | comp_mai | STATE_DROWNED_FIGHT | We do not know. | none | none | drowned_attack | DT_096. |
| DLG_CH021_096_BINH_002 | comp_binh | STATE_DROWNED_FIGHT | Then do not let it take someone else's name. | none | none | drowned_attack | DT_096. |
| DLG_CH021_char_binh_001 | char_binh | STATE_BASE | Dad, the ocean is so big! But the water is too salty to drink, and it smells like dead fish. | Choice 1: "Are you scared of the water?" : STATE_BINH_CHAT_SEA \| Choice 2: "How is the boat?" : STATE_BINH_CHAT_BOAT | none | none | none |
| DLG_CH021_char_binh_002 | char_binh | STATE_BINH_CHAT_SEA | A little. Sometimes I look down and think I see giant shadows moving. | Choice 1: "Just fish, son." : STATE_BINH_CHAT_SEA_FISH \| Choice 2: "We are safe on the boat." : STATE_BASE | none | none | none |
| DLG_CH021_char_binh_003 | char_binh | STATE_BINH_CHAT_SEA_FISH | I hope they don't have big teeth! | none | none | none | none |
| DLG_CH021_char_binh_004 | char_binh | STATE_BINH_CHAT_BOAT | It's noisy and shaky. I wish we could run on land again. | none | none | none | none |
| DLG_CH021_char_mai_001 | char_mai | STATE_BASE | The soil on this island has a strange pH value. Some plants show minor mutations, but nothing like the infected. | Choice 1: "Can we find fresh water?" : STATE_MAI_CHAT_WATER \| Choice 2: "Is the air clean?" : STATE_MAI_CHAT_AIR | none | none | none |
| DLG_CH021_char_mai_002 | char_mai | STATE_MAI_CHAT_WATER | Yes, there is a stream near the center. I'm filtering a sample now. | none | none | none | none |
| DLG_CH021_char_mai_003 | char_mai | STATE_MAI_CHAT_AIR | The wind from the east brings some ashes, but it is safe. For now. | none | none | none | none |

# Dialogue - CH004

Metadata:

- chapterID: CH004
- sourceFilename: chapter_004_ban_than_trong_khoi_lua.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH004_NEIGHBOR_PLEA_001 | npc_neighbor_mention | STATE_BACK_ALLEY_PLEA | Please! My mother is trapped up here! | none | none | north_back_alley | Scene 1. |
| DLG_CH004_TRUNG_001 | char_trung | STATE_BACK_ALLEY_CHOICE | I will tell someone below. | none | set_flag:FLAG_CH004_UNSAVED_PLEA_HEARD | north_back_alley | Scene 1. |
| DLG_CH004_FAKE_GUIDE_001 | npc_fake_guide_leader | STATE_FAKE_ROUTE | Heading to the northern checkpoint? That way is blocked. Pay us and we will take you through the safe route. | Choice A: Follow them.; Choice B: Challenge the route.; Choice C: Refuse and keep following the chalk. | open_choice | canal_bridge | Scene 2 and SQ_Hoang_04. |
| DLG_CH004_FAKE_GUIDE_002A | npc_fake_guide_leader | STATE_FAKE_ROUTE_ACCEPT | Smart choice. Stay close and do not ask too many questions. | none | set_flag:FLAG_CH004_FAKE_GUIDE_ROUTE_ENTERED | choice:DLG_CH004_FAKE_GUIDE_001:A | Scene 2. |
| DLG_CH004_FAKE_GUIDE_002B | char_trung | STATE_FAKE_ROUTE_CHALLENGE | If this route is safe, why are the chalk marks pointing somewhere else? | none | set_flag:FLAG_CH004_FAKE_GUIDES_EXPOSED;set_flag:FLAG_CH004_INSIGHT_PLUS | choice:DLG_CH004_FAKE_GUIDE_001:B | Scene 2. |
| DLG_CH004_FAKE_GUIDE_002C | char_trung | STATE_FAKE_ROUTE_REFUSE | I have my own trail. Move. | none | set_flag:FLAG_CH004_PRAGMATISM_PLUS | choice:DLG_CH004_FAKE_GUIDE_001:C | Scene 2. |
| DLG_CH004_SURVIVOR_WOMAN_001 | npc_survivor_woman | STATE_FAKE_ROUTE_VICTIM | I told them to stop lying. They keep leading people into that alley. | none | none | fake_guides_exposed | Scene 2. |
| DLG_CH004_HOANG_RESCUE_001 | comp_hoang | STATE_RESCUE_START | Get on! | Choice A: "You actually came."; Choice B: "Mai and Binh are north."; Choice C: "There were people in that alley..." | open_choice | runner_near_death | DT_010. |
| DLG_CH004_HOANG_RESCUE_002A | comp_hoang | STATE_RESCUE_A | I am surprised too. Get on before I change my mind. | none | set_flag:FLAG_CH004_TRUST_HOANG_PLUS | choice:DLG_CH004_HOANG_RESCUE_001:A | DT_010 Choice A. |
| DLG_CH004_HOANG_RESCUE_002B | comp_hoang | STATE_RESCUE_B | I know. I saw them on camera. Live first, feel later. | none | set_flag:FLAG_CH004_FAMILY_DRIVE_PLUS | choice:DLG_CH004_HOANG_RESCUE_001:B | DT_010 Choice B. |
| DLG_CH004_HOANG_RESCUE_002C | comp_hoang | STATE_RESCUE_C | Do you want to carry them out, or should I carry your body back to your wife and child? | none | set_flag:FLAG_CH004_HOANG_PRAGMATISM_SEED | choice:DLG_CH004_HOANG_RESCUE_001:C | DT_010 Choice C. |
| DLG_CH004_HOANG_BANTER_001 | comp_hoang | STATE_BIKE_BANTER | The city ends and you still review my driving like this is a ride app. | none | none | hoang_motorbike_escape | Scene 4. |
| DLG_CH004_TRUNG_BANTER_001 | char_trung | STATE_BIKE_BANTER | You drive like a maniac. | none | none | hoang_motorbike_escape | Scene 4. |
| DLG_CH004_HOANG_REASON_001 | comp_hoang | STATE_HOANG_REASON | You owe me coffee money. Apocalypse rates. One cup is half a tank of gas. | none | set_flag:FLAG_CH004_TRUST_HOANG_PLUS | hoang_reunited | Scene 4. |
| DLG_CH004_CAMERA_001 | comp_hoang | STATE_CAMERA_TERMINAL | I am reusing public infrastructure during a crisis. That sounds more legal than hacking. | none | none | traffic_camera_terminal | Scene 5. |
| DLG_CH004_CAMERA_002 | char_trung | STATE_CAMERA_FIND | Mai. That is Mai. | none | set_flag:FLAG_CH004_MAI_BINH_CAMERA_CONFIRMED | camera_feed_active | Scene 5. |
| DLG_CH004_CAMERA_003 | comp_hoang | STATE_CAMERA_WARNING | The node is being taken over. I am not the only one inside this system. | none | set_flag:FLAG_CH004_UNKNOWN_CAMERA_ACCESS_SEEN | camera_feed_cutting | Scene 5 lore seed. |
| DLG_CH004_SURVIVORS_001 | npc_trapped_survivor_leader | STATE_TRAPPED_CALL | Hoang! You said you would come back! | none | set_flag:FLAG_CH004_HOANG_SECRET_REVEALED | trapped_survivors_heard | Scene 6 and DT_013. |
| DLG_CH004_TRUNG_SURVIVORS_001 | char_trung | STATE_SURVIVOR_ARGUMENT | There are people upstairs. | none | none | trapped_survivors_heard | DT_011. |
| DLG_CH004_HOANG_SURVIVORS_001 | comp_hoang | STATE_SURVIVOR_ARGUMENT | There are infected below, fire behind us, and your wife and child ahead of us. | Choice A: "I am saving them."; Choice B: "We go."; Choice C: "We leave directions and open the outside lock." | open_choice | trapped_survivors_heard | DT_011. |
| DLG_CH004_HOANG_SURVIVORS_002A | comp_hoang | STATE_SURVIVOR_A | You always choose the longest road. | none | set_flag:FLAG_CH004_SURVIVORS_RESCUED;set_flag:FLAG_CH004_COMPASSION_PLUS;set_flag:FLAG_CH004_HOANG_CONCERN_PLUS | choice:DLG_CH004_HOANG_SURVIVORS_001:A | DT_011 Choice A. |
| DLG_CH004_HOANG_SURVIVORS_002B | comp_hoang | STATE_SURVIVOR_B | First sensible thing you have said today. | none | set_flag:FLAG_CH004_SURVIVORS_ABANDONED;set_flag:FLAG_CH004_PRAGMATISM_PLUS;set_flag:FLAG_CH004_GUILT_PLUS | choice:DLG_CH004_HOANG_SURVIVORS_001:B | DT_011 Choice B. |
| DLG_CH004_HOANG_SURVIVORS_002C | comp_hoang | STATE_SURVIVOR_C | Half decent, half alive. I can accept that. | none | set_flag:FLAG_CH004_SURVIVORS_AIDED;set_flag:FLAG_CH004_BALANCED_PLUS | choice:DLG_CH004_HOANG_SURVIVORS_001:C | DT_011 Choice C. |
| DLG_CH004_SECRET_001 | npc_trapped_survivor_leader | STATE_SECRET_REVEAL | You came back because your friend made you. | Choice A: Question Hoang now.; Choice B: Stay silent until escape.; Choice C: Defend Hoang in front of them. | open_choice | survivors_rescued | DT_013. |
| DLG_CH004_SECRET_002A | comp_hoang | STATE_SECRET_A | I chose to find you first. Be angry later if we live. | none | set_flag:FLAG_CH004_HOANG_SECRET_REVEALED | choice:DLG_CH004_SECRET_001:A | DT_013 Choice A. |
| DLG_CH004_SECRET_002B | char_trung | STATE_SECRET_B |  | none | set_flag:FLAG_CH004_SUSPICION_PLUS | choice:DLG_CH004_SECRET_001:B | DT_013 Choice B. |
| DLG_CH004_SECRET_002C | char_trung | STATE_SECRET_C | He came back this time. Move. | none | set_flag:FLAG_CH004_TRUST_HOANG_PLUS;set_flag:FLAG_CH004_PRAGMATISM_PLUS | choice:DLG_CH004_SECRET_001:C | DT_013 Choice C. |
| DLG_CH004_INNER_CIRCLE_001 | comp_hoang | STATE_INNER_CIRCLE | From now on, we live by the inner circle. | none | set_flag:FLAG_CH004_INNER_CIRCLE_DEFINED | bike_to_checkpoint | DT_012. |
| DLG_CH004_INNER_CIRCLE_002 | char_trung | STATE_INNER_CIRCLE | What circle? | none | none | bike_to_checkpoint | DT_012. |
| DLG_CH004_INNER_CIRCLE_003 | comp_hoang | STATE_INNER_CIRCLE | Our people. Mai, Binh, you, me. Anyone outside that circle, we help if we can. If not, we keep moving. | none | none | bike_to_checkpoint | DT_012. |
| DLG_CH004_INNER_CIRCLE_004 | char_trung | STATE_INNER_CIRCLE | If everyone thinks like that, the world dies. | none | none | bike_to_checkpoint | DT_012. |
| DLG_CH004_INNER_CIRCLE_005 | comp_hoang | STATE_INNER_CIRCLE | The world is already dead. You are talking about its funeral. | none | set_flag:FLAG_CH004_INNER_CIRCLE_DEFINED | bike_to_checkpoint | DT_012. |

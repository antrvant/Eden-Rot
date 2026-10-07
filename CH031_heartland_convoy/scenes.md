# Scenes - CH031

Metadata:

- chapterID: CH031
- sourceFilename: chapter_031_heartland_convoy.md
- language: English

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |
|---|---|---|---|---|---|---|---|---|---|
| SCN_CH031_EMPTY_SEAT | Empty Seat | LOC_CH031_MORNING_CONVVOY_CAMP | Process Hoang's absence and establish convoy burden | Morning after CH030 | Convoy must move before Cult scouts regroup | char_trung;comp_mai;comp_binh | none | ITM_CH031_HOANG_PACKET_LOG;ITM_CH031_HOANG_DEPARTURE_NOTE | Scene 1. |
| SCN_CH031_MOBILE_NATION | Mobile Nation | LOC_CH031_ROLLING_HIGHWAY | Define mobile base systems | Convoy on highway | VALE core logs MIGRANT NATION TRACE | char_trung;comp_mai;npc_thu;npc_ong_tu_nieu;npc_june;npc_mother_elian;npc_doctor | none | none | Scene 2. |
| SCN_CH031_TRUCK_STOP | Truck Stop Without Coffee | LOC_CH031_TRUCK_STOP | First salvage and community test | Convoy arrives at truck stop | Fake checkpoint exposed; supplies salvaged | char_trung;comp_mai;npc_pike | ENM_CH031_ROAD_BANDITS | none | Scene 3. |
| SCN_CH031_DRONE_OVER_CORN | Drone Over Cornfields | LOC_CH031_CORN_FIELDS | Introduce drone hunter tracking Binh/Hoang | Drone spotted over fields | Hoang's false pings identified; decoys built | npc_thu;char_trung;comp_binh | ENM_CH031_VALE_DRONE_HUNTER | ITM_CH031_SIGNAL_DECOY_EMITTERS | Scene 4. |
| SCN_CH031_CHILDREN_NEED_NAMES | Children Who Need Names | LOC_CH031_NIGHT_CAMP_OVERPASS | Deep emotional chapter center | Night camp under overpass | Name circle held; TRACE HUMANIZED BY ROLL CALL | comp_mai;comp_binh;char_trung;npc_noah;npc_mother_elian;npc_june | none | ITM_CH031_CHILD_NAME_TOKENS | Scene 5. |
| SCN_CH031_SIGNAL_ABSENT | Signal of the Absent | LOC_CH031_RADIO_TRUCK | Hoang intercut and chase escalation | Coded ping received | Ambush confirmed; convoy reroutes | char_trung;npc_pike;npc_mara | none | none | Scene 6. |
| SCN_CH031_GRAIN_ELEVATOR_AMBUSH | Grain Elevator Ambush | LOC_CH031_GRAIN_ELEVATOR_TOWN | Main action setpiece | Cult scouts and bandits converge | Hoang saves Binh then flees | char_trung;comp_binh;comp_hoang | ENM_CH031_CULT_PURSUIT_SCOUTS;ENM_CH031_ROAD_BANDITS;ENM_CH031_VALE_DRONE_HUNTER;ENM_CH031_HIGHWAY_HORDE | none | Scene 7. |
| SCN_CH031_WONT_SHOOT_YOU | I Won't Shoot You | LOC_CH031_RAIL_LINE | Redemption seed | Trung sees Hoang across rail line | Trung chooses convoy; Hoang pulls pursuit away | char_trung;comp_hoang | none | none | Scene 8. |
| SCN_CH031_HOME_MOVES | Home Moves | LOC_CH031_MOVING_CONVVOY_DAWN | Resolution and NORAD hook | Convoy survives; resources depleted | NORAD coordinates recovered; Binh writes "HOME MOVES" | char_trung;comp_mai;comp_binh | none | ITM_CH031_EMERGENCY_BROADCAST_NODE | Scene 9. |

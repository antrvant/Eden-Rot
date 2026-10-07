# Flags - CH018

Metadata:

- chapterID: CH018
- sourceFilename: chapter_018_ban_than_ban_dung.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH018_BINH_HOANG_CLUE | emotional | false | Binh tells Mai he heard Hoang walk past the classroom late at night. | Investigation path; Mai reports to Trung. | Scene 1. |
| FLAG_CH018_MUD_EVIDENCE_FOUND | progression | false | Player inspects mud and cloth fiber in storage. | Investigation logic; prevents false refugee accusation. | SQ_Betrayal_01. |
| FLAG_CH018_CLOTH_MARKER_IDENTIFIED | progression | false | Player identifies cloth as bandit route marker. | Confirms external involvement. | SQ_Betrayal_01. |
| FLAG_CH018_FENCE_GAP_CONFIRMED | progression | false | Worker Lead confirms fence gap is security-only knowledge. | Narrows suspect to security team. | Scene 4. |
| FLAG_CH018_HOANG_ABSENCE_NOTICED | progression | false | Player connects Binh's clue with Hoang's shift swap inconsistency. | Opens tracking path. | Scene 1. |
| FLAG_CH018_HOANG_LEAVES_BASE | world_state | false | Hoang exits through fence gap before dawn. | Triggers checkpoint trade scene. | Scene 2. |
| FLAG_CH018_CHECKPOINT_TRADE_COMPLETE | world_state | false | Hoang trades information for fuel and medicine. | Sets betrayal flag; unlocks fuel evidence. | Scene 3. |
| FLAG_CH018_HOANG_BETRAYAL_STARTED | world_state | false | Hoang completes checkpoint trade with bandits. | Long-term story flag; changes Hoang's status. | Rewards section. |
| FLAG_CH018_HOANG_SOLD_COORDINATES | world_state | false | Trung discovers checkpoint-sealed fuel cans. | Confrontation trigger. | Scene 4. |
| FLAG_CH018_HOANG_DID_NOT_NAME_BINH | world_state | false | Hoang did not directly say Binh's name to trader. | Moral complexity; does not erase harm. | Character Notes. |
| FLAG_CH018_BANDIT_TRADE_NETWORK_REVEALED | intel | false | Player observes or learns about bandit trade system. | Unlocks bandit faction understanding. | Scene 3; Lore Reveal. |
| FLAG_CH018_EDEN_BROKER_HINT | intel | false | Player sees clean-clothed broker receive NODE? envelope. | Long-term EDEN network connection. | Scene 3. |
| FLAG_CH018_EDEN_BROKER_CONNECTED_TO_EDEN_NODE_RUMOR | intel | false | Bandit trader mentions child/Edenrot information as high-value trade item. | Connects bandit economy to EDENROT rumor economy. | Scene 3. |
| FLAG_CH018_BANDITS_KNOW_EDENROT_CHILD_RUMOR | world_state | false | Bandit trader asks about child who walked through Edenrot. | Increases future danger for Binh. | Scene 3. |
| FLAG_CH018_FUEL_EVIDENCE_PRESENTED | progression | false | Trung shows checkpoint-sealed fuel cans to Hoang. | Breaks Hoang's "found it" lie. | Scene 4. |
| FLAG_CH018_CONFRONTATION_BEGUN | world_state | false | Trung and Hoang face each other in teachers' room. | Triggers emotional confrontation scene. | Scene 5. |
| FLAG_CH018_HOANG_CORE_LINE_SAID | emotional | false | Hoang says "I sold coordinates, not a soul." | Core betrayal line; defines Hoang's self-justification. | DT_079. |
| FLAG_CH018_BINH_AT_DOOR | emotional | false | Binh appears at classroom door during confrontation. | Stops Trung from physical violence. | Scene 5. |
| FLAG_CH018_HOANG_DEMOTED | world_state | false | Council reduces Hoang's security authority temporarily. | Changes Hoang's available actions. | Scene 5. |
| FLAG_CH018_BANDIT_RAID_CLASSROOM | world_state | false | Bandits attack using sold guard gap information. | Consequence of Hoang's trade. | Scene 6. |
| FLAG_CH018_MAI_EVACUATES_CHILDREN | world_state | false | Mai leads children through secondary exit during raid. | Child safety; Mai's heroic action. | Scene 6. |
| FLAG_CH018_BINH_HIDDEN_SAFE | world_state | false | Binh and So 4 hide in tool cabinet per Mai's instructions. | Child survival; safe-room rules work. | Scene 6. |
| FLAG_CH018_MAI_CAPTURED | world_state | false | Bandit lieutenant captures Mai during raid. | Chapter consequence; Chapter 19 setup. | Scene 6. |
| FLAG_CH018_MAI_CHALK_TRAIL | progression | false | Mai leaves three lines and M on desk edge before capture. | Rescue direction clue; Mai's agency. | Scene 6. |
| FLAG_CH018_HOANG_FOUGHT_IN_RAID | world_state | false | Hoang fights bandits during raid, proving unintended consequence. | Moral complexity flag. | Scene 6. |
| FLAG_CH018_BANDIT_FORT_UNLOCKED | progression | false | Map fragment recovered from dead bandit showing northwest fort. | Unlocks Chapter 19 rescue location. | Scene 7. |
| FLAG_CH018_BINH_TRUST_SHAKEN | emotional | false | Binh asks "Did Uncle Hoang sell Mom?" and nobody answers. | Long-term trust wound for Binh. | DT_080. |
| FLAG_CH018_HOANG_IMMEDIATE_STATUS | world_state | unresolved | Trung delays judgment; Hoang's fate undecided. | Chapter 19 companion availability. | Scene 7. |
| FLAG_CH018_RESCUE_MISSION_PREPARED | progression | false | Trung decides to rescue Mai before dealing with Hoang. | Chapter 19 setup. | Scene 7. |

## Flag Notes

- `FLAG_CH018_HOANG_IMMEDIATE_STATUS` defaults to "unresolved" rather than boolean. Setup tools should treat this as a string state: unresolved, detained, allowed_rescue, exiled.
- `FLAG_CH018_BINH_TRUST_SHAKEN` is a long-term emotional flag that should persist for many chapters and affect Binh's dialogue about trust and forgiveness.
- `FLAG_CH018_MAI_CHALK_TRAIL` should persist into Chapter 19 as a directional clue for the rescue mission.
- `FLAG_CH018_EDEN_BROKER_HINT` and `FLAG_CH018_EDEN_BROKER_CONNECTED_TO_EDEN_NODE_RUMOR` are long-term intel flags connecting the bandit faction to the larger EDEN/Architect network.
- `FLAG_CH018_HOANG_CORE_LINE_SAID` captures the emotional peak of the chapter. "I sold coordinates, not a soul. A soul is worth less than gas."

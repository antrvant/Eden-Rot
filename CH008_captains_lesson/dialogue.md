# Dialogue - CH008

Metadata:

- chapterID: CH008
- sourceFilename: chapter_008_bai_hoc_cua_dai_uy.md
- language: English

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |
|---|---|---|---|---|---|---|---|
| DLG_CH008_RADIO_001 | npc_radio_operator | STATE_MORNING_RADIO | The Screamer flooded the band. I need filters, copper wire, maybe an amplifier from the old pump station. | none | set_flag:FLAG_CH008_RADIO_PARTS_REQUESTED | morning_after | Scene 1. |
| DLG_CH008_MENTOR_BLOCK_001 | npc_mentor | STATE_TRAINING_BLOCK | You go outside after you pass the basics. | none | set_flag:FLAG_CH008_TRAINING_STARTED | morning_after | Scene 1. |
| DLG_CH008_MENTOR_GUN_001 | npc_mentor | STATE_GUN_LESSON | Do you want to shoot because you are angry, or because you need to live? | Choice A: "Both."; Choice B: "Because I need to get home."; Choice C: "I do not want to shoot anyone." | open_choice | firearm_drill | DT_026. |
| DLG_CH008_MENTOR_GUN_002A | npc_mentor | STATE_GUN_A | Then your first shot will miss. | none | set_flag:FLAG_CH008_ANGER_PLUS | choice:DLG_CH008_MENTOR_GUN_001:A | DT_026 Choice A. |
| DLG_CH008_MENTOR_GUN_002B | npc_mentor | STATE_GUN_B | Good. Every shot needs a road home in it. | none | set_flag:FLAG_CH008_FOCUS_PLUS | choice:DLG_CH008_MENTOR_GUN_001:B | DT_026 Choice B. |
| DLG_CH008_MENTOR_GUN_002C | npc_mentor | STATE_GUN_C | No one is asking what you want. I am asking whether you are willing to live. | none | set_flag:FLAG_CH008_RELUCTANCE_PLUS | choice:DLG_CH008_MENTOR_GUN_001:C | DT_026 Choice C. |
| DLG_CH008_MENTOR_BARK_001 | npc_mentor | STATE_TRAINING_BARK | Look. Breathe out. Decide. Fire. | none | set_flag:FLAG_CH008_FIREARM_TIER_1_UNLOCKED | firearm_drill_complete | Implementation Notes. |
| DLG_CH008_MENTOR_BARK_002 | npc_mentor | STATE_TRAINING_BARK | Every shot needs a road home in your head. | none | none | firearm_drill | Implementation Notes. |
| DLG_CH008_HOANG_STEALTH_001 | comp_hoang | STATE_STEALTH_LESSON | I like this lesson. | none | none | stealth_run | DT_027. |
| DLG_CH008_TRUNG_STEALTH_001 | char_trung | STATE_STEALTH_LESSON | Because nobody has to be a hero? | none | none | stealth_run | DT_027. |
| DLG_CH008_HOANG_STEALTH_002 | comp_hoang | STATE_STEALTH_LESSON | Because people who are not seen survive more often than people the whole neighborhood can name. | none | set_flag:FLAG_CH008_HOANG_PRAGMATISM_PLUS | stealth_run | DT_027. |
| DLG_CH008_MENTOR_STEALTH_001 | npc_mentor | STATE_STEALTH_LESSON | Silence is not cowardice. Silence lets you choose when to make noise. | none | set_flag:FLAG_CH008_STEALTH_TIER_1_UNLOCKED | stealth_run | DT_027. |
| DLG_CH008_MENTOR_PRIORITY_001 | npc_mentor | STATE_TARGET_PRIORITY | The most dangerous target is not always the closest one. | none | set_flag:FLAG_CH008_PRIORITY_TARGETING_UNLOCKED | bus_yard_encounter | Implementation Notes. |
| DLG_CH008_PHUC_001 | npc_phuc | STATE_PHUC_TRAINING | My hands keep locking up when I load. | none | set_flag:FLAG_CH008_PHUC_TRAINING_STARTED | phuc_sidequest | SQ_Training_03. |
| DLG_CH008_TRUNG_PHUC_001 | char_trung | STATE_PHUC_TRAINING | Mine did too. Breathe before the magazine, not after. | none | set_flag:FLAG_CH008_PHUC_CONFIDENCE_SEED | phuc_sidequest | SQ_Training_03 emotional note. |
| DLG_CH008_MENTOR_CHILD_001 | char_trung | STATE_MENTOR_TOKEN | You had a child? | none | none | mentor_token_seen | DT_028. |
| DLG_CH008_MENTOR_CHILD_002 | npc_mentor | STATE_MENTOR_TOKEN | Once. | none | set_flag:FLAG_CH008_MENTOR_CHILD_TOKEN_SEEN | mentor_token_seen | DT_028. |
| DLG_CH008_TRUNG_CHILD_001 | char_trung | STATE_MENTOR_TOKEN | I am sorry. | none | none | mentor_token_seen | DT_028. |
| DLG_CH008_MENTOR_CHILD_003 | npc_mentor | STATE_MENTOR_TOKEN | Do not apologize to the dead. Learn so the living do not join them. | none | set_flag:FLAG_CH008_MENTOR_BACKSTORY_SEED | mentor_token_seen | DT_028. |
| DLG_CH008_ARMORY_001 | npc_smith | STATE_ARMORY_ARGUMENT | If there is ammo in there, it could hold the outpost for a week. | none | none | locked_armory | Scene 6. |
| DLG_CH008_HOANG_ARMORY_001 | comp_hoang | STATE_ARMORY_ARGUMENT | Ammo is life. | none | set_flag:FLAG_CH008_HOANG_PRAGMATISM_PLUS | locked_armory | Scene 6. |
| DLG_CH008_MENTOR_ARMORY_001 | npc_mentor | STATE_ARMORY_ARGUMENT | Opening it wrong costs people. | none | none | locked_armory | Implementation Notes. |
| DLG_CH008_MENTOR_RETREAT_001 | npc_mentor | STATE_RETREAT | Retreat. | none | set_flag:FLAG_CH008_RETREAT_ORDER_GIVEN | tank_seen | Scene 6-7. |
| DLG_CH008_TRUNG_RETREAT_001 | char_trung | STATE_RETREAT | We came all this way. | none | none | tank_seen | DT_029. |
| DLG_CH008_MENTOR_RETREAT_002 | npc_mentor | STATE_RETREAT | And we can still go back if you obey. | none | none | tank_seen | DT_029. |
| DLG_CH008_HOANG_RETREAT_001 | comp_hoang | STATE_RETREAT | There is ammo in there. | none | none | tank_seen | DT_029. |
| DLG_CH008_MENTOR_RETREAT_003 | npc_mentor | STATE_RETREAT | There is something in there that will make us pay more blood than the ammo is worth. | Choice A: Obey and retreat.; Choice B: Try to grab more ammo.; Choice C: Let Hoang decide. | open_choice | tank_seen | DT_029. |
| DLG_CH008_MENTOR_RETREAT_004A | npc_mentor | STATE_RETREAT_A | Good. Move. | none | set_flag:FLAG_CH008_RETREAT_LESSON_LEARNED;set_flag:FLAG_CH008_MENTOR_RESPECT_PLUS | choice:DLG_CH008_MENTOR_RETREAT_003:A | DT_029 Choice A. |
| DLG_CH008_MENTOR_RETREAT_004B | npc_mentor | STATE_RETREAT_B | That hesitation costs blood. Go! | none | set_flag:FLAG_CH008_ARMORY_INJURY_RISK;set_flag:FLAG_CH008_AMMO_REWARD_HIGH_RISK | choice:DLG_CH008_MENTOR_RETREAT_003:B | DT_029 Choice B. |
| DLG_CH008_HOANG_RETREAT_002C | comp_hoang | STATE_RETREAT_C | We take what we can carry and run. Fast. | none | set_flag:FLAG_CH008_HOANG_DECIDES_AMMO;set_flag:FLAG_CH008_HOANG_PRAGMATISM_PLUS | choice:DLG_CH008_MENTOR_RETREAT_003:C | DT_029 Choice C. |
| DLG_CH008_MENTOR_END_001 | npc_mentor | STATE_MQ009_UNLOCK | Radio tower tomorrow. You go with the team. Not alone. No breaking orders. No chasing every voice. | none | set_flag:FLAG_CH008_MQ009_RESTORE_RADIO_UNLOCKED | chapter_end | Scene 7. |

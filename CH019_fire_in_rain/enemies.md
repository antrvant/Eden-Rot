# Enemies - CH019

Metadata:

- chapterID: CH019
- sourceFilename: chapter_019_lua_trong_mua.md
- language: English

| enemyID | enemyName | enemyType | variant | roleInChapter | abilities | sourceEvidence |
|---|---|---|---|---|---|---|
| ENM_CH019_BANDIT_LIEUTENANT | Bandit Lieutenant | human_hazard | fort_commander | Primary antagonist; holds Mai captive; uses her as shield; connected to broker network. | Guards hostages; coordinates fort defense; trades info to EDEN broker; uses Mai as human shield. | Metadata, Scene 3, Scene 6. |
| ENM_CH019_BANDIT_GARRISON | Bandit Garrison | human_hazard | fort_guards | Fort defense force; patrol routes; trap management. | Patrol fort perimeter; maintain bell traps and checkpoints; guard server room; respond to alarms. | Scene 4, Scene 5. |
| ENM_CH019_RAIN_HORDE | Rain Horde | infected_hazard | storm_variant | Environmental pressure; drawn by fire/explosion at fort; forces retreat. | Approaches through rain; attracted by noise and fire; overwhelms fort perimeter; creates escape deadline. | Metadata, Scene 6, Scene 7. |
| ENM_CH019_FIRE_HAZARD | Factory Fire | environmental_hazard | industrial_fire | Kiln and fuel ignite under rain; creates title visual; forces evacuation. | Burns on flooded yard; creates steam and smoke; threatens prisoners; blocks escape routes. | Metadata, Scene 6, SQ_FireRain_04. |
| ENM_CH019_BROKER_NETWORK | EDEN/Architect Broker Network | systemic_hazard | info_warfare | Hidden threat revealed through server files; bandits are one node in larger conspiracy. | Tracks immune children; trades maritime routes; pays bounties for Eden Node confirmation; connects bandits to Architects. | Scene 5, DT_084, Lore Reveal. |
| ENM_CH019_MORAL_RAGE | Trung's Rage | emotional_hazard | personal_crisis | Internal threat; Trung's desire to kill Hoang vs. his duty to Binh. | Tempts Trung to execute or abandon Hoang; costs emotional energy to resist; defines Trung's character. | Metadata, Scene 7, DT_085. |

## Enemy Handling Notes

- The bandit lieutenant is the visible antagonist but not cartoonish. He sees hostages as insurance and has real broker connections. He survives the fort burning and can return in later bandit faction arcs.
- `ENM_CH019_BANDIT_GARRISON` provides stealth/combat encounters during infiltration. Rain affects their patrol effectiveness.
- `ENM_CH019_RAIN_HORDE` is a timer mechanic: the explosion draws infected to the fort, creating a deadline for escape.
- `ENM_CH019_FIRE_HAZARD` creates the chapter's title image: fire burning under rain on a flooded yard. It also creates a moral choice: save other prisoners or prioritize Mai.
- `ENM_CH019_BROKER_NETWORK` is the true reveal. Bandits are a local symptom; the server files show EDEN and Architect brokers operating at a maritime logistics level. This enemy does not fight directly but its existence changes the scale of the story.
- `ENM_CH019_MORAL_RAGE` is Trung's personal antagonist. His climax is restraint, not violence. The enemy is the part of him that wants to make Hoang pay with a bullet.

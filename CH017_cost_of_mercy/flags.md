# Flags - CH017

Metadata:

- chapterID: CH017
- sourceFilename: chapter_017_cai_gia_cua_long_thuong.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH017_CONVOY_DISTRESS_RECEIVED | progression | false | Distress signal received from refugee convoy. | Quest trigger; council convenes. | Scene 1. |
| FLAG_CH017_LIMITED_RESCUE_APPROVED | progression | false | Council votes for limited rescue team. | Rescue mission begins. | Scene 2. |
| FLAG_CH017_HOANG_DISSENT_RESCUE | relationship | false | Hoang votes against rescue; records resentment. | Hoang trust meter; Chapter 18 seed. | Scene 2. |
| FLAG_CH017_BANDIT_MARKER_FOUND | lore | false | Red cloth bandit marker found at bridge. | Bandit intel; Chapter 18 ambush setup. | Scene 3. |
| FLAG_CH017_MEDICINE_OVER_FUEL | choice | false | Medicine prioritized over fuel at depot. | Doctor lab progress; generator status. | Scene 4. |
| FLAG_CH017_FUEL_OVER_MEDICINE | choice | false | Fuel prioritized over medicine at depot. | Generator status; injured father may die. | Scene 4. |
| FLAG_CH017_REFUGEES_SAVED | world_state | 0 | Variable: number of refugees rescued to base. | Base population; resource pressure. | Scene 6. |
| FLAG_CH017_BA_SAU_SURVIVED | world_state | false | Ba Sau survives the bridge collapse. | Potential refugee representative. | Scene 6. |
| FLAG_CH017_NAMELESS_CHILD_SAVED | progression | false | So 4 rescued and enters Mai's class. | Child morale; Binh mirror unlock. | Scene 5. |
| FLAG_CH017_SUPPLY_SHORTAGE_SEVERE | world_state | false | Base supply drops critically after rescue. | Resource crisis; ration policy. | Scene 7. |
| FLAG_CH017_LAB_RESEARCH_DELAYED | world_state | false | Doctor uses lab alcohol/bandages on wounded; research slows two days. | Cure progress penalty. | Scene 7. |
| FLAG_CH017_WORKER_RESENTMENT_UP | world_state | false | Worker faction resentful over reduced rations and harder labor. | Morale system; faction tension. | Scene 7. |
| FLAG_CH017_HOANG_SUPPLY_RESENTMENT | relationship | false | Hoang privately records supply losses; core line delivered. | Chapter 18 betrayal seed. | Scene 7. |
| FLAG_CH017_EDENROT_RUMOR_FOLLOWS_BASE | threat | false | Refugees bring Edenrot rumors; stories about "child who walks through Edenrot" spread. | Future refugee arrivals; Binh exposure risk. | Metadata and Lore Reveal. |
| FLAG_CH017_EDENROT_EXPOSURE_PROTOCOL | system | false | Quarantine protocol for Edenrot-exposed refugees established. | Future infected-zone handling. | SQ_Mercy_04B. |
| FLAG_CH017_SUPPLY_THEFT_TRIGGERED | progression | false | Night theft of medicine/fuel from supply room occurs. | Chapter 18 investigation trigger. | Scene 8. |
| FLAG_CH017_BANDIT_CHECKPOINT_LEAD | lore | false | Hoang privately copies bandit checkpoint map location. | Chapter 18 betrayal mechanism. | Scene 8. |
| FLAG_CH017_BINH_TRIGGERED | emotional | false | Binh hears "nameless child" on radio; B-07 memory activated. | Binh emotional state. | Scene 1. |
| FLAG_CH017_BINH_SHARED_BOWL | emotional | false | Binh shares half his porridge with So 4. | Binh recovery milestone. | Scene 7. |
| FLAG_CH017_BRIDGE_BURNED | world_state | false | Final fuel can used as fire wall on bridge. | Route cut; supply lost. | Scene 6. |
| FLAG_CH017_CONVoy_ENTERED_BASE | progression | false | Refugees enter base quarantine/admission. | Refugee intake system unlocked. | Scene 7. |
| FLAG_CH017_SPOTTER_ESCAPED | world_state | false | Bandit spotter escapes from toll station. | Bandit network threat persists. | Scene 4. |
| FLAG_CH017_COMPASSION_CHOSEN | moral | false | Player chooses compassion-leaning rescue options. | Moral alignment; alliance trust. | Metadata. |
| FLAG_CH017_PRAGMATISM_CHOSEN | moral | false | Player chooses pragmatism-leaning options. | Moral alignment; security focus. | Metadata. |
| FLAG_CH017_INVESTIGATION_STARTED | progression | false | Trung orders theft investigation with evidence-first approach. | Quest progression for Chapter 18. | Scene 8. |

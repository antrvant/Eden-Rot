# Chapter Manifest - CH007

## Source Chapter

- sourceChapterID: CH007
- sourceFilename: chapter_007_dem_dau_ngoai_tuong_rao.md
- sourcePath: ../chapters/chapter_007_dem_dau_ngoai_tuong_rao.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: First Night Outside the Fence
- originalTitle: Dem Dau Ngoai Tuong Rao
- act: Act 2 - Family Trail & First Base
- gameplayHours: 4h
- primaryPOV: Trung
- mainQuestID: MQ_007
- mainQuestName: First Night Defense

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH007_OUTPOST_YARD | Army Outpost Yard | Night assignment and duty conflict |
| LOC_CH007_REFUGEE_TENT | Refugee Tent | Humanize refugees and introduce children under protection |
| LOC_CH007_WEST_GATE | West Gate | Main guard post and defense setpiece |
| LOC_CH007_TEMP_FENCE | Temporary Fence | Weak barrier and climber breach point |
| LOC_CH007_WATCH_TOWER | Watch Tower | First Screamer audio observation |
| LOC_CH007_AMMO_SHED | Ammo Shed | Defense resource priority and missing ammo hook |
| LOC_CH007_MATERIAL_DEPOT | Material Depot | Fence reinforcement supplies |
| LOC_CH007_OUTSIDE_KILL_ZONE | Ground Outside Fence | Screamer/horde approach area |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH006_ARMY_OUTPOST_UNLOCKED | Chapter 007 takes place inside the army outpost. |
| FLAG_CH006_MENTOR_TRAINING_ACCEPTED | Mentor has accepted Trung into a training arc. |
| FLAG_CH006_RADIO_FRAGMENT_MAI_HEARD | Radio guilt and Mai fragment carry into this night. |
| FLAG_CH006_PHUC_RESCUED | Phuc can appear as young soldier if rescued in Chapter 006. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH007_GUARD_DUTY_ASSIGNED | Mentor assigns Trung to West Gate night duty. |
| FLAG_CH007_REFUGEE_TENT_VISITED | Trung meets refugees and children as individuals. |
| FLAG_CH007_DEFENSE_PREP_COMPLETE | Player completes fence/resource preparation. |
| FLAG_CH007_FIRST_SCREAMER_HEARD | First Screamer cry is heard. |
| FLAG_CH007_FIRST_SCREAMER_SEEN | Screamer is visually confirmed under flare/light. |
| FLAG_CH007_SCREAMER_KNOWLEDGE_UNLOCKED | Screamer enemy knowledge unlocks. |
| FLAG_CH007_CROWD_PANIC_UNLOCKED | Crowd panic mechanic unlocks. |
| FLAG_CH007_REFUGEE_TENT_PROTECTED | Refugee tent survives the night. |
| FLAG_CH007_AMMO_SHED_PRIORITIZED | Ammo shed receives priority in defense allocation. |
| FLAG_CH007_NHI_NAME_REMEMBERED | Trung repeats and remembers Nhi's name for the separated mother. |
| FLAG_CH007_COMMANDER_SEED | Trung gives effective orders to refugees during defense. |
| FLAG_CH007_MAI_FRAGMENT_BLOCKED | New Mai fragment is blocked/overwritten by Screamer noise. |
| FLAG_CH007_TRAINING_DAY_UNLOCKED | Chapter 008 training day is unlocked. |

## Generated Files

Load in this exact order:

1. chapter_manifest.md
2. characters.md
3. quests.md
4. dialogue.md
5. items.md
6. scenes.md
7. enemies.md
8. factions.md
9. flags.md
10. validation.md

## Canon Summary

On the first night at the army outpost, Trung wants to keep chasing Mai and Binh, but Mentor assigns him to guard the West Gate. The night forces Trung to see strangers as people with names: children in tents, parents guarding families, Phuc at the ammo shed, a mother still searching for Nhi. During defense prep, Trung must choose where limited materials go: ammo shed, refugee tent, main gate, or divided coverage. A Screamer appears, using a distorted cry to draw a horde and panic the living. Trung stops the mother from opening the gate, confirms the sound is a weapon, helps kill or mark the Screamer, and survives the night. A new Mai radio fragment is blocked by Screamer noise, and Mentor schedules training for the next morning.

## Continuity Resolution - Nhi

| issue | decision |
|---|---|
| Chapter 007 names Nhi through the mother at the gate. | Treat this as the same recurring Nhi thread from Chapter 002 and Chapter 005. |
| characterID | Use `npc_lost_mother` and `npc_nhi` as cross-chapter references, not new CH007-only IDs. |
| tooling impact | CH007 may reference `npc_nhi` as absent/missing and set `FLAG_CH007_NHI_NAME_REMEMBERED`. |

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH007_001 | Does Nam, the child in the refugee tent, recur later? | Track as local NPC unless later canon confirms. |
| OQ_CH007_002 | Was the missing ammo an inventory error, theft, or sabotage seed? | Mark as open in side quest. |
| OQ_CH007_003 | When does infected climber become a full enemy variant? | Foreshadow only in CH007 unless later canon escalates. |
| OQ_CH007_004 | Is the Screamer mimicking voices supernaturally, biologically, or through fear response? | Leave ambiguous; only record gameplay effect. |

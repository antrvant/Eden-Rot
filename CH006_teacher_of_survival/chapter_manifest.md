# Chapter Manifest - CH006

## Source Chapter

- sourceChapterID: CH006
- sourceFilename: chapter_006_nguoi_day_cach_song_sot.md
- sourcePath: ../chapters/chapter_006_nguoi_day_cach_song_sot.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: The One Who Teaches Survival
- originalTitle: Nguoi Day Cach Song Sot
- act: Act 1 - Sai Gon Burns
- gameplayHours: 5h
- primaryPOV: Trung
- mainQuestID: MQ_006
- mainQuestName: Meet Mentor

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH006_OUTPOST_ROAD | Retreat Road to Real Army Outpost | Contrast with false safe zone |
| LOC_CH006_REAL_OUTPOST_GATE | Real Army Outpost Gate | Bite check and faction verification |
| LOC_CH006_DECONTAMINATION_LINE | Decontamination Line | Wound inspection and hidden bite event |
| LOC_CH006_TRIAGE_TENT | Triage Tent | Medicine scarcity and doctor moral choice |
| LOC_CH006_RADIO_TENT | Radio Tent | Mai signal fragment and radio clue system |
| LOC_CH006_TRAINING_YARD | Temporary Training Yard | Mentor confrontation and skill gate |
| LOC_CH006_WEST_FENCE | West Fence | Timed rescue test and infected scout group |
| LOC_CH006_SUPPLY_DEPOT | Supply Depot | Optional medicine/radio parts side hooks |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH005_REAL_ARMY_OUTPOST_UNLOCKED | Chapter 006 begins at the real army outpost. |
| FLAG_CH005_RIPPED_TRANSFER_LIST_OBTAINED | Transfer list evidence can be shown to the outpost. |
| FLAG_CH005_FALSE_SAFE_ZONE_EXPOSED | Explains why the army is investigating false checkpoints. |
| FLAG_CH005_FAKE_STAMP_OBTAINED | Optional evidence that changes dialogue/trust if collected. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH006_ARMY_OUTPOST_UNLOCKED | The real army outpost becomes an active hub. |
| FLAG_CH006_BITE_CHECK_PASSED | Trung and Hoang pass the gate inspection. |
| FLAG_CH006_FAKE_STAMP_DELIVERED | Player delivers fake stamp/evidence if collected. |
| FLAG_CH006_HIDDEN_BITE_FOUND | A refugee hiding a bite is discovered. |
| FLAG_CH006_TRIAGE_CHOICE_MADE | Player engages with doctor triage scarcity. |
| FLAG_CH006_RADIO_FRAGMENT_MAI_HEARD | Player hears a noisy fragment that sounds like Mai. |
| FLAG_CH006_RADIO_CLUE_TIER_1_UNLOCKED | Radio clue system tier 1 unlocks. |
| FLAG_CH006_MENTOR_MET | Trung meets Mentor. |
| FLAG_CH006_PHUC_RESCUED | Trung rescues young soldier Phuc at the fence. |
| FLAG_CH006_MENTOR_RESPECT_PLUS | Mentor respects Trung's rescue/discipline. |
| FLAG_CH006_DISCIPLINE_SEED | Trung accepts that training is part of finding his family. |
| FLAG_CH006_MENTOR_TRAINING_ACCEPTED | Mentor accepts training Trung. |

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

After escaping the false safe zone, Trung and Hoang reach a real army outpost that does not promise safety. It demands bite checks, discipline, and hard triage decisions. The outpost investigates false checkpoints and accepts evidence if Trung carries it. A hidden bite case shows why compassion without procedure can endanger everyone. The doctor has too few antibiotics and forces Trung to face triage logic. The radio operator catches a noisy fragment that sounds like Mai telling Binh to lie down, pulling Trung toward panic. Mentor stops him and makes a brutal point: love is a reason to live, not a survival skill. During an infected scout attack, Trung chooses to rescue young soldier Phuc instead of chasing the radio signal. Mentor then agrees to train him.

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH006_001 | What is Mentor's real name and full rank if later canon specifies it? | Use `npc_mentor` and displayName `Mentor`. |
| OQ_CH006_002 | Does young soldier Phuc recur after this chapter? | Track `FLAG_CH006_PHUC_RESCUED`; later chapters can bind recurrence. |
| OQ_CH006_003 | What is the exact source and meaning of the noisy Mai radio fragment? | Treat as uncertain signal and defer to Chapter 09. |
| OQ_CH006_004 | What is the exact outcome of the missing volunteer side quest? | Keep multiple outcomes until later canon confirms. |
| OQ_CH006_005 | What does the `E` mark from Chapter 005 mean? | Still unresolved; do not explain in CH006. |

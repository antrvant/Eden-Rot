# Chapter Manifest - CH037

## Source Chapter

- sourceChapterID: CH037
- sourceFilename: chapter_037_duong_ham_cua_ke_khong_chet.md
- sourcePath: ../chapters/chapter_037_duong_ham_cua_ke_khong_chet.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: Tunnel of the Undead
- originalTitle: Duong Ham Cua Ke Khong Chet
- act: Act 6 - Europe & Africa: Cure and Conscience
- gameplayHours: 5h
- primaryPOV: Binh
- mainQuestID: MQ_037
- mainQuestName: Reach Alpine Lab

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH037_PARIS_DEPARTURE | Paris Metro Departure | Transition from Amelie to Alps; prep supplies |
| LOC_CH037_RAIL_TUNNEL | Rail Tunnel to Geneva Corridor | Establish Binh signal sensing |
| LOC_CH037_MAINTENANCE_ALCOVE | Maintenance Alcove | Three-source route rule establishment |
| LOC_CH037_GENEVA_CHECKPOINT | Abandoned Geneva Quarantine Checkpoint | Lore: containment failure; Margot recordings |
| LOC_CH037_MORGUE_TUNNEL | Checkpoint Morgue Tunnel | Dormant infected enemy intro |
| LOC_CH037_ALPINE_TUNNEL | Alpine Service Tunnel / Ventilation | Oxygen management; route choice |
| LOC_CH037_AVALANCHE_GALLERY | Avalanche Gallery | Action setpiece; drones and charges |
| LOC_CH037_ALPINE_LAB_GATE | Alpine Lab 7 Outer Gate | Arrival; gate puzzle; biomarker reaction |
| LOC_CH037_LAB_VESTIBULE | Lab Vestibule | Cliffhanger; cost acceptance hook |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH036_PATIENT_ZERO_ARCHIVE_SECURED | Group carries Patient Zero archive from Paris. |
| FLAG_CH036_SWISS_ALPINE_ROUTE_UNLOCKED | Swiss Alpine Lab route confirmed. |
| FLAG_CH036_MIMIC_VOICE_RULE_LEARNED | Group knows Mimic voice rule from Paris. |
| FLAG_CH036_BINH_ALPS_SIGNAL | Binh already senses non-radio call from Alps. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH037_THREE_SOURCE_ROUTE_RULE | Ethical navigation rule: no route from one source alone. |
| FLAG_CH037_BINH_SIGNAL_CONSENT_RESPECTED | Binh signal used with consent, not as automatic GPS. |
| FLAG_CH037_GENEVA_QUARANTINE_LOGS | Nurse Margot recordings and containment failure logs recovered. |
| FLAG_CH037_DORMANT_PULSE_COUNTERMEASURE | Dormant infected pulse behavior understood. |
| FLAG_CH037_TUNNEL_AIRFLOW_MANUAL | Manual airflow path chosen over AI recommendation. |
| FLAG_CH037_INVASIVE_PROMPT_REFUSED | Invasive biomarker scan refused at lab gate. |
| FLAG_CH037_ALPINE_GATE_OPENED_ETHICALLY | Lab gate opened with archive key and human voice, no blood. |
| FLAG_CH037_DORMANT_SIGNAL_ARTERY_OPENED | Cliffhanger: lab vestibule opened for Chapter 38. |

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

Rebirth travels from Paris metro through Geneva corridor and Alpine tunnels to reach Alpine Lab 7. Binh begins sensing Patient Zero signal as non-audio pressure. The group establishes a three-source route rule to avoid exploiting Binh. They discover Geneva quarantine failure through nurse Margot recordings, encounter dormant infected that wake on lab pulse, survive low-oxygen tunnels and avalanche gallery, and reach the lab gate where invasive biomarker scan is refused. The chapter ends with the lab vestibule opening and automated voice stating "Human salvation request pending cost acceptance."

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH037_001 | What is the exact nature of Binh's signal sensitivity? Is it viral, psychic, or Architect-related? | Source describes it as non-audio, not radio, not AI voice; mark TODO_DERIVE_OR_APPROVE. |
| OQ_CH037_002 | Is the tunnel maintenance AI remnant a threat or just incompetent? | Source shows it gives contradictory safety instructions; its intent is ambiguous. |
| OQ_CH037_003 | Who is Swiss checkpoint survivor Adrien? | Metadata lists Adrien but source does not detail him; mark TODO_DERIVE_OR_APPROVE. |

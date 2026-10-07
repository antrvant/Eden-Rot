# Chapter Manifest - CH015

## Source Chapter

- sourceChapterID: CH015
- sourceFilename: chapter_015_hoi_dong_cua_nhung_ke_song_sot.md
- sourcePath: ../chapters/chapter_015_hoi_dong_cua_nhung_ke_song_sot.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: Council of Survivors
- originalTitle: Hoi Dong Cua Nhung Ke Song Sot
- act: Act 3 - First Base & Broken Trust
- gameplayHours: 4h
- primaryPOV: Trung, Mai, Hoang, Binh, npc_worker_lead
- mainQuestID: MQ_015
- mainQuestName: Form Council

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH015_BASE_HOME | Base "Home" in School | Main base of operations; all scenes occur within or near this location. |
| LOC_CH015_TEACHER_ROOM | Teacher's Room | Council meeting location; governance rules written on blackboard. |
| LOC_CH015_CLASS_3B | Classroom 3B | Children's safe room; fever scene and Binh's emotional arc. |
| LOC_CH015_CONSTRUCTION_SITE | Construction Site / Gate Area | Stranger arrival screening; Hoang's perimeter. |
| LOC_CH015_TEMP_QUARANTINE | Temporary Quarantine Zone | Fake mother and fever child isolation. |
| LOC_CH015_WELL | Well | Water source; referenced in hygiene and sickness context. |
| LOC_CH015_COMMUNITY_CENTER | Community Center (Nha Van Hoa Xa) | EDEN cache intel location 2km away. |
| LOC_CH015_OLD_MEDICAL_STATION | Old Medical Station | Medicine testing and doctor's workspace. |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH014_BASE_NAMED_HOME | Chapter 14 established the base as "Home"; Chapter 15 tests whether that name can survive governance. |
| FLAG_CH014_BINH_SAFETY_DECISION | Binh's status as hunted child carries into Chapter 15's medicine and council debates. |
| FLAG_CH014_EDEN_PACKAGE_RECEIVED | The EDEN package with medicine, labels, and `EDEN NODE B-07` reference arrives in Chapter 14. |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH015_COUNCIL_FORMED | Provisional council with five voting seats is established. |
| FLAG_CH015_COUNCIL_SEATS_DEFINED | Seats: Security (Hoang), Medical (Doctor), Labor (Worker Lead), Children/Family (Mai), Coordination (Trung). |
| FLAG_CH015_EMERGENCY_AUTHORITY_LIMITED | Trung and Hoang get 30-minute emergency authority, then must report. |
| FLAG_CH015_MEDICINE_FROM_EDEN_USED | Fever child receives tested EDEN medicine; small dose succeeds. |
| FLAG_CH015_FEVER_CHILD_SURVIVED | Fever child survives after medicine use. |
| FLAG_CH015_FAKE_MOTHER_SCOUT_CAPTURED | Scout posing as mother is exposed and detained. |
| FLAG_CH015_FAKE_MOTHER_TREATED_HUMANELY | Scout is questioned without torture; recommended canon. |
| FLAG_CH015_EDEN_CACHE_INTEL | Scout reveals EDEN cache location near community center. |
| FLAG_CH015_HOANG_STRIKE_FIRST_VOTE | Hoang votes to strike EDEN cache; dissent recorded. |
| FLAG_CH015_RECON_BEFORE_STRIKE | Council votes for recon first; recommended canon. |
| FLAG_CH015_BINH_GUILT_THREAD | Binh begins guilt arc about being the reason for danger. |
| FLAG_CH015_EDENROT_PARANOIA_THREAD | Social distrust spreads via `B-07` / `Eden Node` labels. |
| FLAG_CH015_ENEMY_CLASSIFICATION_REJECTED | Council rules ban calling children by enemy codes. |
| FLAG_CH015_WORKER_LEAD_LEGITIMACY | Worker Lead gains council seat and voice for laborers. |
| FLAG_CH015_MAI_CHILD_ADVOCATE_SEAT | Mai becomes Children/Family representative. |
| FLAG_CH015_FIRST_VOTE_COMPLETED | First council vote (medicine use) passes. |
| FLAG_CH015_STRATEGIC_VOTE_COMPLETED | Second council vote (attack vs recon) records Hoang's dissent. |
| FLAG_CH015_BINH_NAME_CHANGE_QUESTION | Binh asks if changing his name would help; emotional continuity seed. |
| FLAG_CH015_FAKE_MOTHER_NAME_LEARNED | Scout's real name is Hanh; reveals EDEN coercion. |
| FLAG_CH015_CHILD_PHUC_IDENTIFIED | Child used as cover by scout is named Phuc, not Nam. |
| FLAG_CH015_ONG_TU_NHIEU_FOOD_ADVISOR | Ong Tu Nhieu accepts non-voting food advisor role. |
| FLAG_CH015_MQ_COMPLETE | MQ_015 completes after council is formed and first vote held. |

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

The first night in base "Home" brings a fever crisis in Classroom 3B. Medicine from the EDEN package could save the child, but using it means accepting leverage and reminding everyone that Binh has been classified as `Eden Node`. A stranger arrives at the gate claiming to be a mother; Mai discovers inconsistencies and the child reveals the woman told him to call her "mom." Worker Lead challenges Trung's authority, forcing Trung to accept limits on his power and form a provisional council. The council votes to use EDEN medicine cautiously; the fever child survives. The fake mother scout confesses EDEN sent her to confirm `B-07` location in exchange for medicine for her sick brother. The council holds its first strategic vote: Trung and the majority choose recon before strike, but Hoang votes to attack the suspected EDEN cache, recording the first formal dissent. The chapter ends with the council established but a rift forming between humanitarian defense and pragmatic survival.

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH015_001 | What happens to the fake mother scout long-term? | Can return as prisoner, messenger, or tragic casualty depending on player choice. |
| OQ_CH015_002 | Does the fever child's survival affect later medical trust? | Track flag; Chapter 16 Doctor may request Binh blood testing. |
| OQ_CH015_003 | When does Hoang's dissent escalate to action? | Track `HoangStrikeFirstVote`; Chapters 17-18 should reference this as start of council distrust. |
| OQ_CH015_004 | Does Binh's name-change question echo later? | Source says this should echo when immune children are assigned codes by Architects. |
| OQ_CH015_005 | What is the long-term role of Worker Lead in council? | Source says he should become a steady council voice, not a one-off challenger. |
| OQ_CH015_006 | What happens to the child Phuc used as cover? | Source says Phuc should remain in base as reminder that EDEN uses real victims as covers. |
| OQ_CH015_007 | Does the EDEN cache near community center become a future mission? | Intel is unlocked; future chapters may use it. |

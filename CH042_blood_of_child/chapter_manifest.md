# Chapter Manifest - CH042

## Source Chapter

- sourceChapterID: CH042
- sourceFilename: chapter_042_mau_cua_con.md
- sourcePath: ../chapters/chapter_042_mau_cua_con.md
- extractionStatus: complete_first_pass

## English Chapter Title

- title: Blood of the Child
- originalTitle: Mau Cua Con
- act: Act 6 - Africa: Bio-Jungle and First Cure
- gameplayHours: 5h
- primaryPOV: Trung
- mainQuestID: MQ_042
- mainQuestName: Decide Cure Protocol

## Locations

| locationID | displayName | chapterUse |
|---|---|---|
| LOC_CH042_MOBILE_LAB | Mobile Lab Convoy | Post-Cairo evacuation vehicle; lab analysis, family argument, ethics table, blood draw, micro-test, beacon decryption |
| LOC_CH042_NILE_DESERT_ROAD | Nile Desert Road | Convoy transit route; Guardian Fight scene, Hoang confession, family vow dawn scene |
| LOC_CH042_FIELD_CLINIC | Temporary Field Clinic | Medical area adjacent to lab; Yusuf recovery, blood draw procedure, Binh fever monitoring |
| LOC_CH042_AMAZON_PLANNING_ROOM | Amazon Route Planning Room | Map and comms area inside convoy; beacon decryption, route selection, Masud rumor response |

## Required Previous Flags

| flagID | reason |
|---|---|
| FLAG_CH041_FIRST_CURE_SUCCESS | Yusuf is alive and cured; proof that cure works |
| FLAG_CH041_BATCH_FAILURE_DISCOVERED | Failed samples reveal resonance gap; justifies Chapter 42 blood protocol discussion |
| FLAG_CH041_ARCHITECT_BEACON_RECOVERED | Beacon from Juggernaut decrypts in Chapter 10 to reveal Amazon coordinates |
| FLAG_CH041_MOBILE_LAB_ACTIVATED | Rebirth is operating from mobile lab after Cairo evacuation |
| FLAG_CH041_BINH_RESONANCE_BRIDGE_SUSPECTED | Binh's resonance connection discovered; triggers Chapter 42 consent question |
| FLAG_CH041_BINH_IS_NOT_FACTOR_CONSENT_REQUIRED | Binh explicitly protected from exploitation in Chapter 41 |
| FLAG_CH041_CHAPTER_042_BLOOD_PROTOCOL_UNLOCKED | Chapter 42 hook activated at end of Chapter 41 |
| FLAG_CH041_HOANG_TRUST_RESTRAINT | Hoang released under restraint protocol; still infected but trusted |
| FLAG_CH041_MASUD_CURE_RANSOM_REJECTED | Masud escaped; now spreading rumors about Binh |

## Flags Set By This Chapter

| flagID | summary |
|---|---|
| FLAG_CH042_MOBILE_LAB_STABILIZED | Lab systems stabilized after Cairo evacuation |
| FLAG_CH042_FIRST_CURE_REVIEWED | First cure and batch failure data reviewed |
| FLAG_CH042_BINH_TRUTH_CONVERSATION_COMPLETE | Binh heard the truth about resonance in age-appropriate language |
| FLAG_CH042_BINH_INFORMED_CONSENT | Binh gave informed consent for minimal blood draw |
| FLAG_CH042_GUARDIAN_CONFLICT_RESOLVED | Trung and Mai resolved their argument and wrote shared rules |
| FLAG_CH042_GUARDIAN_VETO_ACTIVE | Guardian veto protocol established and active |
| FLAG_CH042_BLOOD_PROTOCOL_ESTABLISHED | Blood Protocol drafted and signed by all parties |
| FLAG_CH042_EDENROT_CHILD_CONSENT_FIREWALL_ESTABLISHED | EDENROT CLASS: CHILD CONSENT FIREWALL created |
| FLAG_CH042_CHILD_CONSENT_FIREWALL_ACTIVE | Firewall active in system header |
| FLAG_CH042_BINH_STOP_WORD_CHOSEN | Binh chose his stop word for medical procedures |
| FLAG_CH042_BINH_STOP_WORD | Binh's stop word value: DenDo |
| FLAG_CH042_MINIMAL_BLOOD_SAMPLE_COLLECTED | One minimal blood sample collected from Binh |
| FLAG_CH042_PROCEDURE_STOPPED_ON_COMMAND | Procedure stopped when Binh used stop word |
| FLAG_CH042_STOP_WORD_HONORED_FIREWALL_VERIFIED | Stop word honored; firewall verified as real |
| FLAG_CH042_BINH_CONSENT_RECONFIRMED | Binh re-consented after stop word pause |
| FLAG_CH042_EXTRA_EXTRACTION_REFUSED | Samir's request for extra micro-test refused |
| FLAG_CH042_MINIMAL_DRAW_ONLY_CHILD_NOT_SOURCE | Binh marked as child/person, not source/factor/bridge |
| FLAG_CH042_BETTER_BATCH_MICRO_STABILITY | Binh's sample improved enzyme stability in micro-tests |
| FLAG_CH042_CURE_SCALABILITY_STILL_BLOCKED | Cure cannot scale to mass production yet |
| FLAG_CH042_CURE_MORAL_FLAG | Cure moral flag set: ConsentFirst |
| FLAG_CH042_MASUD_RUMOR_CONTAINED | Masud rumor partially contained via trusted-node comms |
| FLAG_CH042_TRUSTED_ALLIES_BRIEFED | Trusted allies received encrypted truth about cure |
| FLAG_CH042_HOANG_SELF_AWARENESS | Hoang acknowledged his dangerous desire and signed self-restraint |
| FLAG_CH042_ARCHITECT_BEACON_DECODED | Architect beacon decrypted to reveal Amazon coordinates |
| FLAG_CH042_ASTER_NODE_LOCATED | Aster Node location confirmed in Amazon Basin |
| FLAG_CH042_ORISON_ARCHIVE_REVEALED | Orison child resonance archive discovered |
| FLAG_CH042_ORISON_CHILD_RESONANCE_CHAMBER_REVEALED | Child resonance chamber revealed in Architect data |
| FLAG_CH042_FLOODED_AMAZON_ROUTE_CHOSEN | Flooded river route selected for Act 7 |
| FLAG_CH042_CHAPTER_043_FLOODED_AMAZON_UNLOCKED | Chapter 43 Flooded Amazon unlocked |

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

After Cairo, Rebirth evacuates to a mobile lab convoy on the Nile desert road. Yusuf lives as the first cure proof, but batch failures reveal Binh may hold a stronger resonance key. Binh demands truth. Trung and Mai argue about protection versus honesty. They establish the EDENROT CLASS: CHILD CONSENT FIREWALL, draft a strict Blood Protocol, and let Binh choose a stop word. Binh gives one minimal sample, stops once to prove the firewall is real, then re-consents. The sample improves micro-stability but cannot scale. Masud spreads rumors forcing trusted-node comms. Architect beacon decrypts to reveal Amazon Citadel coordinates and Orison child resonance archive. The family vows no one saves the world alone. Convoy enters the flooded Amazon where trees move.

## Open Questions

| questionID | question | currentHandling |
|---|---|---|
| OQ_CH042_001 | Does Lina survive Cairo evacuation? | Mark as unknown; Mai refuses to lie. SQ_042_A tracks search. |
| OQ_CH042_002 | Which trusted allies receive encrypted truth beyond Nia/Kito, NORAD, Amelie cell, Heartland? | Use TODO_DERIVE_OR_APPROVE for additional alliance nodes. |
| OQ_CH042_003 | Does Sable remnant intercept Masud's rumor or the false beacon? | Track as partial containment; resolve in Chapter 43 or 44. |
| OQ_CH042_004 | What is the exact decay rate of Binh's micro-stability improvement? | Mark as TODO for systems balancing; source says 9 minutes max in lab model. |

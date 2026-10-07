# Validation - CH042

Metadata:

- chapterID: CH042
- sourceFilename: chapter_042_mau_cua_con.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_042_mau_cua_con.md`

Referenced workflow:

- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`
- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

Referenced continuity:

- `.agent/production/StorylineData/chapters/CH041_cairo_siege/chapter_manifest.md`
- `.agent/production/StorylineData/chapters/CH041_cairo_siege/characters.md`
- `.agent/production/StorylineData/chapters/CH041_cairo_siege/quests.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | All assets derived from chapter_042_mau_cua_con.md metadata, scene outline, quest sections, dialogue tree, prose draft, emotional design, structural role, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved: Trung, Mai, Binh, Hoang, Samir, Yusuf, Thu, Nia, Kito, Masud, Salma. Stop word "Den Do" preserved with English gloss. |
| Are all IDs stable and ASCII-only? | Yes | All IDs use uppercase/lowercase ASCII, numbers, underscores only. |
| Does the main quest match the chapter's canonical main quest? | Yes | MQ_042 - Decide Cure Protocol matches source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | All DT_262-DT_271 and DT_370 translated preserving emotional weight. Binh's fear, Trung's reflex, Mai's fierce consent defense, Samir's temptation, Yusuf's debt rejection, Hoang's ugly honesty all preserved. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Blood Protocol Doc (protocol drafting), Binh's Sample (micro-test), Stop Word Record (abort mechanic), Cure Data Record (analysis), Architect Beacon (route unlock), Failed Samples (evidence), False Beacon (comms), Seed Packet (memory), Family Vow (emotional), Route Map (route selection), Nia Clause (covenant), Hoang Restraint (future setup). |
| Are open questions clearly marked instead of silently invented? | Yes | Lina survival, additional trusted allies, Sable remnant interception, stability decay rate all marked as open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all 10 required files in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Source, title, locations (4), required previous flags (8), flags set (28), load order, canon summary, open questions (4). |
| characters.md | complete | 12 characters: 3 playable (Trung, Mai, Binh), 1 companion (Hoang), 7 NPCs (Samir, Yusuf, Amelie, Kareem, Thu, Nia, Salma), 1 antagonist (Masud), 1 scout. Notes on arc, emotional state, signature lines. |
| quests.md | complete | Main quest MQ_042 with 18 objectives, 6 optional objectives, 5 fail states, 7 rewards, 5 unlocks, 12 continuity flags, 5 side quest hooks (SQ_042_A through SQ_042_E). |
| dialogue.md | complete | 52 dialogue entries covering all 12 scenes. Includes DT_262-DT_271, DT_370, scene transitions, stop word mechanic, consent reconfirmation, batch result, Hoang confession, beacon reveal, family vow. |
| items.md | complete | 12 items: 5 quest items, 2 system items, 3 memory items, 1 evidence, 1 consumable. All tied to quest, scene, or progression logic. |
| scenes.md | complete | 12 scenes matching source outline: Lab Night, Truth Meeting, Guardian Fight, Ethics Table, Yusuf Wake, Masud Rumor, Small Needle, Better Batch, Hoang Confession, Beacon Decrypt, Family Vow, Green Water. |
| enemies.md | complete | 6 entries: 2 social hazards (Time Pressure, Language Dehumanization), 1 information hazard (Masud Rumor), 1 environmental foreshadow (Architect Signal), 1 offscreen human hazard (Sable Listener), 1 environmental foreshadow (Moving Trees). No traditional combat enemies. |
| factions.md | complete | 7 factions: Trung Family, Rebirth Alliance, Masud Network, Sable Remnant, Architect, Heartland Convoy, NORAD. Notes on behavior and future implications. |
| flags.md | complete | 38 flags covering progression (14), emotional (5), system (3), choice (3), relationship (2), moral (1), item_state (1), world_state (4), lore (2), sidequest (2), faction (1). |
| validation.md | complete | This file. |

## English Output Checklist

| item | status |
|---|---|
| Descriptions are in English | pass |
| Quest text is in English | pass |
| Dialogue text is in English | pass |
| Item names are in English | pass |
| Scene names are in English | pass |
| Enemy descriptions are in English | pass |
| Faction descriptions are in English | pass |
| Vietnamese proper names preserved only as names | pass |

## Missing Data / TODOs

| todoID | detail | reason |
|---|---|---|
| TODO_CH042_001 | Confirm Lina survival status in future chapter. | Source says location unknown, not confirmed dead. SQ_042_A tracks search. |
| TODO_CH042_002 | Identify additional trusted alliance nodes beyond Nia/Kito, NORAD, Amelie cell, Heartland. | Source lists these four but leaves room for more. |
| TODO_CH042_003 | Determine Sable remnant response to false beacon or real comms intercept. | Source says "Sable remnant listens" but does not resolve. |
| TODO_CH042_004 | Define exact micro-stability decay rate for systems balancing. | Source says 9 minutes max in lab model; needs tuning data. |
| TODO_CH042_005 | Confirm whether BinhDistrust is a numeric counter or threshold enum. | Source says "wrong answers increase BinhDistrust" but does not define exact system. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH042_001 | Chapter has no traditional combat enemies; combat system may expect enemy entries. | Enemies are social/linguistic/environmental hazards. Tooling should accept non-combat enemy types. |
| RISK_CH042_002 | Stop word mechanic requires real-time UI prompt during blood draw scene. | Scene 07 interaction notes specify breath rhythm input, stop word button always visible, hard fail if ignored. |
| RISK_CH042_003 | Blood Protocol is an interactive document, not a standard choice wheel. | Player selects clauses, rejects coercive language. Implementation notes specify bad wording examples to reject. |
| RISK_CH042_004 | BinhDistrust and BinhTrust are relationship counters that interact across scenes. | Setup tool should treat relationship flags as counters, not booleans. |
| RISK_CH042_005 | CureMoralFlag = ConsentFirst influences all future child/immune arcs and endings. | Must persist across chapters and be checked by future Orison/child-resonance scenes. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH043

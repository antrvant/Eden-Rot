# Validation - CH012

Metadata:

- chapterID: CH012
- sourceFilename: chapter_012_nha_tho_khong_chuong.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_012_nha_tho_khong_chuong.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from CH012 metadata, scene outline, quest sections, dialogue tree samples, prose draft, emotional design, character notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved: Trung, Mai, Binh, Hoang, O Tu Nieu, Edenrot. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. All prefixed with CH012. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_012 - Find Mai`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves reunion pain, "they took him" moral anchor, Mai's testimony, Hoang's privacy gesture, and Priest's faith-in-silence. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support quest progression (chalk, note), emotional continuity (scarf, recording), and evidence (cloth fragment, tobacco). |
| Are open questions clearly marked instead of silently invented? | Yes | Yellow coat identity, Edenrot nature, Binh immunity mechanics, girl companion timing, and church bell consequences remain open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions, carryover evidence. |
| characters.md | complete | Includes Trung, Mai, Hoang, Binh, Priest, Girl, Doctor, Radio Operator, Old Cook, Nam, Yellow Coat Watcher, O Tu Nieu, Church Refugee. |
| quests.md | complete | Includes MQ_012, 10 objectives, 5 optional objectives, fail states, rewards, unlocks, 5 side quest hooks. |
| dialogue.md | complete | Includes DT_042 (Priest gate), DT_043 (reunion), DT_044 (Mai testimony), DT_045 (Hoang privacy), plus barks and choice branches. |
| items.md | complete | Includes chalk, broken chalk, Binh scarf, O Tu Nieu note, yellow cloth, tobacco, bandage request, girl item, bell rope, Edenrot map, dog tag, recording, survivor list, candles, mural. |
| scenes.md | complete | Includes 7 scenes: road, silent bell, girl witness, reunion, testimony, watcher, departure. |
| enemies.md | complete | Includes Edenrot street hazard, church perimeter infected, yellow coat watcher, bell-triggered zombie horde. |
| factions.md | complete | Includes family, Hoang friendship, church survivors, yellow coats, survivor group, industrial zone, Edenrot zone. |
| flags.md | complete | Includes 30 flags covering progression, emotional, choice, relationship, lore, sidequest, item_state, world_state, system types. |

## English Output Checklist

| item | status |
|---|---|
| Descriptions are in English | pass |
| Quest text is in English | pass |
| Dialogue text is in English | pass |
| Item names are in English | pass |
| Scene names are in English | pass |
| Faction descriptions are in English | pass |
| Vietnamese proper names preserved only as names | pass |

## Missing Data / TODOs

| todoID | detail | reason |
|---|---|---|
| TODO_CH012_001 | Girl's specific lost item type not defined in source. | Source says "item/photo" but does not specify. Marked as TODO_DERIVE_OR_APPROVE in items.md. |
| TODO_CH012_002 | Full identity of yellow coat faction. | Source seeds them as child hunters but does not reveal full faction name/structure. |
| TODO_CH012_003 | Mechanical nature of Binh's immunity. | Source says "no fever after exposure" but does not explain scientifically. |
| TODO_CH012_004 | Church refugee informant role. | Source mentions an elderly refugee may be watching for yellow coats; loyalty uncertain. |
| TODO_CH012_005 | Consequences of church bell choice in future chapters. | SQ_012_03 bell choice is tracked but payoff is in later chapters. |
| TODO_CH012_006 | Girl companion hook payoff timing. | Source seeds companion hook but does not specify when girl joins. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH012_001 | Setup tool might treat yellow coat watcher as combat encounter. | Enemies and validation state watcher is social/perception threat only. |
| RISK_CH012_002 | Edenrot might be loaded as explorable zone. | Validation and enemies state it is a route hazard to avoid, not engage. |
| RISK_CH012_003 | FamilyTrust flag might be missed if player skips reunion dialogue. | Flag is set at key emotional beat; dialogue tree forces the choice. |
| RISK_CH012_004 | Binh's absence might be confused with Binh being present. | Characters.md marks Binh as missing_child; scene NPCs exclude Binh. |
| RISK_CH012_005 | Church bell choice might be treated as mandatory. | SQ_012_03 is a side quest hook; bell choice is optional. |
| RISK_CH012_006 | O Tu Nieu might be confused with Old Cook from outpost. | Continuity notes in source specify they are different people. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH013

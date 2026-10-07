# Validation - CH015

Metadata:

- chapterID: CH015
- sourceFilename: chapter_015_hoi_dong_cua_nhung_ke_song_sot.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_015_hoi_dong_cua_nhung_ke_song_sot.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`
- `.agent/production/StorylineData/chapters/CH008_captains_lesson/` (format reference)

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 15 metadata, scene outline, quest sections, dialogue tree samples, prose draft, emotional design, character notes, council system design, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Mai, Binh, Hoang, Ong Tu Nhieu, Hanh, Phuc, Lan, Nam. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. All prefixed with CH015. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_015 - Form Council`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Binh's guilt, Trung's choice to be limited, Mai's structured compassion, Hoang's pragmatic honesty, Worker Lead's citizenship birth, and Hanh's coerced desperation. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support medicine decision, scout evidence, voting system, council governance, and emotional continuity. |
| Are open questions clearly marked instead of silently invented? | Yes | Seven open questions listed in chapter_manifest.md covering scout future, fever child trust, Hoang escalation, Binh name echo, Worker Lead role, Phuc continuity, and EDEN cache mission. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions. |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Ong Tu Nhieu, Worker Lead, Doctor, Radio Operator, Lan, Fever Child, Hanh (Fake Mother), Phuc, Base Survivor. |
| quests.md | complete | Includes MQ_015, 13 objectives, 6 optional objectives, 5 fail states, 11 rewards, 8 unlocks, 9 continuity flags, 6 side quest hooks. |
| dialogue.md | complete | Includes fever night, Binh medicine offer, Worker Lead challenge, Mai children advocacy, scout expose, medicine question, Hoang strike vote, council close, Ong Tu Nhieu advisor, gate screening, scout confession. 62 dialogue entries. |
| items.md | complete | Includes EDEN medicine, package label, yellow thread, Binh drawing, first vote slip, council rulebook, EDENROT notice, fever compress, chalk votes, scout map, water cup, rope restraint. |
| scenes.md | complete | Includes fever night, gate stranger, emergency meeting, council seats, medicine decision, scout expose, strategic vote, closing. 8 scenes. |
| enemies.md | complete | Includes social paranoia, fever outbreak, EDEN scout infiltrator, night probe, EDENROT language, rumor network. All social/environmental hazards. |
| factions.md | complete | Includes Family Core, Security, Workers, Medical, Children, Food Advisors, Base Survivors, EDEN Network, EDEN Scout. |
| flags.md | complete | Includes 28 flags covering council formation, medicine, scout, Hoang vote, Binh guilt, EDENROT paranoia, enemy classification rejection, and all supporting state flags. |
| validation.md | complete | This file. |

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
| TODO_CH015_001 | Confirm fake mother scout's long-term fate (prisoner, messenger, or casualty). | Source says it depends on player choice in later chapters. |
| TODO_CH015_002 | Confirm when Hoang's dissent escalates to action. | Source says Chapters 17-18 should reference `HoangStrikeFirstVote`. |
| TODO_CH015_003 | Confirm Binh's name-change echo timing. | Source says it should echo when immune children are assigned codes by Architects. |
| TODO_CH015_004 | Confirm Worker Lead's long-term council role. | Source says he should become a steady council voice. |
| TODO_CH015_005 | Confirm child Phuc's continuity role. | Source says Phuc should remain in base as reminder. |
| TODO_CH015_006 | Confirm if EDEN cache near community center becomes a mission. | Intel is unlocked but mission not yet defined. |
| TODO_CH015_007 | Confirm fever child's name. | Source does not assign a name to the fever child. |
| TODO_CH015_008 | Confirm exact previous flags from CH014. | CH014 package not yet generated; flags inferred from source. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH015_001 | Setup tool might treat this as a combat chapter. | Enemies and validation state all threats are social, medical, and infiltration. No traditional infected combat. |
| RISK_CH015_002 | Hoang's strike-first vote could be read as betrayal. | Character notes and dialogue preserve Hoang's honesty; dissent is recorded, not punished. |
| RISK_CH015_003 | Fake mother scout could be written as purely evil. | Character notes explicitly state she should hurt the reader; her lie is awful but understandable. |
| RISK_CH015_004 | Binh's guilt thread could be over-dramatized. | Source says children hear fear even when they miss words; Binh's arc is quiet but devastating. |
| RISK_CH015_005 | Council system could feel modern/clean. | Source explicitly says democracy here is improvised, tired, and fragile. |
| RISK_CH015_006 | EDENROT labels could be treated as mere plot devices. | Source says Edenrot is not only biological infection but social distrust; the rot is inside the community. |
| RISK_CH015_007 | Mai could be written as "let everyone in" idealist. | Character notes say she supports quarantine, screening, and truth-telling; compassion is structured. |
| RISK_CH015_008 | Previous flags from CH014 are inferred, not verified. | Marked as TODO; CH014 package should be checked when generated. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH016

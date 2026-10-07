# Validation - CH020

Metadata:

- chapterID: CH020
- sourceFilename: chapter_020_bien_dong_day_xac.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_020_bien_dong_day_xac.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`

Referenced format:

- `.agent/production/StorylineData/chapters/CH008_captains_lesson/` (all 10 files)

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | All assets derived from Chapter 020 metadata, scene outline, quest sections, dialogue tree samples, prose draft, cast state, emotional design, lore reveal, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved: Trung, Mai, Binh, Hoang, Ba Sau, So 4, Lan, Phuc, Lam, Thu, Ong Tu Nieu, Mekong, Mê Linh, Edenrot. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores only. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_020 - Reach the Coast`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Hoang's uncomfortable limbo, Binh's identity milestone, Mai's trauma admission, Lam's river pilot pragmatism, Thu's distrust, and the bio-storm terror. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support Architect drive route, chalk symbol, Lam's map, Edenrot sample, ship repair, bio-storm evidence, and radio signal log. |
| Are open questions clearly marked instead of silently invented? | Yes | Lam's brother, boat naming, unnamed island, So 4 stay/go, Edenrot ecology, and Hoang trust remain open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions, continuity resolution. |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Doctor, Worker Lead, Ong Tu Nieu, Ba Sau, So 4, Lan, Phuc, radio operator, Lam, Thu. |
| quests.md | complete | Includes MQ_020, 12 objectives, 5 optional objectives, 5 fail states, 8 rewards, 8 unlocks, 10 continuity flags, 5 side quest hooks. |
| dialogue.md | complete | Includes Hoang judgment (DT_087), blackboard farewell (DT_088), river pilot negotiation (DT_089), sea first view (DT_090), bio-storm (DT_091). |
| items.md | complete | Includes Architect drive, naval route, chalk fragments, convoy cloth, tide map, Edenrot sample, ship parts, bio-storm debris, radio signal log. |
| scenes.md | complete | Includes 7 scenes: Hoang judgment, leaving home, corpse river, ferry pilot, fishing port, departure, bio-storm. |
| enemies.md | complete | Includes drowned infected swimmers, drowned infected boarders, bandit pursuers, maritime Edenrot bloom, bio-storm hazard. |
| factions.md | complete | Includes travel team, base caretakers, Hoang limbo, river survivors, coastal survivors, bandit pursuers, maritime Edenrot, Architect network. |
| flags.md | complete | Includes 35 flags covering progression, moral, emotional, choice, skill, world_state, lore, sidequest, and continuity types. |

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
| TODO_CH020_001 | Confirm whether Lam's brother ship Mê Linh payoff is Chapter 21 or later. | Source only records the promise; payoff timing unknown. |
| TODO_CH020_002 | Confirm if boat receives a name in Chapter 21. | Source says unnamed at chapter end. |
| TODO_CH020_003 | Confirm unnamed island identity as Eden maritime relay. | Source implies it; Chapter 21 should confirm. |
| TODO_CH020_004 | Confirm So 4's role in later chapters after staying at base. | Source recommends stay; future chapters may revisit. |
| TODO_CH020_005 | Confirm full Edenrot ecology escalation in Chapters 21-25. | Source introduces concept; later chapters expand. |
| TODO_CH020_006 | Confirm if Hoang earns partial trust by Chapter 21 end. | Source explicitly says no forgiveness yet. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH020_001 | Setup tool might treat bio-storm as a combat encounter. | Enemies and validation state bio-storm is survival/forced movement, not combat. |
| RISK_CH020_002 | Hoang might be loaded as full companion instead of monitored asset. | Character and flag explicitly state monitored status with restrictions. |
| RISK_CH020_003 | Drowned infected might be treated as land zombie variant. | Enemy notes emphasize aquatic behavior: floats, waits, does not swim, carried by current. |
| RISK_CH020_004 | Edenrot might be confused with Architect classification. | Factions section documents the language split: survivors say Edenrot, Architects say relay/node. |
| RISK_CH020_005 | Base caretakers might be forgotten in future chapters. | Flag and faction preserve base as return node. |
| RISK_CH020_006 | Chalk fragment emotional item might be dropped by optimization. | Items and validation flag it as recurring symbol for ship/classroom scenes. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH021

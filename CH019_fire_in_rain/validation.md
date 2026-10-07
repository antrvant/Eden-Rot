# Validation - CH019

Metadata:

- chapterID: CH019
- sourceFilename: chapter_019_lua_trong_mua.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_019_lua_trong_mua.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`
- `.agent/production/StorylineData/chapters/CH015_council_of_survivors/` (format reference)

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | All assets derived from Chapter 19 metadata, scene outline, quest sections, dialogue tree samples, prose draft, emotional design, character notes, lore reveal, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved where they are names: Trung, Mai, Binh, Hoang, Ba Sau, So 4, Ong Tu Nhieu. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. All prefixed with CH019. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_019 - Rescue Mai`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Trung's restraint, Mai's active captivity, Hoang's self-aware guilt, Binh's justice question, lieutenant's pragmatic cruelty, and Ong Tu Nhieu's philosophical anchor. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support chalk tracking, server recovery, lockpicking, smoke distraction, trap freeing, blackboard repair, and emotional continuity. |
| Are open questions clearly marked instead of silently invented? | Yes | Seven open questions listed in chapter_manifest.md covering Hoang status, prisoner fate, lieutenant return, Mai trauma, base departure, Ba Sau echo, and young prisoner continuity. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions. |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Worker Lead, Doctor, Ba Sau, So 4, Ong Tu Nhieu, Bandit Lieutenant, Bandit Trader, Radio Operator, Tied Prisoner, Young Female Prisoner. 14 characters. |
| quests.md | complete | Includes MQ_019, 14 objectives, 8 optional objectives, 5 fail states, 10 rewards, 6 unlocks, 11 continuity flags, 5 side quest hooks. |
| dialogue.md | complete | Includes family goodbye (DT_081), forest tracking (DT_082), Mai captive (DT_083), server room (DT_084), canal bridge (DT_085), base return (DT_086), server decode, Mai return, lieutenant shield, rescue planning, Ba Sau, prisoner, Ong Tu Nhieu, Worker Lead. 52 dialogue entries. |
| items.md | complete | Includes Mai's chalk, Architect broker drive, bandit trade log, metal shard, smoke bomb, server files printout, fort keys, chalk dust, iron bar, repaired blackboard. 10 items. |
| scenes.md | complete | Includes unclean promise, chalk in rain, Mai in fort, rain infiltration, server brick, fire in rain, chance to kill, home not whole. 8 scenes. |
| enemies.md | complete | Includes bandit lieutenant, bandit garrison, rain horde, fire hazard, broker network, moral rage. All enemy types: human, infected, environmental, systemic, emotional. |
| factions.md | complete | Includes Family Core, Rescue Team, Base Defense, Bandits, Children, EDEN/Architect Broker Network. |
| flags.md | complete | Includes 19 flags covering Mai rescue, Hoang spare, Architect file, EDENROT confirmation, naval route, fort weakened, Hoang fate, justice question, classroom repair, Act 3 completion, and supporting state flags. |
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
| TODO_CH019_001 | Confirm Hoang's formal status after return (detained, monitored, exiled, forced labor). | Source says council decides in Chapter 20. |
| TODO_CH019_002 | Confirm tied prisoner's long-term survival and role. | Source does not specify; may return as witness or informant. |
| TODO_CH019_003 | Confirm bandit lieutenant's return arc. | Source says he survives; can return in later bandit faction arcs. |
| TODO_CH019_004 | Confirm Mai's trauma continuation in Chapter 20+. | Source says she is strong but not unaffected; should be referenced. |
| TODO_CH019_005 | Confirm exact timing of group leaving "Home." | Source says Chapter 20 begins Act 4; departure should occur early. |
| TODO_CH019_006 | Confirm young female prisoner's fate and continuity role. | Source does not specify; Mai drew a circle (name symbol) for her. |
| TODO_CH019_007 | Confirm previous flags from CH018. | CH018 package not yet generated; flags inferred from source. |
| TODO_CH019_008 | Confirm server file choice (delete/copy/broadcast) canon outcome. | Source says copy is recommended canon; delete and broadcast are alternate branches. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH019_001 | Setup tool might treat Hoang as redeemed. | Character notes and dialogue explicitly state helping rescue is damage control, not redemption. Hoang's future arc remains open. |
| RISK_CH019_002 | Mai could be written as passive captive. | Character notes and scene outline require her to be active: counting guards, leaving chalk, misdirecting, picking locks, creating opening. |
| RISK_CH019_003 | Trung's restraint could read as weakness. | Emotional design and dialogue make restraint cost him; it is strength defined by what he refuses to do, not what he cannot do. |
| RISK_CH019_004 | Server files could be treated as minor plot device. | Lore reveal section explicitly states files confirm EDEN/Architect broker network tracking Edenrot dormancy at maritime logistics level. This opens Act 4. |
| RISK_CH019_005 | Binh's justice question could be over-simplified. | Character notes say it is the moral center; Binh is asking what justice looks like when the person who hurt you was once family. |
| RISK_CH019_006 | Bandit lieutenant could be written as pure villain. | Enemy notes state he is not cartoonish; he sees hostages as insurance and has broker connections. |
| RISK_CH019_007 | Fire/rain visual could be treated as mere backdrop. | Source says fire burning under rain is the chapter's title image and thematic core: some fires do not go out under rain; they change form. |
| RISK_CH019_008 | Previous flags from CH018 are inferred, not verified. | Marked as TODO; CH018 package should be checked when generated. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH020

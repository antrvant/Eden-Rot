# Validation - CH002

Metadata:

- chapterID: CH002
- sourceFilename: chapter_002_thanh_pho_khong_con_den_do.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_002_thanh_pho_khong_con_den_do.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 002 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Mai, Binh, Hoang, Nhi, Sai Gon. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_002 - Reach Home`, matching the source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves family urgency, Mai's active survival, Hoang's pragmatic concern, store moral pressure, and the lost-child choice. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items are tied to route clues, scavenging, barter, rescue, memory, or Chapter 003 progression. |
| Are open questions clearly marked instead of silently invented? | Yes | Phone-missing fallback, coworker survival, and Mai's exact northern route are marked as open. Nhi is confirmed as the recurring lost-child thread by later canon references. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, required previous flags, flags set, load order, summary, open questions. |
| characters.md | complete | Includes remote family, Hoang, conditional coworker, street civilians, looters, store owner, apartment figures. |
| quests.md | complete | Includes MQ_002, objectives, optional objectives, fail states, rewards, unlocks, side hooks. |
| dialogue.md | complete | Includes Hoang call tree, store owner choice, lost mother choice, Mai calls/texts, final fridge note. |
| items.md | complete | Includes phone, power bank, water, bandage, milk, gasoline, car/key items, ribbon, chalk, fridge note, broken toy. |
| scenes.md | complete | Includes basement, intersection, store, alley call, lost child bus, apartment building, empty home. |
| enemies.md | complete | Includes infected and human hazards without forcing every human threat into combat. |
| factions.md | complete | Includes family, Hoang friendship, civilians, price gougers, looters, collapsed authority, infected. |
| flags.md | complete | Includes progression, moral, relationship, resource, choice, sidequest, and world-state flags. |

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
| TODO_CH002_001 | Define alternate clue delivery if `FLAG_CH001_PHONE_RECOVERED` is false. | Chapter 002 relies on phone calls/messages, while Chapter 001 allows leaving without the phone. |
| TODO_CH002_002 | Confirm whether npc_coworker_01 separates, survives, or dies if present in Chapter 002. | Source says he may continue if alive, and later may reappear, but does not lock Chapter 002 endpoint. |
| TODO_CH002_003 | Define the exact route north that Mai took after leaving apartment 1208. | Source only establishes chalk marks and that Chapter 003 begins with investigation. |
| TODO_CH002_004 | Confirm exact later scene/location for npc_lost_mother and npc_nhi after rescue. | Later canon references confirm the thread recurs, but setup still needs exact spawn/location handling. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH002_001 | Chapter 002 references `ENM_CH001_INFECTED_BOSS` as a conditional carryover. | Setup tool should allow cross-chapter references only when prior flags indicate the enemy is unresolved. |
| RISK_CH002_002 | Some flags are counters while others are booleans. | Use `type` column to parse moral/personality/relationship counters separately from boolean progression flags. |
| RISK_CH002_003 | Human hazards may not map cleanly to enemy prefab spawning. | Treat `enemyType=human_hazard` as scene behavior, dialogue, crowd, or combat depending on setup rules. |
| RISK_CH002_004 | Phone-dependent content conflicts with possible Chapter 001 phone failure path. | TODO_CH002_001 must be resolved before final automated setup. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH003

# Validation - CH003

Metadata:

- chapterID: CH003
- sourceFilename: chapter_003_loi_nhan_tren_tu_lanh.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_003_loi_nhan_tren_tu_lanh.md`

Continuity search performed:

- Searched all `.agent/production/chapters` for `Nhi`.
- Chapter 002 introduces Nhi as the lost child near the overpass.
- Later chapters reference the lost mother/Nhi thread, confirming Chapter 002 Nhi is the recurring Nhi.
- Chapter 003's locked-apartment child also says the name "Nhi" in prose, but the scene context conflicts with the recurring Chapter 002 Nhi. This package therefore uses `npc_locked_child` and marks the display name as `TODO_DERIVE_OR_APPROVE`.

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 003 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Mai, Binh, Hoang, Ba Bay. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_003 - Find First Clue`, matching the source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Mai's trust, Trung's guilt, Binh's traces, neighbor fear, Ba Bay's care, and Hoang's blunt warning. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items are tied to investigation, tracking, emotional memory, stealth loot, medicine side quest, mutation foreshadow, or Chapter 004 route. |
| Are open questions clearly marked instead of silently invented? | Yes | Locked child name conflict, Bloater activation, Ba Bay recruitment, and exact checkpoint route are marked as open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, load order, Nhi continuity resolution, open questions. |
| characters.md | complete | Includes family traces, Hoang, neighbor, Ba Bay, selfish residents, manager, locked child, infected threats. |
| quests.md | complete | Includes MQ_003, objectives, optional objectives, fail states, rewards, unlocks, side hooks. |
| dialogue.md | complete | Includes fridge note choices, neighbor dialogue, lying neighbor, Ba Bay, locked child clue, Hoang checkpoint call. |
| items.md | complete | Includes fridge note, chalk trail, family objects, medicine, milk powder, Bloater clue, north route items. |
| scenes.md | complete | Includes empty apartment, chalk stairwell, neighbor trade, mini mart Bloater, locked apartment, north arrow. |
| enemies.md | complete | Includes apartment infected, trapped infected, locked apartment infected, mini mart infected, Bloater foreshadow/hazard. |
| factions.md | complete | Includes family, Hoang, residents, selfish neighbors, caretaker survivors, management, survivor group, infected. |
| flags.md | complete | Includes tracking, social, moral, sidequest, mutation, route, and emotional inventory flags. |

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
| TODO_CH003_001 | Rename the locked-apartment child in canon or approve keeping the duplicate name. | Chapter 002 Nhi is recurring in later chapters; Chapter 003 child cannot safely share `npc_nhi`. |
| TODO_CH003_002 | Confirm whether the Bloater activates as gameplay in Chapter 003 or remains pure foreshadow. | Source says it can become an encounter if noise is made, but does not require combat. |
| TODO_CH003_003 | Confirm Ba Bay's later recruit/base NPC role. | Source says Ba Bay can be a future recruit/NPC if alive. |
| TODO_CH003_004 | Confirm the exact name/location ID of the northern military checkpoint for Chapter 004. | Chapter 003 only points north toward a checkpoint. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH003_001 | Source prose uses "Nhi" for two contextually different children across Chapters 002 and 003. | CH003 uses `npc_locked_child` and marks display name as `TODO_DERIVE_OR_APPROVE`; no second `npc_nhi` is created. |
| RISK_CH003_002 | Bloater may be either foreshadow or optional active hazard. | Separate `ENM_CH003_BLOATER_FORESHADOW` from `ENM_CH003_OPTIONAL_BLOATER_HAZARD`. |
| RISK_CH003_003 | Flags include counters and booleans in one table. | Use `type` column to parse counters separately. |
| RISK_CH003_004 | `FLAG_CH003_CHALK_MARKS_FOUND_COUNT` expects numeric increment behavior. | Setup tool should support counter flags or derive count from found marker IDs. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH004

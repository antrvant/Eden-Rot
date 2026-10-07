# Validation - CH036

Metadata:

- chapterID: CH036
- sourceFilename: chapter_036_paris_khong_anh_den.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_036_paris_khong_anh_den.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from metadata, scene outline, quest sections, dialogue samples, prose draft, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese names preserved: Binh, Mai, Trung, Amelie, Celine, Mimic. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII, numbers, underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | MQ_036 - Find Research Archive matches source metadata. |
| Are dialogue lines faithful to the emotional intent? | Yes | Attendance ritual, Mimic voice horror, data follows people all preserved. |
| Are all items actually needed by quest, scene, or progression? | Yes | Items tied to objectives, puzzles, emotional memory. |
| Are open questions clearly marked instead of silently invented? | Yes | Mimic identity, Celine backstory, Mimic survival marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 files present in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | All named and referenced characters from Chapter 036. |
| quests.md | complete | Main quest, objectives, fail states, rewards, side hooks. |
| dialogue.md | complete | DT_207 through DT_215 translated to English. |
| items.md | complete | Quest items, puzzle items, memory items, environmental clues. |
| scenes.md | complete | All 9 scenes with locations and NPCs. |
| enemies.md | complete | Mimic, ice horde, darkness, false voices, archive decay. |
| factions.md | complete | Rebirth, Paris School, Mimic, Ice Horde, VALE/Architect. |
| flags.md | complete | Progression, moral, emotional, world state, choice flags. |

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
| TODO_CH036_001 | Confirm whether Mimic is infected variant or signal-altered predator. | Source describes both possibilities; needs production decision. |
| TODO_CH036_002 | Confirm Celine's full backstory and possible return in later chapters. | Source gives librarian role only. |
| TODO_CH036_003 | Confirm Mimic's long-term arc: recurring enemy or chapter-local. | Source shows it learns and retreats. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH036_001 | Mimic enemy type may need special sound-voice system beyond standard enemy framework. | Mark for production review when enemy system is finalized. |
| RISK_CH036_002 | Attendance roll call mechanic may need custom interaction system. | Flag for UI/UX design review. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH037

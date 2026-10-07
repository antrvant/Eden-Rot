# Validation - CH007

Metadata:

- chapterID: CH007
- sourceFilename: chapter_007_dem_dau_ngoai_tuong_rao.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_007_dem_dau_ngoai_tuong_rao.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 007 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Hoang, Mentor, Phuc, Nam, Nhi. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_007 - First Night Defense`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves duty conflict, Hoang's circle warning, refugee humanization, Screamer panic, and dawn exhaustion. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support defense prep, ammo hook, Screamer analysis, mother gate interaction, refugee trust, or aftermath. |
| Are open questions clearly marked instead of silently invented? | Yes | Nam recurrence, missing ammo cause, climber timing, and Screamer mechanism remain open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, Nhi continuity, load order, open questions. |
| characters.md | complete | Includes Trung, Hoang, Mentor, engineer, doctor, radio operator, Phuc, refugees, Nam, lost mother/Nhi. |
| quests.md | complete | Includes MQ_007, objectives, optional objectives, fail states, rewards, unlocks, side hooks. |
| dialogue.md | complete | Includes Mentor assignment, Hoang defense priority, refugee tent, mother gate, Screamer, aftermath. |
| items.md | complete | Includes defense materials, ammo hook, child ear cloth, Screamer sample, flare, repair plan. |
| scenes.md | complete | Includes night assignment, refugee tent, reinforce fence, first scream, night wave, mother gate, dawn aftermath. |
| enemies.md | complete | Includes Screamer, horde, climber foreshadow, gate pressure infected, crowd panic hazard. |
| factions.md | complete | Includes family, Hoang, Mentor, army outpost, defense crew, refugees, radio operators, infected. |
| flags.md | complete | Includes defense choices, wave outcomes, Screamer knowledge, crowd panic, Nhi thread, Hoang pressure, training unlock. |

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
| TODO_CH007_001 | Confirm whether Nam recurs later. | Source introduces Nam in refugee tent but does not define later role. |
| TODO_CH007_002 | Confirm missing ammo cause: accounting error, theft, or sabotage. | Source deliberately leaves this as seed for Chapter 10-11. |
| TODO_CH007_003 | Confirm when infected climber becomes a full enemy variant. | CH007 only foreshadows the behavior. |
| TODO_CH007_004 | Keep Screamer voice mechanism ambiguous. | Source says it may make people hear what they fear; no full biological explanation yet. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH007_001 | Defense allocation needs downstream wave simulation. | Store explicit defense choice flags and outcome flags separately. |
| RISK_CH007_002 | Nhi appears only through the mother and is absent. | Reference recurring `npc_nhi` as absent, and set continuity flag only. |
| RISK_CH007_003 | Screamer dialogue uses a bracketed non-verbal cry. | Keep text field as descriptive bark; audio system can map to sound asset later. |
| RISK_CH007_004 | Crowd panic is not a standard enemy. | Use `enemyType=social_hazard` for setup flexibility. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH008

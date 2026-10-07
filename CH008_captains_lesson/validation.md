# Validation - CH008

Metadata:

- chapterID: CH008
- sourceFilename: chapter_008_bai_hoc_cua_dai_uy.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_008_bai_hoc_cua_dai_uy.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 008 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Hoang, Mentor, Phuc, Lam. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_008 - Survival Training`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves breath discipline, stealth morality, Mentor's grief, Hoang pragmatism, and retreat lesson. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support training, radio bridge, ammo seed, Mentor backstory, armory risk, and MQ_009 unlock. |
| Are open questions clearly marked instead of silently invented? | Yes | Mentor child details, missing ammo cause, Tank timing, and Phuc payoff remain open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions. |
| characters.md | complete | Includes Trung, Hoang, Mentor, scout, smith, engineer, Phuc, doctor, Lam, Mentor child memory. |
| quests.md | complete | Includes MQ_008, objectives, optional objectives, fail states, rewards, unlocks, side hooks. |
| dialogue.md | complete | Includes gun lesson, stealth lesson, Phuc help, Mentor keepsake, armory retreat, MQ_009 unlock. |
| items.md | complete | Includes training rifle, magazine, radio parts, toy car, ammo crate, missing ammo, armory clues. |
| scenes.md | complete | Includes morning after, breathing drill, stealth house, target priority, Mentor token, armory, retreat lesson. |
| enemies.md | complete | Includes gunshot-attracted zombies, bus infected, panic fire hazard, armored infected, Tank foreshadow. |
| factions.md | complete | Includes family, Hoang, Mentor training, outpost, scout team, armory supply, radio operators, infected. |
| flags.md | complete | Includes training unlocks, radio parts, Phuc seed, Mentor backstory, Tank foreshadow, retreat, MQ009 unlock. |

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
| TODO_CH008_001 | Keep Mentor's child backstory minimal until later canon expands it. | Source only opens a small crack. |
| TODO_CH008_002 | Confirm missing ammo cause in Chapters 10-11. | Source seeds sabotage but does not resolve it. |
| TODO_CH008_003 | Confirm when Tank/armored infected becomes a full encounter. | CH008 is explicit retreat/foreshadow. |
| TODO_CH008_004 | Confirm Phuc's later payoff timing. | Source says Phuc can later save Trung, likely Chapter 11. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH008_001 | Setup tool might treat Tank as required combat. | Enemies and validation state Tank is foreshadow only and retreat is canonical success. |
| RISK_CH008_002 | Radio parts are required bridge to Chapter 009. | Use `FLAG_CH008_RADIO_FILTER_PARTS_OBTAINED` and `FLAG_CH008_MQ009_RESTORE_RADIO_UNLOCKED`. |
| RISK_CH008_003 | Missing ammo is unresolved. | Store as continuity seed, not solved side quest. |
| RISK_CH008_004 | Mentor backstory item could over-reveal. | Keep item as lore hint with restrained dialogue. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH009

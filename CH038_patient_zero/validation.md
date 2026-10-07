# Validation - CH038

Metadata:

- chapterID: CH038
- sourceFilename: chapter_038_patient_zero.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_038_patient_zero.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from metadata, scene outline, quest sections, dialogue samples, prose draft, implementation notes, and quest implementation notes. |
| Is every output line in English? | Yes | Vietnamese names preserved: Binh, Mai, Trung, Thu, Lam, Pike, Elise Moreau. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII, numbers, underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | MQ_038 - Retrieve Patient Zero Data matches source metadata. |
| Are dialogue lines faithful to the emotional intent? | Yes | Consent horror, Plague Doctor persuasion, Elise restoration, Binh validation refusal all preserved. |
| Are all items actually needed by quest, scene, or progression? | Yes | Items tied to data, ethics, memory, and route progression. |
| Are open questions clearly marked instead of silently invented? | Yes | Plague Doctor form, Elise state, Binh future need marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 files present in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | All named and referenced characters from Chapter 038. |
| quests.md | complete | Main quest, objectives, fail states, rewards, side hooks. |
| dialogue.md | complete | DT_225 through DT_233 translated to English. |
| items.md | complete | Data items, memory items, lore items, tools. |
| scenes.md | complete | All 9 scenes with locations and NPCs. |
| enemies.md | complete | Plague Doctor boss, drones, dormant infected, injectors, simulation. |
| factions.md | complete | Rebirth, Alpine Lab, Plague Doctor, Patient Zero, VALE/Architect. |
| flags.md | complete | Progression, moral, lore, choice, world state flags. |

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
| TODO_CH038_001 | Confirm Plague Doctor encounter form: recording, drone-avatar, infected-in-suit, or hybrid. | Source says "depending production." |
| TODO_CH038_002 | Confirm Elise Moreau's exact current state: dead, dormant, preserved tissue + neural record. | Source lists multiple possibilities. |
| TODO_CH038_003 | Confirm whether cure formula requires Binh biomarker at any future synthesis point. | Source says "not the cure itself" but can validate stability later. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH038_001 | Plague Doctor boss needs both ideological and mechanical systems. | Flag for boss design review. |
| RISK_CH038_002 | Cure simulation temptation UI needs careful design to not feel like standard "accept/decline." | Flag for UX review. |
| RISK_CH038_003 | Cryo ward horror must balance respect for victims with gameplay tension. | Flag for narrative design review. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH039

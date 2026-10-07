# Validation - CH006

Metadata:

- chapterID: CH006
- sourceFilename: chapter_006_nguoi_day_cach_song_sot.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_006_nguoi_day_cach_song_sot.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 006 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Hoang, Mai, Binh, Phuc. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_006 - Meet Mentor`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Mentor's hard truth, Trung's family panic, Hoang's uneasy support, and doctor triage discomfort. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items are tied to evidence, bite inspection, triage, radio clue, training, or fence rescue. |
| Are open questions clearly marked instead of silently invented? | Yes | Mentor real name, Phuc recurrence, Mai signal source, volunteer outcome, and `E` meaning remain open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, load order, summary, open questions. |
| characters.md | complete | Includes Trung, Hoang, Mentor, commander, doctor, radio operator, Phuc, refugees, hidden bite case, conditional mother. |
| quests.md | complete | Includes MQ_006, objectives, optional objectives, fail states, rewards, unlocks, side hooks. |
| dialogue.md | complete | Includes Mentor meeting, radio fragment confrontation, Hoang/Mentor exchange, doctor triage, Phuc rescue, final training line. |
| items.md | complete | Includes carryover evidence, bite tag, hidden bite clue, antibiotics, noisy Mai signal, filter parts, training items. |
| scenes.md | complete | Includes real outpost, bite check, triage, radio noise, Mentor, fence test, first order. |
| enemies.md | complete | Includes outpost approach infected, hidden bite turning, infected scout group, gate pressure infected, triage turn risk. |
| factions.md | complete | Includes real army, Mentor training, medical triage, radio operators, refugees, infected, false safe zone investigation. |
| flags.md | complete | Includes progression, relationship, faction trust, sidequest, evidence, radio, and training flags. |

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
| TODO_CH006_001 | Confirm Mentor's real name and full rank if later canon specifies it. | Source uses Mentor/Dai uy Mentor without full personal name. |
| TODO_CH006_002 | Confirm whether Phuc becomes a recurring soldier. | Source names him after rescue but does not define future role. |
| TODO_CH006_003 | Confirm exact origin/time of the Mai radio fragment in later radio chapters. | Source explicitly says it may be old, live, reflected, or noisy. |
| TODO_CH006_004 | Confirm missing volunteer outcome. | Side quest hook supports multiple outcomes. |
| TODO_CH006_005 | Keep `E` meaning unresolved. | CH006 does not explain Chapter 005's `E` mark. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH006_001 | CH006 references optional CH005 evidence. | Treat `ITM_CH005_FAKE_MILITARY_STAMP` as optional and `ITM_CH005_RIPPED_TRANSFER_LIST` as primary continuity evidence. |
| RISK_CH006_002 | Radio signal could be misread as exact live location. | Dialogue and item descriptions mark it as uncertain/noisy and point future resolution to Chapter 09. |
| RISK_CH006_003 | MentorRespect and ArmyTrust are different relationships. | Use separate factions/flags for Mentor training and army outpost trust. |
| RISK_CH006_004 | Triage choice has no clean moral answer. | Store chosen approach through moral flags; do not mark one as objectively correct. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH007

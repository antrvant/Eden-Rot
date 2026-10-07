# Validation - CH004

Metadata:

- chapterID: CH004
- sourceFilename: chapter_004_ban_than_trong_khoi_lua.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_004_ban_than_trong_khoi_lua.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 004 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Hoang, Mai, Binh. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_004 - Reunite Hoang`, matching the source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves long friendship banter, Hoang's practical loyalty, Trung's moral discomfort, and the inner-circle philosophy. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items are tied to carryover memory, degraded tracking, fake guide scam, Hoang rescue, camera puzzle, survivor choice, or route confirmation. |
| Are open questions clearly marked instead of silently invented? | Yes | Survivor identities, yellow truck faction, fake guide recurrence, and Chapter 005 checkpoint ID are marked as open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, load order, summary, open questions. |
| characters.md | complete | Includes Trung, Hoang, absent Mai/Binh, fake guides, trapped survivors, teacher group reference. |
| quests.md | complete | Includes MQ_004, objectives, optional objectives, fail states, rewards, unlocks, side hooks. |
| dialogue.md | complete | Includes Hoang rescue, fake guide confrontation, survivor debate, secret reveal, inner circle dialogue. |
| items.md | complete | Includes carryover emotional items, degraded chalk, Hoang motorbike, camera terminal, server drive, evidence items. |
| scenes.md | complete | Includes chalk smoke, fake guides, Runner fire, Hoang rescue, traffic cam, left behind, inner circle. |
| enemies.md | complete | Includes Runner, alley infected, looters, server room infected, warehouse infected, road chase infected. |
| factions.md | complete | Includes family, Hoang friendship, fake guides, looters, trapped survivors, information exploiters, infected. |
| flags.md | complete | Includes progression, moral, relationship, system, lore, sidequest, and companion flags. |

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
| TODO_CH004_001 | Confirm exact names/identities of trapped survivor group. | Source defines group members by role, not names. |
| TODO_CH004_002 | Confirm faction ownership of the yellow rescue truck. | Source uses it as a danger clue, not a named faction reveal. |
| TODO_CH004_003 | Confirm whether fake guide group returns later. | Source frames them as motif for Chapter 05 but does not guarantee recurrence. |
| TODO_CH004_004 | Confirm final `locationID` for the northern checkpoint in Chapter 005. | Chapter 004 unlocks the destination but Chapter 005 should define exact location. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH004_001 | CH004 references carryover item IDs from CH003. | Keep original CH003 IDs and mark itemType as `carryover_item` in CH004 items. |
| RISK_CH004_002 | Hoang has both positive trust and secret/suspicion flags. | Relationship parser should not collapse Hoang into one approval number. |
| RISK_CH004_003 | `FAC_CH004_INFORMATION_EXPLOITERS` is a lore seed, not a revealed faction. | Do not spawn as an active group until later canon confirms identity. |
| RISK_CH004_004 | Human hazards may be combat, stealth, or dialogue. | Use `enemyType=human_hazard` to let setup decide implementation. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH005

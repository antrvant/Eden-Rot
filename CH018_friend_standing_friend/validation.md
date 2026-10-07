# Validation - CH018

Metadata:

- chapterID: CH018
- sourceFilename: chapter_018_ban_than_ban_dung.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_018_ban_than_ban_dung.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from Chapter 018 metadata, scene outline, quest sections, dialogue tree samples, prose draft, emotional design, character notes, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved: Trung, Mai, Binh, Hoang, Ong Tu Nhieu, Ba Sau, So 4, Hanh, Lan, Phuc, Tuan. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII letters, numbers, and underscores only. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_018 - Hoang Betrayal`, matching the source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Hoang's rationalization, trader's businesslike horror, Trung's denial-breaking discovery, core betrayal lines, Mai's corrections, Binh's devastating question, and the unresolved ending. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items tied to investigation evidence, trade proof, EDEN intel, rescue clues, and emotional markers. |
| Are open questions clearly marked instead of silently invented? | Yes | Hoang's Chapter 19 status, EDEN broker identity, rescue timing, and Binh's trust duration are marked as open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes manifest, characters, quests, dialogue, items, scenes, enemies, factions, flags, and validation in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | Includes all named, referenced, and implementation-relevant characters: Trung, Hoang, Mai, Binh, Worker Lead, Doctor, Ong Tu Nhieu, Ba Sau, So 4, Hanh, bandit trader, bandit lieutenant, EDEN broker, Lan, Phuc. |
| quests.md | complete | Includes main quest with 15 objectives, 10 optional objectives across 5 side quests, 5 fail states, 8 rewards, 3 unlocks, 6 continuity flags, 5 side quest hooks. |
| dialogue.md | complete | Includes all dialogue tree samples translated to English: DT_076 (Hoang rationalizes), DT_077 (bandit trader), DT_078 (Trung confronts), DT_079 (core betrayal line), DT_080 (Binh asks), plus scene-required dialogue across all 7 scenes. |
| items.md | complete | Includes 11 items: mud sample, cloth fiber, checkpoint map copy, fuel cans, medicine bag, fort map, chalk mark, EDEN envelope, fence gap marker, shoe print, cigarette stub. |
| scenes.md | complete | Includes 7 scenes: theft investigation, Hoang walks alone, fuel trade, Trung tracks, friend-enemy confrontation, raid, aftermath. |
| enemies.md | complete | Includes 3 enemies: checkpoint guards, raid squad, bandit lieutenant. |
| factions.md | complete | Includes 7 factions: base home, refugees, children, security team, bandit network, EDEN network, Hoang fracture. |
| flags.md | complete | Includes 30 flags covering progression, world state, emotional, intel, and system states. |

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
| TODO_CH018_001 | Confirm whether Hoang accompanies rescue in Chapter 19 or is detained. | Source ends with "unresolved" status; Trung delays judgment. |
| TODO_CH018_002 | Confirm EDEN broker identity and full role in later chapters. | Source shows broker only as shadow figure at checkpoint with NODE? envelope. |
| TODO_CH018_003 | Confirm whether bandit lieutenant is a recurring enemy or defeated in Chapter 19. | Source does not specify lieutenant's fate beyond this chapter. |
| TODO_CH018_004 | Confirm Lord Duc's relationship to the bandit network. | Source mentions Lord Duc only in character list, not in scene action. |
| TODO_CH018_005 | Confirm exact mechanic for Binh's trust shake affecting future dialogue. | Source establishes emotional wound but does not specify implementation duration. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH018_001 | `FLAG_CH018_HOANG_IMMEDIATE_STATUS` is a string state (unresolved) not a boolean. | Setup tool should treat this flag as string-type, not boolean. |
| RISK_CH018_002 | Dialogue file is large with 70+ entries across 7 scenes and 5 dialogue trees. | Load dialogue by scene state to manage context. |
| RISK_CH018_003 | EDEN broker is a one-scene appearance with long-term weight. | Flag persists for later chapter connection; do not invent broker identity. |
| RISK_CH018_004 | Binh's trust wound is emotional and long-term but has no hard numeric implementation yet. | Track as persistent flag; define duration when Binh arc chapters are designed. |
| RISK_CH018_005 | Recommended canon path leaves Hoang unresolved, which may conflict with binary choice systems. | Implement Hoang status as multi-state string, not forced binary. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH019

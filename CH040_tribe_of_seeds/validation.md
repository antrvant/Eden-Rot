# Validation - CH040

Metadata:

- chapterID: CH040
- sourceFilename: chapter_040_bo_lac_cua_nhung_hat_giong.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_040_bo_lac_cua_nhung_hat_giong.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from metadata, scene outline, quest sections, dialogue samples, prose draft, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese names preserved: Binh, Mai, Trung, Thu, Lam, Ong Tu Nien, Kito, Nia, Sefu, Ama, Samir. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII, numbers, underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | MQ_040 - Earn Tribal Alliance matches source metadata. |
| Are dialogue lines faithful to the emotional intent? | Yes | Listening circle, toxic surrender, seed vault, enzyme harvest, alliance all preserved. |
| Are all items actually needed by quest, scene, or progression? | Yes | Items tied to alliance, enzyme, memory, and ethics. |
| Are open questions clearly marked instead of silently invented? | Yes | Village political structure, alliance future support, transport method marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 files present in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | All named and referenced characters from Chapter 040. |
| quests.md | complete | Main quest, objectives, fail states, rewards, side hooks. |
| dialogue.md | complete | DT_243 through DT_251 translated to English. |
| items.md | complete | Data items, memory items, knowledge items, tools. |
| scenes.md | complete | All 9 scenes with locations and NPCs. |
| enemies.md | complete | Raiders, Architect drone, distrust, extraction logic, toxic compound. |
| factions.md | complete | Rebirth, Seed Tribe, Raiders Remnant, Architect, Cairo. |
| flags.md | complete | Progression, moral, knowledge, reputation, choice flags. |

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
| TODO_CH040_001 | Confirm full political structure of seed village beyond Sefu and Ama. | Source gives two elders only. |
| TODO_CH040_002 | Confirm whether tribal alliance can support final endings if honored. | Continuity notes suggest yes; needs production confirmation. |
| TODO_CH040_003 | Confirm exact transport method for enzyme to Cairo (convoy, boat, etc.). | Source mentions both; specific method TBD. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH040_001 | Listening circle needs dialogue restraint system: no interrupt option. | Flag for dialogue system review. |
| RISK_CH040_002 | Toxic weapon surrender needs inventory removal/transform system. | Flag for inventory system review. |
| RISK_CH040_003 | Village defense needs non-toxic combat tools system. | Flag for combat system review. |
| RISK_CH040_004 | Enzyme harvest timing needs ritual/patience interaction. | Flag for interaction system review. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH041

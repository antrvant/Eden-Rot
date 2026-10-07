# Validation - CH047

Metadata:

- chapterID: CH047
- sourceFilename: chapter_047_lien_minh_tan_vo.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_047_lien_minh_tan_vo.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from metadata, scene outline, quest sections, dialogue samples, prose draft, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese names preserved: Mai, Trung, Binh, Hoang, Samir, Yusuf, Amelie, Iara, King, Ana, Mateo, Luz, Rafi, Nina, Nia. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII, numbers, underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | MQ_047 - Survive Citadel Collapse matches source metadata. |
| Are dialogue lines faithful to the emotional intent? | Yes | Custody language, Hunter shot, Binh on protection, theme line, Hunter tag, Hoang pod, Antarctica broadcast, Guardian Circle, southward all preserved. |
| Are all items actually needed by quest, scene, or progression? | Yes | Items tied to evacuation, Hunter, Hoang, Antarctica, and charter. |
| Are open questions clearly marked instead of silently invented? | Yes | Hunter status, charter signatories, Southern Ocean feasibility marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 files present in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | All named characters: Trung, Mai, Binh, Samir, Yusuf, Amelie, Iara, King, Ana, Mateo, Luz, Rafi, Nina, Hoang, Hunter, NORAD officer, Heartland soldier, merchant rep, Nia, Amazon leader. |
| quests.md | complete | Main quest MQ_047, 18 objectives, fail states, rewards, 5 side hooks. |
| dialogue.md | complete | DT_314 through DT_322 translated to English. |
| items.md | complete | 10 items: name cards, rope loop, child records, Hoang pod, Hunter marker, auxiliary power, coords, countdown broadcast, charter document, green water sample. |
| scenes.md | complete | All 12 scenes with locations and NPCs. |
| enemies.md | complete | Hunter, citadel collapse, ownership fracture, Stalker risk, faction fear. |
| factions.md | complete | Rebirth, Immune Children, NORAD, Heartland, Merchant, Tribal, Amazon Local, Architect. |
| flags.md | complete | 28 progression/moral/knowledge flags, 6 choice flags. |

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
| TODO_CH047_001 | Confirm whether Hunter is dead or only repelled. | Source says "not confirmed dead"; needs production decision. |
| TODO_CH047_002 | Determine exact number of faction reps who sign Guardian Circle Charter. | Source lists NORAD, merchant, tribal, Amazon local, Rebirth; exact count TBD. |
| TODO_CH047_003 | Define Southern Ocean route feasibility for CH048. | Source says "murder"; specific challenges TBD. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH047_001 | Hunter boss needs false muzzle flash detection system. | Flag for boss encounter system review. |
| RISK_CH047_002 | Citadel collapse needs dynamic route rotation system. | Flag for environment system review. |
| RISK_CH047_003 | Faction council needs multi-party diplomacy minigame. | Flag for dialogue system review. |
| RISK_CH047_004 | Guardian Circle needs charter signing interaction system. | Flag for governance system review. |
| RISK_CH047_005 | Hunter tracker removal needs careful interaction (heat-reading). | Flag for interaction system review. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH048

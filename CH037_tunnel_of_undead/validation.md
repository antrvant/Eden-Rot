# Validation - CH037

Metadata:

- chapterID: CH037
- sourceFilename: chapter_037_duong_ham_cua_ke_khong_chet.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_037_duong_ham_cua_ke_khong_chet.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from metadata, scene outline, quest sections, dialogue samples, prose draft, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese names preserved: Binh, Mai, Trung, Thu, Lam, Pike, June. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII, numbers, underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | MQ_037 - Reach Alpine Lab matches source metadata. |
| Are dialogue lines faithful to the emotional intent? | Yes | Binh signal consent, three-source rule, Geneva recording, cost acceptance all preserved. |
| Are all items actually needed by quest, scene, or progression? | Yes | Items tied to objectives, survival, ethics, and gate access. |
| Are open questions clearly marked instead of silently invented? | Yes | Binh signal nature, maintenance AI intent, Adrien identity marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 files present in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | All named and referenced characters from Chapter 037. |
| quests.md | complete | Main quest, objectives, fail states, rewards, side hooks. |
| dialogue.md | complete | DT_216 through DT_224 translated to English. |
| items.md | complete | Quest items, data items, tools, consumables. |
| scenes.md | complete | All 9 scenes with locations and NPCs. |
| enemies.md | complete | Dormant infected, drones, AI, avalanche, oxygen hazards. |
| factions.md | complete | Rebirth, Paris School, Geneva, Alpine Lab systems, VALE/Architect. |
| flags.md | complete | Progression, moral, choice, system rule, risk flags. |

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
| TODO_CH037_001 | Confirm exact nature of Binh signal sensitivity: viral, psychic, or Architect-related. | Source describes as non-audio; needs production decision. |
| TODO_CH037_002 | Confirm whether maintenance AI is salvageable threat or just incompetent. | Source shows contradictory behavior without clear intent. |
| TODO_CH037_003 | Confirm Adrien's role and whether he appears alive or as recording. | Metadata lists Adrien; source does not detail. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH037_001 | Binh signal sensitivity may need custom non-audio feedback system. | Mark for UX review when signal system is designed. |
| RISK_CH037_002 | Dormant infected pulse timing needs precise rhythm-based gameplay. | Flag for combat/stealth system review. |
| RISK_CH037_003 | Oxygen management may need survival system integration. | Flag for survival mechanics review. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH038

# Validation - CH046

Metadata:

- chapterID: CH046
- sourceFilename: chapter_046_loi_hua_cua_mai.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_046_loi_hua_cua_mai.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from metadata, scene outline, quest sections, dialogue samples, prose draft, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese names preserved: Mai, Trung, Binh, Ana, Mateo, Luz, Rafi, Nina, Samir, Yusuf, Amelie, Iara, King, Hoang. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII, numbers, underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | MQ_046 - Free the Children matches source metadata. |
| Are dialogue lines faithful to the emotional intent? | Yes | Mai's rule, Ana's test, Orison consent, name circle, trade rejection, Glutton reveal, Antarctica, counting names all preserved. |
| Are all items actually needed by quest, scene, or progression? | Yes | Items tied to rescue, records, Antarctica, and child trust. |
| Are open questions clearly marked instead of silently invented? | Yes | Total child count, transferred children fate, Glutton status marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 files present in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | All named characters: Mai, Trung, Binh, Samir, Yusuf, Amelie, Iara, King, Ana, Mateo, Luz, Rafi, Nina, Orison, Glutton. |
| quests.md | complete | Main quest MQ_046, 18 objectives, fail states, rewards, 5 side hooks. |
| dialogue.md | complete | DT_304 through DT_313 translated to English. |
| items.md | complete | 10 items: records, name cards, buddy line, tap pattern, crawlspace code, cold battery, terraform fragment, coordinates, breathing board, reversal agent. |
| scenes.md | complete | All 12 scenes with locations and NPCs. |
| enemies.md | complete | Glutton, feeder tendrils, Orison doctrine, future-material language, time locks, power drain. |
| factions.md | complete | Rebirth, Immune Children, Orison, Architect, Heartland. |
| flags.md | complete | 26 progression/moral/knowledge/reputation flags, 7 choice flags. |

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
| TODO_CH046_001 | Confirm total number of children in Orison custody before rescue. | Source mentions twenty-seven in trade offer; total count unclear. |
| TODO_CH046_002 | Determine fate of children transferred before rescue. | Source says some pods already moved; resolution in later chapters. |
| TODO_CH046_003 | Confirm whether Glutton is fully destroyed or only disabled. | Source says "collapsed, not exploded"; ambiguous status. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH046_001 | Name circle needs dialogue system that supports non-verbal input (tap code). | Flag for dialogue system review. |
| RISK_CH046_002 | Timed pod rescue needs countdown timer system. | Flag for timer system review. |
| RISK_CH046_003 | Glutton boss has 5 phases with environmental interactions. | Flag for boss encounter system review. |
| RISK_CH046_004 | Child escort needs panic meter and trust meter systems. | Flag for escort system review. |
| RISK_CH046_005 | Data choice (child records vs terraforming) needs binary download system. | Flag for data system review. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH047

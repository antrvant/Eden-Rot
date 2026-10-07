# Validation - CH043

Metadata:

- chapterID: CH043
- sourceFilename: chapter_043_amazon_ngap_mau_xanh.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_043_amazon_ngap_mau_xanh.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from Chapter 43 metadata, scenes, quests, dialogue, items, enemies, factions, flags, and lore. |
| Is every output line in English? | Yes | Vietnamese proper names preserved: Trung, Mai, Binh, Hoang, Samir, Yusuf, Amelie, Iara, Thu. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is MQ_043 - Navigate Flooded Jungle. |
| Are dialogue lines faithful to the emotional intent? | Yes | Dialogue preserves Blood Protocol, stop word respect, family code, Hoang confession, party split, citadel reveal. |
| Are all items actually needed by quest, scene, or progression? | Yes | Items support navigation, Stalker countermeasures, Orison archive, and citadel hook. |
| Are open questions clearly marked instead of silently invented? | Yes | Stalker stats, heat trail mechanics, reverse current physics, voice mimicry design, party split vignettes remain open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions. |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Samir, Yusuf, Amelie, Iara, Thu, Paulo, King. |
| quests.md | complete | Includes MQ_043, 18 objectives, 5 optional objectives, 5 fail states, 8 rewards, 6 unlocks, 7 continuity flags, 5 side quest hooks. |
| dialogue.md | complete | Includes Iara map correction, trees moving, Binh stop word, green water, first Stalker, Orison schoolroom, fuel/names choice, Hoang echo, family code, split, citadel edge. |
| items.md | complete | Includes Blood Protocol, mobile lab, Iara map, algae sample, child name sheets, Orison label, child drawing, family code, navigation tools, countermeasures, signal items. |
| scenes.md | complete | Includes 12 scenes from water arrival through citadel cliffhanger. |
| enemies.md | complete | Includes Stalker Pack with roles, Living Flood, Voice Mimicry, Human Opportunists, Architect Ecology. |
| factions.md | complete | Includes Rebirth (split), Stalker Pack, Orison, Architect Ecology, Human Opportunists, Iara's Community. |
| flags.md | complete | Includes chapter progression, story, system unlock, and choice flags with full metadata. |

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

| todoID | issue | currentHandling |
|---|---|---|
| TODO_CH043_001 | Stalker Pack combat stats (health/damage/learning AI parameters). | TODO: derive or approve. |
| TODO_CH043_002 | Green water heat trail mechanics (storage duration, detection radius). | TODO: derive or approve. |
| TODO_CH043_003 | Reverse current physics (pump root flow rates, anchor mechanics). | TODO: derive or approve. |
| TODO_CH043_004 | Moving canopy pathfinding (tree movement speed, route closure logic). | TODO: derive or approve. |
| TODO_CH043_005 | Voice mimicry audio design (real vs fake voice differentiation). | TODO: derive or approve. |
| TODO_CH043_006 | Family code UI (code input and verification interface). | TODO: derive or approve. |
| TODO_CH043_007 | Party split vignette design (three-group playable segments). | TODO: derive or approve. |
| TODO_CH043_008 | Amazon navigation tutorial (current/canopy/sound/heat trail systems). | TODO: derive or approve. |
| TODO_CH043_009 | Orison schoolroom level design (hidden room layout and investigation flow). | TODO: derive or approve. |
| TODO_CH043_010 | Tree-citadel visual design (wound/door opening, metal vines, Aster Node gate). | TODO: derive or approve. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH043_001 | Stalker Pack adaptive AI could be too complex for current combat system. | Treat as encounter-specific behavior scripts; learn player patterns across scenes. |
| RISK_CH043_002 | Voice mimicry may confuse players without clear real/fake differentiation. | Use family code mechanic as verification system; audio design must support distinction. |
| RISK_CH043_003 | Party split requires multi-group chapter structure not yet proven. | Use SCN_CH043_THREE_GROUPS to establish structure; each group has short playable vignettes. |
| RISK_CH043_004 | Fuel vs names choice could lock players out of Chapter 46 rescue data. | Canon path saves names; alternate path uses unknown IDs instead of real names. |
| RISK_CH043_005 | Reverse current physics could frustrate players if anchor timing is too tight. | Design fail-forward: split occurs regardless; anchor timing affects which group gets which route. |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH044
```

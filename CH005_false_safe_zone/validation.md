# Validation - CH005

Metadata:

- chapterID: CH005
- sourceFilename: chapter_005_khu_an_toan_gia.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_005_khu_an_toan_gia.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 005 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names are preserved where they are names: Trung, Hoang, Mai, Binh. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_005 - Reach Safe Zone`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves false hope, Hoang's correct suspicion, family urgency, child separation horror, and the trust wound. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items are tied to registry access, fake authority evidence, Lurker tutorial, Mai's chalk warnings, transfer records, or Chapter 006 destination. |
| Are open questions clearly marked instead of silently invented? | Yes | Manager name, separated mother recurrence, `E` meaning, and real outpost ID are open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, load order, summary, open questions. |
| characters.md | complete | Includes family, Hoang, fake management, guards, separated parent/child, retired soldier, refugees, scouts. |
| quests.md | complete | Includes MQ_005, objectives, optional objectives, fail states, rewards, unlocks, side hooks. |
| dialogue.md | complete | Includes loudspeaker, Hoang suspicion, fee dialogue, separated mother, Lurker warning, transfer list reveal, ending wound. |
| items.md | complete | Includes erased chalk, registry, fake stamp, transfer list, E mark, ring, tent lock, flare, outpost map. |
| scenes.md | complete | Includes false gate, registry, price of safety, quarantine tent, fake stamp reveal, gate collapse, after fence. |
| enemies.md | complete | Includes Lurker, quarantine infected, hidden infected, fake guards, brokers, bandit scouts, crowd hazard. |
| factions.md | complete | Includes family, Hoang, false safe zone operators, refugees, separated children/parents, real army seed, Eden seed. |
| flags.md | complete | Includes progression, moral, relationship, evidence, lore, sidequest, and enemy knowledge flags. |

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
| TODO_CH005_001 | Confirm proper name for `npc_false_safe_manager`. | Source defines role but not a personal name. |
| TODO_CH005_002 | Confirm whether `npc_separated_mother` returns later as a named side/faction quest NPC. | Source says she can return later, but does not define exact identity. |
| TODO_CH005_003 | Do not explain `E` until later canon reveals Eden/Architect meaning. | CH005 only seeds the mark. |
| TODO_CH005_004 | Confirm exact `locationID` and official name for the real army outpost in Chapter 006. | CH005 only unlocks the destination. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH005_001 | Fake safe zone can be mistaken for real army faction. | Use separate `FAC_CH005_FALSE_SAFE_ZONE_OPERATORS`; real army remains `FAC_CH005_REAL_ARMY_OUTPOST_SEED`. |
| RISK_CH005_002 | `E` mark may tempt premature lore reveal. | Store as `ITM_CH005_EDEN_E_MARK` and `FLAG_CH005_EDEN_MARK_SEEN`, but keep description unexplained. |
| RISK_CH005_003 | Lurker requires different AI than basic infected. | Mark as `infected_mutation` and include light/shadow behavior in enemies.md. |
| RISK_CH005_004 | Evidence bundle may depend on optional fake stamp pickup. | Setup should allow MQ completion with transfer list, and stronger Chapter 006 dialogue if fake stamp is also obtained. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH006

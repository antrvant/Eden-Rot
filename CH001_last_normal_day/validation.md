# Validation - CH001

Metadata:

- chapterID: CH001
- sourceFilename: chapter_001_ngay_binh_thuong_cuoi_cung.md
- validationDate: 2026-05-18
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_001_ngay_binh_thuong_cuoi_cung.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets were derived from Chapter 001 metadata, scene outline, quest sections, dialogue tree samples, prose draft, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names and place names are preserved as allowed: Trung, Mai, Binh, Hoang, Sai Gon. |
| Are all IDs stable and ASCII-only? | Yes | IDs use uppercase/lowercase ASCII letters, numbers, and underscores only. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_001 - Escape Office`, matching the source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves the missed-call wound, Mai's restrained hurt, Binh's waiting, boss hypocrisy, and rescue choice cost. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items are tied to objectives, scenes, emotional memory, tutorial interaction, or route progression. |
| Are open questions clearly marked instead of silently invented? | Yes | Boss survival, Mai's mother's exact location, and Chapter 05 coworker return are marked as open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes manifest, characters, quests, dialogue, items, scenes, enemies, factions, flags, and validation in load order. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, flags, load order, canon summary, open questions. |
| characters.md | complete | Includes all named, referenced, and implementation-relevant characters from Chapter 001. |
| quests.md | complete | Includes main quest, objectives, optional objectives, fail states, rewards, unlocks, flags, side hooks. |
| dialogue.md | complete | Includes required dialogue, dialogue tree samples translated to English, combat barks, final call. |
| items.md | complete | Includes quest items, memory items, weapons, interactables, route clues, environmental clues. |
| scenes.md | complete | Includes apartment, office, missed call, first bite, locked room, stairs, parking escape. |
| enemies.md | complete | Includes first infected, guard, sick coworker risk, bitten manager, generic infected, infected boss, parking hazard. |
| factions.md | complete | Includes family, management, workers, security, infected, Hoang friendship reference. |
| flags.md | complete | Includes progression, moral, emotional, world state, and system unlock flags. |

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
| TODO_CH001_001 | Confirm whether `ENM_CH001_INFECTED_BOSS` is killed, trapped, or escapes after the Base outdoor-parking encounter. | Source continuity notes say the Boss does not need to die permanently in Chapter 001. |
| TODO_CH001_002 | Confirm exact location ID for Mai's mother's home. | Source says Mai may take Binh there but does not provide an address or named district. |
| TODO_CH001_003 | Confirm which rescued coworker appears in Chapter 05 and under what name/status. | Source says one NPC may return in Chapter 05 if rescued but does not lock identity beyond coworker rescue logic. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH001_001 | Dialogue `choices` field contains semicolon-separated choice text that may need stricter schema later. | Keep current markdown human-readable; convert to structured JSON/YAML only when setup tool schema is finalized. |
| RISK_CH001_002 | Some flags are numeric moral increments but stored with default `0` in the same table as booleans. | Setup tool should treat `type=moral`, `type=reputation`, and `type=personality` as counters. |
| RISK_CH001_003 | `npc_coworker_02` can be an NPC or hazard depending on implementation. | Character and enemy files both mark this as variable/unstable rather than forcing a single outcome. |
| RISK_CH001_004 | Folder slug uses English `CH001_last_normal_day`, while older README example also shows Vietnamese slug. | Chosen to follow workflow rule: `CH###_english_slug` and Output Language: English. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH002

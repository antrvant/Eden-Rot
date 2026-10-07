# Validation - CH013

Metadata:

- chapterID: CH013
- sourceFilename: chapter_013_dua_tre_khong_khoc.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_013_dua_tre_khong_khoc.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/README.md`
- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from CH013 metadata, scene outline, quest sections, dialogue tree samples, prose draft, character notes, emotional design, moral motifs, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved as names: Trung, Mai, Binh, Hoang, Ong Tu Nieu, Lan, Thao. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. All prefixed with CH013. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is MQ_013 - Rescue Binh, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Binh's silence, Mai's restraint, Trung's guilt, Hoang's distance, Ong Tu Nieu's ambiguity, Factory Boss's rationalization. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support quest progression (floor plan, keys, ledger), emotional continuity (teddy bear, fabric), investigation (drawings, marks), and lore (Eden Node note). |
| Are open questions clearly marked instead of silently invented? | Yes | Eden Node network scope, Binh immunity type, Factory Boss fate, yellow jacket network, Binh trust timeline, and Edenrot/Eden bridge remain open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations (10), previous flags, flags set (15+), summary, open questions (6). |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Ong Tu Nieu, Factory Boss, Worker Lead, Lan, Guard Thao, Guard Soft (TODO), children group, forced workers, yellow jacket courier. |
| quests.md | complete | Includes MQ_013 (13 objectives), 5 optional objectives, 4 fail states, 10 rewards, 5 unlocks, 6 continuity flags, 5 side quest hooks. |
| dialogue.md | complete | Includes perimeter (DT_046), cafeteria (DT_047), worker floor, child ledger, children's room, medical reunion (DT_048), Factory Boss (DT_049), cold storage counting, loading yard choice, outside fence (DT_050, DT_051), Eden Node lore. |
| items.md | complete | Includes floor plan, Binh's marks, guard drawing, child ledger, false trail, teddy bear, fabric, Eden Node note, bandaged arm, guard keys, rice parcels, factory stamp, chalk marks. |
| scenes.md | complete | Includes 10 scenes: perimeter, cafeteria, worker floor, child ledger, children's room, medical room, Factory Boss, cold storage, loading yard, outside fence. |
| enemies.md | complete | Includes gate guards, factory guards, guard patrol, medical guard, boss guards, chained infected, Spitter foreshadow, returning guards, Factory Boss (social_hazard). |
| factions.md | complete | Includes Trung family, Hoang friendship, Factory Network, Yellow Jacket Network, factory workers, factory guards, detained children, Ong Tu Nieu redemption, EDEN lore bridge. |
| flags.md | complete | Includes 33 flags covering progression, investigation, choice, moral, emotional, relationship, lore, world_state, sidequest, and system types. |
| validation.md | complete | This file. |

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
| TODO_CH013_001 | Confirm exact previous flags from CH012 package when available. | CH012 package not yet generated; used reasonable assumptions. |
| TODO_CH013_002 | Confirm if npc_guard_soft is the same character as npc_guard_thao or a separate NPC. | Source metadata lists both; prose only names Thao. |
| TODO_CH013_003 | Confirm Factory Boss faction ID for connection to larger EDEN infrastructure. | Source says he connects to EDEN but faction hierarchy not yet defined. |
| TODO_CH013_004 | Confirm yellow jacket courier network scope in later chapters. | Referenced but not directly encountered in CH013. |
| TODO_CH013_005 | Confirm Binh's slow trust milestone timing across chapters 14-20. | Source says "many chapters" but specific milestones not defined. |
| TODO_CH013_006 | Confirm when Doctor interprets Silent Blood as abnormal viral dormancy. | Source says "later" but specific chapter not confirmed. |
| TODO_CH013_007 | Confirm when Spitter becomes a full boss fight. | CH013 is foreshadow only; escalation deferred. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH013_001 | Setup tool might treat Spitter as required combat enemy. | Enemies and validation state Spitter is foreshadow only; canonical outcome is escape. |
| RISK_CH013_002 | Factory Boss might be treated as combat boss. | Enemies list him as social_hazard; no combat abilities defined. |
| RISK_CH013_003 | Binh trauma state might be ignored in subsequent chapters. | FLAG_CH013_BINH_TRAUMA_STATE = silent_fear must persist; source says slow trust milestones. |
| RISK_CH013_004 | Child ledger might be treated as simple quest item instead of lore/evidence chain. | Items and flags track ledger as evidence_item with long-term consequence. |
| RISK_CH013_005 | Ong Tu Nieu might be accepted too easily by all survivors. | Factions note some workers may blame him; redemption arc is slow. |
| RISK_CH013_006 | Eden Node note might over-reveal EDEN infrastructure. | Keep as first bridge only; Doctor interprets later. |
| RISK_CH013_007 | Hoang's emotional distance might be missed. | FLAG_CH013_HOANG_OUTSIDE_FAMILY_SEED and DT_050 dialogue preserve this thread. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH014

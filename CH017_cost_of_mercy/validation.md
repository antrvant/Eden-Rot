# Validation - CH017

Metadata:

- chapterID: CH017
- sourceFilename: chapter_017_cai_gia_cua_long_thuong.md
- validationDate: 2026-05-29
- validator: AI
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_017_cai_gia_cua_long_thuong.md`

Referenced workflow:

- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | All assets derived from CH017 metadata, scene outline, quest sections, dialogue tree samples (DT_070-DT_075), prose draft, emotional design, moral choice matrix, character notes, cast state, structural role, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved as names: Trung, Mai, Binh, Hoang, Ong Tu Nieu, Ba Sau, So 4, Lan, Phuc, Hanh, Nha. |
| Are all IDs stable and ASCII-only? | Yes | All IDs use ASCII letters, numbers, and underscores. No diacritics in IDs. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_017 - Save or Secure`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves: council split, Ba Sau meeting, So 4 naming, bridge hold debate, Binh's smaller porridge, Hoang's core line, theft investigation. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support rescue mission, triage choices, clue gathering, theft investigation, and emotional continuity. |
| Are open questions clearly marked instead of silently invented? | Yes | Theft perpetrator, Ba Sau future, Hoang's checkpoint use, So 4 development, Edenrot rumor escalation, injured father survival, and Cult whisperer role are marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 required files present in manifest load order with source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions, continuity resolution, carryover evidence. |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Doctor, Worker Lead, Ong Tu Nieu, Ba Sau, So 4, Injured Father, Refugee Children, Hanh, Lan, Phuc, Bandit Spotter, Cult Whisperer. |
| quests.md | complete | Includes MQ_017 with 14 objectives, 19 optional objectives, 5 fail states, 11 rewards, 5 unlocks, 16 continuity flags, 7 side quest hooks. |
| dialogue.md | complete | Includes all DT_070 through DT_075 dialogue trees plus additional scene dialogue for distress signal, council, convoy, bridge, porridge, and theft scenes. |
| items.md | complete | Includes radio signal, medical supplies, fuel cans, bandit markers, So 4 tag, stuffed toy, porridge, stolen supplies, checkpoint symbol, mud trace. |
| scenes.md | complete | Includes all 8 scenes: Distress Signal, Council Split, Stuck Convoy, Medicine or Fuel, Nameless Child, Bridge Retreat, Thinner Porridge, Night Theft. |
| enemies.md | complete | Includes canal infected, rushed horde, bandit spotter, hunger systemic, supply theft, resentment systemic, bandit network. |
| factions.md | complete | Includes Trung family, base community, refugees, Hoang pragmatists, worker faction, children's group, bandit network, EDEN network, Cult network. |
| flags.md | complete | Includes 25 flags covering progression, relationship, world_state, lore, choice, threat, system, emotional, and moral types. |
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
| TODO_CH017_001 | Confirm who stole the supplies from inside the base. | Source deliberately leaves this unresolved; Chapter 18 investigation. |
| TODO_CH017_002 | Confirm Ba Sau's long-term role if she survived. | Conditional on survival flag; potential elder/refugee representative. |
| TODO_CH017_003 | Confirm what Hoang does with the bandit checkpoint lead. | Seeds Chapter 18 betrayal; he copies the location but action is deferred. |
| TODO_CH017_004 | Track So 4 development as Binh's mirror in future classroom scenes. | Source establishes mirror; future chapters must develop. |
| TODO_CH017_005 | Confirm whether Edenrot rumor attracts Cult or EDEN agents to base. | Flag set; future chapters will escalate. |
| TODO_CH017_006 | Confirm injured father survival based on medicine/fuel choice. | Doctor warns infection risk; outcome deferred to Chapter 18. |
| TODO_CH017_007 | Confirm Cult whisperer identity and direct confrontation timing. | Source mentions Cult watching; not directly confronted in this chapter. |
| TODO_CH017_008 | Confirm exact refugee count saved (variable in source). | Source uses variable; needs gameplay decision tracking. |
| TODO_CH017_009 | Confirm whether bridge burning creates permanent route loss. | Source has bridge burned; long-term routing impact open. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH017_001 | Setup tool might treat bandit spotter as combat encounter. | Enemies and validation state spotter is non-combat; noise lure and escape only. |
| RISK_CH017_002 | So 4 might be treated as a temporary NPC with no persistence. | Flag and character entries mark So 4 as persistent; joins classroom 3B. |
| RISK_CH017_003 | Hoang's checkpoint copy might be missed as a story-critical item. | Flag, item, and scene all reference it; Hoang pockets paper in Scene 8. |
| RISK_CH017_004 | Supply theft might be resolved too early. | Investigation starts in CH017 but resolution deferred to CH018. |
| RISK_CH017_005 | Edenrot quarantine might be treated as dehumanizing containment. | Source explicitly warns against this; humane language required. |
| RISK_CH017_006 | Hunger and resentment are systemic enemies, not encounter-based. | Do not spawn as combat; manifest through resource meters and dialogue tension. |
| RISK_CH017_007 | Binh's porridge sharing might be coded as mandatory rather than player-influenced. | Source says Mai corrects shame-based sharing; Binh chooses freely. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH018

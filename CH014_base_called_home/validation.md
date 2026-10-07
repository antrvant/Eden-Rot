# Validation - CH014

Metadata:

- chapterID: CH014
- sourceFilename: chapter_014_can_cu_mang_ten_nha.md
- validationDate: 2026-05-29
- validator: AI
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_014_can_cu_mang_ten_nha.md`

Referenced workflow:

- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | All assets derived from CH014 metadata, scene outline, quest sections, dialogue tree samples (DT_052-DT_057), prose draft, emotional design, moral motifs, character notes, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved as names: Trung, Mai, Binh, Hoang, Ong Tu Nieu, Lan, Nha. |
| Are all IDs stable and ASCII-only? | Yes | All IDs use ASCII letters, numbers, and underscores. No diacritics in IDs. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_014 - Build First Base`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves: Binh hiding under truck, fence-vs-sleep debate, Ong Tu Nieu kitchen shame, classroom name rules, admission pragmatism vs fairness, EDEN trade rejection. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support water system, fence construction, child clues, EDEN evidence, medical treatment, and emotional continuity. |
| Are open questions clearly marked instead of silently invented? | Yes | EDEN offer follow-up, Ong Tu Nieu trust arc, Hoang escalation, scout network scope, and Binh exploitation risk are marked open. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | All 10 required files present in manifest load order with source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions, continuity resolution, carryover evidence. |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Ong Tu Nieu, Worker Lead, Lan, Doctor, rescued children, wounded workers, silent villagers, yellow jacket scout. |
| quests.md | complete | Includes MQ_014 with 13 objectives, 7 optional objectives, 5 fail states, 11 rewards, 8 unlocks, 15 continuity flags, 5 side quest hooks. |
| dialogue.md | complete | Includes all DT_052 through DT_057 dialogue trees plus additional scene dialogue for kitchen, classroom, admission, and package scenes. |
| items.md | complete | Includes pump belt, filter cloth, scrap metal, Binh's drawings, EDEN package contents, EDENROT notice, factory notebook, stuffed bear, chalk, blackboard text. |
| scenes.md | complete | Includes all 9 scenes: Cannot Go On, The School, Fence or Beds, Muddy Well, Coward's Kitchen, Classroom Without Blackboard, Admission List, First Fence, Gate Package. |
| enemies.md | complete | Includes school infected, brick yard pack, yellow jacket scout, hunger systemic, fear systemic, contaminated water. |
| factions.md | complete | Includes Trung family, survivor community, children's group, Hoang pragmatists, EDEN network, Ong Tu Nieu redemption. |
| flags.md | complete | Includes 27 flags covering progression, system, world_state, lore, moral, emotional, relationship, sidequest, and choice types. |
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
| TODO_CH014_001 | Confirm Chapter 15 stress-test details for the new base. | Source says CH015 should test sickness, outsider admission, or night raid. |
| TODO_CH014_002 | Confirm when Ong Tu Nieu earns full kitchen trust. | Source gives conditional role; future chapters must develop. |
| TODO_CH014_003 | Confirm how Hoang's tension escalates after the trade offer. | Perimeter captain role gives leverage; escalation path open. |
| TODO_CH014_004 | Confirm yellow jacket scout network size and capabilities. | Source implies one scout; network extent undefined. |
| TODO_CH014_005 | Track whether Binh's drawing ability becomes exploitative. | Source warns adults must not exploit this; monitor in future chapters. |
| TODO_CH014_006 | Confirm which survivor types approach the base for admission in CH015+. | Source mentions bitten parent with child, thief with medicine, scout pretending to be refugee. |
| TODO_CH014_007 | Confirm water purification timeline and disease event trigger. | SQ_Base_01 says disease in CH015 if mishandled. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH014_001 | Setup tool might treat yellow jacket scout as combat encounter. | Enemies and validation state scout is non-combat; package delivery only. |
| RISK_CH014_002 | Ong Tu Nieu kitchen flag might be treated as permanent unlock. | Flag is conditional; requires shared-key supervision and future chapter validation. |
| RISK_CH014_003 | Binh's drawing clues might be over-valued as guaranteed intel. | Source warns drawings are child observations, not tactical certainty; adults must verify. |
| RISK_CH014_004 | EDEN trade offer might be resolved too early. | The offer is received and rejected in CH014, but the threat persists into CH015+. |
| RISK_CH014_005 | Admission rules might be treated as final. | Rules are a draft; future chapters will create dilemmas that test them. |
| RISK_CH014_006 | Hunger and fear are systemic enemies, not encounter-based. | Do not spawn as combat; manifest through resource meters and dialogue tension. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH015

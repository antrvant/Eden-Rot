# Validation - CH016

Metadata:

- chapterID: CH016
- sourceFilename: chapter_016_mien_dich.md
- validationDate: 2026-05-29
- validator: Codex
- language: English

## Source Chapter Checked

Checked source:

- `.agent/production/chapters/chapter_016_mien_dich.md`

Referenced workflow:

- `.agent/production/StorylineData/chapter_data_workflow.md`
- `.agent/production/StorylineData/AI_CHAPTER_RESOURCE_GENERATION_GUIDE.md`
- `.agent/production/StorylineData/chapters/CH015_council_of_survivors/` (format reference)

## Canon Coverage Checklist

| question | answer | notes |
|---|---|---|
| Did every generated asset come from the source chapter? | Yes | Assets derived from Chapter 16 metadata, scene outline, quest sections, dialogue tree samples, prose draft, emotional design, character notes, Cure Ethics protocol, scientific lore, continuity notes, and implementation notes. |
| Is every output line in English? | Yes | Vietnamese proper names preserved where they are names: Trung, Mai, Binh, Hoang, Ong Tu Nhieu, Lan, Hanh, Phuc. Vietnamese consent note "Con noi co" preserved as in-world artifact text. |
| Are all IDs stable and ASCII-only? | Yes | IDs use ASCII letters, numbers, and underscores. All prefixed with CH016. |
| Does the main quest match the chapter's canonical main quest? | Yes | Main quest is `MQ_016 - Test Immunity`, matching source metadata. |
| Are dialogue lines faithful to the emotional intent of the chapter? | Yes | Dialogue preserves Binh's fear of not being normal, Trung's struggle between protection and control, Mai's structured compassion and language guard, Doctor's ethical fear, Hoang's pragmatic honesty, and the Cult's religious framing. |
| Are all items actually needed by quest, scene, memory, or progression logic? | Yes | Items support blood draw, lab setup, Cult documentation, consent protocol, and emotional continuity. |
| Are open questions clearly marked instead of silently invented? | Yes | Eight open questions listed in chapter_manifest.md covering immunity variants, transmission, repeated exposure, programmed key, other immune children, Cult arrival timing, Cure Ethics future, and clinic revisiting. |
| Can this chapter folder be loaded independently by a setup tool? | Yes | Folder includes all required files in manifest load order and references source filename in metadata. |

## Generated File Coverage

| file | status | coverageNotes |
|---|---|---|
| chapter_manifest.md | complete | Includes source, title, locations, previous flags, flags set, summary, open questions. |
| characters.md | complete | Includes Trung, Mai, Binh, Hoang, Doctor, Ong Tu Nhieu, Worker Lead, Radio Operator, Lan, Hanh, Cult Scout, Base Survivors. 12 characters. |
| quests.md | complete | Includes MQ_016, 14 objectives, 14 optional objectives, 5 fail states, 11 rewards, 7 unlocks, 12 continuity flags, 7 side quest hooks. |
| dialogue.md | complete | Includes Doctor proposal, Binh normal question, blood rules, Binh stop moment, dormancy result, Cult rumor, Mai language correction, Doctor fear, Binh Eden question, Binh Lan request, Hoang security, label reclamation, Ong sugar water, Worker ethics, Hanh Cult intel. 52 dialogue entries. |
| items.md | complete | Includes blood sample, microscope, needles, vials, alcohol, generator, slides, viral swab, Cult symbols, consent doc, logbook, Hoa nameplate, sugar water, chalk drawings, scout map. 16 items. |
| scenes.md | complete | Includes Doctor proposal, clinic scavenge, explain Binh, Cure Ethics, blood draw, dormancy result, Cult rumor. 7 scenes. |
| enemies.md | complete | Includes ethics pressure, Cult rumor network, infected nurse, infected patient, internal fear, strategic pressure, needle fear, language rot. 8 enemies. All social/environmental/infected hazards. |
| factions.md | complete | Includes Family Core, Security, Workers, Medical, Children, Food Advisors, Base Survivors, EDEN Network, EDEN Scout, Cult of Evolution. 10 factions. |
| flags.md | complete | Includes 30 flags covering Cure Ethics, consent protocol, Binh stop/respect, dormancy discovery, enemy label rejection, Cult threat, language correction, and all supporting state flags. |
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
| In-world Vietnamese artifact text preserved (e.g., "Con noi co") | pass |

## Missing Data / TODOs

| todoID | detail | reason |
|---|---|---|
| TODO_CH016_001 | Confirm whether Binh is immune to all Eden Strain variants. | Source says Doctor does not know yet; dormancy may not apply to all variants. |
| TODO_CH016_002 | Confirm whether Binh can transmit dormancy effect via blood transfusion. | Source says Doctor flags this as dangerous unknown. |
| TODO_CH016_003 | Confirm whether repeated Eden exposure changes Binh over time. | Source leaves unanswered; seed for future tension. |
| TODO_CH016_004 | Confirm whether Eden Strain is reacting to Binh or recognizing a programmed key. | Doctor raises this as fear; EDEN language pushes toward "Eden Node." |
| TODO_CH016_005 | Confirm whether other immune children exist. | Source leaves unanswered; Cult behavior suggests they may believe so. |
| TODO_CH016_006 | Confirm when Cult of Evolution physically arrives at base. | Radio rumor heard; symbol found; approaching base. Chapter 17+ timing TBD. |
| TODO_CH016_007 | Confirm long-term role of Cure Ethics protocol. | Source says breaking it should be a major moral failure branch. |
| TODO_CH016_008 | Confirm if abandoned medical station becomes recurring scavenge location. | Supplies partially recovered; may return for more. |
| TODO_CH016_009 | Confirm infected nurse Hoa's narrative beyond nameplate. | Doctor takes nameplate; source does not specify further use. |
| TODO_CH016_010 | Confirm exact previous flags from CH015. | CH015 package exists; flags cross-referenced but may need final alignment. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH016_001 | Setup tool might treat this as a combat chapter. | Enemies and validation state most threats are ethical, social, and linguistic. Only clinic scavenge has infected combat. |
| RISK_CH016_002 | Dormancy result could be read as "Binh is the cure." | Character notes and dialogue explicitly correct this: "Binh's blood" not "Binh is blood"; dormancy is not immunity. |
| RISK_CH016_003 | Hoang could be written as villain. | Character notes say he is pragmatic and honest but lacking softness; dissent is recorded, not punished. |
| RISK_CH016_004 | Cult could be written as generic evil cult. | Source says they interpret dormancy as sacred sign; their language contrasts with EDEN's clinical language. Both erase the child in different ways. |
| RISK_CH016_005 | Binh's consent could be treated as one-time yes/no. | Source explicitly says consent is a process: think, ask Lan, stop, restart, choose. Scene 5 shows stop-and-resume. |
| RISK_CH016_006 | Doctor could be written as mad scientist. | Source says he is the person most afraid of doing this wrong; he fears becoming a softer Factory Boss. |
| RISK_CH016_007 | Language rot could be treated as mere word policing. | Source says the language around results can corrupt humans faster than the virus; Cure Ethics is the defense. |
| RISK_CH016_008 | Previous flags from CH015 are cross-referenced but may need final alignment. | Marked as TODO; CH015 package should be verified. |

## Approval Status

- packageStatus: ready_for_review
- nextAction: wait_for_user_review_before_processing_CH017

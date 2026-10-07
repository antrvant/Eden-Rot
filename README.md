# StorylineData Pipeline - Chapter-Based English Game Data

Status: Proposed workflow, awaiting approval before data generation
Last Updated: 2026-05-18
Default Game Language: English
Canon Source: ../chapters/chapter_001_*.md through ../chapters/chapter_050_*.md

## Purpose

This folder will store implementation-facing storyline data for the game setup tool. From this point forward, StorylineData must be generated only from the 50 completed chapter packets in `../chapters/`, from `chapter_001_*` through `chapter_050_*`.

The 50 chapter files remain the only creative canon for this pipeline. StorylineData is the English, tool-friendly extraction layer.

## Non-Negotiable Rules

1. Source of truth: every character, quest, dialogue line, item, scene, enemy, faction, and flag must be derived from exactly one of the 50 completed chapter files in `../chapters/`.
2. Output language: all generated StorylineData content must be written in English because the game's default language is English.
3. Work order: process exactly one chapter per pass. A pass must create the complete resource package for that single chapter before any next chapter is touched.
4. Organization: every generated asset must live under its own chapter folder, grouped by chapter, so later tools can load, validate, or regenerate one chapter without touching others.
5. Traceability: every generated file must include the source chapter filename and chapter ID in its metadata.
6. No silent invention: if a needed character, item, quest, or line is not supported by the chapter, mark it as `TODO_DERIVE_OR_APPROVE` instead of inventing canon.
7. Existing full-table files in this folder are not canon for the new pipeline; they are format references only until replaced by chapter-based English packages.

## Proposed Folder Structure

```text
StorylineData/
  README.md
  chapter_data_workflow.md
  _schemas/
    character_schema.md
    quest_schema.md
    dialogue_schema.md
    item_schema.md
    scene_schema.md
    faction_schema.md
  chapters/
    CH001_ngay_binh_thuong_cuoi_cung/
      chapter_manifest.md
      characters.md
      quests.md
      dialogue.md
      items.md
      scenes.md
      enemies.md
      factions.md
      flags.md
      validation.md
    CH002_thanh_pho_khong_con_den_do/
      ...same structure...
```

Do not create the per-chapter data folders until the user approves this workflow.

## 50-Chapter Canon Boundary

The valid source set is exactly the completed chapter range below:

- Start: `../chapters/chapter_001_ngay_binh_thuong_cuoi_cung.md`
- End: `../chapters/chapter_050_rebirth_warrior.md`

No StorylineData asset should be generated from root production summaries, older data tables, implementation plans, or memory. Those files may help understand format, but they cannot create canon content.

## One-Chapter Complete Resource Workflow

For each chapter, create the complete resource package in this order:

1. Read only the target source chapter, for example `../chapters/chapter_001_ngay_binh_thuong_cuoi_cung.md`.
2. Identify the canonical chapter metadata: chapter ID, title, act, location, POV, main quest, characters, enemies, emotional beat, lore reveal, and ending hook.
3. Extract characters that appear or are referenced with implementation value.
4. Extract the main quest and any side quest hooks explicitly supported by the chapter.
5. Extract required dialogue beats and convert them into English dialogue states.
6. Extract items, quest items, resources, evidence objects, weapons, medicine, documents, keys, logs, and environmental interactables.
7. Extract scenes and setpieces from the scene outline and prose draft.
8. Extract factions, reputation changes, enemies, bosses, and system unlocks if present.
9. Write the chapter folder files in English.
10. Run a validation pass against the source chapter and write `validation.md`.
11. Stop. Wait for review or instruction before moving to the next chapter. Do not start another chapter in the same pass.

## Required Files Per Chapter

### chapter_manifest.md
High-level metadata and load order for this chapter package.

Required sections:

- Source Chapter
- English Chapter Title
- Act
- Main Quest ID
- Location IDs
- Required Previous Flags
- Flags Set By This Chapter
- Generated Files
- Open Questions

### characters.md
Characters introduced, used, changed, recruited, killed, or referenced by the chapter.

Required columns:

| characterID | displayName | role | type | factionID | firstSeenInChapter | statusAtEnd | sourceEvidence |

### quests.md
Main quest and supported side/companion hooks for the chapter.

Required sections:

- Main Quest
- Objectives
- Optional Objectives
- Fail States
- Rewards
- Unlocks
- Continuity Flags
- Side Quest Hooks

### dialogue.md
English dialogue states derived from required dialogue beats and key prose scenes.

Required columns:

| dialogueID | speakerID | stateID | text | choices | action | condition | sourceBeat |

### items.md
Items needed for quests, scenes, crafting, evidence, memory, or progression.

Required columns:

| itemID | itemName | itemType | chapterUse | relatedQuestID | canPersist | description | sourceEvidence |

### scenes.md
Playable scenes, cutscene beats, setpieces, and environmental storytelling.

Required columns:

| sceneID | sceneName | locationID | purpose | entryState | exitState | requiredNPCs | enemies | interactables | sourceScene |

### enemies.md
Enemy types, bosses, hazards, and special infected behavior introduced or required in this chapter.

Required columns:

| enemyID | enemyName | enemyType | variant | roleInChapter | abilities | sourceEvidence |

### factions.md
Faction presence and reputation changes for this chapter.

Required columns:

| factionID | factionName | roleInChapter | relationshipChange | reason | sourceEvidence |

### flags.md
State flags used by quests, dialogue, scenes, endings, and later chapters.

Required columns:

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |

### validation.md
A human-readable QA report for the chapter extraction.

Required sections:

- Source Chapter Checked
- Canon Coverage Checklist
- English Output Checklist
- Missing Data / TODOs
- Potential Tooling Risks
- Approval Status

## ID Naming Rules

Use stable English IDs. Do not use Vietnamese diacritics in IDs.

- Chapter folder: `CH001_slug`
- Quest: `MQ_001`, `SQ_001_01`, `CQ_HOANG_001`
- Character: `char_trung`, `char_mai`, `char_binh`, `comp_hoang`, `npc_ch001_neighbor_01`
- Dialogue: `DLG_CH001_MAI_001`
- Item: `ITM_CH001_FAMILY_PHOTO`, `ITM_CH001_APARTMENT_KEY`
- Scene: `SCN_CH001_APARTMENT_MORNING`
- Enemy: `ENM_CH001_FIRST_INFECTED`
- Flag: `FLAG_CH001_TRUNG_PROMISE_HOME`

## English Localization Rules

- Translate meaning, not word-for-word phrasing.
- Keep Vietnamese proper names: Trung, Mai, Binh, Hoang, Sai Gon.
- Keep faction names in English unless the Vietnamese name is a proper noun.
- Dialogue should sound natural in English, short during action, longer during rest/council/family scenes.
- Preserve emotional intent from the Vietnamese chapters: family, trust, betrayal, moral cost, fragile hope.

## Existing Full-Table Data Policy

The current full-table files in this folder were created before the 50-chapter chapter-package pipeline was approved. They must not be treated as canon for new generation. They may be used only as format references until replaced by chapter-based English packages generated from `../chapters/`.

Existing full-table files include:

- characters_name_stats_full.md
- dialogue_script_full.md
- faction_system.md
- item_database.md
- quest_data_main.md
- quest_data_pq_dq.md
- quest_data_sq.md
- scene_database.md

## Approval Gate

Before generating any chapter data, the user should approve:

1. Folder structure.
2. Required files per chapter.
3. Table columns/schema level.
4. Whether existing full-table files should remain as format references or be archived after chapter-based packages are generated.



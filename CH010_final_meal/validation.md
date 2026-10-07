# Validation - CH010

Metadata:

- chapterID: CH010
- sourceFilename: chapter_010_bua_toi_cuoi_cung.md
- validationDate: 2026-05-29
- validatedBy: AI Agent

## Source Chapter Checked

- Source file: `.agent/production/chapters/chapter_010_bua_toi_cuoi_cung.md`
- Source status: Exists and fully read
- Extraction status: complete_first_pass

## Canon Coverage Checklist

| Item | Covered | Notes |
|---|---|---|
| Old Cook introduction | Yes | Scene 1 |
| Last rice package retrieval | Yes | Scene 2 |
| Broken seal discovery | Yes | Scene 2 |
| Supply count copying | Yes | Scene 2 |
| Edenrot rumor | Yes | Scene 2 |
| Unsent letters reading | Yes | Scene 3, 4 |
| Shared meal centerpiece | Yes | Scene 4 |
| Trung takes 3 portions | Yes | Scene 4 |
| Hoang gives food to Nam | Yes | Scene 4 |
| Mai's recording replay | Yes | Scene 5 |
| Mentor safe place conversation | Yes | Scene 5 |
| Mentor retreat priority | Yes | Scene 6 |
| Mentor letter/dog tag | Yes | Scene 6 |
| Night shadow near storage | Yes | Scene 7 |
| Side gate light flicker | Yes | Scene 7 |
| Screamer outside fence | Yes | Scene 7 |

## Generated File Coverage

| File | Status | Notes |
|---|---|---|
| chapter_manifest.md | Complete | All required sections present |
| characters.md | Complete | 11 characters defined |
| quests.md | Complete | MQ_010 + 5 side quests |
| dialogue.md | Complete | 35+ dialogue entries |
| items.md | Complete | 10 items defined |
| scenes.md | Complete | 7 scenes defined |
| enemies.md | Complete | 3 enemy entries |
| factions.md | Complete | 3 factions defined |
| flags.md | Complete | 30+ flags defined |
| validation.md | Complete | This file |

## English Output Checklist

| Check | Status |
|---|---|
| All dialogue in English | Yes |
| All item names in English | Yes |
| All scene names in English | Yes |
| All enemy names in English | Yes |
| All faction names in English | Yes |
| Vietnamese proper names preserved | Yes (Trung, Mai, Binh, Hoang, Nam, Phuc) |
| No Vietnamese diacritics in IDs | Yes |
| ASCII-only IDs | Yes |

## Missing Data / TODOs

| todoID | issue | currentHandling |
|---|---|---|
| TODO_CH010_001 | Spy identity | TODO_DERIVE_OR_APPROVE (Revealed in CH011) |
| TODO_CH010_002 | Mother who lost child name | TODO_DERIVE_OR_APPROVE (Track as community NPC) |
| TODO_CH010_003 | Old Cook backstory | TODO_DERIVE_OR_APPROVE (Only surface details) |
| TODO_CH010_004 | Mentor's child details | TODO_DERIVE_OR_APPROVE (Only hint via toy car) |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH010_001 | Cooking system needs resource management | Flag for gameplay system |
| RISK_CH010_002 | Shared meal needs NPC AI for eating behavior | Flag for NPC system |
| RISK_CH010_003 | Night patrol needs stealth/detection system | Flag for stealth system |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH011
```

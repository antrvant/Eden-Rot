# Validation - CH009

Metadata:

- chapterID: CH009
- sourceFilename: chapter_009_tin_hieu_cua_mai.md
- validationDate: 2026-05-29
- validatedBy: AI Agent

## Source Chapter Checked

- Source file: `.agent/production/chapters/chapter_009_tin_hieu_cua_mai.md`
- Source status: Exists and fully read
- Extraction status: complete_first_pass

## Canon Coverage Checklist

| Item | Covered | Notes |
|---|---|---|
| Radio fragment replay from CH007 | Yes | Scene 1 |
| Mission assignment by Mentor | Yes | Scene 1 |
| False safe zone frequency encounter | Yes | Scene 2 |
| Post office exploration and scavenge | Yes | Scene 3 |
| Infected postal workers | Yes | enemies.md |
| Unsent letters collection | Yes | items.md, Scene 3 |
| Antenna climb setpiece | Yes | Scene 4 |
| Mai's radio conversation | Yes | Scene 5 |
| Binh's location (industrial zone) | Yes | Scene 5 |
| Yellow coat warning | Yes | Scene 5 |
| Hoang pulling Trung from microphone | Yes | Scene 6 |
| EDEN NODE ACTIVE detection | Yes | Scene 6 |
| Horde arrival and retreat | Yes | Scene 6 |
| Recording playback at outpost | Yes | Scene 7 |
| Trung accepts waiting one night | Yes | Scene 7 |

## Generated File Coverage

| File | Status | Notes |
|---|---|---|
| chapter_manifest.md | Complete | All required sections present |
| characters.md | Complete | 10 characters defined |
| quests.md | Complete | MQ_009 + 5 side quests |
| dialogue.md | Complete | 40+ dialogue entries |
| items.md | Complete | 11 items defined |
| scenes.md | Complete | 7 scenes defined |
| enemies.md | Complete | 6 enemy entries |
| factions.md | Complete | 4 factions defined |
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
| Vietnamese proper names preserved | Yes (Trung, Mai, Binh, Hoang, Sai Gon) |
| No Vietnamese diacritics in IDs | Yes |
| ASCII-only IDs | Yes |

## Missing Data / TODOs

| todoID | issue | currentHandling |
|---|---|---|
| TODO_CH009_001 | npc_engineer full details | TODO_DERIVE_OR_APPROVE (Only mentioned as fuel provider) |
| TODO_CH009_002 | npc_scout full details | TODO_DERIVE_OR_APPROVE (Only mentioned as driver and detector) |
| TODO_CH009_003 | False broadcaster identity | TODO_DERIVE_OR_APPROVE (Marked as bandit group; no individual ID) |
| TODO_CH009_004 | Girl with Mai | TODO_DERIVE_OR_APPROVE (Unnamed; tracked for later chapters) |
| TODO_CH009_005 | Old cook helping Mai | TODO_DERIVE_OR_APPROVE (Unnamed; tracked for later chapters) |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH009_001 | Mai voice-only character may need special handling | Flag for audio/cutscene system |
| RISK_CH009_002 | EDEN NODE signal needs visual/audio design | Lore seed only; implement later |
| RISK_CH009_003 | Antenna climb setpiece needs vertical traversal system | Flag for level design |
| RISK_CH009_004 | Recording replay system needed for CH010 | Track item persistence |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH010
```

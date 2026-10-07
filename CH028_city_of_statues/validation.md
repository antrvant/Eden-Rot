# Validation - CH028

## Source Chapter Checked

- sourceFilename: chapter_028_thanh_pho_cua_nhung_buc_tuong.md
- sourcePath: ../chapters/chapter_028_thanh_pho_cua_nhung_buc_tuong.md
- extractionStatus: complete_first_pass

## Canon Coverage Checklist

| section | covered | notes |
|---|---|---|
| Act identified | Yes | Act 5 - North America: The Fallen Empire |
| Main Quest defined | Yes | MQ_028 - Negotiate Entry |
| All scenes outlined | Yes | 9 scenes |
| Characters documented | Yes | 13 characters |
| Dialogue samples | Yes | 9 dialogue trees (DT_131 to DT_139) |
| Enemies defined | Yes | 5 enemy types (all social/political) |
| Items catalogued | Yes | 17 items including key items, resources, interactables |
| Factions documented | Yes | 6 factions |
| Flags defined | Yes | 24 flags |
| Side quests | Yes | 5 side quests |
| EDENROT classification | Yes | CIVIC FILTER |

## Generated File Coverage

| file | status |
|---|---|
| chapter_manifest.md | complete |
| characters.md | complete |
| quests.md | complete |
| dialogue.md | complete |
| items.md | complete |
| scenes.md | complete |
| enemies.md | complete |
| factions.md | complete |
| flags.md | complete |

## English Output Checklist

| check | status |
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
| TODO_CH028_001 | Exact enclave population | ~5000 inside, exact TBD. |
| TODO_CH028_002 | Market item prices | Balance with game economy TBD. |
| TODO_CH028_003 | Enclave map layout | Environmental design TBD. |
| TODO_CH028_004 | Council member names beyond Ada | TBD. |
| TODO_CH028_005 | Guard patrol routes | Stealth mechanics TBD. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH028_001 | AI core might be accidentally connected to enclave network | Use `FLAG_CH028_AI_CORE_AIR_GAP` gate. |
| RISK_CH028_002 | Hoang might be handed over privately | Use `FLAG_CH028_HOANG_HEARING_UNLOCKED` to enforce public process. |
| RISK_CH028_003 | Riot might escalate to massacre | Use `FLAG_CH028_NO_GATE_MASSACRE` to track non-lethal outcome. |
| RISK_CH028_004 | Consent protocol must be enforced at gate | Use `FLAG_CH028_BINH_SCAN_REFUSED` gate. |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH029
```

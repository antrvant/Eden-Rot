# Validation - CH022

## Source Chapter Checked

- sourceFilename: chapter_022_thanh_pho_nguoi_may_chet.md
- sourcePath: ../chapters/chapter_022_thanh_pho_nguoi_may_chet.md
- extractionStatus: complete_first_pass

## Canon Coverage Checklist

| section | covered | notes |
|---|---|---|
| Tech port approach | Yes | Scene 1 establishes dead automated city with cranes still operating. |
| Biometric scan targeting Binh | Yes | Scene 2 covers camera flagging and Hoang's transparent hack. |
| Container yard hazards | Yes | Scene 3 covers forklifts, cranes, and corpse-as-cargo horror. |
| Engineer story and daycare | Yes | Scene 4 covers Chen Wei keycard, voice log, and daycare discovery. |
| Server hall decoding | Yes | Scene 5 covers Architect signal decoding and Binh data blocking. |
| Cybernetic infected encounter | Yes | Scene 6 covers first exosuit infected with joint weak points. |
| Tokyo signal | Yes | Scene 7 covers departure and Tokyo relay signal reception. |
| Hoang transparency arc | Yes | Narrates every hack step under watch. |
| Mai language guardian role | Yes | Corrects "asset" and "anomaly" language. |
| EDENROT port-array classification | Yes | Confirmed in server hall scene. |

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
| validation.md | complete |

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
| TODO_CH022_001 | Did Binh data sync before block? | Track as unknown risk; FLAG_CH022_BINH_DATA_PRIOR_SYNC_UNKNOWN. |
| TODO_CH022_002 | Aster's full role in relay chain | Named as signal authority; direct appearance in Chapter 23. |
| TODO_CH022_003 | Can cybernetic infected be freed from exosuits? | Not resolved; combat only disables joints. |
| TODO_CH022_004 | Chen Wei's daughter Lili fate | Lore only; daycare empty except names board. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH022_001 | Setup tool might treat port automation as hostile AI. | Enemies and validation state it is purposeless, not evil. |
| RISK_CH022_002 | Binh data block is recommended but not mandatory. | FLAG_CH022_BINH_DATA_OUTBOUND_BLOCKED defaults to true; prior sync unknown. |
| RISK_CH022_003 | Cybernetic infected requires joint targeting, not headshots. | Enemies and dialogue document weak points explicitly. |
| RISK_CH022_004 | Tokyo signal is required bridge to Chapter 23. | FLAG_CH022_TOKYO_RELAY_SIGNAL_RECEIVED set on departure. |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH023
```

# Validation - CH021

## Source Chapter Checked

- sourceFilename: chapter_021_dao_khong_ten.md
- sourcePath: ../chapters/chapter_021_dao_khong_ten.md
- extractionStatus: complete_first_pass

## Canon Coverage Checklist

| section | covered | notes |
|---|---|---|
| Vessel damage assessment | Yes | Scene 1 establishes bio-storm damage and parts needed. |
| Island exploration | Yes | Scene 2 covers fishing village, map clue, relay symbol, glowing tide. |
| Mobile classroom setup | Yes | Scene 3 covers Mai's classroom and Binh's chalk writing. |
| Lighthouse relay salvage | Yes | Scene 4 covers relay logs, EDENROT classification, battery retrieval. |
| Drowned infected encounter | Yes | Scene 5 covers first maritime zombie attack and swimmer foreshadow. |
| Boat naming | Yes | Scene 6 covers naming debate and Binh's "Nha Di" decision. |
| Escape and signal | Yes | Scene 7 covers escape, swimmer hull cling, port array signal. |
| Hoang trust arc | Yes | Useful but untrusted; near-apology with Binh in DT_094. |
| Me Linh thread | Yes | SQ_Island_04 seeds Lam's personal quest. |

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
| TODO_CH021_001 | Me Linh boat signal: real or relay ghost? | Track as future side quest seed. |
| TODO_CH021_002 | Full EDEN maritime relay chain scope | Relay 03 confirmed; port array and Tokyo relay follow. |
| TODO_CH021_003 | Swimmer/climber variant evolution details | Foreshadow only; boarding threat for later chapters. |
| TODO_CH021_004 | Does Hoang's technical service earn real trust? | Useful but socially untrusted arc continues. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH021_001 | Setup tool might treat swimmer variant as full combat encounter. | Enemies and validation state swimmer is foreshadow only. |
| RISK_CH021_002 | Relay logs are required bridge to Chapter 22. | Use FLAG_CH021_PORT_ARRAY_SIGNAL_RECEIVED and FLAG_CH021_MARITIME_RELAY_03_DISCOVERED. |
| RISK_CH021_003 | Boat naming is canon, not optional. | FLAG_CH021_VESSEL_NAMED is set in main quest flow. |
| RISK_CH021_004 | Hoang trust status must remain ambiguous. | FLAG_CH021_HOANG_TECHNICAL_SERVICE tracks service, not trust. |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH022
```

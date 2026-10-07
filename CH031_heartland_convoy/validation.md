# Validation - CH031

## Source Chapter Checked

- sourceFilename: chapter_031_heartland_convoy.md
- sourcePath: ../chapters/chapter_031_heartland_convoy.md
- extractionStatus: complete_first_pass

## Canon Coverage Checklist

| section | covered | notes |
|---|---|---|
| Act and chapter ID | Yes | Act 5 - North America: The Fallen Empire, CH031 |
| Main quest defined | Yes | MQ_031 - Protect Convoy |
| All scenes outlined | Yes | 9 scenes |
| Characters documented | Yes | 12 characters |
| Dialogue samples | Yes | 10 dialogue trees (DT_160 to DT_169) |
| Enemies defined | Yes | 5 enemy types |
| Items catalogued | Yes | 7 items |
| Factions documented | Yes | 5 factions |
| Flags defined | Yes | 25 flags |
| Side quests | Yes | 5 side quests |
| EDENROT classification | Yes | MIGRANT NATION TRACE |
| Hoang redemption seed | Yes | CQ_HOANG_04 |
| Hoang absence arc | Yes | Empty seat through rescue to disappearance |

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
| TODO_CH031_001 | Convoy vehicle stats | Derive vehicle health/fuel/speed values |
| TODO_CH031_002 | Drone hunter combat mechanics | Dart payload effects pending |
| TODO_CH031_003 | Truck stop layout art | Environmental design pending |
| TODO_CH031_004 | Grain elevator map | Combat encounter layout pending |
| TODO_CH031_005 | Convoy morale system values | Morale modifiers/penalties pending |
| TODO_CH031_006 | Child name token list | Specific items per child pending |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH031_001 | Hoang's false pings could be missed by player | Use FLAG_CH031_HOANG_FALSE_PINGS_DETECTED |
| RISK_CH031_002 | Name circle is core canon moment | FLAG_CH031_CHILD_NAME_CIRCLE_HELD must be enforced |
| RISK_CH031_003 | Convoy over Hoang choice must be canonical | FLAG_CH031_CONVOY_CHOSEN_OVER_HOANG enforced |
| RISK_CH031_004 | NORAD broadcast node must be recovered | FLAG_CH031_NORAD_BROADCAST_RECOVERED required for CH032 |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH032
```

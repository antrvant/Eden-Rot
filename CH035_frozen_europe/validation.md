# Validation - CH035

## Source Chapter Checked

- sourceFilename: chapter_035_chau_au_dong_bang.md
- sourcePath: ../chapters/chapter_035_chau_au_dong_bang.md
- extractionStatus: complete_first_pass

## Canon Coverage Checklist

| section | covered | notes |
|---|---|---|
| Atlantic Fleet rendezvous and trade | Yes | Scene 1 covers Moreno alliance. |
| Channel crossing and terraforming cold | Yes | Scene 2 covers unnatural cold identification. |
| UK coast landing and frozen evacuation | Yes | Scene 3 covers frozen city thesis. |
| Ice horde first encounter and rules | Yes | Scene 4 covers reanimation mechanic. |
| False relief waystation and Ingrid | Yes | Scene 5 covers social detection and rescue. |
| Night camp and emotional rest | Yes | Scene 6 covers snow question and heat kits. |
| Paris signal verification | Yes | Scene 7 covers Amelie and child-safety phrase. |
| Ice horde climax | Yes | Scene 8 covers reanimation combat. |
| Mimic voice warning | Yes | Scene 7 and 9 cover Mimic foreshadow. |
| EDENROT classification | Yes | CRYOSTATIC FRONTIER classified. |
| Doctor ethics | Yes | Scene 8 covers escape over samples. |

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
| TODO_CH035_001 | Ice horde combat stats (health/damage/reanimation timers). | TODO_DERIVE_OR_APPROVE. |
| TODO_CH035_002 | Cold exposure mechanics (hypothermia system values). | TODO_DERIVE_OR_APPROVE. |
| TODO_CH035_003 | Heat kit crafting recipe (materials and process). | TODO_DERIVE_OR_APPROVE. |
| TODO_CH035_004 | Channel crossing map layout. | TODO_DERIVE_OR_APPROVE. |
| TODO_CH035_005 | UK coast level design (frozen evacuation zone art). | TODO_DERIVE_OR_APPROVE. |
| TODO_CH035_006 | Motorway pileup encounter layout. | TODO_DERIVE_OR_APPROVE. |
| TODO_CH035_007 | Mimic behavior design for Chapter 36. | TODO_DERIVE_OR_APPROVE. |
| TODO_CH035_008 | Terraforming weather visual effects. | TODO_DERIVE_OR_APPROVE. |

## Potential Tooling Risks

| riskID | risk | mitigation |
|---|---|---|
| RISK_CH035_001 | Setup tool might treat Ice horde as normal infected. | Enemies and validation state reanimation rules; standard shooting fails. |
| RISK_CH035_002 | Mimic could be treated as full enemy this chapter. | Enemies states Mimic is foreshadow only; voice in Scene 7, Chapter 36 enemy. |
| RISK_CH035_003 | Doctor could be forced into dangerous sample delay. | Flag tracks ethics maintained; escape prioritized over samples. |

## Approval Status

```text
packageStatus: ready_for_review
nextAction: wait_for_user_review_before_processing_CH036
```

# Flags - CH050

Metadata:

- chapterID: CH050
- sourceFilename: chapter_050_rebirth_warrior.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH050_FINAL_BATTLEFIELD_STABILIZED | progression | false | Battlefield stabilized around Binh | CH050 progression | Scene 1. |
| FLAG_CH050_EDENROT_HUMAN_COVENANT_REWRITE_IDENTIFIED | lore | false | EDENROT class final answer identified | CH050 validation | Scene 9. |
| FLAG_CH050_PRIME_BINH_CONNECTION_BLOCKED | moral | false | Prime blocked from using Binh connection | CH050 humane path | Scene 1. |
| FLAG_CH050_BRIDGE_DATA_FROM_VIOLATION_REJECTED | moral | false | Bridge data from violation rejected | CH050 humane rewrite requirement | Scene 1. |
| FLAG_CH050_APEX_PREDATOR_BORN | progression | false | Apex Predator final guardian born | CH050 boss fight | Scene 2. |
| FLAG_CH050_LOCAL_ALLIANCE_VOICES_RECONNECTED | progression | false | Local alliance voices arrive under ice | CH050 alliance payoff | Scene 3. |
| FLAG_CH050_APEX_PHASE_ONE_COUNTERED | progression | false | Apex phase one patterns countered | CH050 boss fight | Scene 4. |
| FLAG_CH050_PRIME_FINAL_ARGUMENT_REJECTED | moral | false | Prime's final argument rejected | CH050 ideology | Scene 5. |
| FLAG_CH050_HOANG_FINAL_INTERVENTION_RESOLVED | relationship | false | Hoang's final intervention resolved | CH050 Hoang arc | Scene 6. |
| FLAG_CH050_FINAL_CHOICE_CONSOLE_PROTECTED | progression | false | Final choice console protected | CH050 final choice | Scene 7. |
| FLAG_CH050_ENDING_MATRIX_EVALUATED | progression | false | Ending matrix evaluated | CH050 final choice | Scene 8. |
| FLAG_CH050_HUMANE_REWRITE_PREREQUISITES_VERIFIED | moral | false | Humane rewrite prerequisites verified | CH050 final choice | Scene 8. |
| FLAG_CH050_HYBRID_REBIRTH_REWRITE_AVAILABLE | progression | false | Hybrid Rebirth Rewrite available | CH050 final choice | Scene 8. |
| FLAG_CH050_FINAL_CHOICE_SELECTED | choice | none | Final choice selected | CH050 ending branch | Scene 8. |
| FLAG_CH050_BINH_FREED_FROM_SOURCE | world_state | false | Binh freed from Source | CH050 emotional climax | Scene 10. |
| FLAG_CH050_SOURCE_RESOLVED | world_state | false | Source resolved | CH050 completion | Scene 10. |
| FLAG_CH050_EDEN_STRAIN_RESOLVED | world_state | false | Eden Strain resolved | CH050 completion | Scene 10. |
| FLAG_CH050_EDENROT_WARNING_DOCTRINE_ESTABLISHED | lore | false | Edenrot warning doctrine established | CH050 in-world term | Scene 9. |
| FLAG_CH050_FACTION_EPILOGUES_PLAYED | progression | false | Faction epilogues played | CH050 epilogue | Scene 11. |
| FLAG_CH050_FAMILY_ARC_CLOSED | relationship | false | Family arc closed | CH050 epilogue | Scene 12. |
| FLAG_CH050_MENTOR_LINE_PASSED_ON | relationship | false | Mentor line passed on to Binh | CH050 epilogue | Scene 12. |
| FLAG_CH050_ONG_TIEU_NIEU_FINAL_MEAL | relationship | false | On Gieu Nhieu final meal scene | CH050 epilogue | Scene 12. |
| FLAG_CH050_EDENROT_COMPLETED | progression | false | EDENROT story completed | CH050 completion | Scene 12. |

## Ending Flags

| flagID | type | ending | conditions |
|---|---|---|---|
| FLAG_CH050_ENDING_REBIRTH_HYBRID | ending | Rebirth/Hybrid | High compassion, alliance trust, family trust, cure ethics, Guardian Circle, Binh trust, tribal alliance, Patient Zero name, nursery partial, Hoang not abandoned |
| FLAG_CH050_ENDING_FAMILY_FIRST | ending | Family First | High family trust, low alliance trust or weak architect knowledge |
| FLAG_CH050_ENDING_IRON_REBIRTH | ending | Iron Rebirth | High pragmatism, army dominance, low Guardian/compassion |
| FLAG_CH050_ENDING_BROKEN_CURE | ending | Broken Cure | Cure ethics fail, Binh/children exploited, partial rewrite |
| FLAG_CH050_ENDING_ARCHITECT_CONTROL | ending | Architect Control | Accept reset/rewrite under Prime or low resistance |
| FLAG_CH050_ENDING_ASH | ending | Ash | Low all flags, reckless destruction, alliance collapse |

## Hybrid Rebirth Rewrite Required Flags

| flagID | source | requirement |
|---|---|---|
| FLAG_CH049_CHILD_INFRASTRUCTURE_CURE_MODEL_REJECTED | CH049 | must be true |
| FLAG_CH049_BRIDGE_DATA_NOT_USED_DURING_VIOLATION | CH049 | must be true |
| FLAG_CH049_SOURCE_DREAM_DATA_CONSENT_BOUND_CARRIED_INTO_CORE | CH049 | must be true |
| FLAG_CH049_BINH_STOP_WORD_HONORED_SOURCE | CH049 | must be true |
| FLAG_CH049_PERMANENT_BINH_BRIDGE_REFUSED | CH049 | must be true |
| FLAG_CH049_MOTHER_NURSERY_PRESERVED_PARTIAL | CH049 | must be true |
| FLAG_CH049_ELISE_WITNESS_INTEGRATED | CH049 | must be true |
| FLAG_CH048_GUARDIAN_CIRCLE_AT_SEA_ACTIVE | CH048 | must be true |
| FLAG_CH048_NO_CHILD_AS_CURRENCY_FLEET_RULE_RESTATED | CH048 | must be true |
| FLAG_CH048_SOURCE_DREAM_DATA_CONSENT_BOUND | CH048 | must be true |
| FLAG_CH047_GUARDIAN_CIRCLE_SIGNED | CH047 | must be true |

## Flag Notes

- FLAG_CH050_FINAL_CHOICE_SELECTED is player_branch: Rebirth_Hybrid, Family_First, Iron_Rebirth, Broken_Cure, Architect_Control, or Ash.
- FLAG_CH050_EDENROT_WARNING_DOCTRINE_ESTABLISHED makes "Edenrot" an in-world survivor term.
- All CH049 moral flags feed into CH050 ending matrix.
- Hybrid Rebirth Rewrite stays locked if any required flag from CH048-CH049 failed.
- FLAG_CH050_FAMILY_ARC_CLOSED and FLAG_CH050_MENTOR_LINE_PASSED_ON close the emotional arcs.
- FLAG_CH050_ONG_TIEU_NIEU_FINAL_MEAL closes the food/meal arc from early chapters.

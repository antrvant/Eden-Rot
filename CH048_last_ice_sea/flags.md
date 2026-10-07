# Flags - CH048

Metadata:

- chapterID: CH048
- sourceFilename: chapter_048_bien_bang_cuoi_cung.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH048_ACT8_STARTED | progression | false | Chapter opens | CH048-CH050 | Metadata. |
| FLAG_CH048_EDENROT_COVENANT_FLEET_STRESS_TEST_IDENTIFIED | lore | false | EDENROT class identified during fleet assembly | CH048 validation | Metadata EDENROT Class. |
| FLAG_CH048_VOLUNTARY_ALLIANCE_CALL_SENT | choice | false | Trung sends broadcast as request, not command | CH048 Scene 2, CH049 alliance support | Scene 1. |
| FLAG_CH048_COUNTDOWN_SHARED_WITHOUT_CHILD_DATA | moral | false | Broadcast includes countdown but not child data | CH048 trust checks | Scene 1. |
| FLAG_CH048_NO_CHILD_AS_CURRENCY_FLEET_RULE_RESTATED | moral | false | NoChildAsCurrency restated before fleet assembly | CH048-CH050 Guardian Circle enforcement | Scene 1. |
| FLAG_CH048_FINAL_ALLIANCE_RESPONSES_RECEIVED | progression | false | All allied frequencies answer the call | CH048 fleet assembly, CH049-CH050 alliance support | Scene 2. |
| FLAG_CH048_WORLD_IS_COMING | progression | false | Radio operator reports all frequencies answered | CH048 emotional payoff | Scene 2. |
| FLAG_CH048_GUARDIAN_CIRCLE_AT_SEA_ACTIVE | moral | false | Guardian Circle enforced in ship pod assignments | CH048-CH050 child protection | Scene 3. |
| FLAG_CH048_CHILDREN_NOT_IN_SECURE_CARGO_DECK | moral | false | Children placed in mixed pods, not cargo deck | CH048 child trust | Scene 3. |
| FLAG_CH048_PASSENGERS_NOT_CARGO_DOCTRINE_ACTIVE | moral | false | Passenger not cargo doctrine written on ship boards | CH048-CH050 fleet culture | Scene 3. |
| FLAG_CH048_MATEO_HULL_CODE_ESTABLISHED | system | false | Mateo tap code adapted for hull communication | CH048 whiteout, CH049-CH050 communication | Scene 10, SQ_048_E. |
| FLAG_CH048_HOANG_COLD_HOLD_STABLE | relationship | false | Hoang pod stable in cold hold | CH048-CH049 Hoang thread | Scene 4. |
| FLAG_CH048_FIRST_ICE_FIELD_CROSSED | progression | false | Fleet navigates first ice field | CH048 navigation | Scene 5. |
| FLAG_CH048_CHILD_FOOD_SHIP_REPAIRED | choice | false | Ship 4 carrying child food repaired before weather array | CH048 trust increase | Scene 5. |
| FLAG_CH048_SOURCE_DREAMS_DEBRIEFED_WITH_CONSENT | moral | false | Source dreams recorded with consent only | CH048-CH049 dream data handling | Scene 6. |
| FLAG_CH048_SOURCE_DREAM_DATA_CONSENT_BOUND | moral | false | Dream data classified as consent-bound testimony | CH049 Source analysis constraints | Scene 6. |
| FLAG_CH048_FLEAK_LEAK_CONTAINED | choice | false | Fleet leak contained through targeted investigation | CH048 fleet security | Scene 7. |
| FLAG_CH048_NO_COLLECTIVE_CHILD_SEARCH | moral | false | No collective search of child decks | CH048 child trust preserved | Scene 7. |
| FLAG_CH048_ICE_TRAPPED_VESSEL_RESCUED | choice | false | Saint Lark and crew rescued | CH048 alliance trust increase | Scene 8. |
| FLAG_CH048_AURORA_STATIC_SURVIVED | progression | false | Aurora static event stabilized | CH048 approach to Antarctica | Scene 9. |
| FLAG_CH048_DISTRIBUTED_TRUST_PROTOCOL_HIGH | system | false | Distributed trust protocol operational for whiteout | CH048 whiteout survival, CH049-CH050 trust system | Scene 10, SQ_048_E. |
| FLAG_CH048_COVENANT_FLEET_STRESS_TEST_PASSED_PARTIAL | moral | false | Trust works in whiteout but fleet enters isolated | CH048 validation, CH049 isolation | Scene 10. |
| FLAG_CH048_WHITEOUT_SURVIVED | progression | false | Whiteout navigation survived | CH048 approach to Antarctica | Scene 10. |
| FLAG_CH048_ANTARCTICA_ICE_SHELF_REACHED | progression | false | Fleet arrives at Antarctica ice shelf | CH048 completion, CH049 entry | Scene 11. |
| FLAG_CH048_LONG_RANGE_COMMS_LOST | world_state | false | All long-range communications severed | CH048-CH049 isolation | Scene 12. |
| FLAG_CH048_PROCEED_UNDER_ICE_MESSAGE_RECEIVED | progression | false | Internal message received: proceed under ice | CH049 entry trigger | Scene 12. |
| FLAG_CH048_CH49_TERRAFORMING_SOURCE_UNLOCKED | progression | false | Chapter 49 Terraforming Source unlocked | CH048 completion | Scene 12. |

## Side Quest Flags

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH048_RAFI_WHITEOUT_SAFE | sidequest | false | Rafi rope-loop route completed | CH048 whiteout safety | SQ_048_B. |
| FLAG_CH048_HOANG_STILL_INCLUDED | relationship | false | Hoang given honest update | CH048-CH049 Hoang thread | SQ_048_D. |

## Flag Notes

- FLAG_CH048_SOURCE_DREAM_DATA_CONSENT_BOUND must constrain CH049 Source analysis.
- FLAG_CH048_COVENANT_FLEET_STRESS_TEST_PASSED_PARTIAL means trust works but isolation under Antarctica will test again.
- FLAG_CH048_CHILDREN_NOT_IN_SECURE_CARGO_DECK and FLAG_CH048_PASSENGERS_NOT_CARGO_DOCTRINE_ACTIVE are Guardian Circle enforcement flags.
- FLAG_CH048_DISTRIBUTED_TRUST_PROTOCOL_HIGH enables whiteout survival and carries into CH049-CH050.
- FLAG_CH048_LONG_RANGE_COMMS_LOST sets isolated Source infiltration for CH049.

# Quests - CH005

Metadata:

- chapterID: CH005
- sourceFilename: chapter_005_khu_an_toan_gia.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_005 | Reach Safe Zone | main | automatic | Starts after MQ_004 when Trung and Hoang reach the northern checkpoint route | Trung and Hoang escape the false safe zone with evidence pointing to a real army outpost | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ005_001 | MQ_005 | 1 | Reach the northern checkpoint. | GoTo | LOC_CH005_FALSE_CHECKPOINT_ROAD | 1 | Main Quest objective 1. |
| OBJ_MQ005_002 | MQ_005 | 2 | Observe the fence, loudspeaker, and refugee queue. | Observe | LOC_CH005_FALSE_SAFE_GATE | 1 | Main Quest objective 2. |
| OBJ_MQ005_003 | MQ_005 | 3 | Find Mai's erased chalk mark near the gate. | Investigate | ITM_CH005_ERASED_CHALK_MARK | 1 | Main Quest objective 3. |
| OBJ_MQ005_004 | MQ_005 | 4 | Question the safe zone manager about Mai and Binh. | TalkTo | npc_false_safe_manager | 1 | Main Quest objective 4. |
| OBJ_MQ005_005 | MQ_005 | 5 | Access the entry registry. | Evidence | ITM_CH005_ENTRY_REGISTRY | 1 | Main Quest objective 5. |
| OBJ_MQ005_006 | MQ_005 | 6 | Investigate the child priority area and quarantine tent. | Investigate | LOC_CH005_QUARANTINE_TENT | 1 | Main Quest objective 6. |
| OBJ_MQ005_007 | MQ_005 | 7 | Survive the first Lurker encounter. | Survive | ENM_CH005_FIRST_LURKER | 1 | Main Quest objective 7. |
| OBJ_MQ005_008 | MQ_005 | 8 | Find the transfer records. | Evidence | ITM_CH005_RIPPED_TRANSFER_LIST | 1 | Main Quest objective 8. |
| OBJ_MQ005_009 | MQ_005 | 9 | Escape when the gate collapses. | Escape | LOC_CH005_SERVICE_GATE | 1 | Main Quest objective 9. |
| OBJ_MQ005_010 | MQ_005 | 10 | Secure the clue to the real army outpost. | DestinationUnlock | ITM_CH005_REAL_OUTPOST_MAP | 1 | Main Quest objective 10. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ005_01_001 | SQ_005_01 | View, steal, bribe for, or forge access to the entry registry. | Reveals Mai/Binh transfer clue. | SQ_Safe_01. |
| OBJ_SQ005_02_001 | SQ_005_02 | Recover the scraped wedding ring taken for a false ticket. | Compassion +1 and emotional mirror to Trung/Mai. | SQ_Safe_02. |
| OBJ_SQ005_03_001 | SQ_005_03 | Open the quarantine tent and identify who can still be saved. | Can rescue witnesses and unlock Lurker knowledge. | SQ_Safe_03. |
| OBJ_SQ005_04_001 | SQ_005_04 | Take the fake military stamp as evidence. | Evidence for Mentor/Army Outpost in Chapter 006. | SQ_Safe_04. |
| OBJ_SQ005_05_001 | SQ_005_05 | Track the child-priority vehicle route. | Seeds industrial zone/child transfer arc. | SQ_Safe_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ005_HEALTH_ZERO | MQ_005 | Trung dies to Lurker, infected, guards, crowd crush, or collapse. | Reload checkpoint. | Gameplay beats. |
| FAIL_MQ005_NO_TRANSFER_CLUE | MQ_005 | Player leaves without transfer list or outpost clue. | Main quest cannot complete; return to admin evidence search. | Main Quest objectives 8-10. |
| FAIL_SQ005_03_TENT_LOCKED | SQ_005_03 | Player refuses to open the tent or leaves too early. | Quarantine witnesses may die; Lurker knowledge delayed. | SQ_Safe_03. |
| FAIL_SQ005_05_CHILD_TRUCK_LOST | SQ_005_05 | Player fails to record child-priority vehicle clue. | Later child route clue becomes weaker. | SQ_Safe_05. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ005_FACTION_SUSPICION | MQ_005 | system_unlock | Faction Suspicion | Rewards section. |
| REW_MQ005_LURKER_KNOWLEDGE | MQ_005 | enemy_knowledge | Lurker | Rewards section. |
| REW_MQ005_TRANSFER_LIST | MQ_005 | item | ITM_CH005_RIPPED_TRANSFER_LIST | Rewards section. |
| REW_MQ005_FAKE_STAMP | MQ_005 | item | ITM_CH005_FAKE_MILITARY_STAMP | Rewards section. |
| REW_MQ005_REAL_OUTPOST | MQ_005 | destination_unlock | Real Army Outpost | Rewards section. |
| REW_MQ005_COMPASSION | MQ_005 | moral_flag | Compassion +1 if helping separated parent or tent survivors | Rewards section. |
| REW_MQ005_PRAGMATISM | MQ_005 | moral_flag | Pragmatism +1 if bribing to get information fast | Rewards section. |
| REW_MQ005_TRUST_HOANG | MQ_005 | relationship_flag | TrustHoang +1 if listening to Hoang's warning | Rewards section. |
| REW_MQ005_ANGER_CORRUPTION | MQ_005 | moral_flag | AngerAtCorruption +1 if exposing manager | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH005_CROWD_NAVIGATION | MQ_005 | Crowd navigation | Enter checkpoint queue. |
| UNLOCK_CH005_REGISTRY_APPROACHES | MQ_005 | Bribe/lie/intimidate registry approach | Registry table encounter. |
| UNLOCK_CH005_FACTION_SUSPICION | MQ_005 | Faction Suspicion concept | Notice fake safe zone evidence. |
| UNLOCK_CH005_LURKER_TUTORIAL | MQ_005 | Darkness enemy tutorial | Quarantine tent encounter. |
| UNLOCK_CH005_EVIDENCE_COLLECTION | MQ_005 | Evidence collection | Obtain fake stamp or transfer list. |
| UNLOCK_CH005_ESCAPE_SETPIECE | MQ_005 | Gate collapse escape | Safe zone riot/collapse starts. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH005_FALSE_SAFE_ZONE_EXPOSED | MQ_005 | Player discovers forged authority and transfer records. |
| FLAG_CH005_MAI_BINH_TRANSFER_LIST_FOUND | MQ_005 | Player finds Mai/Binh in transfer records. |
| FLAG_CH005_EDEN_MARK_SEEN | MQ_005 | Player sees the unexplained `E` mark beside Binh. |
| FLAG_CH005_REAL_ARMY_OUTPOST_UNLOCKED | MQ_005 | Player obtains route to real army outpost. |
| FLAG_CH005_LURKER_KNOWLEDGE_UNLOCKED | MQ_005 | Player survives or observes Lurker behavior. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_005_01 | Entry Registry | registry trigger | Access the entry/transfer registry through bribe, lie, theft, intimidation, or Hoang's forged paperwork. | Reveals Mai/Binh transfer clue. | SQ_Safe_01. |
| SQ_005_02 | Wedding Ring for a Ticket | separated spouse/parent | Recover a scraped wedding ring taken for a false safety ticket. | Compassion +1; marriage-memory mirror. | SQ_Safe_02. |
| SQ_005_03 | Quarantine Tent | cries from inside tent | Open the tent, identify survivors, and survive Lurker. | Rescued NPCs may testify about fake safe zone later. | SQ_Safe_03. |
| SQ_005_04 | Fake Military Stamp | comp_hoang | Take fake military stamp as evidence. | Unlocks dialogue with Mentor/Army Outpost in Chapter 006, but may create suspicion. | SQ_Safe_04. |
| SQ_005_05 | Children First | npc_separated_mother | Track the vehicle/path used to take separated children. | Seeds industrial zone/child transfer arc. | SQ_Safe_05. |

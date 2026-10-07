# Quests - CH012

Metadata:

- chapterID: CH012
- sourceFilename: chapter_012_nha_tho_khong_chuong.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_012 | Find Mai | main | char_trung | Starts after CH011 outpost collapse and radio fragment | Mai rejoins group and industrial zone objective unlocks | Metadata and Main Quest premise. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ012_001 | MQ_012 | 1 | Regroup survivors after outpost collapse. | PartyState | npc_doctor;npc_radio_operator | 1 | Main Quest objective 1. |
| OBJ_MQ012_002 | MQ_012 | 2 | Travel to the old church northeast. | GoTo | LOC_CH012_OLD_CHURCH | 1 | Main Quest objective 2. |
| OBJ_MQ012_003 | MQ_012 | 3 | Negotiate with Priest to enter the church. | SocialTrust | npc_priest | 1 | Main Quest objective 3. |
| OBJ_MQ012_004 | MQ_012 | 4 | Find Mai's chalk mark inside the church. | Investigate | ITM_CH012_MAI_CHALK | 1 | Main Quest objective 4. |
| OBJ_MQ012_005 | MQ_012 | 5 | Meet the girl and get her clue. | TalkTo | npc_girl | 1 | Main Quest objective 5. |
| OBJ_MQ012_006 | MQ_012 | 6 | Reunite with Mai in the prayer shelter. | Cutscene | char_mai | 1 | Main Quest objective 6. |
| OBJ_MQ012_007 | MQ_012 | 7 | Listen to Mai's testimony about Binh and the industrial zone. | Narrative | char_mai | 1 | Main Quest objective 7. |
| OBJ_MQ012_008 | MQ_012 | 8 | Cross-reference Edenrot risk map with Priest's warnings to choose exit route. | RouteChoice | LOC_CH012_EDENROT_STREET | 1 | Main Quest objective 8. |
| OBJ_MQ012_009 | MQ_012 | 9 | Investigate the watcher outside the church. | Perception | npc_yellow_coat_watcher | 1 | Main Quest objective 9. |
| OBJ_MQ012_010 | MQ_012 | 10 | Prepare to leave church for the industrial zone. | UnlockQuest | MQ_013 | 1 | Main Quest objective 10. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ012_01_001 | SQ_012_01 | Find bandages or medicine for Priest's wound. | ChurchTrust +1, access to hidden supplies. | SQ_Church_01. |
| OBJ_SQ012_02_001 | SQ_012_02 | Retrieve the girl's lost item from the churchyard. | Girl trust, unlock future companion hook. | SQ_Church_02. |
| OBJ_SQ012_03_001 | SQ_012_03 | Inspect the bell tower and decide what to do with the silent bell. | Affects escape/defense option if church is attacked. | SQ_Church_03. |
| OBJ_SQ012_04_001 | SQ_012_04 | Find all chalk pieces in the church to trace Mai's journey. | Emotional flashback snippets. | SQ_Church_04. |
| OBJ_SQ012_05_001 | SQ_012_05 | Chase, trap, or avoid the watcher outside the gate. | Clue about Bandit/Factory Boss. | SQ_Church_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ012_NEGOTIATION_FAILED | MQ_012 | Player threatens Priest or forces entry. | Priest refuses cooperation; delayed entry. | Scene 2. |
| FAIL_MQ012_WATCHER_ALERTED | MQ_012 | Watcher escapes and alerts yellow coat faction. | Reduced time to leave church. | Scene 6. |
| FAIL_MQ012_BLAME_MAI | MQ_012 | Player dialogue blames Mai for losing Binh. | FamilyTrust penalty; Mai emotional damage. | Scene 4. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ012_MAI_REUNION | MQ_012 | party_member | Mai rejoins core story party | Rewards section. |
| REW_MQ012_INDUSTRIAL_ZONE | MQ_012 | quest_unlock | Unlock Industrial Zone objective | Rewards section. |
| REW_MQ012_GIRL_HOOK | MQ_012 | companion_hook | Unlock npc_girl companion hook | Rewards section. |
| REW_MQ012_BINH_SCARF | MQ_012 | item | ITM_CH012_BINH_SCARF | Rewards section. |
| REW_MQ012_O_TU_NIEU_NOTE | MQ_012 | item | ITM_CH012_O_TU_NIEU_NOTE | Rewards section. |
| REW_MQ012_FAMILYTRUST | MQ_012 | relationship_flag | FamilyTrust +1 if Trung does not blame Mai | Rewards section. |
| REW_MQ012_HOANGRESPECT | MQ_012 | relationship_flag | HoangRespect +1 if player gives couple privacy | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH012_INDUSTRIAL_ZONE | MQ_012 | Industrial Zone objective | Mai testimony complete. |
| UNLOCK_CH012_GIRL_COMPANION | MQ_012 | Girl companion hook | Girl trust gained. |
| UNLOCK_CH012_MQ013 | MQ_012 | CH013 Rescue Binh | Church departure. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH012_MAI_REUNITED | MQ_012 | Trung and Mai reunite in basement. |
| FLAG_CH012_BINH_LOCATION_KNOWN | MQ_012 | Mai reveals Binh is in industrial zone. |
| FLAG_CH012_INDUSTRIAL_ZONE_UNLOCKED | MQ_012 | Industrial zone objective unlocks. |
| FLAG_CH012_FAMILYTRUST_PLUS | MQ_012 | Trung does not blame Mai. |
| FLAG_CH012_HOANGRESPECT_PLUS | MQ_012 | Hoang gives couple privacy. |
| FLAG_CH012_MQ_COMPLETE | MQ_012 | Group leaves church. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_012_01 | Injured Priest | npc_priest | Find bandages or medicine for Priest's wound. | ChurchTrust +1; access to hidden supplies; Priest may become ally. | SQ_Church_01. |
| SQ_012_02 | Girl Saved by Mai | npc_girl | Retrieve the girl's lost item from the churchyard. | Girl trust; unlock future companion hook. | SQ_Church_02. |
| SQ_012_03 | Silent Church Bell | npc_priest / environment | Inspect bell tower; choose to keep silent, prepare bell as zombie distraction, or take bell wire for metal. | Affects escape/defense if church is attacked. | SQ_Church_03. |
| SQ_012_04 | White Chalk and Candle | Mai's chalk trail | Find all chalk pieces in church to trace Mai's journey. | Emotional flashback snippets; Mai teacher identity reinforced. | SQ_Church_04. |
| SQ_012_05 | Watcher Outside Gate | comp_hoang | Chase, trap, or avoid the watcher. | Clue about Bandit/Factory Boss; affects escape timing. | SQ_Church_05. |

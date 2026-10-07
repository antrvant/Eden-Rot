# Quests - CH023

Metadata:

- chapterID: CH023
- sourceFilename: chapter_023_tokyo_duoi_mua_den.md
- language: English

## Main Quest

| questID | questName | questType | giver | startCondition | completionCondition | sourceEvidence |
|---|---|---|---|---|---|---|
| MQ_023 | Find Naval Codes | main | automatic | Nha Di follows Tokyo relay warning into black rain after CH022 | Naval codes and naval base coordinates obtained; Aster survived; enclave trust established | Main Quest section. |

## Objectives

| objectiveID | questID | order | objectiveText | objectiveType | targetID | requiredAmount | sourceEvidence |
|---|---|---|---|---|---|---|---|
| OBJ_MQ023_001 | MQ_023 | 1 | Approach Tokyo Bay during black rain cycle | Navigate | LOC_CH023_TOKYO_BAY | 1 | MQ_023_01. |
| OBJ_MQ023_002 | MQ_023 | 2 | Land at secondary port or metro entrance | Navigate | LOC_CH023_METRO_ENTRANCE | 1 | MQ_023_02. |
| OBJ_MQ023_003 | MQ_023 | 3 | Survive first black rain interval | Survive | LOC_CH023_TOKYO_BAY | 1 | MQ_023_03. |
| OBJ_MQ023_004 | MQ_023 | 4 | Contact enclave guards | TalkTo | LOC_CH023_METRO_ENTRANCE | 1 | MQ_023_04. |
| OBJ_MQ023_005 | MQ_023 | 5 | Choose negotiation party | Decision | LOC_CH023_METRO_ENTRANCE | 1 | MQ_023_05. |
| OBJ_MQ023_006 | MQ_023 | 6 | Negotiate without using Binh as proof or payment | Diplomacy | LOC_CH023_ENCLAVE_MEETING | 1 | MQ_023_06. |
| OBJ_MQ023_007 | MQ_023 | 7 | Meet Aiko, Kenji, and Yui | TalkTo | LOC_CH023_ENCLAVE_MEETING | 1 | MQ_023_07. |
| OBJ_MQ023_008 | MQ_023 | 8 | Assist enclave with relay access | Mission | LOC_CH023_RELAY_CHAMBER | 1 | MQ_023_08. |
| OBJ_MQ023_009 | MQ_023 | 9 | Decode naval code fragment | DataExtract | LOC_CH023_RELAY_CHAMBER | 1 | MQ_023_09. |
| OBJ_MQ023_010 | MQ_023 | 10 | Survive Aster relay event | Survive | LOC_CH023_RELAY_ROOFTOP | 1 | MQ_023_10. |
| OBJ_MQ023_011 | MQ_023 | 11 | Receive naval base coordinates | UnlockQuest | MQ_024 | 1 | MQ_023_11. |
| OBJ_MQ023_012 | MQ_023 | 12 | Return to Nha Di | Escape | LOC_CH023_DEPARTURE | 1 | MQ_023_12. |

## Optional Objectives

| objectiveID | questID | optionalText | rewardOrConsequence | sourceEvidence |
|---|---|---|---|---|
| OBJ_SQ023_01_001 | SQ_023_01 | Observe rain warning lights and find covered route | Black rain resistance and protocol | SQ_Tokyo_01. |
| OBJ_SQ023_02_001 | SQ_023_02 | Surrender weapons and choose negotiator | Enclave relationship | SQ_Tokyo_02. |
| OBJ_SQ023_03_001 | SQ_023_03 | Let children meet under supervision and exchange chalk/mask | Binh healing and Yui contact | SQ_Tokyo_03. |
| OBJ_SQ023_04_001 | SQ_023_04 | Earn Aiko's permission and access archive for code combination | Chapter 24 unlock | SQ_Tokyo_04. |
| OBJ_SQ023_05_001 | SQ_023_05 | Identify warning source and find recorded message | Enclave trust and future broadcasts | SQ_Tokyo_05. |

## Fail States

| failStateID | questID | condition | consequence | sourceEvidence |
|---|---|---|---|---|
| FAIL_MQ023_FORCE_ENTRY | MQ_023 | Force entry into enclave | Enclave hostility; naval code access harder | Fail States section. |
| FAIL_MQ023_USE_BINH_LEVERAGE | MQ_023 | Bring Binh as bargaining chip | Family Trust and Cure Ethics damage | Fail States section. |
| FAIL_MQ023_HOANG_UNSUPERVISED | MQ_023 | Let Hoang hack unsupervised | Enclave trust collapse | Fail States section. |
| FAIL_MQ023_IGNORE_RAIN_TIMING | MQ_023 | Ignore black rain timing | Contamination or injury | Fail States section. |
| FAIL_MQ023_RESPOND_WITH_BINH_DATA | MQ_023 | Respond to Aster with Binh data | Tracking worsens | Fail States section. |

## Rewards

| rewardID | questID | rewardType | value | sourceEvidence |
|---|---|---|---|---|
| REW_MQ023_NAVAL_CODES | MQ_023 | item | ITM_CH023_NAVAL_CODE_FRAGMENT | Rewards section. |
| REW_MQ023_NAVAL_BASE_COORDS | MQ_023 | item | ITM_CH023_NAVAL_BASE_COORDINATES | Rewards section. |
| REW_MQ023_ASTER_INTRODUCED | MQ_023 | lore | Architect Commander Aster first direct appearance | Rewards section. |
| REW_MQ023_BLACK_RAIN_CODEX | MQ_023 | system_unlock | Black rain hazard codex | Rewards section. |
| REW_MQ023_ENCLAVE_CONTACT | MQ_023 | relationship | Tokyo enclave contact established | Rewards section. |
| REW_MQ023_TRUST_ITEMS | MQ_023 | item | ITM_CH023_PAPER_MASK;ITM_CH023_CHALK_PIECE | Rewards section. |
| REW_MQ023_DIPLOMACY_REP | MQ_023 | relationship | Diplomacy reputation for later continents | Rewards section. |

## Unlocks

| unlockID | questID | unlockName | condition |
|---|---|---|---|
| UNLOCK_CH023_BLACK_RAIN_HAZARD | MQ_023 | Black rain hazard system | First black rain interval survived. |
| UNLOCK_CH023_DIPLOMACY_PATTERN | MQ_023 | Alliance diplomacy pattern | Mai's negotiation succeeds. |
| UNLOCK_CH023_ASTER_ANTAGONIST | MQ_023 | Aster as active antagonist | Aster relay event survived. |
| UNLOCK_CH023_MQ024_NAVAL_BASE | MQ_023 | Chapter 24 naval base mission | Naval base coordinates received. |

## Continuity Flags

| flagID | questID | setWhen |
|---|---|---|
| FLAG_CH023_TOKYO_ENCLAVE_CONTACT | MQ_023 | First contact with enclave guards. |
| FLAG_CH023_MAI_DIPLOMACY_MAJOR | MQ_023 | Mai successfully negotiates without using Binh. |
| FLAG_CH023_NAVAL_CODES_FRAGMENT_ACQUIRED | MQ_023 | Aiko gives naval codes after negotiation and relay assistance. |
| FLAG_CH023_ASTER_FIRST_CONTACT | MQ_023 | Aster appears through relay screens and rain static. |
| FLAG_CH023_ASTER_RECORDED_BINH_NAME | MQ_023 | Aster records Binh's name during relay event. |
| FLAG_CH023_FALLEN_NAVAL_BASE_UNLOCKED | MQ_023 | Naval base coordinates received from relay. |

## Side Quest Hooks

| questID | questName | giver | objectiveSummary | longTermConsequence | sourceEvidence |
|---|---|---|---|---|---|
| SQ_023_01 | Black Rain | environmental | Observe rain warnings, find covered route, collect sample | Black rain resistance and protocol | SQ_Tokyo_01. |
| SQ_023_02 | Enclave Trusts No One | npc_aiko | Surrender weapons, choose negotiator, share limited truth, respect quarantine | Enclave relationship | SQ_Tokyo_02. |
| SQ_023_03 | Child Meets Mask | npc_yui | Let children meet under supervision, exchange chalk/mask, discuss names | Binh healing and Yui contact | SQ_Tokyo_03. |
| SQ_Tokyo_04 | Naval Codes | npc_aiko | Earn permission, access archive, decode relay fragment, combine code | Chapter 24 unlock | SQ_Tokyo_04. |
| SQ_023_05 | Stranger's Warning | environmental | Identify warning source, find recorded message, decide broadcast | Enclave trust and future broadcasts | SQ_Tokyo_05. |

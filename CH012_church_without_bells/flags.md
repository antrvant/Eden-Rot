# Flags - CH012

Metadata:

- chapterID: CH012
- sourceFilename: chapter_012_nha_tho_khong_chuong.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH012_ROUTE_CHOSEN | progression | false | Trung chooses to go around Edenrot block. | Scene 1 route decision. | Scene 1. |
| FLAG_CH012_MENTOR_WOUND_TOUCHED | emotional | false | Hoang says Trung orders like Mentor; Trung is wounded. | Emotional state tracking. | Scene 1. |
| FLAG_CH012_TENSION_PLUS | relationship | 0 | Player gives aggressive answer at church gate. | Priest trust. | DT_042 Choice A. |
| FLAG_CH012_CHURCH_TRUST_GAINED | progression | false | Player negotiates peacefully with Priest. | Church entry. | DT_042 Choice B. |
| FLAG_CH012_EDENROT_STREET_KNOWN | lore | false | Player asks about Edenrot street at gate. | Route knowledge. | DT_042 Choice D. |
| FLAG_CH012_GIRL_SAVED_BY_MAI_CONFIRMED | lore | false | Girl confirms Mai saved her from yellow coats. | Mai's actions while separated. | Scene 3. |
| FLAG_CH012_GIRL_TRUST_GAINED | sidequest | false | Player answers girl's song question correctly. | Girl companion hook. | Scene 3. |
| FLAG_CH012_HOANGRESPECT_PLUS | relationship | 0 | Hoang gives couple privacy or speaks well at gate. | Hoang relationship. | DT_045, DT_042 Choice C. |
| FLAG_CH012_FAMILYTRUST_PLUS | relationship | 0 | Trung says "They took him" instead of blaming Mai. | Family relationship. | DT_043. |
| FLAG_CH012_FAMILY_HONEST | choice | false | Trung refuses Mai's choose-between question honestly. | Family dynamic. | Scene 5 Choice A. |
| FLAG_CH012_FAMILY_PROMISE | choice | false | Trung promises both. | Family dynamic. | Scene 5 Choice B. |
| FLAG_CH012_FAMILY_DEFIANCE | choice | false | Trung refuses to choose at all. | Family dynamic. | Scene 5 Choice C. |
| FLAG_CH012_MAI_REUNITED | progression | false | Trung and Mai reunite in basement. | MQ_012 core objective. | Scene 4. |
| FLAG_CH012_BINH_LOCATION_KNOWN | progression | false | Mai reveals Binh is in industrial zone. | MQ_012, CH013 unlock. | Scene 5. |
| FLAG_CH012_EDENROT_PHRASE_HEARD | lore | false | Player hears "Edenrot does not eat him." | Lore tracking. | DT_044. |
| FLAG_CH012_WATCHER_DETECTED | world_state | false | Hoang detects yellow coat watcher. | Urgency trigger. | Scene 6. |
| FLAG_CH012_WATCHER_ESCAPED | world_state | false | Watcher flees before being caught. | Reduced time at church. | Scene 6. |
| FLAG_CH012_WATCHER_CAUGHT | world_state | false | Player catches or traps watcher. | SQ_012_05 outcome. | SQ_Church_05. |
| FLAG_CH012_CHURCH_BELL_CHOICE_MADE | choice | false | Player decides fate of church bell. | SQ_012_03 outcome. | SQ_Church_03. |
| FLAG_CH012_BELL_KEPT_SILENT | choice | false | Player chooses to leave bell silenced. | SQ_012_03 Option A. | SQ_Church_03. |
| FLAG_CH012_BELL_PREPARED_DISTRACTION | choice | false | Player prepares bell as zombie distraction. | SQ_012_03 Option B. | SQ_Church_03. |
| FLAG_CH012_BELL_WIRE_TAKEN | choice | false | Player takes bell wire for metal/cordage. | SQ_012_03 Option C. | SQ_Church_03. |
| FLAG_CH012_PRIEST_WOUND_TREATED | sidequest | false | Player finds bandages for Priest. | SQ_012_01. | SQ_Church_01. |
| FLAG_CH012_GIRL_ITEM_RETURNED | sidequest | false | Player retrieves girl's lost item. | SQ_012_02. | SQ_Church_02. |
| FLAG_CH012_ALL_CHALK_FOUND | sidequest | false | Player finds all chalk pieces in church. | SQ_012_04. | SQ_Church_04. |
| FLAG_CH012_MAI_READY | progression | false | Mai says she is ready to leave for industrial zone. | Departure. | Scene 6. |
| FLAG_CH012_INDUSTRIAL_ZONE_UNLOCKED | progression | false | Industrial zone objective unlocks. | CH013 start. | Scene 7. |
| FLAG_CH012_GIRL_COMPANION_HOOK | system | false | Girl companion hook unlocks. | Future companion. | Rewards. |
| FLAG_CH012_BINH_SCARF_OBTAINED | item_state | false | Player obtains Binh's scarf. | Memory item. | Scene 7. |
| FLAG_CH012_O_TU_NIEU_NOTE_OBTAINED | item_state | false | Player obtains note from O Tu Nieu. | Clue item. | Scene 5. |
| FLAG_CH012_MQ_COMPLETE | progression | false | MQ_012 completes when group leaves church. | Chapter completion. | Main Quest completion. |

## Flag Notes

- `FLAG_CH012_FAMILYTRUST_PLUS` is the key moral flag. It is set when Trung refrains from blaming Mai. This echoes through future chapters.
- `FLAG_CH012_HOANGRESPECT_PLUS` rewards the player for allowing the emotional scene to play out without rushing.
- `FLAG_CH012_WATCHER_DETECTED` vs `FLAG_CH012_WATCHER_ESCAPED` track the urgency state; escaped watcher means less time.
- `FLAG_CH012_EDENROT_PHRASE_HEARD` seeds the phrase "Edenrot does not eat him" for future lore threads about Binh's immunity.
- The three `FLAG_CH012_FAMILY_*` choice flags are mutually exclusive based on player response to Mai's question.

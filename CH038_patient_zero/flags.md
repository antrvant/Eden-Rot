# Flags - CH038

Metadata:

- chapterID: CH038
- sourceFilename: chapter_038_patient_zero.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH038_PATIENT_ZERO_DATA_RECOVERED | progression | false | Patient Zero dataset extracted from chamber. | Cure formula; Chapter 39 setup. | MQ_038 completion. |
| FLAG_CH038_CURE_FORMULA_PARTIAL | progression | false | Formula obtained but incomplete; needs bio-enzyme. | Chapter 39 route unlock. | Scene 9. |
| FLAG_CH038_AFRICA_BIO_ENZYME_REQUIRED | progression | false | Bio-enzyme from Congo/Nigeria required. | Chapter 39 route. | Scene 9. |
| FLAG_CH038_PLAGUE_DOCTOR_INTRODUCED | lore | false | Dr. Elias Vorn lore encountered. | Lore reference. | Scene 4. |
| FLAG_CH038_PLAGUE_DOCTOR_PROTOCOL_DISABLED | progression | false | Forced cost acceptance protocol disabled. | Lab safety. | Scene 8. |
| FLAG_CH038_PATIENT_ZERO_NAME_RESTORED | moral | false | Patient Zero restored as Elise Moreau. | Ethics tracking. | DT_227; SQ_PZ_03. |
| FLAG_CH038_CONSENT_RECORDS_RECOVERED | progression | false | Ethics/consent records recovered. | Cure legitimacy. | SQ_PZ_01. |
| FLAG_CH038_THERAPEUTIC_ORIGIN_REVEALED | lore | false | Virus origin as therapeutic platform revealed. | Lore reference. | Scene 2. |
| FLAG_CH038_BINH_VALIDATION_REFUSED | moral | false | Binh biomarker validation shortcut refused. | Ethics tracking. | DT_229; SQ_PZ_05. |
| FLAG_CH038_SALVATION_COST_ENGINE_DISPUTED | moral | false | EDENROT cost engine classification challenged. | Ethics framework. | DT_233. |
| FLAG_CH038_AFRICA_BIO_JUNGLE_ROUTE_UNLOCKED | progression | false | Chapter 39 route unlocked. | Chapter transition. | Scene 9. |
| FLAG_CH038_FORCED_COST_ACCEPTANCE_DISABLED | progression | false | Forced validation protocol destroyed. | Lab safety. | Scene 8. |
| FLAG_CH038_ELISE_CHAMBER_STABILIZED | moral | false | Elise's containment stabilized, not collapsed. | Ethics tracking. | Scene 7. |
| FLAG_CH038_CONSENT_RECORDS_ONLY | choice | false | Player extracts formula only, losing ethics context. | Ethics loss. | Player Choice Pillars. |
| FLAG_CH038_RESTORE_CONSENT_TOO | choice | false | Player recovers consent records alongside formula. | Ethics gain. | Player Choice Pillars. |
| FLAG_CH038_TREAT_PZ_AS_SUBJECT | choice | false | Player treats Patient Zero as subject ID. | Trust damage. | Player Choice Pillars. |
| FLAG_CH038_DESTROY_PLAGUE_DOCTOR | choice | false | Player destroys all Plague Doctor data. | Prevents abuse but loses clues. | Player Choice Pillars. |
| FLAG_CH038_SECURE_SEAL_PLAGUE_DOCTOR | choice | false | Player secures and seals Plague Doctor data. | Balanced approach. | Player Choice Pillars. |
| FLAG_CH038_KILL_ALL_POD_INFECTED | choice | false | Player kills all cryo pod infected. | Safer route; destroys records. | Player Choice Pillars. |
| FLAG_CH038_PRESERVE_KEY_PODS | choice | false | Player preserves key pods/data. | Harder; preserves records. | Player Choice Pillars. |
| FLAG_CH038_IMPLIED_CONSENT_EXPOSED | world_state | false | Implied consent model exposed. | Ethics reference. | Implementation Notes. |
| FLAG_CH038_ABSTRACT_COST_LABEL_DISPUTED | moral | false | Abstract cost label challenged with real name. | Ethics tracking. | Scene 3. |

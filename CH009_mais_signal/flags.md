# Flags - CH009

Metadata:

- chapterID: CH009
- sourceFilename: chapter_009_tin_hieu_cua_mai.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH009_MISSION_STARTED | progression | false | Mentor approves Trung for radio mission | MQ_009 start | Scene 1 |
| FLAG_CH009_TEAM_ASSEMBLED | progression | false | Team (Trung, Hoang, Mentor, radio operator, engineer, scout) departs | MQ_009 progression | Scene 1 |
| FLAG_CH009_FALSE_FREQ_DETECTED | progression | false | Team detects false rescue frequency | SQ_009_04 | Scene 2 |
| FLAG_CH009_FALSE_FREQ_INVESTIGATED | progression | false | Team investigates false frequency source | SQ_009_04 | Scene 2 |
| FLAG_CH009_FALSE_FREQUENCY_DESTROYED | choice | false | Trung destroys false transmitter | SQ_009_04 completion | Scene 2 - "No one else." |
| FLAG_CH009_FALSE_FREQ_BAIT_USED | choice | false | Player uses transmitter as zombie bait (alternate) | SQ_009_04 alternate | Scene 2 alternate choice |
| FLAG_CH009_POST_OFFICE_ENTERED | progression | false | Team enters post office/radio station | MQ_009 progression | Scene 3 |
| FLAG_CH009_GENERATOR_STARTED | progression | false | Generator fueled and started | MQ_009 progression | Scene 3 |
| FLAG_CH009_FILTER_COLLECTED | progression | false | Radio filter found in sorting room | MQ_009 progression | Scene 3 |
| FLAG_CH009_COPPER_WIRE_COLLECTED | progression | false | Copper wire found | MQ_009 progression | Scene 3 |
| FLAG_CH009_FUSE_COLLECTED | progression | false | Fuse found | MQ_009 progression | Scene 3 |
| FLAG_CH009_CASSETTE_FOUND | progression | false | Cassette tape found for recording | SQ_009_01 | Scene 3 |
| FLAG_CH009_UNSENT_LETTERS_COLLECTED | sidequest | false | 3 unsent letters collected | SQ_009_05 | Scene 3 - "These letters do not weigh more than bullets." |
| FLAG_CH009_LETTER_TO_GRANDMOTHER | lore | false | First unsent letter picked up | SQ_009_05 | Scene 3 |
| FLAG_CH009_ANTENNA_CLIMB_STARTED | progression | false | Trung begins climbing antenna | MQ_009 progression | Scene 4 |
| FLAG_CH009_ANTENNA_REPAIR_SUCCESS | progression | false | Filter installed and antenna operational | MQ_009 progression | Scene 4 |
| FLAG_CH009_SCREAMER_NEARBY | world_state | false | Screamer patrol detected near antenna | Scene tension | Scene 4 |
| FLAG_CH009_BREATHING_DISCIPLINE_USED | skill | false | Player uses CH008 breathing lesson during antenna climb | Skill validation | Scene 4 - Mentor says "Breathe evenly." |
| FLAG_CH009_MAI_SIGNAL_RECEIVED | progression | false | Trung hears Mai's voice clearly | MQ_009 core objective | Scene 5 |
| FLAG_CH009_MAI_TRUST_MAINTAINED | choice | false | Trung admits injury to Mai instead of lying | Mai relationship | Scene 5 - Choice B |
| FLAG_CH009_MAI_LIED_TO | choice | false | Trung lies about injury; Mai catches him | Mai relationship penalty | Scene 5 - Choice A |
| FLAG_CH009_MAI_LOCATION_LEARNED | clue | false | Mai at northeast church with a girl | CH010+ progression | Scene 5 |
| FLAG_CH009_BINH_LOCATION_LEARNED | clue | false | Binh taken to industrial zone | CH010+ progression | Scene 5 |
| FLAG_CH009_BINH_HUNTED_CONFIRMED | clue | false | Yellow coats hunting Binh specifically | CH010+ threat thread | Scene 5 |
| FLAG_CH009_YELLOW_COAT_WARNING | threat | false | Mai warns about yellow rescue coats | CH010+ threat thread | Scene 5 |
| FLAG_CH009_MAI_RECORDED | progression | false | Mai's message captured on cassette tape | MQ_009 completion | Scene 5/6 |
| FLAG_CH009_HOANG_PULLED_TRUNG | relationship | false | Hoang physically pulls Trung from microphone | Hoang-Trung tension | Scene 6 |
| FLAG_CH009_TRUNG_ANGER_AT_HOANG | emotional | false | Trung feels anger toward Hoang for pulling him away | Emotional state | Scene 6 - "In one second, he hated his friend." |
| FLAG_CH009_EDEN_NODE_DETECTED | lore | false | EDEN NODE ACTIVE signal appears on radio | Long-term lore thread | Scene 6 |
| FLAG_CH009_BROADCAST_STOPPED | progression | false | Transmission stopped by Mentor order | MQ_009 progression | Scene 6 |
| FLAG_CH009_HORDE_APPROACHING | world_state | false | Horde enters ground floor of building | Retreat trigger | Scene 6 |
| FLAG_CH009_RETREAT_WITH_RECORDING | progression | false | Team retreats with Mai's recording tape | MQ_009 completion | Scene 6/7 |
| FLAG_CH009_OUTPOST_RETURNED | progression | false | Team returns to outpost safely | MQ_009 completion | Scene 7 |
| FLAG_CH009_RECORDING_PLAYBACK | progression | false | Trung listens to recording at outpost | Emotional resolution | Scene 7 |
| FLAG_CH009_TRUNG_ACCEPTS_WAIT | progression | false | Trung agrees to wait one night before acting | Chapter resolution | Scene 7 - "One night." |
| FLAG_CH009_FAMILY_TRUST_PLUS | relationship | 0 | Trung admits injury to Mai | Mai relationship | DT_MAI_TRUST choice |
| FLAG_CH009_PANIC_PLUS | emotional | 0 | Trung asks about Binh before hearing Mai out | Emotional state | DT_MAI_BINH choice |
| FLAG_CH009_THREAT_AWARENESS_PLUS | emotional | 0 | Trung asks who is chasing Mai | Threat awareness | DT_MAI_THREAT choice |

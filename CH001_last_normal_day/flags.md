# Flags - CH001

Metadata:

- chapterID: CH001
- sourceFilename: chapter_001_ngay_binh_thuong_cuoi_cung.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH001_BINH_WAITING | emotional | false | Binh asks whether Trung will come home early. | Dialogue and later guilt echoes. | Scene 1. |
| FLAG_CH001_TRUNG_PROMISED_HOME | continuity | false | Trung promises Binh he will come home early. | Family objective, guilt logic, later echoes. | Scene 1. |
| FLAG_CH001_MAI_WARNING_GIVEN | emotional | false | Mai asks Trung not to let Binh wait alone. | Missed call emotional context. | Scene 1. |
| FLAG_CH001_FAMILY_TRUST_PLUS | reputation | 0 | Player chooses to listen to Mai before meeting. | Family relationship tuning. | DT_001 Choice A. |
| FLAG_CH001_GUILT_PLUS | moral | 0 | Player delays family, abandons coworker, or hesitates too long. | Moral profile and later internal dialogue. | Rewards section and DT_001/DT_003. |
| FLAG_CH001_MAI_HURT_PLUS | emotional | 0 | Player treats Mai's call as not serious. | Family relationship tuning. | DT_001 Choice C. |
| FLAG_CH001_COMPLIANCE_PLUS | personality | 0 | Player hands over phone without resisting. | Early personality profile. | DT_002 Choice A. |
| FLAG_CH001_DEFIANCE_PLUS | personality | 0 | Player refuses the boss's phone demand. | Early personality profile. | DT_002 Choice B. |
| FLAG_CH001_DECEPTION_SEED | personality | 0 | Player lies about the phone battery. | Early personality profile. | DT_002 Choice C. |
| FLAG_CH001_OFFICE_MEETING_DONE | progression | false | The Floor 1 meeting and phone-surrender sequence finishes. | Unlocks the missed-call beat. | Office runtime beat chain. |
| FLAG_CH001_MAI_CALL_MISSED | continuity | false | Trung misses or delays Mai's call during the meeting. | Emotional wound and phone log. | Scene 3. |
| FLAG_CH001_PHONE_RECOVERED | progression | false | Player retrieves Trung's phone from the meeting room/tray. | Phone log, Mai route clue, final call setup. | SQ_Office_01 and Scene 5. |
| FLAG_CH001_BINH_VOICE_HEARD | emotional | false | Player listens to Binh's voice message. | Guilt/family memory references. | Scene 3 and SQ_Office_01. |
| FLAG_CH001_MAI_LOCATION_KNOWN | progression | false | Player reads Mai's message about taking Binh to her mother's home. | Chapter 02 family search route. | Scene 3 and SQ_Office_01 failure consequence. |
| FLAG_CH001_BUILDING_LOCKDOWN | world_state | false | Building announcement closes exits for security reasons. | Scene routing and blocked exits. | Scene 3. |
| FLAG_CH001_FIRST_BITE_SEEN | world_state | false | Player witnesses the elevator hallway bite. | Horror transition and combat tutorial. | Scene 4. |
| FLAG_CH001_FIRST_BITE_DONE | progression | false | The complete first-bite story beat finishes after the witness dialogue and Trung's command. | Unlocks the locked-meeting-room betrayal beat. | Office runtime beat chain. |
| FLAG_CH001_BOSS_LOCKED_DOOR | continuity | false | Boss locks management inside and leaves workers outside. | Moral motif and later phrase echo. | Scene 5. |
| FLAG_CH001_COMPANY_BETRAYAL_SEEN | emotional | false | Player hears or sees boss prioritize key people/documents. | Later distrust of false safe zones. | Scene 5. |
| FLAG_CH001_BOSS_INFECTED | world_state | false | Bitten manager bites npc_boss. | Infected boss spawn and possible later continuity. | Scene 5. |
| FLAG_CH001_EMERGENCY_STAIRS_DONE | progression | false | Player completes the emergency-stair beat and reaches the route toward the Base level. | Unlocks the Base outdoor-parking escape beat. | Office runtime beat chain. |
| FLAG_CH001_COWORKER_01_RESCUE_DECIDED | choice | false | Player commits to one of the rescue, abandon, or partial-aid outcomes. | Completes the shared MoralChoice objective in MQ_001 and SQ_001_02. | SQ_Office_02 runtime objective. |
| FLAG_CH001_COWORKER_01_RESCUED | choice | false | Player breaks in and saves npc_coworker_01. | Possible Chapter 05 witness. | SQ_Office_02 and DT_003 Choice A. |
| FLAG_CH001_COWORKER_01_ABANDONED | choice | false | Player runs without helping npc_coworker_01. | Guilt profile and later consequences. | DT_003 Choice B. |
| FLAG_CH001_COWORKER_01_AIDED | choice | false | Player gives a tool or aid but does not fully rescue him. | Deferred Chapter 05 resolution. | DT_003 Choice C. |
| FLAG_CH001_COMPASSION_PLUS | moral | 0 | Player rescues coworker at cost. | Moral profile. | Rewards section. |
| FLAG_CH001_PRAGMATISM_PLUS | moral | 0 | Player runs to preserve speed/health. | Moral profile. | Rewards section. |
| FLAG_CH001_CAR_KEY_FOUND | progression | false | Player finds Trung's car key or route clue on Floor 1. | Base outdoor-parking escape pacing. | SQ_Office_03. |
| FLAG_CH001_WRONG_KEY_DISCOVERED | world_state | false | Player discovers someone took the wrong key in panic. | Theme echo: selfishness predates apocalypse. | SQ_Office_03 twist. |
| FLAG_CH001_BASIC_MELEE_UNLOCKED | system | false | Player uses first improvised weapon. | Combat system. | Rewards section and Gameplay Beats. |
| FLAG_CH001_PHONE_LOG_UNLOCKED | system | false | Player recovers phone and completes phone tutorial. | Phone log system. | Rewards section. |
| FLAG_CH001_FAMILY_OBJECTIVE_UNLOCKED | progression | false | Final call cuts out and Trung commits to finding Mai and Binh. | Chapter 02 main drive. | Rewards section and Scene 6 ending. |
| FLAG_CH001_OFFICE_ESCAPED | progression | false | Trung escapes through the Base-level outdoor parking gate. | Chapter completion and Chapter 02 start. | Continuity Notes. |

Compatibility note: `FLAG_CH001_FIRST_BITE_SEEN` records the narrative fact that Trung witnessed the bite, while `FLAG_CH001_FIRST_BITE_DONE` records completion of the entire runtime story beat. They are intentionally separate IDs and must not be merged without a save-data migration.

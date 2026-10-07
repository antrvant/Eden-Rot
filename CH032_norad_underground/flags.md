# Flags - CH032

Metadata:

- chapterID: CH032
- sourceFilename: chapter_032_norad_duoi_long_dat.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH032_NORAD_ROUTE_COMPLETED | progression | false | Reached NORAD mountain bunker | CH033 context | Scene 2. |
| FLAG_CH032_SATELLITE_NETWORK_PARTIAL_ONLINE | progression | false | Satellite interface activated | CH033 broadcast | Scene 8. |
| FLAG_CH032_GLOBAL_BROADCAST_WINDOW | progression | false | 4-hour broadcast window opened | MQ_033 start | Scene 9. |
| FLAG_CH032_NORAD_SHARED_NODE | choice | false | Bunker as shared governance node | Governance tracking | Scene 9, DT_179. |
| FLAG_CH032_OUTER_GATE_NEGOTIATION | story | false | Outer gate negotiation completed | Scene flow | DT_171. |
| FLAG_CH032_EDENROT_SHELTER_CAPACITY_ENGINE | world_state | false | NORAD classified under EDENROT | EDENROT tracking | Scene 2. |
| FLAG_CH032_MENTOR_CODE_ACCEPTED | story | false | Mentor legacy challenge passed | Mentor payoff | Scene 3, DT_172. |
| FLAG_CH032_CQ_MENTOR_04_COMPLETE | story | false | Mentor quest payoff achieved | Long-term tracking | Scene 3. |
| FLAG_CH032_SHELTER_ROTATION_PROTOCOL | governance | false | Transparent triage established | Bunker governance | Scene 4, DT_173. |
| FLAG_CH032_PUBLIC_INTAKE_LEDGER | governance | false | Names collected publicly | Bunker governance | Scene 4, DT_174. |
| FLAG_CH032_SHELTER_CAPACITY_ENGINE_DISPUTED | story | false | Capacity math challenged by names | EDENROT counter-flag | Scene 4. |
| FLAG_CH032_FAMILY_NOT_PRIVILEGED | choice | false | Trung's family follows same rules | Integrity tracking | Scene 4. |
| FLAG_CH032_LOWER_BUNKER_BREACH_DISCOVERED | story | false | Sealed infection found | King setup | Scene 5. |
| FLAG_CH032_KING_INFECTED_INTRODUCED | world_state | false | King variant encountered | Enemy tracking | Scene 5. |
| FLAG_CH032_KING_INFECTED_DEFEATED | progression | false | King destroyed | Chapter completion | Scene 7. |
| FLAG_CH032_KING_PULSE_COUNTERMEASURE | story | false | Anti-horde rhythm learned | Gameplay unlock | Scene 7, DT_177. |
| FLAG_CH032_INTAKE_CIVILIANS_PROTECTED | choice | false | Trung returned to defend intake | Integrity tracking | Scene 6, DT_176. |
| FLAG_CH032_SATELLITE_SAFE_MODE | choice | false | Broadcast/listen only, no targeting | Satellite governance | Scene 8, DT_178. |
| FLAG_CH032_VALE_COMMAND_INJECTION_BLOCKED | story | false | VALE denied target authority | VALE tracking | Scene 8, DT_178. |
| FLAG_CH032_NODE_MODE_BROADCAST_LISTEN_RELAY | world_state | false | NORAD mode set to relay | System state | Scene 8. |
| FLAG_CH032_ARCHITECT_LISTENER_DETECTED | world_state | false | Non-human listener found | CH033 setup | Scene 8. |
| FLAG_CH032_CH33_BROADCAST_READY | progression | false | Ready for global broadcast | MQ_033 start | Scene 9. |
| FLAG_CH032_BUNKER_FAVORITISM | choice | false | Rebirth circle prioritized (fail path) | Fail tracking | Metadata. |
| FLAG_CH032_NORAD_ARMY_CONTROLLED | choice | false | Army sole control (fail path) | Fail tracking | Metadata. |

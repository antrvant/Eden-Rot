# Flags - CH042

Metadata:

- chapterID: CH042
- sourceFilename: chapter_042_mau_cua_con.md
- language: English

| flagID | type | defaultValue | setWhen | usedBy | sourceEvidence |
|---|---|---|---|---|---|
| FLAG_CH042_MOBILE_LAB_STABILIZED | progression | false | Lab systems stabilized after Cairo evacuation. | Scene 02 access, cure analysis. | Scene 01. |
| FLAG_CH042_FIRST_CURE_REVIEWED | progression | false | First cure and batch failure data reviewed by team. | Ethics Table prerequisite. | Scene 01. |
| FLAG_CH042_TRUNG_SHUT_DOWN_HARD | emotional | false | Trung responds too harshly to Binh's question. | BinhDistrust increment. | Scene 01. |
| FLAG_CH042_TRUNG_REFLEX | emotional | false | Trung reflexively says "not everything is your business." | BinhDistrust increment. | DT_262. |
| FLAG_CH042_MAI_SUPPORTS_TRUTH | emotional | false | Mai asserts Binh's right to hear truth. | Scene 02 progression. | DT_262. |
| FLAG_CH042_BINH_TRUTH_CONVERSATION_COMPLETE | progression | false | Binh heard truth about resonance in age-appropriate language. | Ethics Table prerequisite. | Scene 02 / DT_265. |
| FLAG_CH042_BINH_INFORMED_CONSENT | progression | false | Binh gave informed consent after truth conversation. | Blood draw prerequisite. | Scene 02 / DT_265. |
| FLAG_CH042_GUARDIAN_CONFLICT_RESOLVED | progression | false | Trung and Mai resolved their argument and wrote shared rules. | Ethics Table prerequisite. | Scene 03 / DT_264. |
| FLAG_CH042_GUARDIAN_VETO_ACTIVE | system | false | Guardian veto protocol established. | Blocks override during blood draw. | Scene 04 protocol clause 4. |
| FLAG_CH042_BLOOD_PROTOCOL_ESTABLISHED | progression | false | Blood Protocol drafted and signed. | All subsequent scenes. | Scene 04. |
| FLAG_CH042_EDENROT_CHILD_CONSENT_FIREWALL_ESTABLISHED | progression | false | EDENROT CLASS: CHILD CONSENT FIREWALL created. | System header for all child/immune research. | Scene 04 / Thu header. |
| FLAG_CH042_CHILD_CONSENT_FIREWALL_ACTIVE | system | false | Firewall active in system. | All child research scenes; must remain active in Act 7. | Scene 04 / protocol header. |
| FLAG_CH042_BINH_STOP_WORD_CHOSEN | sidequest | false | Binh chose his stop word. | Blood draw mechanic. | Scene 04 / SQ_042_B. |
| FLAG_CH042_BINH_STOP_WORD | item_state | DenDo | Stop word value set. | Procedure abort trigger. | SQ_042_B canon: "Den Do" (red light). |
| FLAG_CH042_BINH_TRUST_PLUS | relationship | 0 | Binh trusts adults more after honest answers. | Distrust counterbalance. | Scene 02 / DT_263, DT_265. |
| FLAG_CH042_BINH_DISTRUST | relationship | 0 | Binh distrust increases from dishonest or evasive answers. | Threshold check for consent refusal. | Scene 02 wrong dialogue choices. |
| FLAG_CH042_YUSUF_DEBT_LOGIC_REJECTED | emotional | false | Yusuf tells Binh he owes nothing. | Binh emotional state. | Scene 05 / DT_267. |
| FLAG_CH042_MASUD_RUMOR_CONTAINED | world_state | partial | Masud rumor partially contained via trusted-node comms. | Future chapter threat level. | Scene 06. |
| FLAG_CH042_TRUSTED_ALLIES_BRIEFED | progression | false | Trusted allies received encrypted truth. | Alliance trust. | Scene 06. |
| FLAG_CH042_MINIMAL_BLOOD_SAMPLE_COLLECTED | progression | false | One minimal blood sample collected from Binh. | Micro-test, cure progress. | Scene 07. |
| FLAG_CH042_PROCEDURE_STOPPED_ON_COMMAND | progression | false | Procedure stopped when Binh used stop word. | Firewall verification. | Scene 07 / DT_268. |
| FLAG_CH042_STOP_WORD_HONORED_FIREWALL_VERIFIED | progression | false | Stop word honored; firewall verified as real, not decorative. | All future child/immune procedures. | Scene 07 / Thu log: STOP WORD HONORED. FIREWALL VERIFIED. |
| FLAG_CH042_BINH_CONSENT_RECONFIRMED | progression | false | Binh freely re-consented after stop word pause. | Valid consent for blood draw. | Scene 07. |
| FLAG_CH042_EXTRA_EXTRACTION_REFUSED | choice | false | Samir's request for extra micro-test refused. | CureMoralFlag integrity. | Scene 08. |
| FLAG_CH042_MINIMAL_DRAW_ONLY_CHILD_NOT_SOURCE | system | false | Binh marked as child/person, not source/factor/bridge. | Prevents later escalation. | Scene 08 / Thu flag: MINIMAL DRAW ONLY. CHILD IS NOT SOURCE. |
| FLAG_CH042_BETTER_BATCH_MICRO_STABILITY | progression | false | Binh's sample improved enzyme stability in micro-tests. | Cure progress direction. | Scene 08. |
| FLAG_CH042_CURE_SCALABILITY_STILL_BLOCKED | world_state | true | Cure cannot scale to mass production. | Future chapter cure limitation. | Scene 08. |
| FLAG_CH042_CURE_MORAL_FLAG | moral | ConsentFirst | Cure moral flag set. | Influends endings and ally trust. | Scene 08 / implementation notes. |
| FLAG_CH042_HOANG_SELF_AWARENESS | sidequest | false | Hoang acknowledged dangerous desire and signed self-restraint. | Chapter 45 confrontation extra dialogue. | Scene 09 / SQ_042_C / DT_269. |
| FLAG_CH042_ARCHITECT_BEACON_DECODED | progression | false | Architect beacon decrypted. | Amazon route unlock. | Scene 10. |
| FLAG_CH042_ASTER_NODE_LOCATED | progression | false | Aster Node location confirmed. | Act 7 destination. | Scene 10. |
| FLAG_CH042_ORISON_ARCHIVE_REVEALED | lore | false | Orison child resonance archive discovered. | Act 7 threat thread. | Scene 10. |
| FLAG_CH042_ORISON_CHILD_RESONANCE_CHAMBER_REVEALED | lore | false | Child resonance chamber revealed. | Act 7 moral battlefield. | Scene 10. |
| FLAG_CH042_FLOODED_AMAZON_ROUTE_CHOSEN | choice | false | Flooded river route selected. | Chapter 43 entry. | Scene 10 / DT_370. |
| FLAG_CH042_FAMILY_RULE_ESTABLISHED | emotional | false | Family rule: no one saves the world alone. | Long-term echo near finale. | Scene 11 / DT_271. |
| FLAG_CH042_CHAPTER_043_FLOODED_AMAZON_UNLOCKED | progression | false | Chapter 43 unlocked. | Chapter transition. | Scene 10 / Scene 12. |
| FLAG_CH042_BIO_COVENANT_MAINTAINED | faction | false | Nia's enzyme covenant clause accepted. | Tribal alliance trust. | SQ_042_E. |
| FLAG_CH042_MASUD_ROUTE_CONFUSED | world_state | false | False beacon sent to confuse Masud's pursuers. | Reduces convoy exposure. | SQ_042_D. |
| FLAG_CH042_LINA_LOCATION_UNKNOWN | world_state | false | Lina search inconclusive. | Yusuf emotional state. | SQ_042_A canon outcome. |

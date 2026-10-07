# Characters - CH001

Metadata:

- chapterID: CH001
- sourceFilename: chapter_001_ngay_binh_thuong_cuoi_cung.md
- language: English

| characterID | displayName | role | type | factionID | firstSeenInChapter | statusAtEnd | sourceEvidence |
|---|---|---|---|---|---|---|---|
| char_trung | Trung | Player protagonist and main POV | playable | FAC_CH001_TRUNG_FAMILY | CH001 | Alive; escaped through the Base outdoor parking gate with urgent family objective | Metadata lists Trung as main POV; full draft follows his promise, missed call, and escape. |
| char_mai | Mai | Wife, emotional anchor, phone contact | remote_story_npc | FAC_CH001_TRUNG_FAMILY | CH001 | Alive but separated; last call cuts out during street chaos | Metadata and scenes show Mai through calls, messages, lunch box, and final broken call. |
| char_binh | Binh | Son, memory anchor, voice message | remote_story_npc | FAC_CH001_TRUNG_FAMILY | CH001 | Alive but separated; heard crying during final call | Scene 1 and voicemail establish Binh's performance and question about Trung coming home. |
| comp_hoang_reference | Hoang | Future friend seed through message | referenced_character | FAC_CH001_HOANG_FRIENDSHIP | CH001 | Offscreen; not encountered directly | Emotional Design states Hoang does not appear directly but sends a message asking if Trung is okay. |
| npc_boss | Office Boss | Antagonistic manager and infected mini-boss | npc_boss | FAC_CH001_COMPANY_MANAGEMENT | CH001 | Bitten and infected; pursues Trung from Floor 1 down to the Base outdoor parking area | Metadata names npc_boss after becoming infected; Scenes 5 and 6 show the bite and chase. |
| npc_coworker_01 | Male Coworker | Rescue target and moral choice NPC | npc | FAC_CH001_OFFICE_WORKERS | CH001 | Variable: rescued, abandoned, or aided depending on player choice | Side quest SQ_Office_02 and DT_003 center on this coworker behind a glass door. |
| npc_coworker_02 | Sick Female Coworker | Early infection fear and optional rescue pressure | npc_or_hazard | FAC_CH001_OFFICE_WORKERS | CH001 | Uncertain; may become infected or survive depending on scene handling | Scene 4 describes her fever and fear that she may hurt someone. |
| npc_building_guard | Building Guard | Security worker, first infected victim/attacker | npc_hazard | FAC_CH001_BUILDING_SECURITY | CH001 | Infected or killed during elevator outbreak | Scene 3 and Scene 4 show the guard trying to restrain the delivery man before becoming a threat. |
| npc_unknown_employee | Unknown Employee | Outbreak witness and social panic seed | npc | FAC_CH001_OFFICE_WORKERS | CH001 | Variable or unknown | Metadata lists an unfamiliar employee; Scene 4 includes employees hiding family infection news. |
| npc_intern | Intern | Human darkness victim in first-bite scene | npc | FAC_CH001_OFFICE_WORKERS | CH001 | Variable; nearly sacrificed by team lead | Emotional Design and Scene 4 show a manager pushing an intern forward to inspect danger. |
| npc_team_lead_coward | Cowardly Team Lead | Example of pre-apocalypse selfishness | npc | FAC_CH001_COMPANY_MANAGEMENT | CH001 | Alive or unknown after panic | Emotional Design states a small manager sends an intern toward the dangerous elevator hallway instead of checking it himself. |
| npc_bitten_manager | Bitten Manager | Bite vector for boss infection | npc_hazard | FAC_CH001_COMPANY_MANAGEMENT | CH001 | Infected; bites npc_boss | Scene 5 states a bitten manager rises and bites the boss. |

## Character Notes

- Trung is not careless by nature. His tragedy is that work pressure and the belief that sacrifice now will help his family later have trained him to delay presence.
- Mai must remain strong and restrained. Her calls should not read as simple scolding; she is asking Trung not to make Binh wait alone again.
- Binh's presence is carried by small artifacts: his drawing, a voice message, and the question "Will Dad come home?"
- npc_boss should not become a cartoon villain. His danger is that he can use normal business language to decide who counts as worth saving.

## Office Scene Runtime Identity Notes (2026-08-17)

- Canonical layout: all interactive Office NPCs, including the Boss, are on Floor 1. The optional Boss office on Floor 6 is not part of the required Chapter 001 route.

- `npc_coworker_01` is Steve, the anxious coworker tied to the swapped keys and rescue choice.
- `npc_coworker_02` is Tuan, an observant overworked colleague; the former "Sick Female Coworker" metadata on this runtime asset was corrected.
- `npc_female_clerk` is Linda, the receptionist/clerk who covers for Trung and knows the office's hidden pressures.
- `npc_group_leader` is Team Lead, the self-protective manager exploiting the intern.
- `npc_shipper` is Delivery Worker, a parent forced to finish the route while visibly ill.
- The Building Guard and Intern retain their role names. All eight Office NPCs now have explicit CharacterData and reachable interaction dialogue.

## 3 Literature review

### 3.1 Selection and appraisal

The review uses eight scientific publications [R1–R8] and supporting primary documentation [R9–R25]. Seven of the eight scientific works were published in 2022–2026; the 2019 Project Sidewalk study is retained as a foundational deployment study. Searches on 20 October 2026 covered personalized accessible routing, wheelchair routing and OSM, sidewalk data quality, crowdsourced barriers and user perceptions. This is a focused review, not a systematic review or a claimed Scopus search.

Primary publisher pages, author repositories and official documentation were checked. For R1, R2 and R3 the appraisal is limited to accessible publication records and abstracts; numerical experimental claims are not inferred from unavailable full text. R4–R8 were examined through available article text or author versions. Limitations below include our appraisal of transferability, not necessarily claims made by each author.

| Source | Method and evidence | Main contribution | Limitation and project use |
| --- | --- | --- | --- |
| R1 Majic et al 2026 | OSM suitability analysis and wheelchair network case study in Graz | Identifies relevant tags and compares pedestrian and wheelchair routes | Another city; local completeness is unproven. Audit pilot tags and compare identical OD pairs |
| R2 Nguyen et al 2024 | MyPath combines smartphone surface sensing with accessible route generation | Connects surface information, OSM and routing | Sensor collection exceeds our scope. Use manual surface observations; retain surface-aware cost |
| R3 Darvishy et al 2022 | Zurich case study and accessible-routing vision | Identifies required attributes and combined collection methods | A vision and local study do not establish Astana coverage. Combine import with field audit |
| R4 Darko et al 2022 | Adaptive preference model with reinforcement learning | Treats changing preferences and sidewalk conditions in route choice | Model and evaluation differ from static search. Keep explainable fixed snapshots and defer adaptation |
| R5 Labbé et al 2023 | Workshops with 51 stakeholders | Highlights trust, usability and uses of accessibility data | Qualitative context is not local demand evidence. Design provenance and real consultation |
| R6 Askari et al 2025 | Compares virtual audits with government field data in two US settings | Finds substantial agreement for several infrastructure features | Severity definitions complicate comparison. Use an explicit field-audit rubric |
| R7 Li et al 2025 | Survey of 190 people from five mobility-device groups using 52 barrier images | Shows differences and shared concerns across groups | Image judgments do not establish actual route traversability. Keep profile settings configurable |
| R8 Saha et al 2019 | 18-month remote crowdsourcing deployment and quality analysis | Demonstrates scalable sidewalk labelling and quality trade-offs | Imagery and crowd labels require validation. Moderate reports and retain evidence |

### 3.2 Supporting source analysis

| Source | Role in this project | Limitation |
| --- | --- | --- |
| R9 Google Maps official announcement | Documents stair-free walking routes and data-dependent availability | Does not validate the selected Astana corridors |
| R10 2GIS official help | Documents walking routes, crossings, gates and stair exclusion | Local route quality still requires testing |
| R11 Wheelmap official description | Demonstrates place-level accessibility ratings and unknown status | Place ratings alone do not prove continuous path accessibility |
| R12 openrouteservice documentation | Shows configurable wheelchair restrictions | Capability depends on underlying data and deployment |
| R13 and R14 OSM tagging documentation | Defines slope and kerb representation | Tag presence and correctness are not guaranteed |
| R15 WCAG and R16 Flutter guidance | Inform contrast, labels and mobile accessibility testing | Checklist compliance is not a substitute for user testing |

### 3.3 Critical synthesis and project gap

The reviewed routing work supports personalization, but approaches differ in complexity and evidence. A richer sensing or adaptive model can capture more conditions, while increasing data and validation requirements. For a three-person diploma, a transparent constrained graph model is a defensible starting point. We will state its limits: preferences remain fixed within one request, effort is approximated rather than physiologically measured, and uncertain data can reduce route availability.

The data studies indicate that collecting labels at scale and trusting every label are separate problems. Our design therefore stores source, observation time, verification status and unknown attributes. The engineering implication is that a route result must describe both the path and the evidence behind it. A short route with missing kerb data cannot receive the same explanation as a field-checked route.

The human-centred studies support configurable profiles and consultation. The four Astana interviews add local self-reported examples of barriers and differing detour, interaction and reporting preferences. They inform the decisions in section 2.3 but do not validate the finished interface, calibrated routing parameters, adoption or population demand. Field auditing and later usability evaluation remain necessary.

The proposed contribution is a locally evaluated integration of four mobility presets, a versioned pilot graph, moderated temporal reports and uncertainty-aware route explanations. We do not claim to invent accessible routing or to be the first such solution in Kazakhstan. The research question is whether this bounded implementation reduces known constraint violations relative to distance-only routing while keeping detours and computation cost explicit.

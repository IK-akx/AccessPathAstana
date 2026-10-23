## 1 Project proposal

### 1.1 Project title and problem

Formal title: Development of a Cross Platform Mobile Application for Mobility Aware Pedestrian Routing in Astana.

The shortest pedestrian route may contain steps, unsuitable kerbs, steep segments, uneven surfaces or temporary obstructions. These characteristics affect people differently, so a generic walking route or a single accessibility label may be insufficient. Research supports personalized routing and careful handling of incomplete pedestrian data [R1–R8]. The extent of these problems in our pilot area has not yet been measured.

We will address a specific engineering problem: selecting a traversable route under a chosen set of mobility constraints while communicating gaps in the underlying data. The application will combine a pedestrian graph, profile-dependent rules, verified barrier reports and an accessible mobile interface. It will not certify that a route is universally accessible or that unobserved conditions are safe.

### 1.2 Users and team

Primary users are people using manual or powered wheelchairs, adults travelling with a child stroller, people using crutches, and older pedestrians who want to avoid particular physical obstacles. Four initial presets will provide an understandable starting point; users will review their own constraints because a group label does not determine individual capability. Secondary users are moderators and the project team collecting and validating data.

| Team member | Main responsibility | Primary deliverables |
| --- | --- | --- |
| Iskander Kustayev | Graph model and routing | Profiles, edge costs, Dijkstra and A*, report impact rules, algorithm tests, model and evaluation chapters |
| Alua Sagyndyk | Backend and geodata | REST API, PostgreSQL/PostGIS, import and audit pipeline, moderation, admin interface, Docker, data and architecture chapters |
| Altynay Bolatova | Mobile application and UX | Accessible mockups, map and route views, foreground GPS guidance, report submission, Android/iOS testing, interface chapter |
| All three | Research and integration | Interviews, literature, comparisons, requirements, integration tests, thesis and defense |
| Islam Omirzak | Academic supervision | Review of scope, methodological choices and key deliverables |

### 1.3 Aim and objectives

Aim: develop and evaluate a cross-platform prototype that produces pedestrian routes satisfying explicit mobility constraints in a bounded area of Astana, using open geodata, field observations and moderated user reports.

O1. Identify and validate user needs through three to five real discussions and a structured analysis of relevant research.

O2. Build a versioned pedestrian dataset with documented provenance, missing attributes and a field-audited subset.

O3. Define four configurable mobility presets, hard exclusions, soft penalties and an explicit unknown-data policy.

O4. Implement Dijkstra and A* against the same weighted graph and verify equal optimal cost where their preconditions hold.

O5. Implement route, report and moderation APIs and a mobile client with map, route summary and basic foreground guidance.

O6. Evaluate route constraint compliance, data uncertainty, algorithm performance and completion of key user tasks against stated baselines.

### 1.4 Geographic and functional scope

The pilot is in Astana, within the area bounded by Turar Ryskulov Street, Orynbor Street, Kabanbay Batyr Avenue and Mangilik El Avenue. This replaces the earlier approximate EXPO and Botanical Garden landmark envelope. The four street boundaries are the team's agreed service extent. A georeferenced GeoJSON polygon still needs to be produced from these boundaries and checked against the pedestrian network; no coordinates, area measurement or data completeness are asserted here. Import and endpoint validation will use the same approved polygon.

The initial audit will focus on a connected set of corridors and crossings serving approximately 20–30 evaluation origin–destination pairs. The exact sample will follow the data audit. A small import buffer may preserve graph connectivity; accepted routes must remain inside the agreed service polygon unless the user is explicitly told otherwise. We will not claim coverage of all of Yesil district.

| Included in the diploma | Excluded or conditional |
| --- | --- |
| Four configurable mobility presets | Medical assessment or universal accessibility certification |
| Steps, kerbs, slope, surface and relevant width observations | Automatic recognition of all barriers from images |
| Moderated reports with photos and timestamps | Citywide live monitoring and automatic winter maintenance data |
| Android and iOS prototype testing | App store publication as a required result |
| Route map, textual instructions and foreground GPS | Voice navigation, background tracking and offline routing |
| Basic external lift connectors if verified data exist | Indoor routing and unverified live lift status |
| Controlled algorithm and route comparisons | Proven superiority over commercial services across Astana |

### 1.5 Expected outcomes and engineering complexity

The final deliverables are a mobile prototype, backend API and moderator interface, a documented pilot dataset, a tested routing module, reproducible evaluation scripts and results, and a thesis with limitations. The engineering contribution is the integration of directional graph topology, per-profile edge eligibility, incomplete data, report lifecycles and explainable route output. Implementing two search algorithms alone is not the claimed novelty.

Success requires passing all mandatory acceptance criteria, reporting whether evaluation targets were achieved and explaining failures. The project can produce a valid research outcome even if some routes are unavailable because trustworthy accessibility data are missing.

# User interviews and requirement decisions

### 2.2 User interviews

Four semi-structured interviews were conducted with representatives of the four intended user groups using the same 15-question guide. Participation was voluntary. Participants agreed to anonymized use of their answers; the team retained written notes only, with no audio or video recording. No diagnoses or direct personal identifiers are included in this report. Interviews were held in Russian; the accounts below are close summaries translated into English, not verbatim quotations. Participants are identified by ID only.

All four discussed experience in Astana. P02 also discussed the selected pilot area; specific incident locations have not been supplied and are not assigned to map features. The team introduced the project to participants. Whether participants subsequently checked the English summaries has not been established.

Interview P01

Participant ID: P01. User group: parent with a child stroller. Date: 22 October 2026. Format: call. Interviewer: Altynay Bolatova.

Answers: The participant walks daily with a stroller, mostly alone. On a recent difficult trip, a clinic had a high kerb with no ramp. She lifted the stroller while carrying a bag and holding the child, with help from a passer-by. A shop described as barrier-free had internal steps and no lift. She sometimes turns back at crossings without ramps. In winter, icy ramps and deep snow restrict outings. She uses 2GIS and a neighbourhood parents' chat, but reports not finding the ramp and step information she needs. She would accept a detour of approximately 200–300 metres for the described trips. She would report barriers if submission takes a few taps with a photo and the review outcome is visible. Small fonts, controls difficult to operate with one hand, continuous GPS tracking and unexpected route changes are unwelcome.

Findings: Kerbs without ramps, entrance steps, missing pavements and wide paving joints can interrupt stroller trips. A general accessibility label does not describe the entire journey. Detour tolerance depends on fatigue and the child. These are the participant's reported experiences, not verified attributes of particular pilot edges.

Requirement implications: Supports the stroller preset and configurable constraints (FR-01), step and kerb restrictions (FR-03), route distance (FR-05), brief photo-supported reporting and visible status (FR-08), and large controls (NFR-02). Explicit unknown-data wording and no silent rerouting strengthen FR-04 and FR-07. Rest places, feeding facilities and indoor shopping-centre lifts are recorded for future scope review.

Interview P02

Participant ID: P02. User group: person using crutches temporarily. Date: 19 October 2026. Format: in person. Interviewer: Alua Sagyndyk.

Answers: The participant has used crutches for approximately a month and travels by public transport to university and hospital. A recent crossing with steps was difficult because his hands were occupied and he could not reach his phone. At a building described as accessible, a steep, slippery ramp felt more difficult than stairs with a handrail. Slippery areas and uneven asphalt or paving are major concerns, including anticipated winter conditions. He reports that the navigation apps he uses do not provide the step information he needs. A detour of approximately 100–200 metres is acceptable for the described trips, while longer distances are tiring. He wants prominent text describing unknown conditions rather than small icons. He would prefer one-tap or short voice reporting and spoken guidance that avoids looking at the screen. His discussion included the selected pilot area, without mapped incident coordinates.

Findings: Avoiding steps alone does not establish a suitable crutch route; slope, surface, fatigue and handrail availability also matter. Hands-busy interaction is a significant concern for this participant. His requirements may change as mobility changes.

Requirement implications: Supports editable crutch constraints, considering surface and slope alongside steps (FR-01 and FR-03), distance before starting (FR-05) and prominent warnings (FR-04 and NFR-02). Voice guidance, voice or one-tap reporting, handrail data and an automatically expiring injury setting are candidate extensions. They are not committed mandatory functions of the current pilot.

Interview P03

Participant ID: P03. User group: older pedestrian who uses a cane. Date: 20 October 2026. Format: in person. Interviewer: Iskander Kustayev.

Answers: The participant goes out daily, usually within his neighbourhood for shops or a clinic, and sometimes travels to his daughter by bus. High bus steps and pressure to board quickly made a recent trip difficult. At a clinic, a broken lift required him to climb stairs. He avoids steps without handrails and accepts a longer route, but needs places to sit. Fear of falling greatly reduces winter outings. He knows familiar routes and rarely uses a phone. He prefers large written warnings because colours and icons are difficult to distinguish. He is unlikely to submit barrier reports independently and would expect family help. Small text, many taps, tracking and automatic changes are unwelcome. A large button to contact relatives or a volunteer would be useful to him.

Findings: Fear of falling, rest needs and difficulties at transport or building interfaces affect this participant's mobility. A map-and-reporting application may not be used independently by every intended user. Bus boarding and indoor lift incidents motivate the problem but are outside the outdoor pilot's routing responsibility.

Requirement implications: Supports the older-pedestrian preset (FR-01), a simple interface with large text and non-colour warnings (NFR-02), optional GPS access (FR-02) and no silent route changes (FR-07). Rest-place data and a help button are future candidates. Reporting uptake among older users must not be assumed. A preference for displaying a last-check date is not explicitly established in this summary.

Interview P04

Participant ID: P04. User group: manual wheelchair user. Date: 17 October 2026. Format: call. Interviewer: Altynay Bolatova.

Answers: The participant has used a manual wheelchair for several years and travels independently around the city every day. On a recent trip to a cafe described as accessible, a high kerb without a ramp left him waiting for help. He identifies kerbs, steep slopes, poor surfaces, narrow passages and parked cars as recurring problems. Thresholds, narrow doors and non-working lifts can also prevent access on arrival, so a single accessibility label is insufficient. Winter is particularly difficult. He uses 2GIS and Google Maps, photographs, reviews and a friends' chat. He wants kerb height, slope, width, surface, lift status and the date of the last check. He accepts a substantial detour if it is more reliable, describing an extra ten minutes as preferable to getting stuck. He wants unknown segments clearly identified so that he can make an informed decision. He would submit type, location and photo if reports are checked. Small buttons, a jumping map and retention of route history are unwelcome.

Findings: Vague accessibility labels can omit journey-critical details. This participant values measurable attributes, provenance and freshness, and wants control over individual constraints. Interview statements about lift status do not establish that verified live lift data exist for the pilot.

Requirement implications: Supports editable wheelchair constraints (FR-01), relevant kerb, slope, width and surface attributes (FR-03), explicit unknowns (FR-04), short reports and visible review status (FR-08), provenance and observation dates (FR-14), accessible controls (NFR-02) and minimal location retention (NFR-05). External lifts remain conditional (FR-15). Peer confirmation is a possible design approach, not an explicit request established by the supplied answer summary; moderator verification remains the baseline.

### 2.3 Cross interview analysis and requirement decisions

All four summaries describe steps or kerbs that complicate travel and winter-related concerns. Surface difficulties are explicit in P01, P02 and P04; P03 emphasizes even routes and fear of falling. P01, P02 and P04 describe a place whose accessibility description did not match their experience. P03 describes a broken lift, without stating that the location was labelled accessible. Numeric limits and attribute completeness therefore remain more informative design targets than a single yes/no label.

Detour preferences differ: P01 describes approximately 200–300 metres, P02 approximately 100–200 metres, and P03–P04 prioritize more reliable routes without a common distance limit. These are contextual preferences, not calibrated universal thresholds. The initial profiles remain editable; numeric slope, kerb and penalty values require further justification and field evaluation.

All four raise interaction difficulties. Tracking concerns are explicit in P01, P03 and P04; P02 emphasizes hands-busy operation. P01 and P03 object to automatic changes, while P04 objects to an unstable map. The design therefore retains optional GPS, minimal data retention, clear warnings and user-controlled route rebuilding. P04 explicitly requests the last-check date; the same preference is not directly established for every participant. Date display is also supported by the literature and provenance design.

P01, P02 and P04 express conditional willingness to report, with differing effort limits. P03 expects help from family. This supports brief reporting and visible moderation, but does not establish actual participation rates. P04 wants to decide about unknown sections, while P03 favours more predictable paths. Strict routing remains the default; exploratory routing requires explicit selection and never overrides a known prohibition.

| Finding and evidence | Requirement decision | Scope and verification |
| --- | --- | --- |
| Different detour preferences and mobility constraints, P01–P04 | Retain editable presets, hard restrictions and visible distance; FR-01, FR-03, FR-05 | Core; T01, T03, T05; no universal detour limit inferred |
| Missing information and unreliable labels, P01–P04; freshness request, P04 | Explicit unknowns and barrier provenance; FR-04, FR-14 | Core; T04, T14; observed dates shown as unknown when unavailable |
| Brief reporting and review visibility, P01, P02, P04; assisted reporting, P03 | Streamlined photo-supported form and own-report status; FR-08 | Core; T08; observed usability and uptake remain untested |
| Hands-busy use and readability, P01–P04 | Large controls, prominent text and stable interaction; NFR-02, FR-07 | Core; T07, T17; voice features deferred for feasibility review |
| Tracking and unwanted changes, P01, P03, P04 | Optional GPS, explicit rebuild and minimal location retention; FR-02, FR-07, NFR-05 | Core; T02, T07, T20 |
| Rest places, handrails, help and voice interaction | Record candidate extensions rather than expanding the mandatory pilot | Future backlog; no acceptance or delivery claim |

The interviews do not establish that Google Maps or 2GIS lack stair-avoidance functionality. Participants describe the information available to them in their own use. The official capability comparison in section 4 remains separate from these reported experiences.

### 2.4 Method limitations and evidence records

Four participants cover the intended user groups in Astana, but this is a small requirements-exploration sample. Accounts are self-reported and were not independently checked in the field. P02's pilot-area familiarity does not establish coverage of all paths within the boundary. Recruitment details, interview durations and participant checking of the translated summaries have not been supplied; they are not assumed. The project was introduced to participants, which does not itself validate the wording of these summaries or the finished interface. Findings cannot support population percentages, demand forecasts, algorithm performance or achieved accessibility claims.

Retain the anonymized session notes, the actual 15-question guide and the consent record with appropriate access. The report contains translated summaries rather than full question-by-question transcripts. Requirements should cite P01–P04 only where the supplied accounts support the decision. Implementation feasibility and usability must be tested separately.

# Initial evidence and delivery traceability

P01–P04 are the four dated interview summaries in management/user_interviews.md. They support requirements exploration; they do not establish usability or implementation acceptance. R references refer to docs/references.md. This matrix links the report's requirements to implementation ownership and tests.

| Requirement | Basis | Component and data | Owner | Verification |
| --- | --- | --- | --- | --- |
| FR-01 | R7; P01–P04 | Mobile settings; MobilityProfile | Iskander and Altynay | T01 |
| FR-02 | Pilot scope; P03 | Mobile planner; PilotArea and graph snapping | Altynay and Iskander | T02 |
| FR-03 | R1, R3; core aim | Routing; Edge and Observation | Iskander | T03 |
| FR-04 | R3, R6; P02, P04; H2 data audit pending | Routing and route explanation; null attributes | Iskander | T04 |
| FR-05 | Evaluation design; P01, P02, P04 | Route API and summary; GraphSnapshot | Iskander and Altynay | T05 |
| FR-06 | Scope and constraint integrity | Routing and no-route screen | Iskander and Altynay | T06 |
| FR-07 | Agreed navigation scope; P03 | Foreground mobile GPS and instruction list | Altynay | T07 |
| FR-08 | R8; P01, P02, P04; assisted reporting P03 | Report service; BarrierReport and Photo | Alua and Altynay | T08 |
| FR-09 | Access decision; low-friction design decision | API authorization and mobile session | Alua | T09 |
| FR-10 | R5, R8; moderation and provenance design; P01, P04 | Moderator interface; ModerationAction | Alua | T10 |
| FR-11 | Report-aware routing objective | Report service and graph loader; snapshot versions | Alua and Iskander | T11 |
| FR-12 | Temporal design; moderation and provenance design; P01, P04 | Report lifecycle and edge eligibility | Alua and Iskander | T12 |
| FR-13 | R1, R3; data objective | Import pipeline; Observation and GraphSnapshot | Alua | T13 |
| FR-14 | R5; P04 freshness request | Barrier API and mobile detail screen | Alua and Altynay | T14 |
| FR-15 | Conditional lift scope | Verified connector and status observation | Alua and Iskander | T15 |
| NFR-01 | Proposed performance budget | API and routing | Iskander | T16 |
| NFR-02 | R15–R16; P03 | Mobile controls and semantics | Altynay | T17 |
| NFR-03 | Agreed two-platform scope | Mobile platform integrations | Altynay | T18 |
| NFR-04 | Evaluation reproducibility | Version manifests and benchmark harness | Iskander | T19 |
| NFR-05 | P01, P03, P04; data minimization decision | API, media handling and logs | Alua | T20 |
| NFR-06 | Report integrity decision | Upload validation and idempotency storage | Alua | T21 |
| NFR-07 | Mandatory acceptance gate | CI and fixture suites | All | T22 |
| NFR-08 | Recovery decision | Database and media backup | Alua | T23 |

Candidate extensions and their scope decisions are recorded in report section 2.3. Keep primary notes and do not infer universal numeric limits from these interviews.

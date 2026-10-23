## 6 Requirements specification

Must means required for the agreed final prototype. Should means desirable if the core requirements pass. All non-functional requirements are Must. The requirements incorporate the interview decisions in section 2.3. Interview support does not imply implementation or usability acceptance; further evaluation may revise them. Test IDs in section 9 provide traceability.

### 6.1 Functional requirements

| ID and priority | Requirement | Acceptance criterion |
| --- | --- | --- |
| FR-01 Must | Select and review four presets | All four presets are available and editable; reviewed constraints are saved and sent unchanged in a route request; T01 |
| FR-02 Must | Select origin and destination | Manual selection works without GPS; outside-area and unconnected points receive explicit errors; T02 |
| FR-03 Must | Enforce profile restrictions | Every returned route contains zero edges violating known hard constraints in fixtures; T03 |
| FR-04 Must | Handle unknown critical attributes | Strict mode excludes unknown required attributes; exploratory mode requires explicit selection and shows warnings; T04 |
| FR-05 Must | Explain route result | Distance, cost meaning, unknown-length share, snapshot ID and relevant warnings are shown; T05 |
| FR-06 Must | Handle no suitable route | Disconnected or blocked fixtures produce a no-route result without silently relaxing restrictions; T06 |
| FR-07 Must | Basic foreground guidance | With permission, position and next textual instruction update on a replayed GPS trace; inaccurate fixes trigger a warning; rebuilding requires an explicit action and never silently changes constraints; T07 |
| FR-08 Must | Submit a barrier report | Type, point, observation time and description validate; optional supported photo uploads; receipt confirms pending status; contributors can view their own pending, confirmed or rejected status; T08 |
| FR-09 Must | Provide low-friction access | Browsing and routing require no account; report submission requires an authenticated contributor; T09 |
| FR-10 Must | Moderate and audit reports | Only moderators may confirm, reject, resolve or mark stale; actor, time and reason are retained; T10 |
| FR-11 Must | Apply verified report changes | A new route request uses the committed report version; an already displayed route is labelled with its version and can be refreshed; T11 |
| FR-12 Must | Preserve lifecycle and uncertainty | Temporary stale reports become unresolved information; permanent barriers are not cleared merely by age; T12 |
| FR-13 Must | Import and inspect geodata | Import creates versioned nodes/edges and a completeness summary; malformed records are flagged; T13 |
| FR-14 Must | Show barrier details | Barrier card shows source, verification status and observation and verification dates without publishing contributor identity; missing dates are explicitly unknown; T14 |
| FR-15 Should | Verified external lift connectors | A connector is eligible only under documented profile and status rules; unknown operation is excluded in strict mode; T15 |

### 6.2 Non functional requirements

| ID | Proposed requirement and testable target |
| --- | --- |
| NFR-01 Performance | Route API p95 at most 2 seconds for a warmed graph of at most 50,000 directed edges, 10 concurrent clients and a declared 2-vCPU/4-GB test server; network time reported separately; T16 |
| NFR-02 Interaction | Touch targets at least 48 logical pixels; ordinary text contrast at least 4.5:1; 200% text scaling preserves key tasks; status has text and shape as well as colour; one-handed report entry is included in usability checks; T17 [R15–R16] |
| NFR-03 Platform and robustness | Core tasks pass on one recorded Android device and one iOS device or simulator; denied GPS/camera permissions and network errors have recoverable states; T18 |
| NFR-04 Reproducibility | Every benchmark records graph/report/profile versions, random seed, endpoints, algorithm and environment; reruns reproduce path cost within tolerance; T19 |
| NFR-05 Access and data minimization | Moderator mutations reject unauthorized requests; HTTPS for deployed traffic; photos remove EXIF; no continuous location history stored by default; T20 |
| NFR-06 Upload integrity | Accept only validated JPEG/PNG up to 5 MB; reject malformed uploads and duplicate submissions using an idempotency key; T21 |
| NFR-07 Test quality | All mandatory scenario tests pass; every known hard exclusion has a positive and negative fixture; failures are recorded rather than hidden by coverage percentage; T22 |
| NFR-08 Recovery | Restore the database and photo volume from a test backup and verify report/photo consistency; document observed recovery time; T23 |

The two-second target and graph limit are proposed acceptance targets, not benchmarks already achieved. Accessibility values are project targets informed by guidance; passing selected checks is not a claim of complete WCAG certification.

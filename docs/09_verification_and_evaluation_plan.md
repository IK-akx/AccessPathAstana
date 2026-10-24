## 9 Verification and evaluation plan

### 9.1 Test mapping

| Test IDs | Method | Evidence to retain |
| --- | --- | --- |
| T01–T06 | Unit and API fixtures for profiles, snapping, exclusions, unknowns, explanations and no-route cases | Fixture graph, expected result and automated log |
| T07 | Replay recorded or synthetic GPS traces with permission and accuracy variations | Trace, instruction sequence and screen recording |
| T08–T12 | Report lifecycle and authorization integration tests | API responses, audit log and route version change |
| T13–T15 | Import validation, barrier details and conditional lift fixtures | Import report and source/observation comparisons |
| T16 | Load test under declared server and graph conditions | Raw timings, concurrency configuration and p95 |
| T17–T18 | Accessibility and cross-platform scenario checks | Device/OS list, checklist and defects |
| T19 | Reproducibility rerun | Manifest, seeds and cost comparison |
| T20–T21 | Access control, image validation and metadata inspection | Rejected requests and stored-file inspection |
| T22–T23 | Mandatory suite and restoration rehearsal | Test summary and restore record |

Unit fixtures must cover a unique path, equal-cost alternatives, an unreachable goal, a directed slope, steps, kerb limits, unknown critical attributes, a confirmed closure and origin/destination splitting. Include adversarial topology such as crossing geometries at different levels. Test floating-point costs with an explicit tolerance; tied optimal paths may have different geometry.

### 9.2 Three separate comparisons

Algorithm baseline: Dijkstra against A* using exactly the same eligible graph, weights and request set. Primary correctness criterion is equal cost within 1e-6 × max(1, cost). Compare search time and vertices expanded; a speed-up is a hypothesis, not a required positive result.

Route-quality baseline: distance-only shortest path on the same pedestrian topology, without mobility-specific exclusions. Evaluate both outputs against the same independently audited constraints. Also report the shortest eligible route as a second reference for the cost of soft preferences. If the accessible system returns no route, count that explicitly; do not omit failed requests from the denominator.

External comparison: Google Maps and 2GIS on identical endpoints, dates and their available accessibility options. Since their graphs and costs are unknown, this is a descriptive comparison, not a controlled algorithm benchmark. Record unavailable service or absent output separately. Do not assert a win where route conditions have not been checked.

### 9.3 Measurement design

Select 20–30 origin–destination pairs spanning crossings, alternative paths, different surface conditions and incomplete data; apply all four frozen profiles. Reserve a separate set of at least ten pairs for tuning, where feasible, and do not tune on the final evaluation pairs. The actual sample and exclusions will be documented after the pilot audit.

Freeze graph, reports and profile configuration for each run. Record CPU, memory, OS, code commit, graph size, connected components and missing attribute rates. Use five warm-up runs and 30 timed repetitions per request per algorithm, randomizing order. Report median and p95, expanded vertices, route cost, no-route rate and cold-load time separately. Pair outcomes by request and avoid treating repeated timings as independent users.

Measure field agreement on an independently rechecked subset: a second team member audits the features without seeing the algorithm's recommendation, then disagreements are adjudicated. Define a barrier violation per traversed feature under a profile. Report both route-level violation rate and unknown-length share. A target of zero known hard violations is mandatory; a lower violation rate than the distance baseline is an evaluation hypothesis. Do not infer actual-world zero risk from zero fixture violations.

Detour ratio = accessible route length / distance-only route length, where both exist. Unknown-length share = length of segments missing at least one required attribute / total route length, counting each segment once. Report coverage and no-route rates beside detour statistics to avoid rewarding a system that simply refuses most requests.

Conduct formative usability tests with approximately five to eight volunteers if recruitment permits. Ask them to select a profile, plan a route, interpret uncertainty and submit a report in the prototype or app. Record task completion, errors, assistance and comments. A provisional target is at least 80% completion of core tasks without assistance; with a small sample report counts and avoid population claims. The requirements interviews in section 2 are not task-based usability tests; no actual usability results are available yet. Include hands-busy or one-handed operation and checking report status among the evaluated tasks.

### 9.4 Threats to validity

The pilot may not represent all Astana neighbourhoods. Data collected in one season cannot establish year-round accessibility. Convenience recruitment may miss important mobility needs. GPS errors, observer disagreement and stale barriers may affect outcomes. Product versions and provider data can change. We address these by publishing the evaluation envelope, dates, uncertainty, sampling procedure and failure cases. Weather prediction and automatic ice detection are outside scope; recent reports may describe conditions without guaranteeing completeness.

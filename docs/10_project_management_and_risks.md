## 10 Project management and risks

### 10.1 Repository and task workflow

The source package supplies documentation, editable diagrams, mockups, a README, task register and PR template. The team reports that YouTrack has been created and tasks assigned; its URL and actual task IDs have not yet been supplied for this package. The package itself is not a hosted GitHub/GitLab repository. Add the actual service links, verify access for each member and Islam Omirzak, and grant committee access before submission. Each member must use an individual account.

Create one task per meaningful deliverable with owner, priority, expected outcome, acceptance criteria and deadline. Use a branch such as AP-06-routing-model and reference the actual task key in commits and PRs. Proposed AP identifiers in the task register must be mapped to real YouTrack IDs when created. Review changes before merging into main; attach the PR link to the task and mark it complete only after acceptance.

The initial documentation package may be committed transparently as a starting draft. Subsequent research, corrections and design decisions should be contributed progressively by their actual authors. Do not backdate commits or attribute generated material to work that teammates have not reviewed. Tag the exact first submission pre-defense-1 only when ready; never move a submitted tag. Provide completed work, limitations and outstanding tasks with the tag.

### 10.2 Initial task register

| Proposed task | Owner | Due date | Acceptance outcome |
| --- | --- | --- | --- |
| AP-01 Repository and YouTrack setup | Iskander | 24 Oct 2026 | YouTrack created and tasks assigned per team; add actual URLs and verify repository/access |
| AP-02 Pilot boundary and feasibility audit | Alua | 24 Oct 2026 | Street boundaries agreed; encode polygon and audit data |
| AP-03 User consultation records | Altynay | 24 Oct 2026 | Four dated interviews summarized; retain notes, guide and consent record |
| AP-04 Literature and source review | Iskander | 22 Oct 2026 | Team checks eight scientific sources and synthesis |
| AP-05 Systems and technology decisions | Alua | 22 Oct 2026 | Four-system matrix and justified alternatives reviewed |
| AP-06 Routing model and test plan | Iskander | 23 Oct 2026 | Eligibility, cost, heuristic and fixtures agreed |
| AP-07 Requirements and traceability | Iskander | 23 Oct 2026 | Must criteria map to tests and components |
| AP-08 Architecture and data model | Alua | 23 Oct 2026 | Three diagrams and data relations reviewed |
| AP-09 Prototype walkthrough | Altynay | 23 Oct 2026 | Core scenarios and error states demonstrated |
| AP-10 Supervisor review | Iskander | 23 Oct 2026 | Actual comments and resulting decisions recorded |
| AP-11 Peer review and submission | All with Altynay coordinating | 24 Oct 2026 | Access checked, PRs reviewed, exact tag and presentation prepared |

These are proposed deadlines. Four interviews are summarized in section 2; completion of record checks and supervisor review must still be tracked. Do not mark outstanding evidence or review complete before it is available. The CSV in the package includes priority, dependencies, expected result and acceptance criteria.

### 10.3 Development milestones after submission

| Milestone | Proposed timing | Completion gate |
| --- | --- | --- |
| M1 Feasibility | Weeks 1–2 after submission | Pilot graph, Android/iOS build and one end-to-end route |
| M2 Core routing | Weeks 3–4 | Four presets, tested Dijkstra/A*, unknown handling and benchmark harness |
| M3 Reporting and client | Weeks 5–6 | Report moderation, map, foreground guidance and error handling |
| M4 Field and user evaluation | Weeks 7–8 | Frozen evaluation data, baseline comparison and usability records |
| M5 Final integration | Weeks 9–10 | Defects addressed, reproducible release and thesis results |

This ten-week sequence is a planning baseline, not an official defense calendar. Confirm institutional dates with the supervisor and adjust scope or timing before committing. Dependencies: requirements depend on consultation; graph construction depends on boundary and import; route evaluation depends on independent audit; report-aware integration depends on stable API and lifecycle rules.

### 10.4 Risk register

| Risk | Likelihood / impact | Owner | Trigger and response |
| --- | --- | --- | --- |
| Missing kerb or slope data | High / High | Alua | Completeness too low for connected strict routes; shrink core and audit critical crossings |
| Incorrect graph connectivity | Medium / High | Iskander | Route crosses fence or wrong level; add topology fixtures and field checks |
| Scope exceeds team capacity | High / High | Iskander | Core milestone slips; defer lifts and advanced navigation |
| Stale or false reports | Medium / High | Alua | Conflicting evidence; moderation, provenance and recheck queue |
| No iOS build/test access | Medium / High | Altynay | Week 1 build unavailable; arrange access early and report unresolved platform limitation |
| Limited follow-up and usability recruitment | Medium / High | Altynay | Initial four interviews completed; arrange follow-up clarification and later task-based testing; disclose missing validation |
| Seasonal changes | High / Medium | Alua | Field conditions differ; date snapshots and limit conclusions |
| GPS inaccuracy | Medium / Medium | Altynay | Position jumps or low accuracy; manual origin and uncertainty warning |
| Provider or deployment constraints | Medium / Medium | Alua | Tile/API terms or resources unsuitable; verify provider and keep configurable endpoint |
| Sensitive report photos | Medium / Medium | Alua | Personal details visible; restrict access, remove EXIF and moderate images |

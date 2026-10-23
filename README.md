# AccessPath Astana

Working title for a diploma project at Astana IT University. Supervisor: Islam Omirzak.

## Problem and users
We plan mobility-aware outdoor pedestrian routes for wheelchair users, people with child strollers, crutch users and older pedestrians. The prototype will explain known barriers and missing data rather than treating all walking paths as equally suitable.

## Expected outcome and scope
An Astana pilot bounded by Turar Ryskulov Street, Orynbor Street, Kabanbay Batyr Avenue and Mangilik El Avenue. The street boundaries are agreed; the GeoJSON polygon and network coverage still need verification. Four configurable profiles, Dijkstra/A*, moderated barrier reports, map and basic foreground guidance are planned. Indoor routing, citywide coverage and automatic live condition monitoring are outside scope.

## Team
- Iskander Kustayev: graph, algorithms and evaluation.
- Alua Sagyndyk: backend, geodata and deployment.
- Altynay Bolatova: mobile app, UX and cross-platform testing.
- All: user research, analysis, integration and thesis.

## Current status
Analysis and design package prepared on 20 October 2026 and revised on 23 October 2026. No application implementation or field dataset exists. Four interviews were conducted on 17–22 October 2026, with anonymized translated summaries and requirement decisions included. The team reports YouTrack creation and task assignment; its URL and actual IDs must be added. A hosted Git repository URL has not been supplied. Topic approval is reported by the team; substantive review of this package is pending.

## Proposed technologies
Flutter and flutter_map; Python/FastAPI with an internal routing package; PostgreSQL/PostGIS; REST/OpenAPI; Docker Compose. See docs/05_technology_comparison.md for alternatives.

## Documentation
- [Complete report](report.md)
- [Proposal](docs/01_project_proposal.md)
- [Requirements](docs/06_requirements_specification.md)
- [Architecture](docs/07_architecture_and_diagrams.md)
- [Evaluation](docs/09_verification_and_evaluation_plan.md)
- [References](docs/references.md)
- [Requirement traceability](management/traceability.md)
- [User interviews and decisions](management/user_interviews.md)
- Diagrams: editable SVG and Mermaid/PlantUML with PNG exports in diagrams/.
- Prototype: editable SVG and PNG sheets in prototype/.
- Tasks: management/youtrack_tasks.csv. Proposed IDs must be mapped to actual YouTrack IDs.

## Project links
GitHub/GitLab URL: not created yet.
YouTrack URL: created by the team; insert actual URL.
Supervisor review record: management/supervisor_review.md.

## Viewing and running
Open report.md in a Markdown viewer; open PNG/SVG files to inspect diagrams and mockups. There is no application code to execute or test yet. Add setup, dependency, execution and testing commands with the first runnable implementation.

## Contribution workflow
Create a task with owner, outcome, criteria and deadline. Work in an ID-named branch and link commits/PRs. Another team member reviews before merge into main. Record real progressive changes under individual accounts. Do not backdate work or invent review history. Tag the exact first submission pre-defense-1 when ready and keep submitted tags fixed.

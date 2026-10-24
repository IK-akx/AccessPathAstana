## 4 Existing system comparison

We compare four relevant systems across the same eight criteria. Google Maps and 2GIS are general navigation comparators; Wheelmap is an accessibility information comparator; openrouteservice is a technical accessible-routing comparator. This distinction prevents treating a place-rating service as though it promised a complete navigation workflow.

Legend: D = documented in the cited source; U = not established by the reviewed material, not proof of absence; P = proposed for AccessPath, not implemented. No hands-on Astana route comparison has yet been conducted.

| Criterion | Google Maps R9 | 2GIS R10 | Wheelmap R11 | openrouteservice R12 |
| --- | --- | --- | --- | --- |
| Main function | D navigation | D navigation | D place accessibility | D route engine/API |
| Pedestrian route generation | D | D | U | D |
| Stair avoidance | D where data available | D filter | U at route level | D route options |
| User-set slope and kerb limits | U | U | U | D wheelchair restrictions |
| Surface or smoothness restrictions | U | U | U at route level | D |
| Four proposed presets | U | U | U | U as this exact set |
| Accessibility contributions | D place attributes in R9 | U in reviewed page | D place ratings | OSM-based; app workflow U |
| Explicit unknown information | Local attribute coverage U | Local attribute coverage U | D unknown place rating | Attribute dependent; UI U |

For AccessPath all eight criteria are design targets, except that the main function is a bounded research prototype. Planned differences are explicit segment uncertainty, four reviewable presets and a documented report lifecycle linked to a local field-audited graph. These are requirements, not achieved advantages. In particular, stair avoidance is already available in both general navigation comparators.

Before the final defense, record product version, platform, date, selected route options, identical endpoints, route availability and permitted screenshots or manual observations. Keep unsupported cells marked U until evidence changes them. Do not rank a product poorly because a feature was not mentioned in a single help page. Route-level evaluation must distinguish missing service coverage from an actual failed route.

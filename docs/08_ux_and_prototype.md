## 8 UX and prototype

The supplied mockups are design prototypes with illustrative values and a schematic map, not measured routes. They cover profile selection, route planning, route review, guidance, barrier details, reporting, no-route feedback and moderation. SVG sources can be imported into a design tool and edited.

![Prototype screens one to four](../prototype)

![Prototype screens five to eight](../prototype)

Scenario U1: choose a wheelchair preset, review constraints, select two pilot points, build a strict route, inspect distance and uncertainty, then start guidance. If strict routing fails, explain missing or blocked information; offer changing endpoints or explicitly selecting exploratory mode without implying that it is verified.

Scenario U2: inspect a barrier card, choose report, confirm its location, select type, add description and optional photo, and submit. Show a pending receipt, provide access to the contributor's report status and explain that review is required before the report changes routing. If the user is not signed in, preserve the draft through sign-in.

Scenario U3: a moderator reviews evidence and location, checks conflicting observations, makes a decision with a reason and verifies the resulting route snapshot. The confirmation action has a clear consequence and cannot be triggered by an ordinary contributor.

Scenario U4: a user denies location permission and still selects a route manually. Guidance indicates that live position is unavailable. If GPS accuracy is poor, retain the route and avoid claiming a precise current step. Off-route detection offers a rebuild action rather than silently changing constraints.

Use large labelled controls, readable route text and non-colour status markers. Provide a textual route list as an alternative to the map. Review key screens at 200% text scaling and with TalkBack/VoiceOver. The mockups specify interaction intent; implementation and task-based user testing remain future work. Interviews support large controls, explicit uncertainty, a stable map and user-controlled route rebuilding. Voice guidance, voice reporting, benches, handrails, a help button and automatic profile expiry are future candidates, not functions demonstrated by these screens.

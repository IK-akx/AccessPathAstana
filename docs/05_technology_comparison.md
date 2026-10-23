## 5 Technology comparison

The following choices are proposed engineering decisions for this project. Documentation supports capabilities; suitability judgments reflect our scope and must be revisited after an initial integration spike. Versions will be pinned at implementation rather than claiming that the newest release is required.

### 5.1 Server platform

| Alternative | Fit to requirements | Cost or limitation | Decision |
| --- | --- | --- | --- |
| Python with FastAPI R17 | Typed request validation, OpenAPI, direct integration with Python graph code | CPU-heavy routing needs bounded workers and measurement | Selected for the pilot |
| TypeScript with NestJS R18 | Structured modules and a familiar JavaScript ecosystem | Python routing would add a language boundary, or need reimplementation | Viable alternative |
| Java with Spring Boot R19 | Structured application and strong backend tooling | More setup for this team's small Python-based evaluation workflow | Reserve alternative |

The backend will be a modular monolith with an internal routing package. This reduces deployment interfaces while retaining clear component boundaries. A separate routing service becomes justified only if measured load or independent deployment requires it.

### 5.2 Data storage

| Alternative | Fit to requirements | Cost or limitation | Decision |
| --- | --- | --- | --- |
| PostgreSQL with PostGIS R20 | Relational reports and audit records plus spatial distance queries | Server administration and migration discipline | Selected |
| SQLite with SpatiaLite R21 | Spatial SQL in a portable local file | Less aligned with concurrent server moderation and shared writes | Useful for local experiments |
| MongoDB R22 | GeoJSON and spatial querying with flexible documents | Relationship and validation rules would need a different modelling approach | Viable but not preferred |

PostGIS stores authoritative geometries; routing uses an in-memory adjacency representation derived from a versioned snapshot. Database spatial proximity does not by itself establish that two paths are connected.

### 5.3 Mobile platform

| Alternative | Fit to requirements | Cost or limitation | Decision |
| --- | --- | --- | --- |
| Flutter R16 | Shared Android/iOS interface and accessibility testing support | Team must learn Dart and verify native permissions | Selected |
| React Native R23 | Shared code and platform accessibility APIs | Platform-specific behaviour still needs testing | Viable alternative |

Use flutter_map for map display [R24], with a configured tile source and visible attribution. The map widget does not perform our accessible routing. Device GPS and camera integrations require an early Android/iOS proof of concept. Provider terms and available tile access must be checked before deployment; bulk offline tile downloads are outside scope.

### 5.4 Component interaction

| Alternative | Fit to requirements | Cost or limitation | Decision |
| --- | --- | --- | --- |
| HTTPS REST with JSON and OpenAPI R17 | Simple route/report operations, inspectable contracts and mobile integration | More verbose payloads | Selected |
| gRPC R25 | Typed RPC with generated clients | Additional tooling without an established pilot need | Reserve for later service separation |

Photos use multipart upload and private file storage on a backed-up server volume for the pilot. PostgreSQL stores file metadata and access permissions. Docker Compose is the proposed reproducible deployment method. Remote deployment is not established in this package; the repository URL must be added when available.

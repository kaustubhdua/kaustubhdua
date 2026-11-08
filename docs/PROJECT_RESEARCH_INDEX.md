# Project research and evidence index

Last reviewed: 8 November 2026

This is the detailed companion to the six-project Setlist in the profile README. Projects are ordered for resume value and engineering diversity, not commit volume or technology count. Repository READMEs, release gates and commit history remain authoritative. For team projects, claim only work supported by your own commits/PRs.

## Six featured projects

### 1. JIIT Youth Club 128 — official campus platform
**Story:** a real stakeholder-facing platform for the JIIT 128 campus ecosystem.

- **Engineering:** React 19, Vite, React Router, Supabase Cloud, PostgreSQL/RLS, Edge Functions, WebGL/OGL, GSAP/Motion, Sharp media derivatives, route-shell pre-rendering, PWA caching and accessibility.
- **Evidence:** [repository](https://github.com/kaustubhdua/JYC-Website) · [README](https://github.com/kaustubhdua/JYC-Website/blob/main/README.md)
- **Attribution/status:** official internal platform maintained by the authorized technical team; repository is closed to outside contributions. Attribute only personal modules and changes supported by your commit history. Do not claim sole authorship.

### 2. RideForge — transactional bike-taxi booking and dispatch
**Story:** systems-oriented multi-role backend with durable booking and driver-offer state.

- **Engineering:** C++17/Boost.Beast API, PostgreSQL transactions/migrations, React/TypeScript workspaces, Leaflet, routing providers, shortest-path logic, durable 45-second driver offers, expiry and sequential redispatch.
- **Evidence:** [repository](https://github.com/kaustubhdua/Smart_bike_taxi_platform) · [release-readiness evidence](https://github.com/kaustubhdua/Smart_bike_taxi_platform/blob/main/docs/RELEASE_READINESS_EVIDENCE.md) · [OpenAPI](https://github.com/kaustubhdua/Smart_bike_taxi_platform/blob/main/backend/openapi.yaml) · [CI](https://github.com/kaustubhdua/Smart_bike_taxi_platform/actions)
- **Boundary:** portfolio MVP, not a live commercial taxi service. Payments, real identity/vehicle checks and transport operations are outside scope.

### 3. BharatSim — Android resilience testing
**Story:** risk-first test planning and a worker/evidence pipeline for Android test execution.

- **Engineering:** FastAPI, React/TypeScript/Vite, PostgreSQL, APK validation and SHA-256 fingerprints, lease-based worker queue, heartbeats, guarded ADB runner, Android Emulator/Appium fixture workflow, logcat signal analysis and evidence synthesis.
- **Evidence:** [repository](https://github.com/kaustubhdua/Bharat-Sim) · [planner](https://github.com/kaustubhdua/Bharat-Sim/blob/main/docs/PLANNER.md) · [evidence synthesis](https://github.com/kaustubhdua/Bharat-Sim/blob/main/docs/EVIDENCE_SYNTHESIS.md) · [CI](https://github.com/kaustubhdua/Bharat-Sim/actions)
- **Boundary:** controlled-beta MVP. Fixture CI proves the source-built APK path only. Production APK execution remains gated on isolated worker infrastructure; production database/storage round trips are not yet accepted.

### 4. SATARK Sentinel — evidence-first incident investigation
**Story:** deterministic security triage that separates observations, interpretation, uncertainty and human decisions.

- **Engineering:** Python/FastAPI, Next.js/React, Streamlit legacy UI, FIRSTLIGHT investigation, SHA-256 artifact checks, evidence-linked findings, timelines, evidence-gap reporting, JSON export, bounded Linux endpoint sensor and optional self-hosted Ollama summaries.
- **Evidence:** [repository](https://github.com/kaustubhdua/Satark) · [FIRSTLIGHT scope](https://github.com/kaustubhdua/Satark/blob/main/docs/FIRSTLIGHT.md) · [native endpoint sensor](https://github.com/kaustubhdua/Satark/blob/main/docs/NATIVE_ENDPOINT_SENSOR.md) · [CI/security](https://github.com/kaustubhdua/Satark/actions)
- **Boundary:** prototype, not antivirus, full EDR, certified forensics or automatic containment. The FIRSTLIGHT audit chain is session-based; optional Defender/Entra adapters are not live-validated.

### 5. Saathi — local-first Hindi/Hinglish voice assistance
**Story:** multilingual assistant architecture with deterministic control, source provenance and replaceable provider adapters.

- **Engineering:** FastAPI/Python, Next.js/React/TypeScript, deterministic intent routing, local Vosk STT, eSpeak NG TTS, Tesseract OCR, optional Ollama, weather/mandi adapters, WebSockets and Exotel AgentStream.
- **Evidence:** [repository](https://github.com/kaustubhdua/Saathi) · [evaluation](https://github.com/kaustubhdua/Saathi/blob/main/docs/EVALUATION.md) · [voice runtime](https://github.com/kaustubhdua/Saathi/blob/main/docs/VOICE_RUNTIME.md) · [open-source architecture](https://github.com/kaustubhdua/Saathi/blob/main/docs/OPEN_SOURCE_FIRST.md)
- **Attribution/status:** multi-contributor MVP. Synthetic intent tests are not real-world speech accuracy; durable memory, provider-backed latency/accuracy and phone transport remain gates. Attribute your own work from commit history.

### 6. Smart Waste — collection operations and fleet optimization
**Story:** provenance-aware telemetry through prioritization, approved jobs, capacity-aware routes and dispatch.

- **Engineering:** FastAPI, PostgreSQL/PostGIS, SQLAlchemy/Alembic, device-scoped telemetry, freshness/idempotency checks, Sugeno prioritization, OSRM, OR-Tools CVRP, transactional dispatch and optional timestamp-aware Random Forest forecasting.
- **Evidence:** [repository](https://github.com/kaustubhdua/smart_waste_project) · [release checklist](https://github.com/kaustubhdua/smart_waste_project/blob/main/docs/RELEASE_CHECKLIST.md) · [security threat model](https://github.com/kaustubhdua/smart_waste_project/blob/main/docs/SECURITY_THREAT_MODEL.md) · [CI](https://github.com/kaustubhdua/smart_waste_project/actions)
- **Boundary:** engineering prototype on synthetic/demo data. No physical sensor calibration, municipal pilot, production restore drill or measured savings claim is established.

## Additional projects in the expanded profile

- **NIRDHOOM** — field-first crop-residue coordination across farmer requests, time-bound machine capacity, dispatch and traceable residue lots. Multi-contributor prototype; seeded/indicative records are not field-pilot outcomes. [Repository](https://github.com/kaustubhdua/nihdhoom) · [roadmap](https://github.com/kaustubhdua/nihdhoom/blob/main/docs/PRODUCT-RELEASE-ROADMAP.md)
- **PatchPilot** — deterministic explainable triage for untrusted PR diffs. No cloning or execution of submitted code; heuristic scores are not defect probabilities and production precision/recall are unestablished. [Repository](https://github.com/kaustubhdua/PatchPilot) · [benchmark methodology](https://github.com/kaustubhdua/PatchPilot/blob/main/docs/benchmark-methodology.md)
- **Adapt AI** — team-built hardware-aware local Ollama assistant with hardware profiling and streamed chat. Attribute contributions by commit history. [Repository](https://github.com/kaustubhdua/adapt-ai)
- **Infracis** — evidence-first location due diligence with observed facts, calculated metrics, rule-based interpretation and optional grounded AI narrative. Not a valuation or safety guarantee. [Repository](https://github.com/kaustubhdua/infracis) · [research](https://github.com/kaustubhdua/infracis/blob/main/docs/RESEARCH.md)
- **AkashChalak** — India-oriented NAQI and hotspot prototype using CPCB/FIRMS ingestion, IDW interpolation, HCHO/fire clustering and wind vectors. Decision support, not regulatory measurement. [Repository](https://github.com/kaustubhdua/Akash-Chalak)
- **GenomeGuard** — genomic-data governance research prototype exploring consent, access policy, auditability and privacy-aware workflows. Not a clinical diagnostic or production healthcare system. [Repository](https://github.com/kaustubhdua/GenomeGuard)
- **CrickVision** — local-first computer-vision toolkit using a generic pretrained person detector, heuristic shot-cut detection and optional temporary tracking. Cricket-specific accuracy and official statistics are not established. [Repository](https://github.com/kaustubhdua/CrickVision-)
- **JIIT Toppers** — student-entered academic workspace with grade/attendance calculations, CSV workflows and browser-local planners. Not an official JIIT portal; production readiness is not established. [Repository](https://github.com/kaustubhdua/Jiit-toppers-)
- **Weather Core Matrix** — vanilla JavaScript weather client with timeout and explicit network/error states; depends on public wttr.in. [Repository](https://github.com/kaustubhdua/weather-core-matrix)
- **Nord Studio Task Manager** — accessible browser task manager with priorities, filters and localStorage persistence. [Repository](https://github.com/kaustubhdua/nord-studio-task-manager)

## Display rules

- Keep six featured cards and a concise stack summary; put deep implementation detail in this index and the repositories.
- Preserve monochrome art, responsive two-column layout and lazy-loaded below-the-fold assets.
- Preserve team/fork attribution and prototype labels.
- Never turn synthetic benchmarks, sample records, model outputs or CI checks into real-world impact claims.
- Keep the project selection stable until a secondary project has stronger implementation and verification evidence than one of the six featured builds.

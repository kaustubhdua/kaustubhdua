# Featured projects — research and evidence index

Last reviewed: 8 November 2026

This document is the deeper companion to the six-project Setlist in the profile README. It is intended to help readers move from a short project card to the actual implementation, evidence and current maturity. Repository documentation takes precedence over this summary.

## Six featured projects

### JIIT Youth Club — campus platform
**Story:** a public campus information and community platform for the JIIT Youth Club 128 ecosystem.

- **Implemented scope documented by the repository:** society/hub discovery, events and fests, verified media archives, student council/faculty profiles, announcements and calendar views.
- **Engineering:** React 19, Vite, React Router, Supabase Cloud with RLS and Edge Functions, WebGL canvas interactions, image optimisation, route-shell pre-rendering, PWA caching and accessibility/performance workflows.
- **Attribution:** team platform; describe personal work only where supported by commit/PR history.
- **Evidence:** [repository](https://github.com/kaustubhdua/JYC-Website) · [source README](https://github.com/kaustubhdua/JYC-Website/blob/main/README.md)
- **Boundary:** repository is closed and maintained by the authorised JYC 128 technical team; it does not accept external PRs.

### NIRDHOOM — field-first crop-residue coordination
**Story:** connect the field request to machine capacity, dispatch, evidence, residue lots and buyer demand.

- **Engineering:** React/Vite, Supabase/PostgreSQL/PostGIS, RLS, Leaflet, device GPS, private evidence uploads with SHA-256, offline evidence queue, PWA and OR-Tools dispatch.
- **Differentiator:** explicit provenance and human verification across the residue lifecycle; remote-sensing detections are context, not proof about a specific field.
- **Evidence:** [repository](https://github.com/kaustubhdua/nihdhoom) · [product roadmap](https://github.com/kaustubhdua/nihdhoom/blob/main/docs/PRODUCT-RELEASE-ROADMAP.md) · [CI](https://github.com/kaustubhdua/nihdhoom/actions/workflows/ci.yml)
- **Boundary:** prototype/integration foundation; seeded records are not field-pilot outcomes, and payment/authoritative boundary/live-device gates remain.

### Saathi — voice-first multilingual assistance
**Story:** source-aware Hindi/Hinglish assistance with local speech defaults and explicit consent.

- **Engineering:** FastAPI, React/Next.js, deterministic intent routing, Open-Meteo and government mandi adapters, Vosk STT, eSpeak NG TTS, optional Sarvam voice/document adapters, Tesseract OCR and Exotel AgentStream.
- **Differentiator:** deterministic routing and source provenance keep factual answers independent from model guesses; local defaults avoid requiring hosted AI keys for the local speech/reasoning path.
- **Evidence:** [repository](https://github.com/kaustubhdua/Saathi) · [evaluation](https://github.com/kaustubhdua/Saathi/blob/main/docs/EVALUATION.md) · [local/open-source setup](https://github.com/kaustubhdua/Saathi/blob/main/docs/OPEN_SOURCE_FIRST.md)
- **Boundary:** MVP; synthetic intent tests are not speech-accuracy measurements. Durable household persistence, real provider tests and end-to-end phone latency/accuracy remain gates.

### PatchPilot — explainable PR triage
**Story:** deterministic review signals from untrusted unified diffs.

- **Engineering:** Python/FastAPI/CLI, strict schemas, bounded input, diff parser, path/dependency/test heuristics, evidence-linked findings, rate limiting, pytest/Ruff and non-root Docker.
- **Differentiator:** no cloning or executing submitted code; parser incompleteness is visible; findings link back to changed-file evidence.
- **Evidence:** [repository](https://github.com/kaustubhdua/PatchPilot) · [architecture](https://github.com/kaustubhdua/PatchPilot/blob/main/docs/architecture.md) · [benchmark methodology](https://github.com/kaustubhdua/PatchPilot/blob/main/docs/benchmark-methodology.md)
- **Boundary:** early MVP, no hosted demo; heuristic risk score and synthetic corpus do not establish production detection accuracy.

### RideForge — bike-taxi dispatch and routing
**Story:** transactional booking and expiring driver offers across passenger, driver and admin roles.

- **Engineering:** C++17/Boost.Beast, PostgreSQL, React/TypeScript, Leaflet, graph routing, durable 45-second offers, expiry and sequential redispatch.
- **Differentiator:** durable dispatch lifecycle and failure-path testing, not just a ride-booking UI.
- **Evidence:** [repository](https://github.com/kaustubhdua/Smart_bike_taxi_platform) · [release-readiness evidence](https://github.com/kaustubhdua/Smart_bike_taxi_platform/blob/main/docs/RELEASE_READINESS_EVIDENCE.md) · [OpenAPI](https://github.com/kaustubhdua/Smart_bike_taxi_platform/blob/main/backend/openapi.yaml)
- **Boundary:** portfolio MVP in progress; CI evidence is commit-specific and is not proof of commercial deployment.

### Smart Waste — collection operations and fleet optimisation
**Story:** telemetry → prioritisation → approved jobs → capacity-aware routes → driver completion.

- **Engineering:** FastAPI, PostgreSQL/PostGIS, SQLAlchemy/Alembic, device-scoped telemetry, freshness/idempotency checks, Sugeno prioritisation, OSRM, OR-Tools CVRP, transactional dispatch and optional Random Forest forecasting.
- **Differentiator:** provenance-aware readings and a persisted operational workflow, rather than a map-only simulation.
- **Evidence:** [repository](https://github.com/kaustubhdua/smart_waste_project) · [release checklist](https://github.com/kaustubhdua/smart_waste_project/blob/main/docs/RELEASE_CHECKLIST.md) · [CI](https://github.com/kaustubhdua/smart_waste_project/actions)
- **Boundary:** synthetic/demo data; no sensor calibration, field pilot, municipal deployment or measured savings claim.

## Additional projects shown in the expanded profile index

### SATARK Sentinel — incident investigation
Evidence-led security triage and FIRSTLIGHT incident workflow, with local deterministic checks, optional local Ollama, a bounded Linux endpoint sensor and evidence records. It is a prototype—not antivirus or certified forensics. [Repository](https://github.com/kaustubhdua/Satark) · [README](https://github.com/kaustubhdua/Satark/blob/main/README.md)

### Adapt AI — hardware-aware local assistant
Team-built local AI workspace that profiles RAM/VRAM, recommends a locally runnable Ollama model, streams chat, handles attachments and provides an in-browser Python execution surface. Model weights require an initial download; inference is local. Attribute work by commit history. [Repository](https://github.com/kaustubhdua/adapt-ai) · [demo video](https://manofdiamond.vercel.app/demo.mp4)

### Infracis — location due diligence
Evidence-first location comparison with observed facts, calculated metrics, rule-based interpretations, optional grounded AI narrative and explicit unknowns. It is not a property valuation, title verification, safety guarantee or investment recommendation. [Repository](https://github.com/kaustubhdua/infracis) · [research](https://github.com/kaustubhdua/infracis/blob/main/docs/RESEARCH.md)

### AkashChalak — satellite-assisted air-quality signals
India-oriented NAQI map and hotspot prototype combining CPCB/FIRMS ingestion, IDW interpolation, HCHO/fire clustering and wind vectors. Requires configured data-provider credentials for meaningful live data; interpolation and fallbacks must be labelled. It is decision support, not regulatory measurement. [Repository](https://github.com/kaustubhdua/Akash-Chalak)

### BharatSim — Android resilience testing
Controlled-beta Android testing MVP with constrained-device planning, APK validation, Failure DNA log analysis, Interaction Hunter, a lease-based worker protocol and local ADB/Appium execution evidence. Public planning preview is separate from authenticated persistence and isolated APK execution; production launch is not approved. [Repository](https://github.com/kaustubhdua/Bharat-Sim) · [release gates](https://github.com/kaustubhdua/Bharat-Sim/blob/main/docs/PRODUCTION_RELEASE_GATES.md)

### GenomeGuard — genomic data governance
Research prototype exploring consent, access policy, auditability, privacy-aware workflows and provenance-aware dataset intake. Its own documentation says the complete genomic policy engine and real participant consent/release workflow are not yet live. It is not a clinical diagnostic or production healthcare system. [Repository](https://github.com/kaustubhdua/GenomeGuard)

### CrickVision — cricket video computer vision
Local-first experimental toolkit using a generic pretrained person detector, heuristic shot-cut detection and optional temporary IoU tracking. Cricket-specific accuracy, ball tracking and official-statistics claims are not established. [Repository](https://github.com/kaustubhdua/CrickVision-)

### JIIT Toppers — student academic workspace
Student-entered academic records, attendance/grade calculations, CSV import/export, browser-local study/exam planners and a PYQ reference tracker. It is not an official JIIT portal; authentication, database isolation and production deployment remain release gates. [Repository](https://github.com/kaustubhdua/Jiit-toppers-)

### Weather Core Matrix — weather dashboard
Vanilla JavaScript weather client with URL-encoded city lookup, loading/error/timeout states and no build step. Depends on the public wttr.in service and is not safety-critical weather guidance. [Repository](https://github.com/kaustubhdua/weather-core-matrix)

### Nord Studio Task Manager — local task manager
Accessible browser task manager with priority, filters, completion state and localStorage persistence/error handling. Data stays on the user's device/browser. [Repository](https://github.com/kaustubhdua/nord-studio-task-manager)

## Display rules for the profile README

- Keep the six featured cards as the first scan; do not turn the README into a full repository dump.
- Keep the monochrome art and concise one-line descriptions; link the deep evidence index for readers who want implementation detail.
- Preserve explicit team/fork attribution and prototype labels.
- Keep the expanded projects list collapsible.
- Never turn synthetic benchmarks, sample records, model outputs or CI checks into real-world impact claims.
- Do not add projects that are not already part of the curated set; GitGlobe is intentionally excluded from the featured set.

# Repository-wide technology stack audit

**Audit date:** 2026-10-19  
**Scope:** 20 repositories visible under `kaustubhdua`. This is a repository-level inventory from root trees, project manifests where present, and existing project documentation—not a claim that every source line or deployment was executed. Stack labels describe code/configuration evidence, not necessarily production use.

## Portfolio-wide recommendation

The portfolio already spans full-stack web engineering, Python APIs and applied AI, data/optimisation, C++ algorithms, geospatial systems, and interactive graphics. The highest-value improvement is not to add arbitrary frameworks. It is to make every repository reproducible, testable, secure, deployable, and easy to evaluate.

Adopt a consistent baseline where it fits each project:

- **Every repo:** concise README with truthful status, architecture, setup, environment variables, screenshots/demo, test commands, known limitations, license, and contribution/security instructions.
- **Every executable project:** automated CI on pull requests; dependency lockfile; format/lint/type checks where applicable; unit tests; production build; secret scanning; dependency audit; pinned runtime/toolchain.
- **Every web app:** accessibility checks, mobile/browser E2E smoke tests, bundle/build budgets, error states, and a documented deployment/rollback path.
- **Every API/data service:** typed request/response contracts, input validation, authentication/authorization tests, timeouts and bounded resource use, structured redacted logs, migrations, and health/readiness checks.
- **Every AI/ML project:** dataset provenance, train/test separation, baseline metrics, reproducible seeds, model/data versioning, evaluation against failure cases, and explicit labeling of synthetic/demo data.
- **Every deployed project:** a documented live URL and a workflow that smoke-tests the deployed commit. Do not describe a project as production-ready solely because its build passes.

## Repository inventory and targeted next improvements

| Repository | Observed stack / focus | Highest-value next improvement |
|---|---|---|
| [kaustubhdua](https://github.com/kaustubhdua/kaustubhdua) | GitHub profile README, Markdown, SVG assets, GitHub Actions-generated profile visuals | Keep project/stack claims evidence-backed; automate broken-local-asset/link checks and verify generated-artifact workflows. |
| [GitGlobe](https://github.com/kaustubhdua/GitGlobe) | Interactive visual repository discovery; WebGL/3D and data pipeline structure | Document ingestion-to-visualisation data flow, add typed API schemas and deterministic fixture-based pipeline tests, and measure 3D rendering performance. |
| [nihdhoom](https://github.com/kaustubhdua/nihdhoom) | React 19, TypeScript 6, Vite 8, Supabase, Leaflet, Three.js, Vitest/Node tests, integrity/release scripts | Ensure CI uses `npm ci`, pin the Node 24 runtime, split CI into typecheck/test/audit/build gates, and add RLS integration tests for every data-owning role. |
| [Saathi](https://github.com/kaustubhdua/Saathi) | Python/backend, frontend, Streamlit, Docker Compose and Supabase project structure | Make the supported app entry point unambiguous; merge duplicate PR work only after conflict resolution and green tests; test multilingual fallbacks, consent, role boundaries, and external-provider failures. |
| [Satark](https://github.com/kaustubhdua/Satark) | Python, Streamlit, threat-intelligence and media/document processing, optional AI integrations, Supabase | Isolate untrusted file/URL processing, test SSRF and parser limits, pin dependencies, and publish an evaluation set with false-positive/false-negative measurements. |
| [adapt-ai](https://github.com/kaustubhdua/adapt-ai) | Python, FastAPI, Ollama/local inference, browser UI | Add provider-adapter contract tests, model availability/timeouts, deterministic mock mode, and benchmark latency/memory by hardware tier. |
| [JYC-Website](https://github.com/kaustubhdua/JYC-Website) | React/Vite, Supabase, Playwright, sitemap/media and extensive QA scripts | Reduce overlapping release scripts into one documented gate; keep production QA opt-in and environment-safe; test critical public routes and admin authorization. |
| [Smart_bike_taxi_platform](https://github.com/kaustubhdua/Smart_bike_taxi_platform) | C++17/CMake graph algorithms plus React/TypeScript web app, HTTP API, PostgreSQL, Playwright | Prove booking/driver-acceptance race safety with PostgreSQL concurrency tests, implement outbox delivery/reconnect recovery, and verify a clean deployed end-to-end ride lifecycle. |
| [smart_waste_project](https://github.com/kaustubhdua/smart_waste_project) | Python, Streamlit, pandas/NumPy/scikit-learn, fuzzy logic, optimisation, Docker and tests | Separate synthetic/demo data from real observations, version the pipeline inputs, add model baselines and leakage checks, and benchmark route/collection optimisation against a simple heuristic. |
| [AkashChalak](https://github.com/kaustubhdua/AkashChalak) | Python backend, React frontend, geospatial/air-quality decision-support, Docker | Establish one canonical repository (compare with [Akash-Chalak](https://github.com/kaustubhdua/Akash-Chalak)); document provider/source provenance and coordinate systems; test stale/missing sensor data and spatial boundaries. |
| [Akash-Chalak](https://github.com/kaustubhdua/Akash-Chalak) | Parallel project tree to AkashChalak: Python backend, frontend, geospatial analysis | Decide whether this is a fork, alternate deployment, or duplicate; add a canonical-source notice and keep issues/releases/roadmap in one place to avoid divergence. |
| [weather-core-matrix](https://github.com/kaustubhdua/weather-core-matrix) | Vanilla JavaScript, HTML/CSS, browser Fetch API | Add a package-free Node test suite for parsing, timeout, retry and empty/error states; handle API keys server-side if the provider requires secrecy. |
| [nord-studio-task-manager](https://github.com/kaustubhdua/nord-studio-task-manager) | Vanilla JavaScript, HTML/CSS, browser storage and filtering | Add tests for persistence/migrations, keyboard access, empty states and malformed storage; document browser-only limitations and export/backup behavior. |
| [skills-introduction-to-github](https://github.com/kaustubhdua/skills-introduction-to-github) | Git/GitHub learning exercise | Keep it intentionally minimal; avoid adding a needless application stack. Add a short note that it is a learning exercise if the README does not already make that clear. |
| [Jiit-toppers-](https://github.com/kaustubhdua/Jiit-toppers-) | Next.js 16, React 19, TypeScript, Prisma, Zod, ESLint, Node test runner | Commit and verify lockfile-based installs, run Prisma validation/generation against CI, add integration tests for database constraints and authorization, and document migrations/seeding. |
| [Portfolio-](https://github.com/kaustubhdua/Portfolio-) | React 19, custom build scripts/esbuild, custom WebGL voxel renderer, ESLint, Playwright | Treat the custom renderer as a systems/graphics showcase: document render loop and asset pipeline, test reduced-motion/fallback behavior, and track bundle and frame-time budgets. |
| [PatchPilot](https://github.com/kaustubhdua/PatchPilot) | Python 3.11+, FastAPI, Pydantic, CLI, pytest, Ruff, Docker | Add a fixture corpus of real-world diff shapes, property/fuzz tests for hostile diffs, calibrated precision/recall for risk signals, and a CI matrix for supported Python versions. |
| [inkloom](https://github.com/kaustubhdua/inkloom) | TypeScript workspace, pnpm, React/Vite, Drizzle/PostgreSQL, auth, Vitest/Playwright, Docker | Preserve the pnpm lockfile and use frozen installs; test tenant isolation and migrations, run end-to-end tests in CI, and document which services are required for local development. |
| [HEALCONNECT](https://github.com/kaustubhdua/HEALCONNECT) | Next.js/React-era app structure, JavaScript, Jest, Tailwind CSS, Arduino/IoT project folder | Remove generated build-output dumps and accidental OS files from version control; define a clear app architecture, reproducible install/build, sensor protocol contract, and device-simulation tests. |
| [Foodie](https://github.com/kaustubhdua/Foodie) | JavaScript web app, Vite, PWA/service worker, product data, Docker/Compose and tests | Remove `.DS_Store` and unused duplicate assets; replace placeholder tests with real behavior tests, verify offline/cache invalidation, and document API/data licensing and deployment. |

## Cross-repository consistency fixes

1. **Canonical project names:** use one canonical name and repository URL for every project. Resolve the duplicate AkashChalak/Akash-Chalak relationship.
2. **Lockfiles and runtime pins:** use the package manager already selected by each repository; do not mix npm and pnpm. Pin Node/Python versions and use clean-install CI commands.
3. **CI status visibility:** show only meaningful status badges from workflows that actually run on the default branch. Avoid decorative green badges without evidence.
4. **Security baseline:** enable secret scanning where available, dependency updates, minimal workflow permissions, and safe handling of untrusted uploads/URLs. Never commit real `.env` files or tokens.
5. **Deployment truth:** each project README should say whether it is a prototype, demo, staging deployment, or production service. A Dockerfile or deployment manifest alone does not prove a live deployment.
6. **Portfolio focus:** feature 4–6 flagship projects (GitGlobe, NIRDHOOM, PatchPilot, Inkloom, Satark, and the bike-taxi platform), with the remaining projects in an archive/experiments section. This gives reviewers a clear narrative instead of implying every repository has equal maturity.
7. **Stack signal quality:** list only technologies evidenced in the actual repository. Prefer a few deep, tested stacks and measurable outcomes over a longer badge wall.

## Suggested portfolio-wide release gate

For each active repository, the release gate should be the smallest meaningful deterministic command set:

- JavaScript/TypeScript: clean install, lint, typecheck, unit tests, production build, and targeted browser tests.
- Python: locked dependency install, Ruff, type checks if configured, pytest, API contract/security tests, and container build.
- C++: CMake configure/build, CTest, sanitizers, and reproducible benchmark artifacts.
- Data/ML: data validation, leakage checks, baseline comparison, deterministic evaluation, and a report with dataset provenance.
- Hardware/IoT: host-side protocol tests, simulator/fake sensor input, firmware compile, and documented hardware-in-the-loop limitations.

**Definition of done:** a repository is considered release-ready only when its clean setup, tests, security boundaries, build, deployment smoke test, and rollback/recovery story have evidence tied to a specific commit. This audit is a prioritized backlog; it does not claim all listed changes have already been implemented.

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
| [RideForge](https://github.com/kaustubhdua/Smart_bike_taxi_platform) | C++17/CMake graph algorithms plus React/TypeScript web app, HTTP API, PostgreSQL, Playwright | Prove booking/driver-acceptance race safety with PostgreSQL concurrency tests, implement outbox delivery/reconnect recovery, and verify a clean deployed end-to-end ride lifecycle. |
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


## CI signal snapshot observed during this audit

The following is a point-in-time observation of the latest few workflow runs exposed by GitHub Actions on each repository's default branch. It is not a statement that all workflows or all commits are green. Re-check each linked run before a release.

| Repository | Observed recent signal | Follow-up |
|---|---|---|
| [Profile README](https://github.com/kaustubhdua/kaustubhdua/actions) | Profile README QA and contribution-snake workflows passed on `530605d` (2026-10-19). | Keep this as the profile's own regression gate. |
| [smart_waste_project](https://github.com/kaustubhdua/smart_waste_project/actions) | Python CI, browser E2E and CodeQL passed on `8da2b1b`. | Preserve this multi-layer gate; add reproducible ML evaluation metrics. |
| [weather-core-matrix](https://github.com/kaustubhdua/weather-core-matrix/actions) | Latest observed CI passed on `b4873dd` (2026-10-19). | Re-run on current HEAD before a release; this confirms the recent test additions, not external weather-provider availability. |
| [nord-studio-task-manager](https://github.com/kaustubhdua/nord-studio-task-manager/actions) | Latest observed CI passed on `38cfe5b` (2026-10-19). | Keep storage validation and task-state contract tests; add browser-level interaction tests next. |
| [AkashChalak](https://github.com/kaustubhdua/AkashChalak/actions) and [Akash-Chalak](https://github.com/kaustubhdua/Akash-Chalak/actions) | Recent observed Python/frontend CI runs passed in late September/early October. | Choose one canonical source and re-run after consolidation. |
| [adapt-ai](https://github.com/kaustubhdua/adapt-ai/actions) | Latest observed Python CI passed on `c09d5c1` (2026-10-05). | Re-run on current HEAD. |
| [GitGlobe](https://github.com/kaustubhdua/GitGlobe/actions) | Latest observed CI passed on `ea7654f`; an earlier run failed. | Ensure the latest HEAD is tested and keep the earlier failure investigated rather than hidden. |
| [Satark](https://github.com/kaustubhdua/Satark/actions) | CI and CodeQL passed on `acea1e2` (2026-10-19). Production smoke remains red because no verified `SATARK_PRODUCTION_URL` repository variable is configured; the previous hard-coded aliases were invalid or pointed to a different app. | Configure the variable only after confirming the real production deployment; until then, make no live-service claims. |
| [JYC-Website](https://github.com/kaustubhdua/JYC-Website/actions) | CI is rerunning on `43e93e5` after stale media/hero contracts were aligned with the current implementation; CodeQL passed, and CI/browser/Lighthouse were still running at audit refresh. | Confirm every gate is green on the same head before release. |
| [NIRDHOOM](https://github.com/kaustubhdua/nihdhoom/actions) | Latest observed CI passed on `0d12e40` (2026-10-12). | Re-run on current HEAD. |
| [Smart bike taxi platform](https://github.com/kaustubhdua/Smart_bike_taxi_platform/actions) | Dependency audit, PostgreSQL migration smoke and C++ tests passed on `56e8b5a` (2026-10-19); later PR work is tracked separately. | Verify all workflows on the exact PR head and complete a clean end-to-end deployment smoke before release. |
| [JIIT Toppers](https://github.com/kaustubhdua/Jiit-toppers-/actions) | Latest observed CI runs failed on `00cd665` (2026-10-05). | **P0:** restore the CI gate before adding more features. |
| [Saathi](https://github.com/kaustubhdua/Saathi/actions) | Latest observed CI passed on `1342197` (2026-10-18). | Re-run after the next backend or dependency change. |
| [Portfolio](https://github.com/kaustubhdua/Portfolio-/actions) | Latest observed CI and deploy workflows failed on `04ca219` (2026-10-19); build job failed before exposing completed steps. | **P0:** inspect the run logs/runner availability, restore CI first, and make deployment depend on successful verification. |
| [PatchPilot](https://github.com/kaustubhdua/PatchPilot/actions) | CI, security and PR-analysis workflows passed on `6aae286` (2026-10-18). | Keep fixture-based regression tests and security gates. |
| [Inkloom](https://github.com/kaustubhdua/inkloom/actions), [HEALCONNECT](https://github.com/kaustubhdua/HEALCONNECT/actions), [Foodie](https://github.com/kaustubhdua/Foodie/actions) | HEALCONNECT CI passed on `f45235e` (2026-10-19). Inkloom and Foodie returned no Actions runs despite having workflow files. | Verify Actions enablement/branch filters for Inkloom and Foodie; don't infer pass/fail from an empty run list. |
| [skills-introduction-to-github](https://github.com/kaustubhdua/skills-introduction-to-github/actions) | The exercise workflow passed in June 2026. | This is a learning repository; no additional stack is needed. |

## Cross-repository consistency fixes

1. **Canonical project names:** use one canonical name and repository URL for every project. Resolve the duplicate AkashChalak/Akash-Chalak relationship.
2. **Lockfiles and runtime pins:** use the package manager already selected by each repository; do not mix npm and pnpm. Pin Node/Python versions and use clean-install CI commands.
3. **CI status visibility:** show only meaningful status badges from workflows that actually run on the default branch. Avoid decorative green badges without evidence.
4. **Security baseline:** enable secret scanning where available, dependency updates, minimal workflow permissions, and safe handling of untrusted uploads/URLs. Never commit real `.env` files or tokens.
5. **Deployment truth:** each project README should say whether it is a prototype, demo, staging deployment, or production service. A Dockerfile or deployment manifest alone does not prove a live deployment.
6. **Portfolio focus:** feature 4–6 flagship projects (GitGlobe, NIRDHOOM, PatchPilot, Inkloom, Satark, and the bike-taxi platform), with the remaining projects in an archive/experiments section. This gives reviewers a clear narrative instead of implying every repository has equal maturity.
7. **Stack signal quality:** list only technologies evidenced in the actual repository. Prefer a few deep, tested stacks and measurable outcomes over a longer badge wall.

## Follow-up changes made on 2026-10-19

- The profile README now features **PatchPilot**, the **Nether Portfolio**, and **RideForge** with project-specific stack summaries; the expanded stack notes keep technologies mapped to the repository where they are actually evidenced.
- Profile README QA passed on commit `8377f18049164c4281202aa25065c7f46aab8ef2`.
- `weather-core-matrix` and `nord-studio-task-manager` now have dependency-free Node contract tests for request bounds, safe rendering, storage validation, error handling and accessible state; their CI workflows run those tests.
- `Satark` received fixes to streaming request-bound assertions, protected FIRSTLIGHT browser-smoke behavior, and the Vercel production alias. Its current release is still blocked by missing dedicated Supabase tenant-isolation test credentials and browser media-fixture verification; production smoke must pass against the current deployment before it is considered released.
- `JYC-Website` received fixes to stale browser-test selectors and fallback alt text, hero-heading contrast, media classification of known infographics, and media QA contracts. The workflows triggered by these changes must finish green on the same head before release claims are made.
- `Portfolio-` is private and its latest GitHub Actions jobs did not execute their steps (the API reported runner ID 0), so the lockfile-export experiment could not produce a committed lockfile. Enable Actions/runner execution, then generate a genuine lockfile and migrate both CI and Pages build to `npm ci`.

These are recorded changes, not a claim that all 20 repositories are now production-ready. A green static check does not replace a working deployment, external credentials, or runtime verification.

- Follow-up: SATARK's browser/CI checks passed on `3c75b73`; the browser test now scopes its error branch to the media-review panel, avoiding unrelated page alerts. The documented Vercel URL returned 404, and the other hard-coded alias served JYC, so the production smoke gate now requires an explicitly verified `SATARK_PRODUCTION_URL` repository variable instead of guessing. Current CI/CodeQL pass on `acea1e2`; live deployment verification remains blocked pending that variable.
- Follow-up: the profile README now links its Profile QA workflow with a status badge and the Foodie stack notes reflect its actual package scripts rather than claiming GitHub Pages as its deployment tooling. Profile commit: `96fd086196b61abbcd82375d25bbe815f147f3e6`. The connector did not expose a check-run result for this push, so the badge—not this note—is the live workflow status source.
- Follow-up: Foodie's README no longer contains the malformed `<img src="(image.png>` fragment, its tooling section reflects Vite/Jest/Wrangler/Sharp, and checkout/tracking is explicitly described as demo-only unless integrations are validated. Commit: `5aa85a84026e8b11d5164d5540b10f2f774aab9`.

## Suggested portfolio-wide release gate

For each active repository, the release gate should be the smallest meaningful deterministic command set:

- JavaScript/TypeScript: clean install, lint, typecheck, unit tests, production build, and targeted browser tests.
- Python: locked dependency install, Ruff, type checks if configured, pytest, API contract/security tests, and container build.
- C++: CMake configure/build, CTest, sanitizers, and reproducible benchmark artifacts.
- Data/ML: data validation, leakage checks, baseline comparison, deterministic evaluation, and a report with dataset provenance.
- Hardware/IoT: host-side protocol tests, simulator/fake sensor input, firmware compile, and documented hardware-in-the-loop limitations.

**Definition of done:** a repository is considered release-ready only when its clean setup, tests, security boundaries, build, deployment smoke test, and rollback/recovery story have evidence tied to a specific commit. This audit is a prioritized backlog; it does not claim all listed changes have already been implemented.

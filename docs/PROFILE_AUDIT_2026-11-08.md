# Profile README audit — 2026-11-08

## Scope and method

Reviewed the `kaustubhdua/kaustubhdua` profile repository, README, linked project metadata and root READMEs, GitHub Actions workflows, and self-hosted SVG assets. The monochrome studio-motion work from PR #6 is now merged to `main`; this audit is being extended by the recruiter-hierarchy refinement branch.

The audit checks repository existence/visibility, fork status, documented project maturity, repeated or stale project entries, local asset references, contribution-card generation, SVG safety/accessibility, reduced-motion support, and CI evidence. It does **not** claim a pixel-perfect browser audit: GitHub's actual rendered profile still needs a manual light/dark/mobile preview.

## Portfolio corrections

The featured section now contains six distinct projects, with no duplicate PatchPilot entry or repeated project numbering:

| Project | Verified description boundary |
|---|---|
| GitGlobe | Public fork. The README now identifies it as fork-based work rather than implying sole ownership of the upstream project. |
| NIRDHOOM | Field-first crop-residue coordination prototype. Seeded/demo records are not field-pilot or commercial evidence. |
| Saathi | Production-shaped prototype. The README distinguishes working local/default paths from hosted providers, persistence and deployment gates. |
| PatchPilot | Early MVP for explainable diff triage. It is not a security verdict; production precision/recall are not established. |
| RideForge | Portfolio MVP in progress, with C++ API, PostgreSQL workflows, driver dispatch and routing. |
| Smart Waste Collection | Engineering prototype using synthetic demo records; no municipal deployment, sensor calibration or operational savings are claimed. |

Secondary work remains in the expandable archive. Fork-based/team projects are labelled accordingly.

## Accuracy and link cleanup

- Removed the duplicate PatchPilot feature row and repaired the 05/05 numbering error.
- Removed duplicate Weather Core Matrix and Nord Studio Task Manager rows from the stack index.
- Removed the unused 90-day activity-chart workflow and its obsolete combined project-artwork asset; the README now uses the self-hosted overview/lifetime cards and six individual project illustrations.
- Removed stale links to repositories that returned 404 during this audit: Foodie, HEALCONNECT and Inkloom.
- Replaced the legacy AkashChalak link with the active Akash-Chalak repository.
- Removed the inaccurate `private` label from Portfolio- after checking repository metadata.
- Kept the stack inventory tied to project documentation and labelled prototype/team/fork boundaries.

## Contribution and statistics cards

The profile now uses the open-source [Profile Cards Action](https://github.com/seijikohara/profile-cards-action) to generate self-hosted SVG cards from GitHub GraphQL data.

- `overview.light.svg` and `overview.dark.svg`: profile overview statistics.
- `lifetime.light.svg` and `lifetime.dark.svg`: year-by-year contribution history.
- A scheduled workflow refreshes both cards daily and can also be run manually.
- The workflow uses the repository-scoped `GITHUB_TOKEN`, minimum `contents: write` permission, a commit-only-if-changed step and retry/rebase handling for concurrent branch updates.
- The generator's green activity palette is post-processed into a neutral silver/grey ramp to preserve the profile's monochrome identity.
- Generated SVGs are checked for XML validity, reduced-motion support, executable elements, external resource references and unconverted palette colors.

GitHub contribution timestamps use UTC. Private contribution visibility depends on the user's profile setting; the profile card action documents whether private contributions were included. See [GitHub's contribution documentation](https://docs.github.com/en/account-and-profile/concepts/contributions-on-your-profile).

## Visual asset and README QA

Six dedicated project SVGs now represent GitGlobe, NIRDHOOM, Saathi, PatchPilot, RideForge and Smart Waste. They are authored decorative illustrations—not screenshots or claims of live product telemetry.

The profile QA workflow validates:
- original hero banner remains present exactly once;
- six featured artwork assets and project descriptions are present;
- featured numbering is unique and sequential;
- project and stack-index links are explicit and non-duplicated;
- local asset references and in-page anchors resolve;
- SVG XML, IDs, accessible title/description, no script/foreignObject, and reduced-motion rules;
- self-hosted overview/lifetime cards remain monochrome and self-contained;
- remote images return a successful response or a temporary-unavailability warning.

Latest confirmed QA: [Profile README QA run](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42418002455). It checked 29 local asset references, 4 internal anchors, 18 curated repository links, 38 SVG files and 15 remote image URLs. The previous Unicode URL warning was removed by simplifying the badge label to ASCII; the latest run completed without that warning.

## Recruiter-hierarchy refinement (8 Nov 2026)

The next pass applies design patterns found in current profile README galleries and animated-profile writeups: a clear first-screen identity, compact focus areas, a small core tool set, and optional detail rather than a wall of badges. Motion remains self-hosted SVG so the README does not depend on embedded JavaScript.

- Added direct GitHub, LinkedIn and email links near the profile introduction.
- Reframed the intro around three concrete themes: full-stack product work, applied AI/data, and reliability/open source.
- Kept a 12-tool core stack visible and moved the exhaustive tool inventory into a collapsible section; the repository-by-repository evidence table remains available below it.
- Preserved the monochrome palette, original banner, guitar illustration, Studio Loop vinyl/waveform animation, Iris listening links, contribution snake and self-hosted contribution cards.
- Extended profile QA to guard the new first-screen links and focus areas, compact stack treatment, and the music identity/listening links.

The music section is intentionally unchanged in this refinement. Its animated guitar and vinyl artwork is decorative motion; the Spotify and YouTube links remain the actual listening destinations.

## Remaining checks before merge

1. Run the latest-head profile QA workflow and resolve any failures.
2. Preview the GitHub-rendered profile in light mode, dark mode and a narrow/mobile viewport. Source-level CI cannot fully prove GitHub's final rendering.
3. Recheck external streak, badge and music destinations periodically; those remain external runtime dependencies.
4. Confirm the scheduled contribution-card workflow continues to refresh the self-hosted assets on `main` after merge.

## Review boundary

The original monochrome studio-motion work is merged on `main`. The recruiter-hierarchy refinement is isolated to `refine/monochrome-recruiter-profile-20261108` pending its latest-head QA and rendered-profile review.

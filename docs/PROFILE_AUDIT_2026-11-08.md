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

## Final state — 8 Nov 2026

- Recruiter-hierarchy refinement PR [#7](https://github.com/kaustubhdua/kaustubhdua/pull/7) was merged to `main` as `5518ce829313b19ac936470d7ebcf692f0a11267`.
- Latest-head Profile README QA [run #480](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42485267431) completed successfully. The job passed the new quick-link, three-part focus, compact-stack and music-preservation assertions, plus the existing README, link, SVG safety/accessibility, reduced-motion, monochrome palette and external-image checks.
- The job checked 29 local asset references, 4 internal anchors, 18 curated repository links, 38 SVG files and 15 remote image URLs.
- The music section was byte-for-byte unchanged by the README refinement. Spotify and YouTube links remain present; the guitar and Studio Loop animations remain self-hosted.

## Remaining manual checks

1. Preview the GitHub-rendered profile in light mode, dark mode and a narrow/mobile viewport. Source-level CI cannot fully prove GitHub's final rendering. Automated hosted page inspection was unavailable during this pass because the connected browser-research service had exhausted its daily credits.
2. Recheck external streak, badge and music destinations periodically; those remain external runtime dependencies.
3. Confirm the scheduled contribution-card workflow continues to refresh the self-hosted assets on `main`.

## Review boundary

The monochrome studio-motion work and recruiter-hierarchy refinement are both merged to `main`. No changes were made to the separate `Portfolio-` repository.


## Visual restraint pass — 8 Nov 2026

A follow-up polish pass reduces decorative repetition without changing the profile's monochrome identity or removing its music feature:

- Kept the original supplied banner and the cinematic monochrome identity header; removed the extra animated audio ticker and duplicate academic kicker from the opening stack.
- Kept the guitar-studio illustration, the vinyl/waveform Studio Loop and the real Spotify/YouTube listening destinations for “Iris”.
- Removed the third fretboard-progress illustration from the music section. The guitar and record visuals now carry the music story without repeating the same motif.
- Reduced identical signal-chain section transitions from four to two, retaining the chapter breaks around the personal music and contribution sections.
- Tightened the music caption to explain its role as a reset between builds rather than adding another decorative slogan.
- Strengthened Profile README QA to enforce this visual restraint and to validate all four light/dark contribution-card SVGs. The previous workflow accidentally checked only the dark variant because its validation body sat outside the inner theme loop.
- Corrected SVG QA regular expressions so script/foreignObject and CSS fragment references are checked as intended.

The change is deliberately a subtraction pass: no new colour, external music embed, autoplay, JavaScript, or additional animation has been introduced.

## Verification

The updated Profile README QA workflow is the release gate for this pass. A passing run will validate the README references, all project links, SVG XML/accessibility/reduced-motion rules, monochrome generated cards in both themes, and remote image endpoints. GitHub's rendered light/dark/mobile preview remains a separate manual check; source-level validation cannot prove GitHub's final layout.


## Final verification — 8 Nov 2026

The final refinement is merged to `main` as [PR #13](https://github.com/kaustubhdua/kaustubhdua/pull/13), merge commit `19f08980d41562772d987d1f123a9fc026d55de5`.

### Mobile presentation

- Changed the six featured artwork cards from a cramped three-column table to a two-column, three-row grid. Each artwork is now approximately 127 CSS pixels wide in the 390px mobile viewport, instead of roughly 80px.
- The project detail cards remain a two-column table; project scope and maturity labels are unchanged.
- Preserved the monochrome palette, original hero banner, cinematic header, guitar illustration, vinyl/waveform loop, Iris listening links and limited section transitions.
- Clarified that the Iris track display inside the guitar artwork is decorative, not a functional player. Spotify and YouTube are the listening destinations.
- Reworded the statistics console so it no longer implies daily live telemetry: self-hosted profile cards refresh daily, the language card weekly, and the streak card is provided by an external service.

### Actual GitHub-style browser rendering

Added `.github/workflows/profile-render-qa.yml`. It renders the checked-out README using GitHub's GFM Markdown API, injects that HTML into GitHub's own public profile page styling, resolves artwork against the checked-out branch, and runs Playwright at four combinations:

- Desktop: 1440 × 1000, light and dark.
- Mobile: 390 × 844, light and dark.

The browser job checks the real rendered content, both listening destinations, all local README artwork, browser page errors, document horizontal overflow, the two-column/three-row featured grid and mobile artwork width. It uploads four screenshots as a 14-day workflow artifact.

Latest main-branch run: [Profile rendered browser QA](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488011000). All four cases passed:
- 99 README images found per rendered page; no broken local artwork.
- No browser page errors.
- Document width matched the viewport at both desktop and mobile sizes; no horizontal page overflow.
- The six featured project images rendered as two columns by three rows.
- Mobile artwork width: 127px per project card.
- Featured project section, Iris section, Spotify link and YouTube link were present in every case.

The generated desktop/mobile light/dark screenshots are available in the [rendered profile artifact](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488011000/artifacts/13620327360).

### Final workflow verification

All four workflows passed on main commit `19f08980d41562772d987d1f123a9fc026d55de5`:
- [Profile README QA](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488011029)
- [Profile rendered browser QA](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488011000)
- [Contribution history refresh](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488011096)
- [Contribution snake generation](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488011085)

The contribution-history refresh no longer suppresses all CI with `[skip ci]`; the snake generator now runs on its schedule, manually, or when its own workflow changes, rather than on every unrelated push. The browser workflow uses Node 24-compatible first-party actions.

### Remaining external dependencies

The profile itself and its self-hosted SVG artwork are checked in the repository. The following are external services and can still have independent outages or rate limits: Shields.io badges, Spotify/YouTube destinations, the streak card provider, the original banner CDN and GitHub-hosted raw asset delivery. These cannot be guaranteed by repository CI.

No repository-side blocker remains from the source, content, link, SVG, mobile-layout or rendered-browser checks completed here. Private contribution visibility remains controlled by GitHub account/profile settings. The separate `Portfolio-` repository was not changed.



## Final maintenance hardening — 8 Nov 2026

A final workflow review found that the weekly language-card generator still used the older checkout action and pushed generated SVGs without rebasing. This left one inconsistent action version and a possible race with the daily contribution-history refresh.

- Updated the language-card workflow to `actions/checkout@v7`, matching the Node 24-compatible action baseline used by the other profile workflows.
- Added a bounded job timeout and branch-scoped concurrency.
- Added fetch/rebase/retry handling before publishing the generated language SVG, preventing unrelated concurrent profile updates from causing avoidable push failures.
- Extended the Profile README QA assertions to guard the action version and safe-push contract.
- Merged as [PR #15](https://github.com/kaustubhdua/kaustubhdua/pull/15), commit `7f353211fb7fd5efa705c0ea3630a240a7b0e4e3`.
- The PR QA passed: [run 42488741281](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488741281).
- The merged language-card workflow completed successfully, including fetching repository language totals, validating the generated SVG and committing the refreshed monochrome card: [run 42488777101](https://github.com/kaustubhdua/kaustubhdua/actions/runs/42488777101).

The profile README, original banner, monochrome palette, guitar/vinyl music treatment and listening links were not changed in this maintenance pass. The separate `Portfolio-` repository remains untouched.

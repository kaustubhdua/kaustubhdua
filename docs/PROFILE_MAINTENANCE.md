# Profile README maintenance

The profile README is a concise, evidence-backed index of work—not a substitute for each project's repository documentation.

## Before changing project claims

- Confirm the repository exists and is public under the linked name.
- Read its current default-branch README and inspect fork/ownership metadata.
- Distinguish individual work, fork-based contributions, team projects, prototypes, demos and production deployments.
- List only technologies evidenced in the repository's current code, manifests or documentation.
- Keep the featured set to six projects; move secondary work to the expandable archive.
- Check the stack index for duplicate rows and remove links to deleted or inaccessible repositories.

## Visual and accessibility checks

- Preserve the original monochrome, music-inspired profile identity and hero banner.
- Preview the README in GitHub light and dark themes and at mobile widths.
- Give informative images meaningful alt text; decorative artwork must not carry factual project claims.
- SVGs must parse as XML, have unique IDs, accessible title/description labels, no scripts or external resource references, and a `prefers-reduced-motion` fallback.
- Keep the README understandable if an external badge or image provider is unavailable.

## Automated checks

- `.github/workflows/profile-qa.yml` validates project references, local assets, in-page anchors, SVG structure/accessibility, animation fallbacks, duplicate featured entries and remote image availability.
- `.github/workflows/profile-history.yml` runs daily and on manual dispatch. It generates self-hosted overview and lifetime contribution SVGs for light and dark themes, applies the neutral studio palette, validates the SVGs and commits only changed cards.
- `.github/workflows/language-card.yml` refreshes the monochrome language card.
- `.github/workflows/snake.yml` refreshes the contribution snake using the existing palettes.
- The README's remaining streak card, badges and music links depend on their external providers. A passing profile QA run is a point-in-time smoke test, not a guarantee that third-party services will always render.

## Contribution data

GitHub timestamps contribution activity in UTC. Public and private contribution visibility depends on the profile's privacy setting; private details remain anonymized. The generated overview/lifetime cards are sourced from GitHub's GraphQL contribution data. Never invent counts or replace a failed live data fetch with fabricated values.

A README commit appears on the profile contribution graph only when GitHub's contribution requirements are met. Confirm the commit author email is linked to the account and allow time for the graph to refresh.

## Release discipline

- Keep substantial redesign work in a reviewable branch and draft PR.
- Require the latest PR head's QA run to pass.
- Inspect the rendered profile manually in GitHub before merging.
- Do not merge or alter the live profile without explicit approval.

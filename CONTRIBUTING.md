# Contributing

Thank you for your interest. This list is curated, not collected — every entry is personally vouched for and pruned regularly when projects fall out of maintenance.

## Inclusion criteria

Every entry must satisfy all of the following:

1. **Directly useful to developers building SP-API integrations.** Seller-facing SaaS (repricers, inventory tools, advertising tools, analytics dashboards) is out of scope, regardless of quality.
2. **Actively maintained.** For libraries: a release within the last 12 months *or* clear evidence the project tracks recent SP-API model changes (e.g., supports current API versions like Orders v2026-01-01 or Listings 2021-08-01). For documentation/guides: content updated within the last 18 months and not pointing to deprecated APIs.
3. **A README that lets a developer evaluate the project in 60 seconds.** Code examples, install instructions, and scope statement.
4. **A declared license.**
5. (For libraries) **CI on the default branch.**
6. (For documentation) **Not pointing to decommissioned resources** (e.g., no links to `amzn/selling-partner-api-docs`, which was decommissioned May 31, 2024).

## What gets rejected

- **Seller-facing SaaS or paid services.** Use the [Amazon Selling Partner Appstore](https://developer.amazonservices.com/) instead.
- **Forks without meaningful divergence from upstream.** If your fork only updates dependencies, contribute upstream.
- **Repositories that are archived or have no commits in the last 24 months.**
- **Libraries whose README explicitly recommends migrating away** (we follow that recommendation).
- **Awesome lists or directories that link to dead projects** without active pruning.
- **Anything in violation of Amazon's Acceptable Use Policy.**

## How to add an entry

1. Open a PR adding your entry alphabetically within its language or category section.
2. Use the format `- [Name](url) - One sentence ending in a period.`
3. Run `npx awesome-lint` locally — CI will fail otherwise.
4. In the PR body, briefly explain why the resource belongs and link to evidence of recent activity (latest release, recent commits, current API version coverage).

## Removal criteria

Entries are removed when any of the following becomes true:

- The repository is archived or marked deprecated by the maintainer.
- There has been no release for 12+ months *and* no commit activity for 6+ months.
- The library's documentation still points to deprecated SP-API endpoints or to the decommissioned `selling-partner-api-docs` repository.
- A clearly-superior maintained alternative exists (the inferior project is removed in favor of the active one).

PRs to remove entries, including the curator's own projects, are welcome. The curator's projects are subject to the same removal criteria as everyone else's.

## Examples of recent prunings (rationale documented for transparency)

These projects appeared in earlier versions of this list or in adjacent SP-API resource lists; they have been deliberately excluded from this list because they fail the criteria above:

- `clousale/amazon-sp-api-php` — last release 2022; the project's own README recommends migration.
- `ScaleLeap/selling-partner-api-sdk` — repository is marked **Public archive**.
- `ericcj/amz_sp_api` — open issues unresolved since 2021; superseded by `lineofflight/peddler` for active Ruby development.
- `penghaiping/amazon-sp-api` — documentation links to decommissioned `selling-partner-api-docs`; Amazon's official Java SDK is now the recommended path.
- `ansas/amazon-selling-partner-api` — operations frozen at the November 2022 SP-API snapshot; downstream of `jlevers/selling-partner-api` without tracking new endpoints.
- `vikingcodes/awesome-spapi` — outdated awesome-list with dead-repo links and no maintenance.

If you believe any of these now meet the criteria, open a PR with current evidence.

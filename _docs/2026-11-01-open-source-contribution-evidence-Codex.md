# 2026-11-01 Open-source Contribution Evidence — Codex

- **Date**: 2026-11-01 JST
- **Implementer**: Codex

## Overview

Updated the profile README and added static SVG visuals to show Hermes Agent and Strata contributions with separate credit and review states. Fixed previously broken image references. No application code, dependency, test, or release changes were made.

## Background / Requirements

- R-01: Make Hermes Agent and Strata work immediately visible on the GitHub profile.
- R-02: Include authored commits, co-author trailers, maintainer committers, and salvage/continuation lineage.
- R-03: Show PR states separately from authorship and distinguish merged, open, and closed-without-merge work.
- R-04: Use source-backed, dated counts and preserve original authorship where a maintainer committed a change.
- R-05: Ensure every README-local image path resolves to a repository asset.

## Assumptions / Decisions

- Public GitHub records were checked on 2026-11-01 JST. Counts are a dated snapshot and can change later.
- A `Co-authored-by` trailer is an additional credit signal on an existing commit, not an extra commit.
- A maintainer commit with `zapabob` in the author field is credited as author-originated and maintainer-committed.
- A PR description that mentions salvage documents the stated lineage only. It is not proof that every patch was accepted upstream.
- PR state is presented independently from commit presence. In particular, Strata PR #3954 is closed without a merge record, while its author-preserving commit is present in the upstream repository.
- Categories overlap and dashboard counts must not be summed.

## Applied Standards and Skills

- `C:\Users\downl\AGENTS.md`, `C:\Users\downl\.codex\AGENTS.md`, and canonical pre-implementation context `C:\Users\downl\_docs\prompts\CLAUDE-FABLE-5.md`.
- SOPs: Common MILSPECLLMOps Engineering Standard, Implementation Start Gate, Skill Selection, Deep Research, WebApp Development, Frontend Design, and Internet Connectivity.
- Skills: `milspec-codex-standard`, `deepresearch-defense-standard`, `frontend-ui-engineering`, `documentation-and-adrs`, and `agent-self-review-evolution` (review-only).
- Repository-local `AGENTS.md` and `DESIGN.md`: not present in the checked-out repository.

## Sources Checked

- [Hermes Agent author commits](https://github.com/NousResearch/hermes-agent/commits/main/?author=zapabob): 18 commits in the upstream `main` author-filtered history; 14 have maintainer committers and 4 carry co-author trailers.
- [Hermes Agent authored PR search](https://api.github.com/search/issues?q=repo%3ANousResearch%2Fhermes-agent+author%3Azapabob+is%3Apr): 164 PRs; 5 open and 1 merged, leaving 158 closed without merge.
- [Hermes salvage-description search](https://api.github.com/search/issues?q=repo%3ANousResearch%2Fhermes-agent+author%3Azapabob+is%3Apr+salvage+in%3Abody): 22 PR descriptions mention salvage.
- [Hermes merged PR #68382](https://github.com/NousResearch/hermes-agent/pull/68382): merged 2026-07-29.
- [Hermes salvage PR #114613](https://github.com/NousResearch/hermes-agent/pull/114613) and [#70343](https://github.com/NousResearch/hermes-agent/pull/70343): both closed without merge; descriptions preserve explicit lineage. The #114613 description credits [open PR #63418](https://github.com/NousResearch/hermes-agent/pull/63418), authored by OmarB97.
- [Strata fork-to-upstream comparison](https://api.github.com/repos/Niko1221/Strata/compare/main...zapabob%3Amain): 208 commits ahead, 0 behind; all 208 identify `zapabob` as author and 33 carry co-author trailers.
- [Strata PR #3954](https://github.com/Niko1221/Strata/pull/3954): closed without merge record. Its change appears in [upstream commit c7833932](https://github.com/Niko1221/Strata/commit/c7833932a1a3515bb6e4f4c27255f4bb90a53fc4), authored by zapabob and committed by Niko1221.
- [Strata PRs #4248](https://github.com/Niko1221/Strata/pull/4248), [#4249](https://github.com/Niko1221/Strata/pull/4249), and [#4250](https://github.com/Niko1221/Strata/pull/4250): open at the snapshot date.
- Repository base revision: `883a82244a2775d2cd8dad9dca268d4da52eea36`.

## Changed Files

- `README.md`
- `assets/hermes-portfolio-hero.svg`
- `assets/hermes-contribution-map.svg`
- `assets/hermes-impact-dashboard.svg`
- `_docs/2026-11-01-open-source-contribution-evidence-Codex.md`

## Implementation Details

- Replaced the README's incorrect asset references with three assets that now exist.
- Added a contribution map that pairs project context with authored, co-authored, maintainer-committed, salvage, and PR-state evidence.
- Added a status dashboard that separates upstream Hermes PR outcomes from Strata fork development and upstream commit evidence.
- Rewrote public-facing claims to label the snapshot date, distinguish closed-unmerged proposals, and avoid presenting PR volume as accepted work.
- Kept the prior unrelated SVG assets in place; they are no longer referenced by the README.

## Commands Run

```text
git remote add origin https://github.com/zapabob/zapabob.git
git fetch --no-tags origin main
git switch --track -c codex/open-source-contribution-visualization origin/main
git rev-parse origin/main
git log -1 --format="%h %cI %s" origin/main
README-local SVG reference check: all 3 referenced files exist
System.Xml XML parsing: all 3 new SVGs have an svg root, title, and description
Whitespace scan: all changed text and SVG files passed
git diff --check: passed
CUA browser preview attempt: no iab browser surface available
```

## Test / Verification Results

Static validation passed: all README-local image paths resolve; the three added SVGs parse as XML and each has an accessible title and description; the changed files have no trailing whitespace; and `git diff --check` passed. An initial whitespace scan found two Markdown hard-break spaces in this log; they were removed, and the final scan passed. No automated tests were added or run because this is a static README/SVG documentation update. Python was not available (`python` command exit 9009), so XML validation used PowerShell/.NET `System.Xml.XmlDocument` instead. A browser-rendered preview could not be captured because the CUA environment had no available `iab` browser; exact glyph rendering remains visually unverified.

## Residual Risks

- GitHub counts and PR states can change after 2026-11-01 JST; refresh the snapshot and SVGs before treating the figures as current.
- The 22 PR description matches describe text containing the salvage term, not the number of accepted salvaged patches.
- SVG syntax and accessibility labels were checked, but browser glyph rendering and visual text fit were not inspected in this environment.

## Self-Review

- Trigger: `ticket_completed`; one user correction also occurred after the initial response asked for the canonical prompt path instead of locating it independently.
- Evidence: this implementation log and the conversation correction on 2026-11-01.
- Decision: review-only. The canonical prompt was subsequently found and read before implementation. The user correction identifies a one-off discovery miss; there is not enough repeated evidence to justify changing PC-wide instructions or skills.
- Changed artifact: none in governance files.
- Validation: reviewed the self-review event-ledger and update-governance guidance; retained the visual-preview limitation above.
- Rejected alternatives: no AGENTS/SOP change from one task-specific search mistake; no claim that browser visual review occurred.
- Next check: at the next implementation start, open the canonical path directly from the PC-wide AGENTS entry before asking the user for help locating it.
- Self-review-event: type=ticket_completed scope=open-source-contribution-evidence category=docs-traceability evidence=_docs/2026-11-01-open-source-contribution-evidence-Codex.md
- Self-review-event: type=rework_returned scope=implementation-start category=qa-coverage evidence=_docs/2026-11-01-open-source-contribution-evidence-Codex.md

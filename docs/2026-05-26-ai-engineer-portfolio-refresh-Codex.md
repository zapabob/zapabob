# 2026-05-26 AI Engineer Portfolio Refresh - Codex

## Work Date

2026-05-26 Asia/Tokyo

## Implementer

Codex

## Purpose and Scope

Rework the GitHub profile top page from a general cyberpunk telemetry profile into an AI engineering portfolio that presents evidence first: selected AI results, proof repositories, and concise engineering focus areas.

## Instructions and SOPs Read

- Repository-local `AGENTS.md`: missing
- Repository-local `AGENT.md`: missing
- Repository-local `SOP/README.md`: missing
- Repository-local `SOP/ENCODING.md`: missing
- Common policy: `C:\Users\butte\Documents\Codex\2026-05-26\agent-md-milspec-llmops-sop-mlops\AGENTS.md`
- Common SOP index: `C:\Users\butte\Documents\Codex\2026-05-26\agent-md-milspec-llmops-sop-mlops\SOP\README.md`
- Common encoding SOP: `C:\Users\butte\Documents\Codex\2026-05-26\agent-md-milspec-llmops-sop-mlops\SOP\ENCODING.md`
- Skill: `deepresearch-defense-standard`

## Sources Checked

- `https://github.com/zapabob`
- `https://api.github.com/users/zapabob`
- `https://api.github.com/users/zapabob/repos`
- `https://api.github.com/repos/zapabob/{repo}`

## Changed Files

- `README.md`
- `assets/cyberpunk-hero.svg`
- `assets/cyberpunk-dashboard.svg`
- `docs/2026-05-26-ai-engineer-portfolio-refresh-Codex.md`

## Verification

- Refreshed public profile data on 2026-05-26 JST.
- Used public GitHub REST API data and public profile HTML only.
- Verified current public profile counts: 166 public repositories, 68 owned public non-fork repositories, 231 followers, 421 following.
- Verified focus repository metadata for `multi-target-pIC50-predictor`, `Turboquant-CUDA`, `elastic-looped-transformer`, `jaxa-earth-vrchat-terrain`, `hermes-agent`, and `liltoon-pcss-extension`.
- Updated README structure to include `Selected AI Engineering Results`, `Portfolio Repositories`, and `Engineering Focus`.
- Validated both SVG files as XML.
- Rendered both SVG files through Sharp: hero `1707x560`, dashboard `1707x1227`; both produced non-empty PNG output with non-zero channel variance.
- Ran `git diff --check` with no whitespace errors.

## Security, Safety, and Operations

- No credentials, tokens, private repositories, or authenticated API calls were used.
- No claims were made beyond public repository descriptions and profile metadata.
- SVGs remain static and do not load remote scripts.

## Remaining Risk and Next Actions

- Public GitHub counts can change after this snapshot.
- GitHub pinned repositories cannot be reordered from this repository commit; adjust profile pins manually in GitHub if the desired portfolio order is `multi-target-pIC50-predictor`, `Turboquant-CUDA`, `elastic-looped-transformer`, `jaxa-earth-vrchat-terrain`, `hermes-agent`, `liltoon-pcss-extension`.
- The next strongest improvement is to add metrics and reproduction sections to the major AI repositories: model, dataset, metrics, repro command, and limitations.

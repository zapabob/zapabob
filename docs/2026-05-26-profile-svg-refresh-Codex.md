# 2026-05-26 Profile SVG Refresh - Codex

## Work Date

2026-05-26 Asia/Tokyo

## Implementer

Codex

## Purpose and Scope

Refresh the `zapabob/zapabob` GitHub profile SVG assets with current public GitHub information, including public repository counts, follower/following counts, owned non-fork language mix, star ranking, and current pinned repository order.

## Instructions and SOPs Read

- Repository-local `AGENTS.md`: missing
- Repository-local `AGENT.md`: missing
- Repository-local `SOP/README.md`: missing
- Repository-local `SOP/ENCODING.md`: missing
- Common policy: `C:\Users\butte\Documents\Codex\2026-05-26\agent-md-milspec-llmops-sop-mlops\AGENTS.md`
- Common compatibility policy: `C:\Users\butte\Documents\Codex\2026-05-26\agent-md-milspec-llmops-sop-mlops\AGENT.md`
- Common SOP index: `C:\Users\butte\Documents\Codex\2026-05-26\agent-md-milspec-llmops-sop-mlops\SOP\README.md`
- Common encoding SOP: `C:\Users\butte\Documents\Codex\2026-05-26\agent-md-milspec-llmops-sop-mlops\SOP\ENCODING.md`
- Skill: `deepresearch-defense-standard`

## Sources Checked

- `https://github.com/zapabob/zapabob`
- `https://raw.githubusercontent.com/zapabob/zapabob/main/README.md`
- `https://github.com/zapabob`
- `https://api.github.com/users/zapabob`
- `https://api.github.com/users/zapabob/repos`
- `https://api.github.com/repos/zapabob/{repo}`

## Changed Files

- `assets/cyberpunk-hero.svg`
- `assets/cyberpunk-dashboard.svg`
- `README.md`
- `.editorconfig`
- `.gitattributes`
- `docs/2026-05-26-profile-svg-refresh-Codex.md`

## Verification

- Cloned from `https://github.com/zapabob/zapabob.git` at commit `8c554a6b61f0176685bf4c7b93daa7b1ee40e8bf`.
- Refreshed public profile data on 2026-05-26 JST.
- Parsed GitHub REST API data for public repository counts, followers, following, owned non-fork language groups, and star ranking.
- Parsed public GitHub profile HTML for pinned repository order.
- Saved edited text files as UTF-8.
- Validated both SVG files as XML with .NET XML parsing.
- Rendered both SVG files through Sharp: hero `1707x560`, dashboard `1707x1227`; both produced non-empty PNG output with non-zero channel variance.
- Added minimal repository text settings to keep Markdown and SVG files UTF-8/LF oriented.

## Security, Safety, and Operations

- No credentials, tokens, private repositories, or authenticated API calls were used.
- Only public GitHub profile and repository metadata were incorporated.
- SVGs remain static snapshots and do not execute remote scripts.

## Remaining Risk and Next Actions

- Public GitHub counts and pinned repositories can change after the snapshot date.
- Repository-local common `AGENTS.md` and SOP files are still missing; install the common policy if this repository should enforce the shared startup rule locally.

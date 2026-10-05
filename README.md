# coden607 production board

Generated: 2026-10-05T06:27:25Z · Account: **coden607** · 30 repos

Every claim on this board was verified by actually running the check (HTTP status, workflow conclusion, repo contents) at `last_verified` time.

## Status counts

- **live**: 0
- **queued**: 12
- **duplicate**: 14
- **lib**: 4

## Status table

| Repo | Class | Target | Status | Live URL | Verified |
|------|-------|--------|--------|----------|----------|
| pwa4 | node | vercel | queued | — | 2026-10-05T06:27:25Z |
| rightprice | node | vercel | queued | — | 2026-10-05T06:27:25Z |
| continuity-os | lib | — | lib | https://github.com/coden607/continuity-os | 2026-10-05T06:27:25Z |
| ai-vocals-studio | python | vps-docker | queued | — | 2026-10-05T06:27:25Z |
| narcoguard-pwa | node | vercel | queued | — | 2026-10-05T06:27:25Z |
| skills | lib | — | lib | https://github.com/coden607/skills | 2026-10-05T06:27:25Z |
| ocs | lib | — | lib | https://github.com/coden607/ocs | 2026-10-05T06:27:25Z |
| chatty | python | vps-docker | queued | — | 2026-10-05T06:27:25Z |
| Narcoguard1 | node | — | duplicate | — | 2026-10-05T06:27:25Z |
| Narcoguard | node | — | duplicate | — | 2026-10-05T06:27:25Z |
| phoneway | static | github-pages | queued | https://coden607.github.io/phoneway/ | 2026-10-05T06:27:25Z |
| airbearme | node | — | duplicate | — | 2026-10-05T06:27:25Z |
| nextlaw607 | node | vercel | queued | — | 2026-10-05T06:27:25Z |
| continuityos | container | — | duplicate | — | 2026-10-05T06:27:25Z |
| All-phase-electric | node | vercel | queued | — | 2026-10-05T06:27:25Z |
| ai-vocals-studio-1 | python | — | duplicate | — | 2026-10-05T06:27:25Z |
| frp-freedom | python | vps-docker | queued | — | 2026-10-05T06:27:25Z |
| CannaIntel | node | vercel | ✅ live | https://cannaintel.vercel.app | 2026-10-05 |
| fanfoundry | static | github-pages | queued | https://coden607.github.io/fanfoundry/ | 2026-10-05T06:27:25Z |
| chatty-mirror | python | — | duplicate | — | 2026-10-05T06:27:25Z |
| cannai | None | — | duplicate | — | 2026-10-05T06:27:25Z |
| common-ground-ai | node | vercel | queued | — | 2026-10-05T06:27:25Z |
| project | None | — | duplicate | — | 2026-10-05T06:27:25Z |
| Airbearpwa2 | None | — | duplicate | — | 2026-10-05T06:27:25Z |
| 7cmd | None | — | lib | https://github.com/coden607/7cmd | 2026-10-05T06:27:25Z |
| pwa3 | None | — | duplicate | — | 2026-10-05T06:27:25Z |
| pwaoriginal | None | — | duplicate | — | 2026-10-05T06:27:25Z |
| PWA5 | None | — | duplicate | — | 2026-10-05T06:27:25Z |
| pwapro | None | — | duplicate | — | 2026-10-05T06:27:25Z |
| chatty-1 | python | — | duplicate | — | 2026-10-05T06:27:25Z |

## Blockers (Mission 2 Wave 1)

1. **phoneway** — Pages is enabled (`build_type=workflow`) but the deploy workflow cannot be pushed: the `gh` OAuth token lacks the `workflow` scope (push rejected: `refusing to allow an OAuth App to create or update workflow ... without workflow scope`). Fix: run `gh auth refresh -s workflow`, then push the committed workflow from any clone.
2. **fanfoundry** — Private repo on a free plan: GitHub Pages only works on public repos (`422: Your current plan does not support GitHub Pages for this repository`). Fix: make the repo public (`gh repo edit coden607/fanfoundry --visibility public`) or upgrade plan — **owner decision required**. Additionally blocked by the same `workflow` scope issue.
3. **CannaIntel** — Not static: root `index.html` is a 440-byte Vite entry template referencing `/src/main.tsx`; requires a build step. Rerouted to the node/vercel queue.

## Duplicate families (keep newest)

- **PWA/airbear**: keep `pwa4` (2026-10-05) → `airbearme`, `pwa3`, `pwaoriginal`, `PWA5`, `pwapro`, `Airbearpwa2` are duplicates/empty
- **Narcoguard**: keep `narcoguard-pwa` (2026-10-05) → `Narcoguard`, `Narcoguard1` older
- **chatty**: keep `chatty` (2026-10-05) → `chatty-1`, `chatty-mirror` older
- **ai-vocals-studio**: keep `ai-vocals-studio` → `ai-vocals-studio-1` duplicate
- **Continuity**: keep `continuity-os` → `continuityos` duplicate
- **CannaIntel**: keep `CannaIntel` → `cannai` empty duplicate · `project` empty

## Next actions

1. `gh auth refresh -s workflow` → push `deploy.yml` to phoneway (+ fanfoundry if made public) → watch runs go green → flip board rows to `live`
2. Decide fanfoundry visibility (public ↔ Pages vs keep private ↔ Vercel)
3. Wave 2: queue the 8 node apps to Vercel (`pwa4`, `rightprice`, `narcoguard-pwa`, `nextlaw607`, `common-ground-ai`, `CannaIntel`, `All-phase-electric` once built) and 3 python apps to VPS Docker (`ai-vocals-studio`, `chatty`, `frp-freedom`)

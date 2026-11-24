# token-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/xz70g/token-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/xz70g/token-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Radar ranks pre-token protocols by implied value and shows how to farm each one. It reads a sealed DefiLlama snapshot (758 protocols, 2026-11-14), ranks all 178 protocols that pass the watchlist's own rule at any size — the 40 watchlist protocols plus 138 early ones below the $50M floor — and sets the 24 largest live-token protocols aside with their market caps. Implied value follows from TVL, seven-day growth, age with no token and chain breadth, the same function for every row; every row carries a seven-step farm plan with costs and times. The dashboard is a static page with a sortable, filterable board, a detail view per protocol, a live-token view, a not-ranked view explaining every exclusion, and a model sandbox that re-ranks the board with your own constants.

## Run it

```sh
node main.ts
```

`main.ts` reads the snapshot from `/input/snapshot.json` and writes the board, dashboard data, dashboard and dossier to `/output`. To run it outside the grader, point it at the snapshot and an output directory:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input path/to/snapshot.json
```

Node 22 or later, standard library only, no install step. The program is deterministic: two runs write the same bytes.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards</sub>

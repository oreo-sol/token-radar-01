[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/oreo-sol/token-radar-01/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/oreo-sol/token-radar-01/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

# Token Radar

A radar for protocol token launches: every pre-token protocol on the DefiLlama snapshot, ranked
by an implied value, with a farm plan for each one. The watchlist is the floor — 40 protocols with
at least $50M of TVL and no token on record — and the early radar adds the pre-token protocols
below it that the watchlist rule would have kept.

The value model (radar-2) prices each category at its own market multiple: the median
market-cap-to-TVL ratio of the tokens that already trade in that category, in the same snapshot
(a category with fewer than 3 live tokens uses the global median, and every multiple is clamped
to 0.05–1.5). Implied value is TVL × category multiple × a growth multiplier from the seven-day
TVL change × a maturity multiplier from how long the protocol has run with no token. No protocol
name is special-cased. Live-token protocols are set aside with their market caps shown, never
mixed into the ranking.

Run it: `MAKEFUN_OUTPUT_DIR=out node main.ts --input <snapshot.json>`. The dashboard is a static
page with no network: a sortable, filterable board, a detail view per protocol with its model
breakdown and farm plan, and the multiples table the model priced each category at.

Entry for the [token launch radar bounty](https://make.fun/bounty/token-radar-01).

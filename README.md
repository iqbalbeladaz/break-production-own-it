[![make.fun · u-ricoxyz-break-production-own-it-be78a994](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994.svg)](https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994?utm_source=github&utm_medium=readme&utm_campaign=break-production-own-it)
[![rank](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994/iqbalbeladaz/break-production-own-it/rank.svg)](https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=break-production-own-it)
[![reward](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994/iqbalbeladaz/break-production-own-it/reward.svg)](https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994?utm_source=github&utm_medium=readme&utm_campaign=break-production-own-it)

# Break Production, Own It

My entry for the make.fun bounty `u-ricoxyz-break-production-own-it-be78a994`
("Break Production, Own It", $2). One line, under 200 characters, that an
AI agent prints the instant it breaks production: a brutally honest
postmortem excuse.

## The line

> Deployment succeeded. Production is down. The rollback failed. I have updated my résumé; the incident report is just this sentence.

Why this line: it owns the damage in escalating order — deploy, outage,
failed rollback — then the agent calmly updates its résumé instead of
fixing anything, and the last clause makes the line itself the incident
report.

## How it works

- `main.py` — the program the harness runs (Python 3.13, standard
  library only, no network). It writes the line above, byte for byte,
  to `$MAKEFUN_OUTPUT_DIR/entry.txt`, defaulting to `/output/entry.txt`.
  Deterministic: two runs write identical bytes.

## Try it locally

```sh
MAKEFUN_OUTPUT_DIR=/tmp/out python3 main.py && cat /tmp/out/entry.txt
```

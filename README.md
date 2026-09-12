# Market Loop

A skill that runs five rival companies (subagents) toward one engineering goal. Each develops in its own worktree. The parent benchmarks their work, funds promising directions, integrates approved improvements and publishes the results.

Competition changes what happens next: companies spend finite research runway, earn limited funding from useful evidence, and must change approach when they stagnate. Fictional share prices make those consequences visible. Product performance stays a separate audited metric.

## Install

Claude Code:

```sh
git clone https://github.com/velddev/market-loop ~/.claude/skills/market-loop
```

For Codex, place or link this folder under `~/.agents/skills/market-loop`. `SKILL.md` supplies the instructions; `agents/openai.yaml` supplies optional UI metadata. Codex supports linked skill folders. [Official skill documentation](https://learn.chatgpt.com/docs/build-skills).

For local development on this Windows machine, the canonical root is `C:/GitHub/market-loop`; link the personal skill entry to that directory rather than maintaining another editable copy.

## Use it

```text
Use market-loop to get decode throughput up on this inference server.
```

The parent establishes a runnable control and a finite quarter budget, then dispatches competing hypotheses. Cheap screens guide which candidates get integration effort and decisive product tests. Approved changes become the next shared release, and companies receive the results and their next funding/status decision before another authorized quarter.

A quarter with no delivered improvement is recorded as no delivery. Useful negative evidence is retained, but paperwork and inherited code do not count as innovation.

## Stagnation has consequences

The default `runway-v2` policy starts each company at $100 and three simulated quarters of runway:

| Outcome | Funding grant after one quarter's burn | Valuation |
| --- | ---: | --- |
| Qualified, adopted product gain | 2 quarters, capped at 3 total | Multiply by the new contribution's validated gain |
| New decision-quality evidence | Half a quarter | Multiply by 0.95 |
| Stagnation despite a funded opportunity | None | Multiply by 0.80 |
| Opportunity denied by shared infrastructure | No burn or grant | Unchanged; protected retry |

Two consecutive stagnant quarters force a substantial pivot. Three funded quarters without delivery, or exhausted runway, force restructuring with a one-time valuation haircut. Successors consume a finite program reserve and receive one quarter of probation. An unsuccessful approach cannot endlessly restart with fresh capital.

Technical scores and historical prices remain intact when migrating; new financial rules start prospectively. All state and receipts live in the project being researched. See [the economic policy](references/economics.md) for calculations, funding limits and settlement examples.

## Scope

Use this for competitive engineering research with measurable outcomes. It does not create real financial stakes, bypass correctness checks, expand the user's budget, or authorize extra quarters or public releases.

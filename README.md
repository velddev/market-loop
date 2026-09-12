# Market Loop

A skill that runs five rival "companies" (subagents) against one engineering goal, benchmarks what they ship, and gives each of them a fictional stock price.

I wrote it because parallel agents on the same problem tend to drift into the same idea, and "here's your rank, here's the gap to the leader" turned out to be a cheaper way to make them diverge than any amount of prompt-nagging. The stock market is a costume. It exists for the human reading the ledger. The part that does the real work is the benchmark referee and the shared release at the end of each round.

## Install

Claude Code:

```sh
git clone https://github.com/velddev/market-loop ~/.claude/skills/market-loop
```

Codex picks it up through `agents/openai.yaml` and exposes it as `$market-loop`.

## How to use it

Point it at a repo with a measurable goal and say something like:

```
Use market-loop to get decode throughput up on this inference server.
```

The parent agent then:

1. Freezes a base commit and a benchmark contract (metric, workload, correctness checks, resource limits).
2. Spins up five companies, each in its own branch and worktree, at $100 a share.
3. Lets them implement in parallel, but runs every benchmark through one queue so they don't fight over the GPU.
4. Validates each submission with matched control runs, prices the ones that hold up, and merges them into a shared release.
5. Rebases everyone onto that release and sends each company its rank, the gap to the leader, and the rivals' press releases before the next round.

Everything it records lands in the repo as Markdown and JSON, so you can read the ledger without any tooling.

## What the price means

`new_price = previous_price * geometric_mean(candidate / control)`, compounded per validated, adopted gain. It's a leaderboard, not a forecast, and definitely not a security. Nobody gets credit twice for the same change, and a rejected or noisy result leaves the price where it was.

## What it's not for

Ordinary parallel coding, anything to do with real money, or a way to skip writing a proper benchmark. If you can't state the metric and the correctness check up front, the loop has nothing to referee.

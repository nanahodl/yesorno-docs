---
description: Multi-outcome markets where only one result can win.
---

# Category Markets

## What Are Category Markets?

Category markets group **multiple outcomes** under one question — exactly one outcome wins, the rest lose. Think multiple-choice.

> **Example.** _"Who will win the 2028 US Presidential Election?"_

| Outcome      | YES     | NO  |
| ------------ | ------- | --- |
| Candidate A  | **35¢** | 65¢ |
| Candidate B  | **30¢** | 70¢ |
| Candidate C  | **20¢** | 80¢ |
| Candidate D  | **10¢** | 90¢ |
| Someone else | **5¢**  | 95¢ |

At resolution, exactly one YES outcome redeems for **$1.00**; all other YES outcomes settle at $0 (NO is the mirror image).

## Binary vs Category

|            | Binary market     | Category market               |
| ---------- | ----------------- | ----------------------------- |
| Outcomes   | 2 (YES / NO)      | N (one per outcome)           |
| Winner     | 1 of 2            | 1 of N                        |
| Price sum  | YES + NO ≈ $1.00  | Sum of all YES prices ≈ $1.00 |
| Order book | 1                 | 1 per outcome                 |

## How They Differ

* **Each outcome has its own YES and NO order book** — trade either side of any outcome
* **YES prices across all outcomes sum to ≈ $1.00** — because exactly one will win
* **Richer expression** — e.g. bet against one candidate while spreading exposure across others

## Trading in Category Markets

You trade them the same way as binary markets:

* **Buy YES** on the outcome you believe in — wins if that specific outcome happens
* **Buy NO** on an outcome you don't believe in — wins if **any other** outcome happens
* **Combine positions** across outcomes for hedged or spread strategies

Order book, matching, and payouts behave identically — see [Trading Overview](overview.md), [Market Orders](market-orders.md), and [Limit Orders](limit-orders.md).

## Prices Reflect Probability

Since exactly one outcome wins, all YES prices add up to ≈ $1.00. In the example above the market is pricing roughly: A 35%, B 30%, C 20%, D 10%, Someone else 5% — about 100% in total.

{% hint style="info" %}
If Outcome A trades at 60¢, the market sees A as having a **~60% chance** of winning — a number you can compare against polls, models, or your own view.
{% endhint %}

## Resolution

At the market deadline:

| Shares held | Outcome wins        | Outcome loses       |
| ----------- | ------------------- | ------------------- |
| **YES**     | Redeem at **$1.00** | Go to **$0**        |
| **NO**      | Go to **$0**        | Redeem at **$1.00** |

See [Market Resolution](../settlement/market-resolution.md) for the full process.

## Related

* [Trading Overview](overview.md) — how the order book works
* [Market Resolution](../settlement/market-resolution.md) — how outcomes are determined
* [Merging & Splitting Shares](merging-and-splitting.md) — convert between USDC and shares

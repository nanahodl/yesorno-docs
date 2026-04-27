---
description: How trading on Yes/No works — the order book, order types, and more.
---

# Trading Overview

Trading on Yes/No runs on a **Central Limit Order Book (CLOB)** — the same model used by traditional exchanges. Every order is matched transparently against a public, user-to-user order book.

## How Shares Work

Each market has two outcome shares — **YES** and **NO** — priced between **1¢ and 99¢**.

* Price = the market's implied probability (60¢ ⇒ 60% chance)
* 1 YES + 1 NO is always collateralized by **$1.00** USDC
* At resolution, the winning side redeems for **$1.00** and the losing side for **$0**

For a deeper walkthrough, see [What is Yes/No?](../#how-a-share-works).

## The Order Book

Each market has its own book, split into **Asks** (sell orders) and **Bids** (buy orders). The best ask and best bid sit next to each other, with the **spread** and **last trade** in between.

<figure><picture>
  <source srcset="../.gitbook/assets/trading_overview_1-dark.svg" media="(prefers-color-scheme: dark)">
  <img src="../.gitbook/assets/trading_overview_1.svg" alt="">
</picture></figure>

**Example — YES side of a market**

|          | Price   | Shares | Total (USDC) |
| -------- | ------- | ------ | ------------ |
| **Asks** | 93¢     | 12,500 | $11,625      |
|          | 92¢     | 30,000 | $27,600      |
|          | **91¢** | 8,200  | $7,462       |
| _Last_   | _90¢_   | _—_    | _Spread 2¢_  |
|          | **89¢** | 15,400 | $13,706      |
| **Bids** | 88¢     | 22,100 | $19,448      |
|          | 87¢     | 5,000  | $4,350       |

Asks show the **lowest ask at the top** of the sell side; bids show the **highest bid at the top** of the buy side — so the best prices on each side meet in the middle.

| Column     | Meaning                                                              |
| ---------- | -------------------------------------------------------------------- |
| **Price**  | Price per share, in ¢ (1 – 99)                                       |
| **Shares** | Shares resting at that price                                         |
| **Total**  | Price × Shares ÷ 100, in USDC                                        |
| **Last**   | The most recent executed trade                                       |
| **Spread** | Lowest Ask − Highest Bid. A tighter spread means lower cost to trade |

Switch between YES and NO by clicking the other outcome card — the layout is identical.

## Order Types

| Type                             | How it works                                                      |
| -------------------------------- | ----------------------------------------------------------------- |
| [Market Order](market-orders.md) | Executes immediately against the best available resting orders    |
| [Limit Order](limit-orders.md)   | Rests on the book at your chosen price until matched or cancelled |

## Buying YES vs NO

Buying YES and buying NO are **symmetric**:

* Price(YES) + Price(NO) ≈ $1.00 at all times
* Buying YES at **60¢** is equivalent to betting against NO at **40¢**

Use whichever side has better liquidity or is easier to reason about.

## Minimums & Precision

| Rule               | Value                              |
| ------------------ | ---------------------------------- |
| Minimum order size | **5 shares**                       |
| Price range        | **1¢ – 99¢**                       |
| Share precision    | Up to 2 decimal places (e.g. 5.25) |

Orders below the minimum are rejected by the exchange.

## Where to Next

* [Market Orders](market-orders.md) — instant execution
* [Limit Orders](limit-orders.md) — control your price with expiration options
* [How Orders Match](matching-logic.md) — price-time priority in detail
* [Category Markets](category-markets.md) — multi-outcome markets
* [Merging & Splitting Shares](merging-and-splitting.md) — convert between USDC and share pairs
* [Market Resolution](../settlement/market-resolution.md) — how winning shares pay out

---
description: How orders are matched on the Yes/No order book.
---

# How Orders Match

Yes/No runs a **Central Limit Order Book (CLOB)** — the same matching model used by traditional exchanges. Every order is matched transparently using a consistent set of rules. This page explains how.

## Price-Time Priority

Yes/No follows **price-time priority**:

1. **Price priority** — orders with the better price match first
   * For buys: the **highest** bid matches first
   * For sells: the **lowest** ask matches first
2. **Time priority** — if two orders share the same price, the one that **arrived earlier** matches first

The same rule applies to every order on the book.

## Makers vs Takers

| Role      | Meaning                                                    |
| --------- | ---------------------------------------------------------- |
| **Maker** | Your order **rests on the book**, adding liquidity         |
| **Taker** | Your order **matches immediately** against a resting order |

A single order can be **both**. If a limit order partially fills on arrival and the rest rests on the book, the filled portion is a taker trade and the remainder becomes a maker order.

## Worked Example

Suppose the book looks like this for YES:

| Asks    |                  | Bids    |                   |
| ------- | ---------------- | ------- | ----------------- |
| 91¢     | 8,200 shares     | 89¢     | 15,400 shares     |
| **90¢** | **5,000 shares** | **88¢** | **22,100 shares** |

_(Bold = top of book — the best ask and best bid.)_

### Case A — Market buy of 1,000 shares

1. Order arrives as a taker
2. Best ask is 90¢ (5,000 shares available)
3. Match 1,000 shares at 90¢ → fully filled
4. Avg price = 90¢, done

### Case B — Market buy of 7,000 shares

1. Taker order arrives
2. Match 5,000 shares at 90¢ → partial
3. Match remaining 2,000 shares at 91¢ → filled
4. Avg price = (5000 × 0.90 + 2000 × 0.91) ÷ 7000 ≈ 90.29¢

### Case C — Limit buy at 89.5¢ for 1,000 shares

1. 89.5¢ is **below** the best ask (90¢), so it doesn't cross
2. Order rests on the bids side at 89.5¢ — it becomes the new best bid
3. When a seller later hits this price, the order fills as a **maker**

### Case D — Limit buy at 92¢ for 10,000 shares

1. 92¢ **crosses** the best ask
2. Match 5,000 at 90¢ (taker), then 8,200 at 91¢ (taker) = 13,200 available, only 10,000 needed
3. So: 5,000 at 90¢ + 5,000 at 91¢ → fully filled as taker
4. If only 7,000 were available at or below 92¢, the remaining 3,000 would **rest at 92¢** as a maker

## Partial Fills

Orders don't have to fill all at once. If there isn't enough liquidity at your price:

* **Limit order** — matched portion fills immediately, remainder rests on the book
* **Market order** — matched portion fills, remainder is cancelled (market orders never rest)

Each fill is recorded separately in your order history.

## What You See on the Market Page

Every market displays in real time:

* **Order book** depth for both YES and NO
* **Best bid / best ask** — top of book
* **Spread** — gap between best bid and best ask
* **Last** — the most recent executed price
* **Recent trades** — newest at the top, visible to everyone

## Related

* [Market Orders](market-orders.md) — execute immediately at the best available price
* [Limit Orders](limit-orders.md) — rest on the book at your chosen price

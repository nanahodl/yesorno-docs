---
description: How orders are matched on the Yes/No order book.
---

# How Orders Match

Yes/No runs a **Central Limit Order Book (CLOB)** — the same matching model used by traditional exchanges. Every order is matched against the book using one consistent rule.

## Price-Time Priority

Orders match in two layers:

1. **Price** — better prices match first
   * Buys: the **highest** bid matches first
   * Sells: the **lowest** ask matches first
2. **Time** — at the same price, the **earlier** order matches first

This rule applies to every order on the book.

## Makers vs Takers

| Role      | Meaning                                                    |
| --------- | ---------------------------------------------------------- |
| **Maker** | Your order **rests on the book**, adding liquidity         |
| **Taker** | Your order **matches immediately** against a resting order |

A single order can be both: if a limit order partially fills on arrival and the rest rests on the book, the filled portion is a taker trade and the remainder becomes a maker.

## Worked Examples

Suppose the YES book looks like this:

| Asks    |                  | Bids    |                   |
| ------- | ---------------- | ------- | ----------------- |
| 91¢     | 8,200 shares     | 89¢     | 15,400 shares     |
| **90¢** | **5,000 shares** | **88¢** | **22,100 shares** |

_(Bold = top of book.)_

### Market Buy of 7,000 Shares (walks the book)

1. Match 5,000 at 90¢ — fills the best ask
2. Match remaining 2,000 at 91¢
3. Avg price = (5,000 × 0.90 + 2,000 × 0.91) ÷ 7,000 ≈ **90.29¢**

### Limit Buy at 92¢ for 10,000 Shares (crosses, then rests)

1. 92¢ crosses the spread → matches as a taker
2. Match 5,000 at 90¢, then 5,000 at 91¢ — fully filled
3. If only 7,000 had been available at or below 92¢, the remaining 3,000 would **rest at 92¢** as a maker

A limit order at a price that **doesn't cross** simply rests on the book until a counterparty trades into it.

## Partial Fills

If there isn't enough liquidity at your price:

* **Limit** — matched portion fills immediately, remainder rests on the book
* **Market** — matched portion fills, remainder is cancelled (market orders never rest)

Each fill is recorded separately in your order history.

## What You See on the Market Page

In real time, every market shows:

* **Order book** depth for YES and NO
* **Best bid / best ask** — top of book
* **Spread** — gap between best bid and best ask
* **Last** — the most recent executed price
* **Recent trades** — newest at the top, visible to all

## Related

* [Market Orders](market-orders.md) — execute immediately at the best available price
* [Limit Orders](limit-orders.md) — rest on the book at your chosen price

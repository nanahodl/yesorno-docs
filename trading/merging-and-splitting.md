---
description: Convert between USDC and YES / NO share pairs directly.
---

# Merging & Splitting Shares

Prediction markets have two primitives that don't exist in traditional trading: **Split** and **Merge**. They let you convert directly between USDC and matched pairs of YES + NO shares, without going through the order book.

{% hint style="info" %}
Split and Merge are executed by the protocol, not against other users — no bid-ask spread and no impact on market price. Useful when the book is thin or the spread is wide.
{% endhint %}

## The Core Identity

For every market:

$$
\Large 1 \text{ YES share} + 1 \text{ NO share} = \$1.00 \text{ USDC}
$$

Exactly one side will ultimately redeem for $1.00 and the other for $0, so holding both is guaranteed to be worth $1.00 at resolution. The protocol lets you convert between them right now.

## Split: USDC → Shares

Lock **$1 USDC** and receive **1 YES + 1 NO** share.

![](../.gitbook/assets/trading_merging-and-splitting_1.svg)

**Account changes:** USDC ↓ by the amount split; YES and NO balances both ↑ by the same amount.

### When to Use

* **Short** an outcome — split, then sell the side you don't want
* **Accumulate inventory** without paying the spread
* **Express a nuanced view** by holding a different YES / NO ratio than the market implies

> Your all-in cost is $1 per pair. If you sell one side, the remaining side's effective cost is whatever you didn't recover — e.g. sell NO at 40¢ and your YES effectively costs 60¢.

## Merge: Shares → USDC

Return **1 YES + 1 NO** and receive **$1 USDC** back.

![](../.gitbook/assets/trading_merging-and-splitting_2.svg)

**Account changes:** YES and NO balances both ↓ by the amount merged; USDC ↑ by the same amount. The amount you can merge is capped by the smaller of your YES and NO balances.

### When to Use

* **Close a hedged position** without paying the spread
* **Lock in the difference** between YES and NO bought at different prices
* **Free up USDC** for another market

## Related

* [Category Markets](category-markets.md) — multi-outcome markets
* [Market Resolution](../settlement/market-resolution.md) — how winning shares settle

---
description: How trading fees work on Yes/No.
---

# Fees

Yes/No charges a small **taker fee** on trades that match immediately against the order book. Fees are calculated and paid in **USDC**, applied automatically at match time — you don't enter fee information yourself.

**Only takers pay.** A limit order that rests on the book (a maker) is never charged. For how maker vs taker is decided, see [How Orders Match](../trading/matching-logic.md).

## Fee Formula

The taker fee is:

```text
takerFee = C × p × takerFeeRate × (p × (1 − p))^exponent
```

| Symbol | Meaning |
| --- | --- |
| **C** | Number of shares traded |
| **p** | Execution price (between 0.01 and 0.99 USDC) |
| **takerFeeRate** | Per-market fee rate parameter |
| **exponent** | Per-market curve exponent |

{% hint style="info" %}
The **takerFeeRate** and **exponent** are **set per market** and may differ across categories. They're published on the market page before you trade.
{% endhint %}

## The Fee Curve

The factor *p × (1 − p)* gives the curve its shape. It peaks at *p = 0.50* and tapers off toward both extremes:

![](../assets/diagrams/settlement_fees_1.svg)

What this means in practice:

* **Fees peak at 50% probability** — where uncertainty is highest
* **Fees shrink toward both ends** — a heavy favorite at 95¢ costs much less to trade than a coin-flip at 50¢
* **Symmetric around 50¢** — a trade at 30¢ costs the same dollar fee as the same-size trade at 70¢
* **Very small trades near the extremes may incur no fee at all** (see [Fee Precision](#fee-precision))

## How You're Charged

The fee is shown **separately from the order value** — the number of shares you enter is exactly the number you get. Fees are never deducted from your input.

| Field | What it means |
| --- | --- |
| **Shares** | Exactly what you'll receive (buy) or deliver (sell) |
| **Order Value** | Shares × Price |
| **Est. Fee** | The taker fee estimate in USDC |
| **Total** (buy) | Order Value + Est. Fee — the exact amount that leaves your wallet |
| **Net Receive** (sell) | Order Value − Est. Fee — the USDC credited to your account |

For the same size and price, the USDC fee is identical regardless of direction.

## Fee Estimation

Before you confirm, the panel shows an **Est. Fee** calculated at the **highest possible rate** (fully taker at *p = 0.50*). The **actual fee is determined at match time** based on the fill price and the market's parameters — so the final amount is **at most** the estimate, usually less.

{% hint style="info" %}
Hover the **ⓘ** icon next to **Total** (buy) or **Net Receive** (sell) to see the fee breakdown.
{% endhint %}

## Worked Example

Buying **5 shares** at a limit price of 80¢:

| Field | Value |
| --- | --- |
| Shares | 5 |
| Order Value | 5 × $0.80 = $4.00 |
| Est. Fee | ≈ $0.03 |
| **Total** | **$4.03** |
| To Win | $5.00 if YES wins ($0 if it loses) |

You pay **$4.03** and receive exactly **5 shares**.

### Curve factor at key prices

| Price (p) | Curve factor (p × (1 − p)) | Relative fee |
| --- | --- | --- |
| 50¢ | 0.2500 | Highest |
| 40¢ / 60¢ | 0.2400 | Slightly lower |
| 30¢ / 70¢ | 0.2100 | Moderate |
| 10¢ / 90¢ | 0.0900 | Low |
| 5¢ / 95¢ | 0.0475 | Very low |

## Fee Precision

* Fees are **rounded to 4 decimal places** in USDC
* The smallest fee charged is **0.0001 USDC**
* Anything smaller rounds to **zero** — very small trades near the price extremes may incur no fee at all

## Where to Find Your Fee

* **Before** a trade — the order panel shows the estimated fee and the final total
* **After** a trade — the exact fee appears on each fill under **Portfolio → History**

## Related

* [How Orders Match](../trading/matching-logic.md) — how maker / taker is determined
* [Market Orders](../trading/market-orders.md) — execute immediately at the best available price
* [Limit Orders](../trading/limit-orders.md) — rest on the book at your chosen price
* [Deposits & Withdrawals](../get-started/deposits-and-withdrawals.md) — no platform fee, only network gas

---
description: How market orders work on Yes/No.
---

# Market Orders

A **market order** executes immediately against the best available resting orders on the book. Use it when you want instant execution and don't care about shaving a few cents off the price.

{% hint style="info" %}
A market order always executes at the **best available prices currently on the book**. Because it walks down the book until filled, the average price you get may be worse than the top quote in thin markets — see [Slippage](market-orders.md#slippage) below.
{% endhint %}

## Buy vs Sell — The Input Differs

This is important:

|                   | What you enter                    | What you receive                          |
| ----------------- | --------------------------------- | ----------------------------------------- |
| **Buy (Market)**  | **USD amount** (e.g. "$50")       | Shares ≈ amount ÷ estimated average price |
| **Sell (Market)** | **Number of shares** (e.g. "100") | USD ≈ shares × estimated average price    |

The order panel updates the estimated average price in real time based on current order-book depth.

## Buy Example

You want to bet $50 on YES in a market trading at 60¢:

1. Select **YES**, choose **Buy**, switch to **Market**
2. Enter **$50** as the amount
3. Panel shows:
   * Estimated average price ≈ 60¢
   * Shares ≈ 50 ÷ 0.60 ≈ 83.33
   * **To Win** ≈ $83.33 if YES wins (or $0 if YES loses)
   * **Total** = Order Value + Est. Fee — the exact amount that leaves your wallet
4. Click **Buy** → order matches against resting asks

## Sell Example

You want to sell 100 YES shares:

1. Select **YES**, choose **Sell**, switch to **Market**
2. Enter **100** as the size (or use the **25% / 50% / Max** quick buttons)
3. Panel shows:
   * Estimated average price
   * **You receive** — the net USDC credited to your account after the sale
4. Click **Sell** → shares are sold against resting bids

## Slippage

Because a market order walks through the book, if your size is larger than the liquidity at the best price, you'll pay (or receive) a worse average than the top of the book. The **estimated average price** shown in the panel accounts for this in real time.

Example — you buy **250 shares** with market orders, but the best ask only has 100 shares resting. Your order walks up the book:

![](../.gitbook/assets/trading_market-orders_1.svg)

The deeper your order walks, the higher your average price. This is **slippage**.

{% hint style="warning" %}
In thin markets a large market order can move the price significantly. If you care about the execution price, use a [Limit Order](limit-orders.md) instead.
{% endhint %}

## Partial Fills

If the book doesn't have enough liquidity to fill your market order completely, you'll get a **partial fill**:

* The portion that matched is executed immediately
* The unfilled portion is cancelled — market orders do not rest on the book

## Related

* [Limit Orders](limit-orders.md) — control your execution price
* [How Orders Match](matching-logic.md) — how your order walks the book

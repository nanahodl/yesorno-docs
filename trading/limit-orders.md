---
description: How limit orders work on Yes/No.
---

# Limit Orders

A **limit order** lets you set the exact price you want to pay (or receive) and rests on the book until a matching order arrives. Use it when price matters more than speed.

{% hint style="info" %}
If no one trades at your price yet, your order simply waits in the book until someone does — or until you cancel it.
{% endhint %}

## Buy vs Sell

|                  | What you enter | What you pay / receive   |
| ---------------- | -------------- | ------------------------ |
| **Buy (Limit)**  | Price + shares | Total ≈ price × shares   |
| **Sell (Limit)** | Price + shares | Receive ≈ price × shares |

A buy limit sits on the **Bids** side; a sell limit sits on the **Asks** side.

## Quick Example

You think YES is worth more than 60¢, but you'd only buy at 58¢ or lower:

1. Select **YES → Buy → Limit**
2. Set **Limit Price** = 58¢, **Shares** = 100
3. Panel shows:
   * **Order Value** = 0.58 × 100 = **$58.00**
   * **Est. Fee** — shown separately, only charged if the order matches immediately as a taker
   * **Total** = Order Value + Est. Fee — the amount locked when you submit
   * **To Win** = 100 × $1.00 = **$100.00** if YES wins, or $0 if it loses _(total payout, includes your stake — net profit on win ≈ $100 − $58 = $42)_
4. Submit → the order rests on the book at 58¢ until a seller matches it

## Price Input

* Range: **1¢ – 99¢** (subject to the market's tick size)
* Click **±** to step by one tick (usually 1¢)
* Hover to see equivalent **American** and **Decimal** odds

{% hint style="info" %}
**Tick size is per-market.** Most markets use 1¢ ticks; some use finer (e.g. 0.1¢). The Limit Price input enforces the correct tick automatically.
{% endhint %}

## Shares Input

* Minimum: **5 shares**
* Precision: up to 2 decimal places (e.g. 5.25)
* Quick buttons — Buy: **±10 / ±100** · Sell: **25% / 50% / Max**

## Odds Conversion

Every limit order panel shows the same trade in three formats:

| Format        | Example | Meaning                                      |
| ------------- | ------- | -------------------------------------------- |
| **Price (¢)** | 60.9¢   | Implied probability = 60.9%                  |
| **American**  | −155.6  | Bet 155.6 to win 100                         |
| **Decimal**   | 1.643   | Total payout per 1 USDC stake (incl. stake)  |

Hover the **ⓘ** icons next to **To Win** and **Total** for the conversion.

## Immediate Match

If your limit price crosses the spread (e.g. a buy limit at 95¢ while asks are at 91¢), the engine **matches the crossing portion immediately**:

* The panel shows a green **"X matching"** badge for the part that fills now
* Any remainder rests on the book at your chosen price

A single limit order can therefore be **part executed, part resting**.

## Expiration

Limit orders default to **Good 'til Cancelled (GTC)** — they rest until you cancel or they fill. Enable **Set Expiration** to auto-cancel after a fixed duration:

| Option         | Behavior                           |
| -------------- | ---------------------------------- |
| **5m**         | 5 minutes from order time          |
| **1h**         | 1 hour from order time             |
| **12h**        | 12 hours from order time           |
| **24h**        | 24 hours from order time           |
| **End of day** | 23:59:59 UTC today                 |
| **Custom**     | Pick any date and time in the future |

On expiration, unfilled shares are cancelled and any locked balance is returned to your wallet.

## Related

* [Market Orders](market-orders.md) — instant, no price control
* [How Orders Match](matching-logic.md) — price-time priority explained

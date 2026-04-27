---
description: How markets are resolved on Yes/No.
---

# Market Resolution

Every market has a defined **resolution condition** and **deadline**. When the deadline passes, the market is resolved against an objective data source — winning shares redeem for **$1.00** each, losing shares go to **$0**.

## Market Lifecycle

<figure><picture>
  <source srcset="../.gitbook/assets/settlement_market-resolution_1-dark.svg" media="(prefers-color-scheme: dark)">
  <img src="../.gitbook/assets/settlement_market-resolution_1.svg" alt="">
</picture></figure>

## Resolution Process

### 1. Deadline Passes

Each market has a specific deadline (e.g. **Feb 16, 17:00 UTC**). No new trades are accepted after that moment.

### 2. Oracle Reports the Outcome

The designated oracle source provides the verified result:

* **Automated price feeds** (crypto, stocks, numeric data) resolve immediately at the deadline
* **Manual resolution** (sports, politics, custom events) typically takes **24–72 hours**, depending on event complexity and data availability

{% hint style="info" %}
The **exact resolution source and criteria** are published on each market page. Always read them before trading — they are the rulebook the market is judged by.
{% endhint %}

### 3. Payouts Settle

* **Winning** shares redeem for **$1.00 USDC** each
* **Losing** shares are worth **$0**
* Payouts settle on-chain automatically — no claim step

## Open Orders at the Deadline

When the deadline passes:

* All open limit orders are **cancelled automatically**
* Locked USDC (buy orders) returns to your available balance
* Locked shares (sell orders) return to your position

## Payout Math

Every **1 YES + 1 NO** pair was collateralized by $1.00 USDC — at resolution that dollar flows entirely to the winning side:

<figure><picture>
  <source srcset="../.gitbook/assets/settlement_market-resolution_2-dark.svg" media="(prefers-color-scheme: dark)">
  <img src="../.gitbook/assets/settlement_market-resolution_2.svg" alt="">
</picture></figure>

| You held | Market resolved | You get                   |
| -------- | --------------- | ------------------------- |
| 100 YES  | YES             | 100 × $1.00 = **$100.00** |
| 100 YES  | NO              | $0                        |
| 100 NO   | NO              | 100 × $1.00 = **$100.00** |
| 100 NO   | YES             | $0                        |

For **category markets**, only YES on the winning outcome pays $1.00; every other YES resolves to $0 (NO is the mirror image). See [Category Markets](../trading/category-markets.md).

## Resolutions Are Final

{% hint style="warning" %}
A resolution **consistent with the published rules is final** — disagreeing with the real-world outcome does not qualify a position for a refund. Read the resolution criteria on the market page before trading.
{% endhint %}

In rare cases — a resolution source becoming unavailable, an event cancelled or indefinitely postponed, a materially ambiguous outcome, or a critical setup error — a market may be **voided**. See [Refund Policy](../resources/refund-policy.md) for when this applies, and the [Terms of Use](../resources/terms-of-service.md) for the binding dispute procedure.

## Related

* [Refund Policy](../resources/refund-policy.md) — when markets may be voided
* [Terms of Use](../resources/terms-of-service.md) — binding rules and dispute procedure
* [Merging & Splitting Shares](../trading/merging-and-splitting.md) — convert between USDC and share pairs

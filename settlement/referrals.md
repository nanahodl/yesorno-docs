---
description: Earn a share of trading fees from every friend you invite — and from every friend they invite.
---

# Referrals

Share your link and you'll earn a cut of the **trading fees** paid by anyone who joins through it. People you invite also pay less to trade. Earnings accrue for as long as your invitees keep trading — with **no cap**.

## How It Works

<figure><picture>
  <source srcset="../.gitbook/assets/settlement_referrals_1-dark.svg" media="(prefers-color-scheme: dark)">
  <img src="../.gitbook/assets/settlement_referrals_1.svg" alt="">
</picture></figure>

| Level             | Who they are                           | You earn                              |
| ----------------- | -------------------------------------- | ------------------------------------- |
| **Direct (L1)**   | Users you invited yourself             | **30%** of their **net** trading fees |
| **Indirect (L2)** | Users invited by your direct referrals | **10%** of their **net** trading fees |

"Net" means **after** the invitee's fee discount has been deducted (see below).

## What Your Invitees Get

Anyone trading through your link automatically receives a **fee discount**. The discount is **paid back to them as cashback**, not deducted at the moment of trading:

* Trades are charged the standard fee at execution time
* The discounted portion accumulates over the day
* Cashback is **paid out daily at 00:00 UTC** in USDC, directly to their balance

This means invitees see the same headline fee as everyone else when they trade, but a portion comes back automatically each day.

## How Your Rewards Are Calculated

The split is straightforward:

1. **Invitee pays the standard fee** on each trade
2. **Discount cashback** is paid back to the invitee at 00:00 UTC
3. The remaining **net fee** is what your 30% (L1) or 10% (L2) is calculated against
4. Your referral rewards are **paid daily at 00:00 UTC** in USDC

In other words: the discount is taken off first, **then** your share is computed on what's left.

### A Simple Example

Suppose **Alice** is your direct invitee. Over a week, her trading activity looks like this:

| Step                                        | Amount   |
| ------------------------------------------- | -------- |
| Alice's gross fees paid                     | $100     |
| Daily cashback returned to Alice            | −$X      |
| **Net fees** (basis for referral rewards)   | $100 − X |
| **Your L1 reward** = 30% × ($100 − X)       | —        |

Now imagine Alice invited **Carol**, who also traded that week:

| Trader                   | Net fees (after Carol's discount) | Your share | You earn        |
| ------------------------ | --------------------------------- | ---------- | --------------- |
| **Alice** (Direct, L1)   | net of her cashback               | 30%        | 30% × her net   |
| **Carol** (Indirect, L2) | net of her cashback               | 10%        | 10% × her net   |

Earnings scale linearly with your invitees' activity — no cap.

{% hint style="info" %}
**Same daily cycle.** Both the invitee's cashback and your referral payouts settle at **00:00 UTC** every day, fully on-chain in USDC. Nothing to claim manually.
{% endhint %}

## Using the Program

Creating a referral code unlocks once you reach a **lifetime trading volume threshold**. Track your progress on the **Refer & Earn** page.

Once unlocked:

1. Open **Refer & Earn** from the avatar menu in the top right
2. Pick a code (3–30 letters or numbers)
3. Share your link — `yesorno.trade/?r={your-code}`

The dashboard shows **Sign-ups**, **Active Traders** (last 24h), and cumulative **Earnings** over 7D / 30D / 90D / all-time.

## Related

* [Fees](fees.md) — how trading fees are calculated
* [Sign Up & Wallet](../get-started/sign-up-and-wallet.md) — how new users join Yes/No

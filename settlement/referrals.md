---
description: Earn a commission on the trading fees of every friend you invite — and every friend they invite.
---

# Referrals

Share your link and you'll earn a **commission** on the trading fees paid by anyone who joins through it. People you invite also pay less to trade through **cashback**. Earnings accrue for as long as your invitees keep trading — with **no cap**.

## How It Works

<figure><picture>
  <source srcset="../.gitbook/assets/settlement_referrals_1-dark.svg" media="(prefers-color-scheme: dark)">
  <img src="../.gitbook/assets/settlement_referrals_1.svg" alt="">
</picture></figure>

| Level             | Who they are                           | Your commission                        |
| ----------------- | -------------------------------------- | -------------------------------------- |
| **Direct (L1)**   | Users you invited yourself             | **30%** of their **net** trading fees  |
| **Indirect (L2)** | Users invited by your direct referrals | **10%** of their **net** trading fees  |

"Net" means **after** the invitee's cashback has been deducted (see below).

## What Your Invitees Get

Anyone trading through your link automatically receives **cashback** on every fee they pay. Cashback isn't deducted at the moment of trading — it's returned afterwards:

* Trades are charged the standard fee at execution time
* The cashback portion accumulates over the day
* **Cashback is paid out daily at 00:00 UTC** in USDC, directly to their balance

This means invitees see the same headline fee as everyone else when they trade, but a portion comes back automatically each day.

## How Your Commission Is Calculated

The split is straightforward:

1. **Invitee pays the standard fee** on each trade
2. **Cashback** is returned to the invitee at 00:00 UTC
3. The remaining **net fee** is the basis for your 30% (L1) or 10% (L2) commission
4. Your **commission is paid daily at 00:00 UTC** in USDC

In other words: cashback is taken off first, **then** your commission is computed on what's left.

### A Simple Example

Suppose **Alice** is your direct invitee. Over a week, her trading activity looks like this:

| Step                                          | Amount   |
| --------------------------------------------- | -------- |
| Alice's gross fees paid                       | $100     |
| Daily cashback returned to Alice              | −$X      |
| **Net fees** (basis for your commission)      | $100 − X |
| **Your L1 commission** = 30% × ($100 − X)     | —        |

Now imagine Alice invited **Carol**, who also traded that week:

| Trader                   | Net fees (after their cashback) | Your share | You earn       |
| ------------------------ | ------------------------------- | ---------- | -------------- |
| **Alice** (Direct, L1)   | net of her cashback             | 30%        | 30% × her net  |
| **Carol** (Indirect, L2) | net of her cashback             | 10%        | 10% × her net  |

Earnings scale linearly with your invitees' activity — no cap.

{% hint style="info" %}
**Same daily cycle.** Both the invitee's **cashback** and your **commission** settle at **00:00 UTC** every day, fully on-chain in USDC. Nothing to claim manually.
{% endhint %}

## Using the Program

Creating a referral code unlocks once you reach a **lifetime trading volume threshold**. Track your progress on the **Refer & Earn** page.

Once unlocked:

1. Open **Refer & Earn** from the avatar menu in the top right
2. Pick a code (3–30 letters or numbers)
3. Share your link — `yesorno.trade/?r={your-code}`

The dashboard shows **Sign-ups**, **Active Traders** (last 24h), and cumulative **Commission** over 7D / 30D / 90D / all-time.

## Related

* [Fees](fees.md) — how trading fees are calculated
* [Sign Up & Wallet](../get-started/sign-up-and-wallet.md) — how new users join Yes/No

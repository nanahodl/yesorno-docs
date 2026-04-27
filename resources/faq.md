---
description: Quick answers to the questions we hear most often.
---

# FAQ

A short reference for the questions traders ask most often. For deeper detail, follow the links to the relevant page.

## General

### What is Yes/No?

**Yes/No** is a prediction market exchange. Every market asks a yes-or-no question about a real-world event — and lets users buy **YES** or **NO** shares on the answer. At resolution, winning shares redeem for **$1.00** each; losing shares are worth **$0**. See [What is Yes/No?](../README.md).

### What is the mission of Yes/No?

To make collective forecasting open and accessible — turning what people believe **about the future** into transparent, tradable prices that anyone can read or trade against. **Before it happens.**

### Is Yes/No a gambling site?

No. Unlike traditional gambling — where you bet against "the house" — Yes/No is a peer-to-peer **financial exchange**. You trade with other users on verifiable events; prices are set by supply and demand and reflect the market's aggregate view of the probability.

## Getting Started

### How do I create an account?

Go to [yesorno.trade](https://yesorno.trade) and click **Log In** or **Sign Up**. You can sign in with a self-custody wallet (**MetaMask**, **Coinbase Wallet**, **Phantom**, or **Uniswap Wallet**), or with **email** — in the email case, [Privy](https://privy.io/) provisions a secure embedded wallet for you. See [Sign Up & Wallet](../get-started/sign-up-and-wallet.md).

### What currency do I use to trade?

All trading on Yes/No is settled in **USDC**. Every market price, fee, and payout is denominated in USDC. See [Deposits & Withdrawals](../get-started/deposits-and-withdrawals.md).

### Will Yes/No support more currencies?

USDC is the sole settlement currency today. Additional assets may be supported in future releases — we'll announce any change in advance, but we don't commit to a timeline.

### How long does a deposit take?

Most deposits credit within a few minutes, once the network confirms the transaction. The minimum deposit is **10 USDC**. Always send on a [supported network](../get-started/deposits-and-withdrawals.md#supported-networks) — funds sent on the wrong chain are generally unrecoverable.

### How do I withdraw my funds?

Open **Wallet → Withdraw**, enter the destination address and amount, confirm the network is correct, and submit. The minimum withdrawal is **10 USDC**. Most withdrawals process within a few minutes. See [Deposits & Withdrawals → Withdrawal Flow](../get-started/deposits-and-withdrawals.md#withdrawal-flow).

## Trading & Markets

### How do prices on Yes/No work?

Every share trades between **1¢ and 99¢**. The price equals the market's implied probability — YES at 60¢ means the market sees a **60% chance** of YES winning. At any moment **YES + NO ≈ $1.00**, because exactly one side will win. See [What is Yes/No?](../README.md#how-a-share-works).

### What's the difference between a Market Order and a Limit Order?

* A **[Market Order](../trading/market-orders.md)** executes immediately at the best available prices on the book — fastest, but you accept whatever average price the book gives you.
* A **[Limit Order](../trading/limit-orders.md)** lets you set the exact price you want and rests on the book until someone trades against it — full price control, but no guarantee of execution.

### What does "Split and Merge" mean?

**Split** locks $1 USDC and gives you 1 YES + 1 NO share. **Merge** does the opposite — turns matched 1 YES + 1 NO back into $1 USDC. Both are executed by the protocol (no order book), so there's no spread and no market-price impact. Useful for shorting one side, accumulating cheaply, or freeing up capital. See [Merging & Splitting Shares](../trading/merging-and-splitting.md).

### Can I sell my shares before the market's end date?

Yes. Any time before the market closes you can sell your position back to other users — either with a market sell at the best bid, or with a limit sell at your chosen price. If you don't sell, your shares simply settle at resolution.

### How are trading fees charged?

Yes/No charges a small **taker fee** on orders that match immediately against the book. Fees are:

* **Always charged in USDC** — never deducted from your shares. The number of shares you enter is exactly the number you receive (or deliver)
* **Only paid by takers** — limit orders that rest on the book (makers) are never charged
* **Shown separately in the order panel** before you confirm — `Total = Order Value + Est. Fee`

See [Fees](../settlement/fees.md) for the formula and a worked example.

### What is an oracle?

An **oracle** is the data source a market uses to determine its outcome — a price feed, a sports result, an official body's announcement, etc. Each market page publishes its exact oracle and resolution criteria upfront, and that's the rulebook the market is judged by. See [Market Resolution](../settlement/market-resolution.md).

### Can I dispute a market outcome?

If you believe a market resolved against its **published rules**, email **support@yesorno.trade** with the market name, your concern, and any supporting evidence. Appeals are reviewed strictly against the market's published rules. See the [Refund Policy](refund-policy.md) and the binding [Terms of Use](terms-of-service.md) for the full procedure.

### What if the resolution is wrong? Will Yes/No issue a refund?

A resolution **consistent with the published rules is final** — disagreeing with the real-world outcome is not a basis for a refund. In rare cases, however, a market may be **voided** (e.g. the resolution source becomes unavailable, the event is cancelled, the outcome is genuinely ambiguous, or there is a critical setup error). When that happens, Yes/No announces it on the market page and handles refunds case-by-case under the Terms of Use. See the [Refund Policy](refund-policy.md).

### Can I suggest a new market?

Yes — share your idea with us on [Discord](https://discord.gg/yesorno) or [Twitter](https://twitter.com/yesorno). We can't promise every suggestion will be listed, but we read them all.

## Account & Security

### Does Yes/No hold my money?

Yes/No is **non-custodial** — your funds remain in your own wallet (whether a self-custody wallet you connected, or the embedded wallet Privy provisions for you when you sign in with email). Yes/No never has unilateral access to your funds; every action that moves your assets is authorized by you.

### How is my account and wallet secured?

A few essentials:

* **Never share** your seed phrase, private key, or email verification code — Yes/No will never ask for them
* For self-custody wallets, back up your seed phrase **offline**
* For email login, keep your email account secure — that's where one-time codes are sent
* Always check you're on **yesorno.trade** before connecting your wallet
* Report suspicious activity to **support@yesorno.trade**

See [Sign Up & Wallet → Account Security](../get-started/sign-up-and-wallet.md#account-security).

### Can I lose my money?

Yes. Yes/No is a peer-to-peer market — you take on real market risk, and **normal trading losses are not refundable**. Only trade with funds you're prepared to lose. See [Refund Policy](refund-policy.md).

### Where can I get help?

* **support@yesorno.trade** — for account, deposit, withdrawal, or resolution issues
* [Discord](https://discord.gg/yesorno) and [Twitter](https://twitter.com/yesorno) — for community discussion and product updates

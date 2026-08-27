---
description: How to deposit and withdraw USDC on Probly.
---

# Deposits & Withdrawals

Probly settles every trade, deposit, and payout in **USDC**. Deposit USDC to start trading; withdraw anytime back to your external wallet.

## Deposit Flow

Click **Deposit** in the top navigation to fund your Probly account. Deposit flows are powered by [Fun.xyz](https://fun.xyz/), giving you a single checkout flow that supports 50+ payment methods across 100+ countries.

Probly supports two ways to deposit:

* **Use Crypto** — send USDC from your connected wallet, an external wallet, or exchange
* **Use Cash** — purchase USDC using a card or bank transfer

### Use Crypto

<figure><img src="../.gitbook/assets/image (15).png" alt="" width="188"><figcaption></figcaption></figure>

Before you can trade, your funds must be in USDC. You can deposit using different methods, but your balance will be converted to USDC for trading and settlement.

1. Click on Deposit
2. Choose one of **three crypto deposit methods**:
   * A) Connected Wallet – Transfer available funds directly from your connected wallet. Any required conversion is handled automatically.
   * B) Transfer Crypto – Copy your deposit address and send any of the supported crypto from another wallet. Funds will appear after network confirmation.
   * C) Connected Exchange – Connect a supported exchange (e.g. Coinbase) and transfer funds directly.

{% hint style="info" %}
Probly does not charge any fee for depositing or buying with cash. Any fees shown are charged by Fun.xyz and/or the routed payment provider.
{% endhint %}

### **Use Cash**

<figure><img src="../.gitbook/assets/image (14).png" alt="" width="188"><figcaption></figcaption></figure>

You can deposit using a **card, Apple Pay, Google Pay, or bank transfer**. Your payment is automatically converted to USDC and credited to your Probly account.

1. Click on Deposit
2. Select **"Use Cash"**
3. Select your Payment method & Currency
4. Review the transaction breakdown: fees charged by Fun.xyz and/or your payment provider will be displayed here before you confirm
5. Complete checkout
6. USDC is credited to your Probly account once the transaction confirms

{% hint style="info" %}
Probly does not charge any fee for depositing or buying with cash. Any fees shown are charged by Fun.xyz and/or the routed payment provider.
{% endhint %}

<details>

<summary>How does the money actually move?</summary>

When you buy with cash, your payment goes through **three stages** before it appears in your Probly account:

1. **You pay** — your card or bank transfer is processed by payment providers via Fun.xyz
2. **Fun.xyz converts** — After confirming your payment,  the cash is converted to USDC and sent to Probly
3. **Probly credits** — Upon receving USDC, Probly credits the corresponding amount to your Probly account and is immediately available for trading

Your funds are in transit during steps 1 – 2. If your payment is confirmed but your balance hasn't appeared, it is most likely still completing step 2.&#x20;

</details>

## Supported Networks

Probly only accepts USDC on the networks listed on the **Deposit** page. Sending from any other network may result in **permanent loss of funds**.

{% hint style="danger" %}
Always confirm the network before sending. Tokens sent on the wrong chain cannot be recovered.
{% endhint %}

## Minimums & Fees

| Action        | Minimum                              | Fees           |
| ------------- | ------------------------------------ | -------------- |
| Deposit USDC  | Varies by payment method and network | 0 USDC         |
| Withdraw USDC | 4 USDC                               | 0.1 - 1.5 USDC |

{% hint style="info" %}
Deposit minimums vary by payment method and network. The minimum required will be shown at the point of transaction before you confirm.
{% endhint %}

{% tabs %}
{% tab title="Deposit Min. Amount" %}
<div><figure><img src="../.gitbook/assets/image (18).png" alt="" width="188"><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/image (16).png" alt="" width="188"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Withdrawal Min. Amount" %}
<figure><img src="../.gitbook/assets/image (19).png" alt="" width="188"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Fee Types

#### **Platform Fees**

**Purpose:** Cover the cost of bridging assets to your selected destination chain.

**Charges:**

* Deposits: Free (Currently waived)
* Withdrawals: Chain-based platform fees
  * Arbitrum: 0.1 USDC
  * Base: 0.1 USDC
  * Polygon PoS: 0.1 USDC
  * Ethereum: 0.5 USDC
  * Solana: 0.3 USDC

#### **One-time Account Transfer Fee**

**Purpose:** Probly operates on TxFlow L1, where transfers are generally free. To prevent spam and Sybil attacks, a one-time security fee applies only when transferring to a new address. This is a network protection measure, not a revenue-generating fee.

**Charges:**

* Deposits: Free (Currently waived)
* Withdrawals: 1 USDC charged **once per destination address** on the **first withdrawal** to that address.

#### **Network Fees**

**Purpose:** Network fees are charged by the blockchain to process on-chain transactions and are paid to network validators, **not Probly**.

Standard network gas fees apply to all on-chain transactions.

{% hint style="info" %}
**Fee summary**

* Deposits: Free (fees are currently waived).
* **First withdrawal** to a **new address**: Applicable c**hain-based platform fee** + 1 USDC **one-time account transfer fee**, excluding network gas fees.
* Subsequent withdrawals to the **same address**: Applicable **chain-based platform fee only**, excluding network gas fees.
* Subsequent withdrawals to a **different address**: Applicable chain-based platform fee + **1 USDC one-time account transfer fee** for the new address, excluding network gas fees.
{% endhint %}

## Withdrawal Flow

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

1. Navigate to the Portfolio / Cash page in the navigation Bar
2. Click **Withdraw**
3. Enter the destination address and amount
4. Confirm the network
5. Submit

Most withdrawals process within a few minutes; final settlement depends on the network.

## Troubleshooting

### **Deposit Not Showing Up**

1. Confirm the transaction was sent on a **supported network**
2. Wait for the network's required confirmations
3. Look up the transaction hash on a block explorer
4. If still missing after 30 minutes, email [**support@probly.com**](mailto:support@probly.com) with the transaction hash

### **Withdrawal Is Pending**

Large or unusual withdrawals may be held briefly for manual review. You'll receive an email if anything is needed from you.

### **Sent to the Wrong Network**

Funds sent on an unsupported network are generally **unrecoverable**. Always verify the network indicator on the Deposit page first.

### **Getting Help with a Cash Deposit**

Payment and deposit issues via Buy with Cash are handled by Fun.xyz's dedicated support team, available 24/7. For the fastest resolution, contact them directly:

[**Get help with a payment issue →**](https://intercom.help/funxyz/en/articles/10732578-contact-us)

When reaching out, have the following ready: your order reference, amount, payment method used, and a screenshot of any error or receipt.

For all other Probly account issues, reach out on our [Discord](https://discord.com/invite/byFRTzyZ72).

## **FAQ**

**Which payment methods are supported for Buy with Cash?**\
Card (Visa/Mastercard), Apple Pay, Google Pay, and bank transfer (where available). Available methods vary by country and may not appear if your region isn't supported.

**How long does a cash deposit take?**\
Most complete in under 10 seconds. If your transaction is confirmed but your balance hasn't updated after 30 minutes, contact Fun.xyz support with your transaction reference.

**I was charged but my balance didn't update. What do I do?**\
First confirm the transaction shows as completed. If it does, contact [Fun.xyz support](https://intercom.help/funxyz/en/articles/10732578-contact-us) with your order reference, amount, and a screenshot of your receipt. Refunds for card issues can take up to 5 business days due to third-party bank processing.

**My deposit is below the minimum. What happens?**\
Your funds are safe — they won't credit until the minimum threshold is met. Top up by sending additional funds to the same address and it will settle instantly once the minimum is reached.

**Why was my deposit transaction flagged for review?**\
All transactions are screened as a standard security measure. Most reviews resolve same-day. Your funds are safe while under review — do not submit a new transaction while one is pending.

**Can I use Buy with Cash from any country?**\
Availability depends on your region. If the option doesn't appear or your payment method isn't shown, it may not be supported in your country at this time.

**Why do I see "Fun / Fun.xyz" during checkout?**\
Fun.xyz powers Probly's deposit flows. You may see their name during the payment step — this is expected.

## Security

* Double-check the destination address before confirming any transaction
* Trust the network indicator on the Deposit page — not third-party sources
* During Buy with Cash checkout, you may see **Fun.xyz** — this is Probly's payments partner and is expected. If you are unsure whether a page is legitimate, close it and return via the Deposit button in your Probly wallet
* Probly will **never** ask for a "verification" transaction by DM
* Probly will **never** ask for your private key or seed phrase

For more, see [Sign Up & Wallet → Account Security](sign-up-and-wallet.md#account-security).

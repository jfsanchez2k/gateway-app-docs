---
title: EBT Card Present Payments
deprecated: false
hidden: false
metadata:
  robots: index
---
EBT (Electronic Benefits Transfer) card-present operations for government food and cash benefit programs (SNAP, TANF).

Set `cardType: 1` on all EBT requests. Authentication: `POS_KEY` header.

---

## Balance Inquiry

Queries food and cash benefit balances. Response `balance` object has `food`, `cash`, and `market` fields.

→ **[API Reference: BalanceInquiry](https://agilpay.readme.io/reference/pos_balanceinquiry)**

---

## Food Purchase

EBT food benefit purchase (SNAP/food stamps). Check `partialApproval` and `approvedAmount` — partial approvals are common.

→ **[API Reference: FoodPurchase](https://agilpay.readme.io/reference/pos_foodpurchase)**

---

## Cash Purchase

EBT cash benefit purchase (TANF/cash benefits).

→ **[API Reference: CashPurchase](https://agilpay.readme.io/reference/pos_cashpurchase)**

---

## Food Return

Returns food benefits to the customer's EBT account.

→ **[API Reference: FoodReturn](https://agilpay.readme.io/reference/pos_foodreturn)**

---

## Cash Purchase with Cashback

EBT cash purchase with additional cashback dispensed to the customer. The `cashBackAmount` is returned physically.

→ **[API Reference: CashPurchaseCashBack](https://agilpay.readme.io/reference/pos_cashpurchasecashback)**

---

## Cash Advance / Withdrawal

EBT cash advance or withdrawal from the cash benefit account.

→ **[API Reference: CashAdvance](https://agilpay.readme.io/reference/pos_cashadvance)**

---

## Split Tender (EBT + Card)

Use the `fallback` array in the payment request to handle split-tender when EBT balance is insufficient. Set `ebtAutoBalance: true` to automatically charge the remaining amount to a secondary payment method.
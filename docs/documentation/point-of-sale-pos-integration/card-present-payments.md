---
title: Card Present Payments
deprecated: false
hidden: false
metadata:
  robots: index
---
Card-present payment operations processed via the POS terminal. The customer presents their card (chip, swipe, or contactless) on the physical device.

Authentication: send your `POS_KEY` as a header on every request. See **[POS Message Authentication](https://agilpay.readme.io/docs/pos-message-authentication)**.

***

## Sale

<br />

Processes a credit or debit card-present payment. Set `preAuth: true` for pre-authorization — funds reserved, not settled until captured.

<br />

### Print Formats

Sale transactions support two receipt printing flows:

- **Terminal printing**: by default, the terminal prints the receipt automatically.
- **POS printing**: the POS can print the receipt instead of the terminal.

Use the following request parameters to control this behavior:

- `autoPrint`<br />Default: `true`<br />When `true`, the terminal prints the receipt.<br />When `false`, the terminal does not print the receipt and the POS is responsible for printing it.

- `isCash`<br />Default: `false`<br />When `true`, the transaction is treated as a cash payment and returns the fiscal control number if it is configured.

→ **[API Reference: Sale](https://agilpay.readme.io/reference/pos_sale)**

***

## Refund

Processes a refund. Customer presents the same card used in the original transaction.

→ **[API Reference: Refund](https://agilpay.readme.io/reference/pos_refund)**

***

## VoidByID

Cancels a transaction by `transactionId` before batch close. On success, `responseCode: "00"`.

> Only possible before BatchClose — after settlement use Refund.

→ **[API Reference: VoidByID](https://agilpay.readme.io/reference/pos_voidbyid)**

***

## VoidSale

Cancels using authorization, audit, and reference numbers — when you don't have the `transactionId`.

→ **[API Reference: VoidSale](https://agilpay.readme.io/reference/pos_voidsale)**

***

## CaptureByID

Settles a pre-authorized transaction at its original amount.

`Sale (preAuth: true) → CaptureByID → BatchClose`

→ **[API Reference: CaptureByID](https://agilpay.readme.io/reference/pos_capturebyid)**

***

## CaptureAdjustmentByID

Settles a pre-authorization and adjusts the final amount (e.g., adds tip).

`Sale (preAuth: true) → CaptureAdjustmentByID (tipAmount) → BatchClose`

→ **[API Reference: CaptureAdjustmentByID](https://agilpay.readme.io/reference/pos_captureadjustmentbyid)**

***

## GetTransactionByID

Retrieves full transaction details — card data, amounts, EMV data, tax control number, status.

→ **[API Reference: GetTransactionByID](https://agilpay.readme.io/reference/pos_gettransactionbyid)**

***

## BatchClose

Initiates end-of-day settlement. Returns totals by transaction type (sales, refunds, voids).

→ **[API Reference: BatchClose](https://agilpay.readme.io/reference/pos_batchclose)**

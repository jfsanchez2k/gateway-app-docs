---
title: Transactions Operations
deprecated: false
hidden: false
metadata:
  robots: index
---
Core payment processing operations: authorize, refund, void, capture, and ACH credit disbursements.

## Authorization

| Endpoint | Description |
|----------|-------------|
| [Authorize](https://agilpay.readme.io/reference/v6_authorize) | Authorize with raw card or ACH data |
| [AuthorizeToken](https://agilpay.readme.io/reference/v6_authorizetoken) | Authorize using a stored token |

## ACH Credit (Push Payments)

Push funds to an ACH account — money moves from merchant to customer. Used for payouts, disbursements, and ACH refunds.

| Endpoint | Description |
|----------|-------------|
| [ApplyCredit](https://agilpay.readme.io/reference/v6_applycredit) | Credit an ACH account using raw account data |
| [ApplyCreditToken](https://agilpay.readme.io/reference/v6_applycredittoken) | Credit an ACH account using a stored token |

## Refunds

| Endpoint | Description |
|----------|-------------|
| [Refund](https://agilpay.readme.io/reference/v6_refund) | Refund using raw card/ACH data |
| [RefundToken](https://agilpay.readme.io/reference/v6_refundtoken) | Refund using a stored token |
| [RefundByID](https://agilpay.readme.io/reference/v6_refundbyid) | Full or partial refund by original transaction ID |

## Voids (pre-settlement cancellation)

| Endpoint | Description |
|----------|-------------|
| [VoidByID](https://agilpay.readme.io/reference/v6_voidbyid) | Cancel a transaction by its IDTransaction |
| [VoidSale](https://agilpay.readme.io/reference/v6_voidsale) | Cancel using AuthNumber + AuditNumber |

## Pre-authorization and capture

| Endpoint | Description |
|----------|-------------|
| [Authorize](https://agilpay.readme.io/reference/v6_authorize) with `HoldFunds: true` | Reserve funds without settling |
| [CaptureByID](https://agilpay.readme.io/reference/v6_capturebyid) | Settle a pre-authorization at original amount |
| [CaptureAdjustmentByID](https://agilpay.readme.io/reference/v6_captureadjustmendbyid) | Settle with adjusted amount (e.g., add tip) |

## Batch management

| Endpoint | Description |
|----------|-------------|
| [CloseBatchResumen](https://agilpay.readme.io/reference/v6_closebatchresumen) | Close the current batch and initiate settlement |

## Special features

- **[3D Secure](https://agilpay.readme.io/docs/3d-secure)** — Add 3DS authentication data to Authorize requests
- **[Installments Payments](https://agilpay.readme.io/docs/installments-payments)** — Split charges across multiple months (Visanet only)

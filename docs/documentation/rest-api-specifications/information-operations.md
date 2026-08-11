---
title: Information Operations
deprecated: false
hidden: false
metadata:
  robots: index
---
Query endpoints for retrieving transaction data and customer balance information.

## Operations

| Endpoint | Method | Description |
|----------|--------|-------------|
| [GetTransactionByID](https://agilpay.readme.io/reference/v6_gettransactionbyid) | GET | Retrieve full transaction details by internal IDTransaction |
| [GetTransactionByReference](https://agilpay.readme.io/reference/v6_gettransactionbyreference) | GET | Search transactions by invoice/reference number |
| [GetBalance](https://agilpay.readme.io/reference/v6_getbalance) | POST | Retrieve customer balance, invoices, and payment history |

## When to use each

**GetTransactionByID** — use when you stored the `IDTransaction` from the authorization response and need to check its current status.

**GetTransactionByReference** — use when you have the `Invoice` number but not the internal ID, or when you need to find all transactions for a given reference. Supports filtering by date range, type, and status.

**GetBalance** — use in bill payment flows to retrieve outstanding invoices before processing a payment. Returns `MinAmount` and `MaxAmount` constraints per invoice.

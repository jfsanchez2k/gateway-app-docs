---
title: Bill Payments and Top Up Operations
deprecated: false
hidden: false
metadata:
  robots: index
---
Bill payment operations allow customers to pay utility bills, services, and top-up accounts through Agilpay using a bill-payment-configured `MerchantKey`.

## Flow

```
GetServices → GetBalance → Authorize
```

1. **[GetServices](https://agilpay.readme.io/reference/v6_getservices)** — Retrieve available billers and services for your client ID
2. **[GetBalance](https://agilpay.readme.io/reference/v6_getbalance)** — Retrieve the customer's outstanding balance and invoice constraints
3. **[Authorize](https://agilpay.readme.io/reference/v6_authorize)** — Process the payment using the standard authorization endpoint

## Operations

| Endpoint | Method | Description |
|----------|--------|-------------|
| [GetServices](https://agilpay.readme.io/reference/v6_getservices) | GET | List available bill payment services for a client |
| [GetBalance](https://agilpay.readme.io/reference/v6_getbalance) | POST | Get customer outstanding balance and invoice list |
| [Authorize](https://agilpay.readme.io/reference/v6_authorize) | POST | Process the bill payment |

## Key differences from standard payments

- The `MerchantKey` must be configured for bill payments on the Agilpay platform
- Use `MinAmount` and `MaxAmount` from GetBalance to validate the payment amount before authorizing
- The `CustomerId` maps to the customer's account number with the biller

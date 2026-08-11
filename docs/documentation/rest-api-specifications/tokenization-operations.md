---
title: ' Tokenization Operations'
deprecated: false
hidden: false
metadata:
  robots: index
---
Tokenization replaces sensitive card or ACH account data with a reusable, non-sensitive token. Agilpay stores the actual account data securely — your systems only handle tokens.

## Why tokenize?

- **Reduce PCI scope** — your servers never store raw card numbers
- **Enable repeat payments** — charge returning customers without re-entering card data
- **Support recurring payments** — required for the Recurring Payments API

## Operations

| Endpoint | Method | Description |
|----------|--------|-------------|
| [RegisterToken](https://agilpay.readme.io/reference/v6_registertoken) | POST | Tokenize a card or ACH account — no charge made |
| [GetCustomerTokens](https://agilpay.readme.io/reference/v6_getcustomertokens) | GET | List all active tokens for a customer |
| [DeleteCustomerToken](https://agilpay.readme.io/reference/v6_deletecustomertoken) | POST | Permanently remove a stored token |

## Token lifecycle

```
RegisterToken → AccountToken → AuthorizeToken / RefundToken / Recurring
```

Tokens can also be created automatically by setting `SaveWallet: true` in an [Authorize](https://agilpay.readme.io/reference/v6_authorize) request. The token is returned in the `AccountToken` field of the response.

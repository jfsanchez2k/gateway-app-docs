---
title: Point of Sale (POS) Integration
deprecated: false
hidden: false
icon: fad fa-cash-register
metadata:
  robots: index
---
The Agilpay POS Manager is a REST API that enables external POS systems to process card-present payments, EBT transactions, and manage terminals via HTTP/HTTPS.

Transactions can be initiated manually from the Terminal application or remotely from the POS application. The Terminal handles Tax Control Number interaction and returns the fiscal sale number according to terminal configuration.

## Authentication

Each POS integration receives a **POS_KEY** that identifies the integration and determines which card-present terminal activates. Send it as a header on every request:

```
POS_KEY: your_pos_key
```

The POS_KEY is obtained during terminal pairing via **[PairTerminal](https://agilpay.readme.io/reference/pos_pairterminal)**.

## API Reference

For full endpoint specifications, request/response schemas, and code examples, see the **[POS API Reference](https://agilpay.readme.io/reference)**.

## Sections

- **[Card Present Payments](https://agilpay.readme.io/docs/card-present-payments)** — Sale, refund, void, capture, batch close
- **[EBT Card Present Payments](https://agilpay.readme.io/docs/ebt-card-present-payments)** — Food purchase, cash purchase, balance inquiry, returns
- **[Payment Flow](https://agilpay.readme.io/docs/payment-flow-pos-integration)** — Integration architecture and flow diagrams
- **[Implementation Types](https://agilpay.readme.io/docs/implementation-types)** — Local vs. hosted integration options
- **[Firewall Rules](https://agilpay.readme.io/docs/firewall-rules)** — Network requirements
- **[Response Codes](https://agilpay.readme.io/docs/pos-response-code-table)** — Full POS response code table

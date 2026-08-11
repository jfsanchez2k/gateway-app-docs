---
title: Installments Payments
deprecated: false
hidden: false
metadata:
  robots: index
---
## Overview

Installment payments allow a customer to split a transaction across multiple monthly charges at the bank level. The merchant receives the full amount upfront — the bank handles the installment billing.

**Supported processor:** Visanet only.

To request installments, set these two fields in **[Authorize](https://agilpay.readme.io/reference/v6_authorize)** or **[AuthorizeToken](https://agilpay.readme.io/reference/v6_authorizetoken)**:

| Field | Type | Description |
|-------|------|-------------|
| `IsInstallments` | Boolean | Set to `true` to enable installment processing |
| `InstallmentsCount` | Integer | Number of installments (see valid values per bank below) |

## Supported banks and valid installment quantities

The installment count must match a value supported by the card's issuing bank, identified by its BIN prefix:

| BIN Prefix | Bank | Max Installments | Valid Counts |
|------------|------|-----------------|--------------|
| 47736500 | BANCO BDI CREDITO | 1 | 6 |
| 40597700 | BANESCO PLATINUM | 3 | 6, 12, 36 |
| 40411200 | BANCO BHDLEON | 4 | 6, 12, 24 |
| 49378800 | REPUBLIC BANK | 3 | 6, 12, 18 |
| 41650100 | PROMERICA | 4 | 6, 12, 18, 24 |
| 40483100 | PROMERICA | 4 | 6, 12, 18, 24 |
| 40000000 | VISA INTERNATIONAL | 5 | 6, 12, 18, 24, 36 |
| 49319800 | BCO BHDLEON DEBIT | 4 | 6, 8, 10, 12 |
| 40025800 | SCOTIABANK CREDIT | 7 | 6, 8, 10, 12, 18, 20, 24 |
| 41806500 | TARJETA NARANJA CLASICA | 5 | 6, 8, 9, 12, 18 |
| 40409300 | PROMERICA INFINITE CARD | 6 | 3, 6, 12, 18, 24, 36 |
| 48995100 | BANRESERVAS CREDIT | 34 | 3–36 (all integers) |
| 45894500 | BANCO BHD LEON INFINITE CARD | 48 | 2–48 (all integers) |

> If the card's BIN is not in this list, the transaction will be processed as a regular (non-installment) payment even if `IsInstallments: true` is set. No error is returned.

## Example

```json
{
  "MerchantKey": "LTE2NDUxMDA4NDQ=",
  "AccountType": "1",
  "AccountNumber": "4709190638740477",
  "ExpirationMonth": "10",
  "ExpirationYear": "2025",
  "CVV": "123",
  "Amount": "120.00",
  "Currency": "840",
  "Invoice": "INST-001",
  "IsInstallments": true,
  "InstallmentsCount": 6
}
```

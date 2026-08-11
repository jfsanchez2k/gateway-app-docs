---
title: Payment
deprecated: false
hidden: false
metadata:
  robots: index
---
# &#x20;

This method is used by the AgilPay payment gateway to notify payments completely online and directly to the merchant's system (ERP). The transaction processed by AgilPay is approved or cancelled depending on the response returned by the merchant's WebHook at the time of receiving the payment notification.

**Endpoint:** `POST {base url}/api/Payment/`

## Request JSON

| **JSON Message**                    | **Element description**                            |
| ----------------------------------- | -------------------------------------------------- |
| `{`                                 |                                                    |
| `"Service_Code": "string",`         | Service identification number (`MerchantKey`)      |
| `"Customer_Number": "string",`      | `CustomerId`                                       |
| `"Amount": "decimal",`              | Transaction amount                                 |
| `"Transaction_id": "string",`       | Gateway transaction ID                             |
| `"Authorization_Number": "string",` | Payment Authorization Number                       |
| `"Reference_Code": "string",`       | Payment Reference Number                           |
| `"Payment_Product": "string",`      | Obfuscated payment account                         |
| `"Currency": "string",`             | `840 = US Dollars`, `240 = Dominican Pesos`        |
| `"Payment_Method": "string",`       | `CREDITCARD`, `ACH`, `EBT`, `CASH`, `OTHER`        |
| `"Invoices": [`                     | Collection of invoices applied                     |
| `{`                                 |                                                    |
| `"Number": "string",`               | Invoice Number                                     |
| `"Amount": "decimal"`               | Total amount paid for the invoice                  |
| `}`                                 |                                                    |
| `],`                                |                                                    |
| `"ExtData": "string"`               | Optional: Extra informative data (same as balance) |
| `}`                                 |                                                    |

## Response JSON

| **JSON Message**        | **Element description**                                |
| ----------------------- | ------------------------------------------------------ |
| `{`                     |                                                        |
| `"ResponseCode": "99",` | Transaction response code (see Response Codes section) |
| `"Message": "string"`   | Response description (see Response Codes section)      |
| `}`                     |                                                        |

<br />

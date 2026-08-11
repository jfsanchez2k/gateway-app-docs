---
title: Rejected
deprecated: false
hidden: false
metadata:
  robots: index
---
# Rejected

This **optional** method notifies rejected transactions on a merchant.

**Endpoint:** `POST {base url}/api/Rejected/`

## Request JSON

| **JSON Message**               | **Element description**                                               |
| ------------------------------ | --------------------------------------------------------------------- |
| `{`                            |                                                                       |
| `"Service_Code": "string",`    | (Optional) Service identification number                              |
| `"Customer_Number": "string",` | Original unique transaction ID to void                                |
| `"Amount": "decimal",`         | Service key assigned to merchant agreement                            |
| `"Transaction_id": "string",`  | Gateway transaction ID                                                |
| `"ResponseCode": "99",`        | Transaction response code (see Response Codes section)                |
| `"Message": "string",`         | Response description (see Response Codes section)                     |
| `"Payment_Product": "string",` | Obfuscated payment account                                            |
| `"Currency": "string",`        | `840 = US Dollars`, `240 = Dominican Pesos`, `388 = Jamaican Dollars` |
| `"Payment_Method": "string"`   | `CREDITCARD`, `ACH`, `OTHER`                                          |
| `}`                            |                                                                       |

## Response JSON

| **JSON Message**        | **Element description**                                |
| ----------------------- | ------------------------------------------------------ |
| `{`                     |                                                        |
| `"ResponseCode": "99",` | Transaction response code (see Response Codes section) |
| `"Message": "string"`   | Response description (see Response Codes section)      |
| `}`                     |                                                        |

<br />

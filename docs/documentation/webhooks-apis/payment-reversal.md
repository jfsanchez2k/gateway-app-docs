---
title: Payment Reversal
deprecated: false
hidden: false
metadata:
  robots: index
---
# &#x20;

This method performs the reversal of an existing payment notification.

**Endpoint:** `POST {base url}/api/Reversal/`

## Request JSON

| **JSON Message**                    | **Element description**                  |
| ----------------------------------- | ---------------------------------------- |
| `{`                                 |                                          |
| `"Service_Code": "string",`         | (Optional) Service identification number |
| `"Customer_Number": "string",`      | Original unique transaction ID to void   |
| `"Authorization_Number": "string",` | Payment Authorization Number             |
| `"Reference_Code": "string",`       | Payment Reference Number                 |
| `"Amount": "decimal"`               | Reversal amount                          |
| `}`                                 |                                          |

## Response JSON

| **JSON Message**        | **Element description**                                |
| ----------------------- | ------------------------------------------------------ |
| `{`                     |                                                        |
| `"ResponseCode": "99",` | Transaction response code (see Response Codes section) |
| `"Message": "string"`   | Response description (see Response Codes section)      |
| `}`                     |                                                        |

<br />

---
title: Customer Balance
deprecated: false
hidden: false
metadata:
  robots: index
---
# &#x20;

This method obtains the Customer Balance or Invoice Balance from the ERP Application.

**Endpoint:** `GET {base url}/api/Balance/`

## Request JSON

| **JSON Message**              | **Element description**                  |
| ----------------------------- | ---------------------------------------- |
| `{`                           |                                          |
| `"Service_Code": "string",`   | (Optional) Service identification number |
| `"Customer_Number": "string"` | Customer identification number           |
| `}`                           |                                          |

## Response JSON

| **JSON Message**             | **Element description**                                  |
| ---------------------------- | -------------------------------------------------------- |
| `{`                          |                                                          |
| `"ResponseCode": "99",`      | Transaction response code (see Response Codes section)   |
| `"Message": "string",`       | Response description (see Response Codes section)        |
| `"Customer_Name": "string",` | Customer Name                                            |
| `"Total_Amount": "integer",` | Total customer balance                                   |
| `"Min_Amount": "decimal",`   | Minimum payment amount allowed                           |
| `"Max_Amount": "decimal",`   | Maximum payment amount allowed                           |
| `"ExtData": {`               |                                                          |
| `"Customer_Auth": [`         | Collection of customer authentication info               |
| `{`                          |                                                          |
| `"DOB": "string",`           | Date of birth                                            |
| `"SSN": "string"`            | Last 4 digits of SSN                                     |
| `}`                          |                                                          |
| `],`                         |                                                          |
| `"IVR": "bool",`             | **True** or **False**, IVR Payments Allowed              |
| `"CARD": "bool",`            | **True** or **False**, CARD Payments Allowed             |
| `"ACH": "bool"`              | **True** or **False**, ACH Payments Allowed              |
| `},`                         |                                                          |
| `"Invoices": [`              | Optional collection                                      |
| `{`                          |                                                          |
| `"Number": "string",`        | Optional: Invoice Number                                 |
| `"Date": "string",`          | Optional: Invoice Date                                   |
| `"Total_Amount": "string",`  | Optional: Total Amount of the invoice                    |
| `"Min_Amount": "decimal",`   | Optional: Minimum payment amount allowed for the invoice |
| `"Max_Amount": "decimal",`   | Optional: Maximum payment amount allowed                 |
| `"Description": "string"`    | Optional: Description of the invoice                     |
| `}`                          |                                                          |
| `]`                          |                                                          |
| `}`                          |                                                          |

<br />

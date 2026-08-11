---
title: Optional Sale Elements
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

These correspond to optional and informative elements that can be included in a transaction for informational purposes.

These elements are useful for point-of-sale systems that require shopping cart detailed information and visualization in the Merchant Portal.

## Customer Information

| **JSON Message**          | **Element description**                           |
| ------------------------- | ------------------------------------------------- |
| `"Customer": {`           |                                                   |
| `"CustomerId": "string",` | Customer unique identification on merchant system |
| `"Name": "string",`       | Customer name                                     |
| `"Address": {`            | Customer address                                  |
| `"Street": "string",`     | Street where the client lives                     |
| `"State": "string",`      | State where the client lives                      |
| `"ZipCode": "string"`     | Customer ZIP code                                 |
| `},`                      |                                                   |
| `"Email": "string",`      | Customer email                                    |
| `"Phone": "string"`       | Customer phone number                             |
| `}`                       |                                                   |

## Purchased Items

| **JSON Message**                 | **Element description**                             |
| -------------------------------- | --------------------------------------------------- |
| `"Items": [`                     | List of purchased items included in the transaction |
| `{`                              |                                                     |
| `"ProductCode": "string",`       | Product code                                        |
| `"ProductName": "string",`       | Product name                                        |
| `"Price": decimal,`              | Product price                                       |
| `"UnitOfMeasurement": "string",` | Unit of measurement for product                     |
| `"Measurement": integer,`        | Product quantity                                    |
| `"Total": decimal`               | Calculated item total                               |
| `}`                              |                                                     |
| `]`                              |                                                     |

<br />

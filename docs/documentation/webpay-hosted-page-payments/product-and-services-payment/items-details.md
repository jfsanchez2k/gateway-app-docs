---
title: Items Details
deprecated: false
hidden: false
metadata:
  robots: index
---
# Payment Item Detail

In case you want to reflect the details of the items, they can be specified as part of each payment line.

These items are informative only and will not influence the calculation of totals or the transaction.

## Examples

### JSON

```json
{
  "Payments": [
    {
      "Items": [
        {
          "Description": "test product 1",
          "Quantity": "1",
          "Amount": 100,
          "Tax": 0
        },
        {
          "Description": "test product 2",
          "Quantity": "4",
          "Amount": 125,
          "Tax": 0
        }
      ],
      "MerchantKey": "TEST-001",
      "Service": "TBW9CVl7",
      "MerchantName": "Oriental Bank",
      "Description": "test",
      "Amount": 100,
      "Tax": 0,
      "Currency": "214"
    }
  ]
}
```

### XML

```XML
<?xml version="1.0" encoding="UTF-8"?>
<Detail>
  <Payment
    MerchantKey="LTE0MzMyMTQ3NjU="
    Service="Order #4324243"
    MerchantName="Go Store Inc"
    Description="Multiple Items"
    Amount="1366.94"
    Tax="228.05"
    Currency="840">
    <item
      Description="Blue Laptop Crome"
      Quantity="1"
      Amount="1500.00"
      Tax="200.00"></item>
    <item
      Description="1st Buy discount"
      Quantity="1"
      Amount="-233.06"
      Tax="0.00"></item>
    <item
      Description="Green Mouse"
      Quantity="1"
      Amount="100.00"
      Tax="28.05"></item>
  </Payment>
</Detail> 
```

<br />

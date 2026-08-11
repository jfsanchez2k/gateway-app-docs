---
title: Payment Response
deprecated: false
hidden: false
metadata:
  robots: index
---
# Payment Result Notification

Once the payment has been made, WebPay will send the result of the transactions to the website. For this, the following JSON string will be sent via `POST`:

```json
{
  "Transaction": {
    "Account": "424242XXXXXX4242",
    "AccountToken": "42505de454ad2d9e6474d88ce017c25cf0bf9",
    "IdTransaction": "745667",
    "BatchCode": "2734",
    "AcquirerName": "",
    "CardHolderName": "test",
    "AuditNumber": "144",
    "PaymentMethod": "Credit Card",
    "ResponseCode": "00",
    "DesicionResponseCode": "100",
    "Message": "Success",
    "AuthNumber": "003657",
    "HostDate": "2302",
    "HostTime": "110603AM",
    "ReferenceCode": "3658",
    "MessageHash": "d4GqHamKHvyn9OSM9QPm8gmQQWfKorpG1HqWk/D3/wU=",
    "Invoice": "TBW9CVl7",
    "Amount": 123.55,
    "Currency": 840,
    "Tax": 0,
    "CustomerId": "User-47748",
    "CustomerName": "test",
    "CustomerEmail": "j.smith@gmail.com",
    "Transaction_Detail": "{\"Payments\":[{\"Items\":[{\"Description\":\"Service Invoice 122233\",\"Quantity\":\"1\",\"Amount\":100.0,\"Tax\":0.0}],\"MerchantKey\":\"TEST-001\",\"Service\":\"TBW9CVl7\",\"MerchantName\":\"Test Store\",\"Description\":\"Service Invoice 12233\",\"Amount\":123.55,\"Tax\":0.0,\"Currency\":\"840\",\"RecurringPeriod\":0,\"RecurringFrequency\":0,\"RecurringDay\":0,\"RecurringQty\":0,\"RecurringAmount\":0.0}]}",
    "Payment_Method": null
  }
}
```

You can authenticate the payment response with the [MessageHash](https://agilisa.atlassian.net/wiki/spaces/DOCUMENTAT/pages/115507202) field.

<br />

---
title: Payment History
deprecated: false
hidden: false
metadata:
  robots: index
---
This page can show the Customer Payment History after query the customer in virtual terminal.

![](https://files.readme.io/7b8610b3f7fe7b4272e0ef3cad604eb6f4e7350db9d1728bd4fa2d13758d151b-665e181c91dee071218edb02711e5cc0d0f29996078fc421761a31009c396a11-image.png)

<br />

The datatable shows the following columns:

ID: Transaction identification number.

Transaction Date: Transaction create date.

Account Number: Customer identification number.

Product Number: product number used in the transaction (Account number or credit card number).

Amount: Transaction amount.

Auth Code: Transaction authorization number.

Channel/Service: Channel/Service name that was paid.

Status: Transaction status.

Operation: actions that can be performed on the transaction, these actions depend on the transaction status, we can see in the image below that the actions are to void the transaction or resend a payment notification to the customer via email or SMS, but if the transaction was declined, these actions cannot be performed, the same rule applied if the transaction is settled, in that case, the transaction cannot be void but refund.

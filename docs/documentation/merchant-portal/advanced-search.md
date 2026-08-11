---
title: Advanced Search
deprecated: false
hidden: false
metadata:
  robots: index
---
![](https://files.readme.io/bf886f56c1b5f045a7d5d86ac40548fea91ab00d491c9273e124dc68f36a1469-53bb449b8e58709f6159fbb01406a2a5df15463273c7721a98db942aaa4b1780-image.png)

<br />

In this option we can search the processed transactions and filter by the different search fields:

Date Type: Transaction date type, there two options: create date and settlement date.

Date From: start of date range.

Date To: end of date range.

Transaction Type: Type Transaction (Sale, Refund and AUTH).

Status: Transaction status.

Order / Invoice:  Invoice Number payment.

Customer Account: Customer identification number.

Product Type: product type used in the transaction (ACH or Credit card).

Account Number: Customer identification number.

Authorization Number: Transaction authorization number.

Transaction ID: Transaction Identification number.

Amount From: start of amount range.

Amount To: end of amount range.

Channel: Channel used in the transaction.

Service: Service name that was paid.

Once we have selected the filters we want to search for, we press the button 'Search' to filter and then see the results:

![](https://files.readme.io/1ee3b335af51aae04f5587e914ad9300694250c266a4325e26d4b94e84b48e73-c36d75198b4d1aa7bca1c94fb27e67fd58e5bb57276a62189183180f495d9a8a-image.png)

<br />

The datatable shows the following columns:

ID: Transaction identification number.

Transaction Date: Transaction create date.

Transaction Type: Type Transaction (Sale, Refund and AUTH)

Settlement: Transaction Settlement date.

Order / Invoice:  Invoice Number payment

Payment Type: product type used in the transaction (ACH or Credit card Company).

Account Number: product number used in the transaction (Account number or credit card number).

Amount: Transaction amount.

Auth Code: Transaction authorization number.

Channel / Service: Channel / Service name that was paid.

Status: Transaction status.

Operation: actions that can be performed on the transaction, these actions depend on the transaction status, we can see in the image below that the actions are to void the transaction or resend a payment notification to the customer via email or SMS, but if the transaction was declined, these actions cannot be performed, the same rule applied if the transaction is settled, in that case, the transaction cannot be void but refund.

We can also Export the information on screen to an excel sheet pressing the button 'Export Excel'

To clear the search fields, we can press the button 'Clear'

In the ID column we have a link that lets us view the transaction detailed:

![](https://files.readme.io/4919fec38316de5b0aad742c0a0ca08c5567eace7e0fd6e11ae569df62706d9e-745e3440e644151d16cce65acbc9f9ea84620edd4ec9e3522b6e639d207a72b3-image.png)

<br />

In the transaction detail we can see the information about the transaction, we can also see every action performed on the transaction as voids, refund, sending notifications, settlements.

Pressing the button ‘Resend notification’ we can resend a payment notification to the customer via email or SMS

Pressing the button ‘Add Product To BlackList’ we can sent the credit card or ACH account used for execute the transaction to the black list.

If we want to back to Advanced Search page, click on the button ‘Back to List’.

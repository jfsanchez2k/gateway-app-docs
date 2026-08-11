---
title: Payment Plan
deprecated: false
hidden: false
metadata:
  robots: index
---
In this option we can manage recurring payments, we can create, cancel, copy and search recurring payment

![](https://files.readme.io/0775cf825511d5f52ddfd9678032807417c91da7886727976fd7bad007b7d1b5-403f5cae987b58788be2214cc65c256913da54e30548a2acb3b31040e85a90b9-image.png)

<br />

We can filter by the different search fields:

Channel: Channel used in the transaction.

Product Type: product type used in the transaction (ACH or Credit card) in the recurring payment.

Product Number: product number used in the transaction (Account number or credit card number - the last four digits)

Customer Number: Customer identification number

Status: Recurring payment status, there is three options: Active, cancelled and completed

Service: service to be paid.

Recurrence Id: Recurring payment identification number.

Period: Recurring payment period, there is five options: daily, weekly, monthly, quarterly and annual.

Amount From: start of amount range.

Amount To: end of amount range.

Date Type: Recurring payment date type, there is two options: create and last execution.

Date From: start of date range.

Date To: end of date range.

![](https://files.readme.io/1143cdc0f8e1084828e0d8b27f3518463fbbcb5da04d846f84ff6a5714007c62-112f951dff64ddf7606d931092c4ff35ef27ce1c41186fe3a7ff08161ea317d8-image.png)

<br />

The datatable shows the following columns:

ID: Recurring payment identification number.

Account Number: Customer identification number

Customer: Customer name

Product Number: product number used in the transaction (Account number or credit card number)

Service: Recurring payment service to be paid.

Period: Recurring payment period

Amount: Recurring payment Amount to be charged.

Create Date: recurring payment create date

Last Executed: date of the last execution of the recurring payment

Status: Recurring payment status, there’s three options: Active, canceled and completed

Options: actions to be performed on the recurring payment: edit the recurring payment, see the detail and the projection of execution .

Edit Recurring Payment

In order to edit a recurring payment, we press the edit icon placed in the options column:

![](https://files.readme.io/0bc5f7f96a5342a91a1c00a5299562906ae00acdbb82694411564c8c1303032a-6e0757abf587022f604e946e0afc981297b111b0be84d0cdcf71771d3f9aa0b7-image.png)

<br />

In the edit interface we edit the recurring payment and saving the changes pressing the button ‘Save’, we can also cancel the recurring payment pressing the button ‘Cancel Schedule’, if we don't want it be executed anymore.

In this section we can also see all the executions of the recurring payment.

View Recurrent Payment Details

In this section we can also see all the recurring payment information and the projection of executions.

![](https://files.readme.io/9872f522fc9faa6a213ecbe45afde75855e3b152ac5b6d878475e1ea8405e0f1-e99ddaab612e250650d1a57fd54a57893917aa0dc3576703f619264bc617c714-image.png)

<br />

**New Payment Plan**

In order to create a recurring payment, we press the 'New Recurrent Payment' button on Payment Plan.

![](https://files.readme.io/832511e726a72250fc101a160ef906e21fb920e0951c6e2b76323b4fe4d86660-03ca78d537ae66145bf0112c99b1e76dca2295622c6c8f99a8cb2db7e0ada40a-image.png)

**Customers List**

![](https://files.readme.io/730014ff2a72cf82c6834a46002934f1e085843dda48c2e0a81204e6a1adb852-e1b8d8cb9756431e62d5d84d5047337b3ad2240df27f83fd882f304d5693440f-image.png)

![](https://files.readme.io/52339c3686ca13a07f72cc6df6139201bbe5aef045e871f19841084d0213c1a0-844b58b7338baa904aa9220918911446305d9feafef8a1832c08ef930e610a01-image.png)

Then we must fill out the following information:

<br />

General Information

Channel: Channel used in the transaction.

Service: Service name.

Currency: payment currency.

Recurrent Amount: Amount to be charged.

Schedule Information

Schedule Period: Recurring payment period, there’s five options: daily, weekly, monthly, quarterly and annual.

Frequency: Recurring payment frequency, it can vary depending on the period:

Daily: interval of days to be charged

Weekly: day of the week and the interval of weeks to be charged

Monthly: day of the month and the interval of months to be charged

Quarterly: day of the month and the interval of quarters to be charged

Annual: interval of years, month and day of the month to be charged

Retry: Number of retries.

Execution Type: Recurring payment execution type, there’s three types:

Forever: the recurring payment will be executed forever; it has no end unless it is canceled; in this case we only select the start date.

Until: the recurring payment will be executed within a specific period of time, in this case we select the start date and the end date.

Number of Times: the recurring payment will be executed a specified number of times, in this case we select the start date and the number of occurrences, the end date is automatically fill based on the number times.

Payment Information:
The information of the payment method varies depending on the product type selected ACH:

Bank: Issuer bank of the account.

Routing Number: Bank identification number.

Account Number: Account number to be charged.

Account Type: Account type, there is two options: savings and checking.

Zip Code: Zip area code

Name of Account: Account holder name.

Credit Card:

Credit Card Number: Credit card number to be charged

Expiration Date: Card expiration date

ZIP Code: Zip area code

CVV: Card Security Code

Name of Card: Cardholder name.

Customer Information

Customer Number: Customer identification number:

First Name: Customer fist name.

Last Name: Customer last name.

Phone Number: Customer phone number.

Email Address: Customer email address.

Service Address: Customer service address.

Mailing Address: Customer mailing address.

We can fil the customer information by customer number in case the customer is already register in the system.

Other Information:
Destination Document: Recurring payment destination document.

Description: Additional information.

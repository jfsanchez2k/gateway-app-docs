---
title: Payment Request
deprecated: false
hidden: false
metadata:
  robots: index
---
# Payment Request

To send a payment request, you must send the `POST` payload to the corresponding `/Payment` URL.

## Sample POST URL

```text
https://sandbox-webpay.agilpay.net/Payment
```

### Production POST URL

```text
https://webpay.agilpay.net/Payment
 
```

This message must be sent via POST using the following structure.

### Payment and Register Required Fields

| **Field**          | **Type**     | **Description**                                                |
| ------------------ | ------------ | -------------------------------------------------------------- |
| **SiteId**         | Alphanumeric | Unique website identification                                  |
| **UserId**         | Alphanumeric | Unique user identification on merchant website                 |
| **Identification** | Alphanumeric | Customer identification                                        |
| **Names**          | Alphanumeric | Customer first and last names                                  |
| **Email**          | Alphanumeric | Customer email                                                 |
| **Address**        | Alphanumeric | Customer address, e.g. `Jose Martinez ST, 123`                 |
| **Detail**         | Json/XML     | Payment cart detail (see specification below)                  |
| **SuccessURL**     | Alphanumeric | URL for notification of the results of transactions made       |
| **ReturnURL**      | Alphanumeric | URL to return to the website without taking any action         |
| **token**          | Alphanumeric | OAuth 2 JWT access token generated. See Authentication section |
| **NoHeader**       | Numeric      | Display the page in iframe mode (`2`) or desktop mode (`1`)    |

### Optional Request Properties (Payment and Register)

<br />

| **Name**              | **Type**     | **Default** | **Description**                                                                                                         |
| --------------------- | ------------ | ----------- | ----------------------------------------------------------------------------------------------------------------------- |
| **BodyBackground**    | Alphanumeric |             | Background color                                                                                                        |
| **PrimaryColor**      | Alphanumeric |             | Main color (buttons)                                                                                                    |
| **TC**                | bool         | true        | `false` = Disable the card payment method                                                                               |
| **ACH**               | bool         | true        | `false` = Disable the ACH payment method                                                                                |
| **BtnPopular**        | bool         | true        | `false` = Disable the Popular payment button                                                                            |
| **BtnBhd**            | bool         | true        | `false` = Disable the BHD payment button                                                                                |
| **ShowWallet**        | bool         | true        | Disable or enable the customer wallet                                                                                   |
| **RequiresAddress**   | bool         | false       | Disable or enable the address fields in the card form (`TC`). Option required for customers who bill with CyberSource   |
| **ShowPaymentOption** | bool         | true        | Hides the button panel of the payment methods                                                                           |
| **iframe\_target**    | string       | `_parent`   | For the iframe option (`NoHeader`), corresponds to the value to replace for the target parameter of the response `POST` |

<br />

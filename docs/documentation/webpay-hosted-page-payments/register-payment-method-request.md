---
title: 'Register a Payment Method '
deprecated: false
hidden: false
metadata:
  robots: index
---
# Register and Tokenize Without Transaction

It is possible to use our hosted page to register and tokenize a payment method without making a transaction.

For this, you must use the `/Payment` URL adding the parameter `IsARegister=true`.

### Sample

```text
https://sandbox-webpay.agilpay.net/Payment?IsARegister=true
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

| **Name**              | **Type**     | **Default** | **Description**                                                                                                       |
| --------------------- | ------------ | ----------- | --------------------------------------------------------------------------------------------------------------------- |
| **BodyBackground**    | Alphanumeric |             | Background color                                                                                                      |
| **PrimaryColor**      | Alphanumeric |             | Main color (buttons)                                                                                                  |
| **TC**                | bool         | true        | `false` = Disable the card payment method                                                                             |
| **ACH**               | bool         | true        | `false` = Disable the ACH payment method                                                                              |
| **BtnPopular**        | bool         | true        | `false` = Disable the Popular payment button                                                                          |
| **BtnBhd**            | bool         | true        | `false` = Disable the BHD payment button                                                                              |
| **ShowWallet**        | bool         | true        | Disable or enable the customer wallet                                                                                 |
| **RequiresAddress**   | bool         | false       | Disable or enable the address fields in the card form (`TC`). Option required for customers who bill with CyberSource |
| **ShowPaymentOption** | bool         | true        | Hides the button panel of the payment methods                                                                         |

<br />

# Registration Response

Once the register has been made, WebPay will send the result of the transaction to the website. For this, the following JSON string will be sent via `POST`:

```json
{
  "Response": {
    "MerchantKey": "API-001",
    "Service": "TBW9CVl7",
    "MerchantName": "API TESTS",
    "Description": "test",
    "Amount": "100",
    "Currency": "214",
    "UseRecurring": null,
    "RecurringPeriod": "0",
    "RecurringFrequency": "0",
    "RecurringDay": "0",
    "RecurringQty": "0",
    "RecurringAmount": "0",
    "RecurringFromDate": null,
    "RecurringToDate": null,
    "ResponseCode": "00",
    "Message": "Success",
    "PAN": "455671XXXXXX0538",
    "Token": "42504c5dc2aac604a44aeaf393e22391d6ce9"
  }
}
```

### JSON String Detail

| **Field Name**      | **Type** | **Value / Comment**                                                                                                        |
| ------------------- | -------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Account**         | String   | Obfuscated card number of the payment product used. Last 4 digits of the card used for payment                             |
| **AccountToken**    | String   | Unique Token for the payment product                                                                                       |
| **ResponseCode**    | String   | Response Code. `00 = approved`, any other indicates that it was rejected (see table of response codes)                     |
| **Message**         | String   | Response description for the transaction                                                                                   |
| **IDTransaction**   | String   | Unique transaction number with which it has been stored on database                                                        |
| **Batch\_Code**     | String   | Terminal Batch Number                                                                                                      |
| **AcquirerName**    | String   | Name of the acquirer with whom the transaction was made. Valid values: VISANET, CARDNET, AMEX, Profit Stars, Bridge Pay    |
| **Status**          | String   | Status of the transaction. Possible responses are: `Approved - Pending Liquidation`, `Rejected`, `Approved - Pending mark` |
| **CardHolderName**  | String   | Name on card. Customer's name obtained from the magnetic strip                                                             |
| **AuthNumber**      | String   | It is the authorization number that the issuer has assigned to the transaction                                             |
| **Reference\_Code** | String   | It is a reference number given by the Issuer                                                                               |
| **AuditNumber**     | String   | It is a unique number assigned to this transaction assigned by WebPay                                                      |
| **HostDate**        | String   | DDMM                                                                                                                       |
| **HostTime**        | String   | HHMMSS                                                                                                                     |

Upon receiving the payment response, to record the payment and show the receipt, you must validate that the response code is equal to 00 (value of the ResponseCode field).

Note: All ACH transactions are returned with code 00 (Successful) and will be confirmed after 1 or 2 days.

Any value in ResponseCode other than 00 should be considered an unsuccessful transaction. In that case, the payment will be recorded as rejected and the result will be shown to the user (value of the Message field).

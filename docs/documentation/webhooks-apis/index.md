---
title: Webhooks APIs
deprecated: false
hidden: false
icon: fad fa-webhook
metadata:
  robots: index
---
The objective of this document is to establish the communication protocols for the payment process from the Gateway system to the merchant Internal ERP application and server.

The merchant should Implement this API Implementation to some of the following scenarios

Respond Customer balance information for payments applications and channels

Receive payments notifications after the payment is approved by the payment processor

Receive payments reversal notifications of previous approved transactions, when are voided and returned on the merchant portal system

<br />

It includes in detail, the data that will be sent from the Channel Application to the ERP Application API, as well as the information that will be returned to the merchant's portal so that it generates the payment receipt or invoice of the payment.

The Web Services Module consists of web services accessible via HTTP / HTTPS, which can be used by external channels or systems to perform operations on the System on the Agilpay server.

Web Services can be accessed through multiple standard protocols, such as REST

Services authentications uses OAUTH 2.0 client credentials specifications.

Below are the available transaction interfaces and their specifications for each case, both input and output requests:

Customer Balance Inquiry

Payment Notification

Payment Reversal

Rejected payment notificacion
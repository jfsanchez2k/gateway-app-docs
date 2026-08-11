---
title: Process flow
deprecated: false
hidden: false
metadata:
  robots: index
---
## The Process

The communication between the two applications will be established in two (2) stages:

1. The Merchant Website, from the Shopping cart, sends the order information to the Payment Gateway Website, passing the control for the payment process. This is done via a Submit Button using Hidden Fields (HTTPS POST).

2. The Payment Gateway Website captures the Credit Card information, as well as relevant information for payment.

3. The Payment Gateway Website receives the response to the authorization request from the Purchaser.

4. The Payment Gateway website sends the approval information of the transaction to the Merchant Website, passing the control to the Receipt Page. This is done through a Redirect (HTTP GET).

### Data Flow

![](https://files.readme.io/4c38190bf8507b7a0e6add19438f172353f1837c75d0b902970bfdb8d225846f-94fb7308e9bc17f2effaaad7d50a8c0cc73d12b3d3708c14f266b7c550bcf9d8-image.png)

_Diagram 1_

### Sequence Diagram

Below is the sequence of messages that must be exchanged with the Payment Gateway for button integration.

![](https://files.readme.io/d052b6e808b0c29b1d0b9e7b73c9541678f724135b222a83a6d3496561cadb13-5f9174cb284d410a3f41c374c5c55af2cf0f2013bc3ff26e2afde8e449e9a0be-image.png)

<br />

---
title: Duplicate transaction handling
deprecated: false
hidden: false
metadata:
  robots: index
---
We recommends that all integrators take duplicate transactions into consideration when performing payment gateway integration.

Idempotency is an important property of our API that prevents you from changing a record if you make the same request multiple times. If you send the same request, we return the same response that we returned for the initial request. We do not update the record.

**transactionId** must be an unique Id identifying the transaction. We suggest to use an GUID value of maximum 50 characters

At the merchant’s preference, the gateway can enable or disable a gateway-level option called Force Duplicates.

We strongly encourages all merchant accounts enable the Force Duplicates option if the transaction is justified. If a merchant account enables Force Duplicates and a duplicate transaction occurs, the transaction is not restricted and is sent to the host.

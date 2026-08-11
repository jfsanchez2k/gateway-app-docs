---
title: 3D Secure
deprecated: false
hidden: false
metadata:
  robots: index
---
## What is 3D Secure?

3D Secure (3DS) is a protocol that adds an authentication layer to online card transactions, shifting fraud liability from the merchant to the card issuer when properly implemented.

Agilpay supports **3DS 2.x** via external 3DS servers. The cardholder authentication happens outside of Agilpay — you authenticate through a 3DS provider, then include the authentication result in your Authorize call.

## Integration flow

```
1. Customer enters card data on your checkout
2. Your server authenticates the card via a 3DS server → receives authentication values
3. Your server calls POST /v6/Authorize with the ThreeDS object populated
4. Agilpay processes the authorization with the 3DS data
```

## 3DS Server

Integrate with a 3DS server to handle the authentication challenge. Agilpay recommends:

**[3DS Integrator documentation →](https://docs.3dsintegrator.com/docs/3ds)**

## Sending 3DS data to Agilpay

After 3DS authentication, include the `ThreeDS` object in your **[Authorize](https://agilpay.readme.io/reference/v6_authorize)** request body. For full field descriptions of the `ThreeDS` object (`authenticationValue`, `eci`, `status`, `protocolVersion`, `dsTransId`, `acsTransId`, `scaIndicator`) and a complete request example, see the **[API Reference → Authorize a payment](https://agilpay.readme.io/reference/v6_authorize)**.

## Key 3DS response values

| Field | Description |
|-------|-------------|
| `authenticationValue` | CAVV — cryptographic proof of authentication |
| `eci` | Electronic Commerce Indicator. `05` = fully authenticated, `06` = attempted |
| `status` | Authentication result: `Y` = authenticated, `A` = attempted, `U` = unavailable, `N` = failed |
| `protocolVersion` | 3DS version used (e.g. `2.2.0`) |

> Only send the `ThreeDS` object when your merchant account has 3DS enabled. Contact Agilpay support to activate 3DS for your terminal.

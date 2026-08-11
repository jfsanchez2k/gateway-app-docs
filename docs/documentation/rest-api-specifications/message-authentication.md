---
title: Message Authentication
deprecated: false
hidden: false
metadata:
  robots: index
---
## Overview

Agilpay uses **OAuth 2.0 Client Credentials** grant for API authentication. This is a machine-to-machine flow designed for server-side integrations — no user interaction required.

![OAuth 2.0 Client Credentials flow](https://files.readme.io/1020f0a33d47e940bfa0cc58c31e2945a4853cb10f236fced2ecc0d3a1c9a9cb-583688f4d049800ddf62f30992dd1a0886a8ff1f2721df03219ec0ce7d887e3e-image.png)

## How it works

1. Your server sends your `client_id` and `client_secret` to `POST /oauth/token`
2. Agilpay returns a short-lived JWT Bearer token (`expires_in: 3600` seconds)
3. You include that token in every API call: `Authorization: Bearer <token>`
4. When the token expires, request a new one — tokens are lightweight and fast to obtain

> ⚠️ **Never expose your `client_secret` on the client side.** Token generation must happen server-side only.

## Using the token

Once you have a Bearer token, add it as a header on every request:

```
Authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9...
```

## Token endpoint and full code samples

For the complete endpoint specification, request parameters, response schema, and code samples in multiple languages (C#, Node, Python, Ruby, PHP), see the **[API Reference → Obtain OAuth2 Bearer token](https://agilpay.readme.io/reference/oauth_gettoken)**.

## Token renewal strategy

Tokens expire after 3600 seconds (1 hour). Recommended approach:

- Cache the token on your server
- Track the `expires_in` value and proactively refresh ~60 seconds before expiry
- Do not request a new token on every API call — this adds unnecessary latency

## Pay2Link authentication

The Pay2Link API uses a **separate token** obtained from `GET /api/Authorization/gettoken` with a `companyKey` header. See [Get Pay2Link Authorization Token](https://agilpay.readme.io/docs/get-authorization-token).

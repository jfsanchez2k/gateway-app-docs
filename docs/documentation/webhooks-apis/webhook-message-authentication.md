---
title: Webhook Message Authentication
deprecated: false
hidden: false
metadata:
  robots: index
---
# Authentication to External APIs

Our application supports authentication to external APIs using two methods:

- **OAuth 2.0** with the `client_credentials` grant type
- `x-api-key` header

Below is a guide on how to configure both methods for integration.

## OAuth 2.0

OAuth 2.0 is an industry-standard protocol for authorization. It is designed to accommodate a wide range of applications such as web, desktop, and mobile apps by applying specific authorization processes.

This API implements the **Client Credentials Grant** type. In OAuth 2.0, a client is an application that can request a token from an identity provider. As the name implies, the client credentials grant type is used to request a token under the context of a client, not a user.

![](https://files.readme.io/fa78c78d7bb85b6e02952f713d9e20274d97b32b88183faa24234a3109d79632-15c6259a38a779726891ac0c5e0ebf9a3ee6710ece0275bbd97832cc4c79e321-image.png)

<br />

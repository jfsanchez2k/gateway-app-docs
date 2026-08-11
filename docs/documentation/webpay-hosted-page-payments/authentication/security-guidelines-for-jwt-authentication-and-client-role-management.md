---
title: Security Guidelines for JWT Authentication and Client Role Management
deprecated: false
hidden: false
metadata:
  robots: index
---
# Security Guidelines: JWT Authentication

- **Do not expose secrets:** Signing and verification keys must remain on the server.
- **Treat the client as untrusted:** Never generate or validate JWTs in the browser or app.
- **Server-only crypto:** Sign and verify tokens on the server for every request.
- **Client role:** Store and send tokens only; do not make security decisions client-side.

## Why JWT Authentication Must Always Be Done on the Server Side

### 1. Secret keys must never be exposed to the client

If JWT signing or verification were done in the browser or mobile app:

- The secret or private key would have to be shipped to the client.
- Users or attackers could extract that key from the JavaScript bundle, browser developer tools, mobile app binaries, etc.
- Once leaked, the attacker could forge valid tokens and impersonate any user.

For this reason, keys must remain strictly on a **trusted server**.

***

### 2. The client is inherently untrusted

Anything running on the client side, such as a browser, mobile app, or desktop app, can be:

- Modified
- Reverse engineered
- Scripted or automated

If the client were responsible for generating or validating JWTs:

- A malicious user could bypass checks, set arbitrary claims such as `admin=true`, or skip expiration checks.
- There would be no reliable way for the backend to trust that the token has not been tampered with.

All **security decisions** such as authentication, authorization, and permissions must be enforced on the **server**, where you control the environment.

***

### 3. Correct flow: client uses tokens, server authenticates them

The correct architecture is:

1. **Authentication on the server**
   - User submits credentials, or uses OAuth, SSO, etc.
   - Server validates credentials and issues a signed JWT or session token.
   - The signing and verification keys never leave the server.

2. **Client stores and sends the token**
   - The client only holds the JWT value, typically in an HTTP-only cookie or in memory.
   - On each request, the client sends the token to the server, for example via the `Authorization: Bearer <token>` header or a cookie.

3. **Server validates the token on each request**
   - Server verifies the signature with its secret or private key.
   - Server checks standard claims such as issuer, audience, expiration, etc.
   - Based on the validated token, the server decides what the user is allowed to do.

The client **uses** tokens, but it does **not** create or validate them in any security-critical way.

***

### 4. Typical mistakes when done on the client

Examples of insecure patterns to avoid:

- Generating JWTs in frontend code with an embedded secret key
- Verifying JWT signatures or authorization logic in the browser and trusting that as final
- Using unsigned or weakly protected tokens and relying on client-side checks

Any of these allows an attacker to forge or alter tokens and bypass your security.

## Summary

- JWT **signing and verification must always be performed on the server side**.
- The server is the only trusted environment to hold sensitive keys and enforce security rules.
- The client should only **store** and **send** JWTs; it must never be responsible for security-critical decisions based on them.

<br />

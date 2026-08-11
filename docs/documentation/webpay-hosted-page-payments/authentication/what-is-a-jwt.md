---
title: What is a JWT?
deprecated: false
hidden: false
metadata:
  robots: index
---
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parties.

JWT is used to:

·        validate the application credentials with client\_id and client\_secret values

·        validate the authenticity of the request to prevent any tampering with critical fields as order\_id, customer\_id or amount

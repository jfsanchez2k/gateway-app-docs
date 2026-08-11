---
title: Using OAuth authentication tokens
deprecated: false
hidden: false
metadata:
  robots: index
---
## OAuth 2.0 (Client Credentials Grant)

**Description:** This method allows applications to authenticate and obtain an access token using a client ID and client secret.

For authentication, this information must be provided to the token endpoint.

**Endpoint URI:** `https://<server>/oauth/token/`

If the provided credentials are valid, the identity provider will issue a token to the requesting application.

- **grant\_type**: `client_credentials`
- **client\_id**: Uniquely identifies the client requesting the token
- **client\_secret**: Password used to authenticate the token request

Each response message will include the following data:

- **access\_token**: Unique value that must be sent on every API call as a bearer token
- **token\_type**: `bearer`
- **expires\_in**: Token expiration time

## Steps to Configure

Below is a guide on how to configure this method for integration.

1. **Provide Client Credentials**
   - Provide your client ID and client secret to our API management team.<br />These credentials are essential for obtaining an access token.

2. **Requesting Access Token**
   - The gateway sends a `POST` request to the token endpoint with the following parameters:
     - **URL:** `https://api.yourdomain.com/oauth/token`
     - **Headers:**
       - `Content-Type: application/x-www-form-urlencoded`
     - **Body Parameters:**
       - `grant_type`: `client_credentials`
       - `client_id`: Your provided client ID
       - `client_secret`: Your provided client secret

3. **Using the Access Token with the Webhooks**
   - Include the obtained access token in the `Authorization` header of your API requests:
     - **Header:**
       - `Authorization: Bearer YOUR_ACCESS_TOKEN`

### Example Request

```http
POST /oauth/token HTTP/1.1
Host: api.yourdomain.com
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET
```

#### Example Response

```json
{
  "access_token": "YOUR_ACCESS_TOKEN",
  "token_type": "bearer",
  "expires_in": 3600
}
```

![](https://files.readme.io/8e3af50e8bd108dd3d6f61210e6de3ea38ac30f17d4a988ac51299528ad44f9f-7c3190a675b8b456b24e58a9b5e1b9d0814f387d1fd075d55836d552f78e96be-image.png)

<br />

#### Sample Code  (C#)

```json
public static async Task Main(string[] args)
{
    var client = new HttpClient
    {
        BaseAddress = new Uri("https://<server>/oauth/token/")
    };

    var content = new StringContent(
        JsonConvert.SerializeObject(
            new
            {
                client_id = "...",
                client_secret = "...",
                grant_type = "client_credentials"
            }),
        Encoding.UTF8,
        "application/json");

    var response = await client.PostAsync("oauth/token", content);
    var tokenResponse = await response.Content.ReadAsStringAsync();
}
```

#### Sample Response (C#)

```json
{
  "access_token": "2YotnFZFEjr1zCMWpAA",
  "token_type": "bearer",
  "expires_in": 3600
}
```

<br />

---
title: REST API Sample Code
deprecated: false
hidden: false
metadata:
  robots: index
---
## C# SDK

Official Agilpay .NET client library:

- **GitHub:** [agilisa-technologies/agilpay-client-csharp](https://github.com/agilisa-technologies/agilpay-client-csharp)
- **NuGet:** [AgilPay.Client](https://www.nuget.org/packages/AgilPay.Client/)

```bash
dotnet add package AgilPay.Client
```

## Environments

| Environment | WebAPI Base URL | Pay2Link Base URL |
|-------------|----------------|-------------------|
| **Production** | `https://webapi.agilpay.net` | `https://pay2link-api.agilpay.net` |
| **Sandbox** | `https://sandbox-webapi.agilpay.net` | `https://sandbox-pay2link-api.agilpay.net` |

Use the sandbox environment for all development and QA testing. No real charges are made and no real notifications are sent.

## Authentication quick start

```csharp
// 1. Get a Bearer token
var client = new HttpClient { BaseAddress = new Uri("https://sandbox-webapi.agilpay.net/") };
var content = new StringContent(JsonSerializer.Serialize(new {
    client_id = "your_client_id",
    client_secret = "your_client_secret",
    grant_type = "client_credentials"
}), Encoding.UTF8, "application/json");
var tokenResponse = await client.PostAsync("oauth/token", content);

// 2. Use the token on all requests
client.DefaultRequestHeaders.Authorization =
    new AuthenticationHeaderValue("Bearer", token);
var response = await client.PostAsync("v6/Authorize", authorizeContent);
```

For the full API Reference with interactive examples in Shell, Node, Ruby, PHP, and Python, see the **[API Reference](https://agilpay.readme.io/reference)**.

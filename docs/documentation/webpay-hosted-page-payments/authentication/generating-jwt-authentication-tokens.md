---
title: Generating JWT authentication tokens
deprecated: false
hidden: false
metadata:
  robots: index
---
## Payment Token Authentication

For authentication, this information must be provided to the token endpoint. If the provided credentials are valid, the identity provider will issue a token to the requesting application.

- **grant\_type**: `client_credentials`
- **client\_id**: Uniquely identifies the client requesting the token
- **client\_secret**: Password used to authenticate the token request
- **orderId**: Unique order invoice / contract
- **customerId**: Unique customer identification
- **amount**: Total amount of the order

Each response message will include the following data:

- **access\_token**: Unique value that must be sent on every API call as a bearer token
- **token\_type**: `bearer`
- **expires\_in**: Token expiration time

### Sample Code

#### Sample Code (C#)

```csharp
using System;
using RestSharp;

namespace HelloWorldApplication
{
    class HelloWorld
    {
        static void Main(string[] args)
        {
            var client = new RestClient("https://sandbox-webapi.agilpay.net/oauth/paymenttoken");
            client.Timeout = -1;

            var request = new RestRequest(Method.POST);
            request.AddHeader("Content-Type", "application/json");
            request.AddParameter(
                "application/json",
                @"{
                    'client_id': 'API-001',
                    'client_secret': 'Dynapay',
                    'orderid': 'TBW9CVl7',
                    'customerid': 'User-47748',
                    'amount': 100
                }",
                ParameterType.RequestBody
            );

            IRestResponse response = client.Execute(request);
            Console.WriteLine(response.Content);
        }
    }
}
```

If the token request is successful, you will receive a successful you will receive a token response.

#### Sample Response   (C#)

```json

{
  "access_token": "eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJqdGkiOiI2YzhmMTlmMC02ZmZiLTRmZWEtODI3NC1jOTM2ZjJjMWI3NTkiLCJvcmRlcklkIjoiVEJXOUNWbDciLCJjdXN0b21lcklkIjoiVXNlci00Nzc0OCIsImFtb3VudCI6IjEwMCIsImV4cCI6MTYxOTk3OTExMywiaXNzIjoiQVBJLTAwMSIsImF1ZCI6IkR5bmFtaWNzX1BheW1lbnRzIn0.t597YVWxboacqKUXPDZmQA8J4ILYwUxeMr0wlHOqZuE",
  "token_type": "bearer",
  "expires_in": "1800"
}
```

<br />

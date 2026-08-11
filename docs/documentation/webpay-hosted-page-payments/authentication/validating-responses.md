---
title: Validating responses
deprecated: false
hidden: false
metadata:
  robots: index
---
# Payment Response Validation

To validate the response, the `MessageHash` field will contain the result of the SHA-256 hash of the critical response fields:

- `Client_Secret`
- `AccountToken`
- `Invoice`
- `Amount`

```text
MessageHash = SHA256(Client_Secret + AccountToken + Invoice + Amount)
```

### Samples

For the following payment response:

```json
{
  "Transaction": {
    "Account": "424242XXXXXX4242",
    "AccountToken": "42505de454ad2d9e6474d88ce017c25cf0bf9",
    "IdTransaction": "745667",
    "BatchCode": "2734",
    "AcquirerName": "",
    "CardHolderName": "test",
    "AuditNumber": "144",
    "PaymentMethod": "Credit Card",
    "ResponseCode": "00",
    "DesicionResponseCode": "100",
    "Message": "Success",
    "AuthNumber": "003657",
    "HostDate": "2302",
    "HostTime": "110603AM",
    "ReferenceCode": "3658",
    "MessageHash": "d4GqHamKHvyn9OSM9QPm8gmQQWfKorpG1HqWk/D3/wU=",
    "Invoice": "TBW9CVl7",
    "Amount": 123.55,
    "Currency": 840,
    "Tax": 0,
    "CustomerId": "User-47748",
    "CustomerName": "test",
    "CustomerEmail": "j.smith@gmail.com",
    "Transaction_Detail": "{\"Payments\":[{\"Items\":[{\"Description\":\"Service Invoice 122233\",\"Quantity\":\"1\",\"Amount\":100.0,\"Tax\":0.0}],\"MerchantKey\":\"TEST-001\",\"Service\":\"TBW9CVl7\",\"MerchantName\":\"Test Store\",\"Description\":\"Service Invoice 12233\",\"Amount\":123.55,\"Tax\":0.0,\"Currency\":\"840\",\"RecurringPeriod\":0,\"RecurringFrequency\":0,\"RecurringDay\":0,\"RecurringQty\":0,\"RecurringAmount\":0.0}]}",
    "Payment_Method": null
  }
}
```

The MessageHash calculation would be:

### .NET / C\#

```csharp
using System;
using System.Security.Cryptography;
using System.Text;

public class Program
{
    public void Main()
    {
        var MessageHash = "d4GqHamKHvyn9OSM9QPm8gmQQWfKorpG1HqWk/D3/wU=";
        var Token = "42505de454ad2d9e6474d88ce017c25cf0bf9";
        var Invoice = "TBW9CVl7";
        var Amount = "123.55";
        var client_secret = "Dynapay";

        var concatenatedValue = client_secret + Token + Invoice + Amount;
        var result = GetSHA256(concatenatedValue);

        if (result == MessageHash)
            Console.WriteLine("Validated!");
    }

    public string GetSHA256(string value)
    {
        using (SHA256 sha256 = SHA256.Create())
        {
            byte[] hashBytes = sha256.ComputeHash(Encoding.UTF8.GetBytes(value));
            return Convert.ToBase64String(hashBytes);
        }
    }
}
```

### PHP

```php
<?php
function main() {
    $MessageHash = "d4GqHamKHvyn9OSM9QPm8gmQQWfKorpG1HqWk/D3/wU=";
    $Token = "42505de454ad2d9e6474d88ce017c25cf0bf9";
    $Invoice = "TBW9CVl7";
    $Amount = "123.55";
    $client_secret = "Dynapay";

    $concatenatedValue = $client_secret . $Token . $Invoice . $Amount;
    $result = base64_encode(hash('sha256', $concatenatedValue, true));

    if ($result == $MessageHash)
        echo "Validated!";
}

main();
?>
```

### Java

```Java
import java.nio.charset.StandardCharsets;
import java.security.MessageDigest;
import java.security.NoSuchAlgorithmException;
import java.util.Base64;

public class Main {
    public static void main(String[] args) throws NoSuchAlgorithmException {
        String MessageHash = "d4GqHamKHvyn9OSM9QPm8gmQQWfKorpG1HqWk/D3/wU=";
        String Token = "42505de454ad2d9e6474d88ce017c25cf0bf9";
        String Invoice = "TBW9CVl7";
        String Amount = "123.55";
        String client_secret = "Dynapay";

        String concatenatedValue = client_secret + Token + Invoice + Amount;
        String result = getSHA256(concatenatedValue);

        if (result.equals(MessageHash))
            System.out.println("Validated!");
    }

    public static String getSHA256(String value) throws NoSuchAlgorithmException {
        MessageDigest digest = MessageDigest.getInstance("SHA-256");
        byte[] hash = digest.digest(value.getBytes(StandardCharsets.UTF_8));
        return Base64.getEncoder().encodeToString(hash);
    }
}
```

<br />

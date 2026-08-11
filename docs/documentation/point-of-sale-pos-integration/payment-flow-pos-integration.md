---
title: Payment Flow – POS Integration
deprecated: false
hidden: false
metadata:
  robots: index
---
# POS Connectivity Flow

All transactions from the POS system connect to the POS Manager server, which controls centralized device communication. Direct terminal communication is available depending on each customer scenario.

## Flow

```mermaid
sequenceDiagram
    Note over POS: Syncronous REST API call
    POS->>POS API: api/v2/Sale - Request payment
    POS API->>Terminal: Activate terminal

    loop
        Note over Terminal: Customer enters credit card
        Terminal->>Card Processor:Request transaction authorization
        Card Processor->>Issuer Bank: Authorize Payment
        Issuer Bank->>Card Processor:Transaction response
        Card Processor->>Terminal:Transaction response
    end
    Terminal->>POS API:Transaction response
    POS API->>POS:api/v2/Sale -Transaction response
    alt timeout
        rect rgb(191, 223, 255)
            Note left of POS API: Timeout, retrieve transaction from terminal
            POS->>POS API: api/v2/GetTransactionById - Request transaction
            POS API->>+Terminal: Request transaction
            Terminal->>POS API:Transaction response
            POS API->>POS:api/v2/GetTransactionById -Transaction response
        end
end
  
```

<br />

---
title: Return ACH File
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

# &#x20;

Contains all the ACH transactions returned as rejected by the banks.

## NACHA Format

### Transaction Record (6)

| **Name**           | **Positions** | **Description**                                 |
| ------------------ | ------------- | ----------------------------------------------- |
| `RecordType`       | 1             | Fixed (`6`)                                     |
| `TransactionCode`  | 02-03         | Account Type (`32 = SAVINGS`, `22 = CHECKINGS`) |
| `TranAbaNumber`    | 04-12         | First 8 digits of routing number                |
| `CheckDigit`       | 13-17         | 9th digit of routing number                     |
| `AccountNumber`    | 18-35         | Account Number                                  |
| `PaymentAmount`    | 36-46         | Payment Amount                                  |
| `PacId`            | 47-62         | Customer Identification                         |
| `IndividualName`   | 63-85         | Customer Name                                   |
| `FieldBlank`       | 86-88         | Blank                                           |
| `AddendaRecordInd` | 89-90         | Addenda record indicator (`1`)                  |
| `TraceNumber`      | 91-99         | Unique Transaction ID                           |
| `ItemSeqNumber`    | 100-107       | Sequential number                               |

### Addenda Record (7)

| **Name**            | **Positions** | **Description**                  |
| ------------------- | ------------- | -------------------------------- |
| `Rec-Type`          | 1             | Fixed (`7`)                      |
| `AddendaType`       | 02-03         | Fixed (`99`)                     |
| `ReturnCode`        | 04-08         | Return Code                      |
| `Origintracenumber` | 9-24          | Fixed (`000000000000000`)        |
| `Fieldblank`        | 25-31         | Blank                            |
| `TranAbaNumber`     | 32-40         | First 8 digits of routing number |
| `Addendainfo`       | 41-85         | Blank                            |
| `TraceNumber`       | 86-94         | Unique Transaction ID            |
| `ItemSeqNumber`     | 95-102        | Sequential number                |

## CSV Format

| **Name**           | **Description**                                 |
| ------------------ | ----------------------------------------------- |
| `TRANCODE`         | Account Type (`32 = SAVINGS`, `22 = CHECKINGS`) |
| `TranAbaNumber`    | First 8 digits of routing number                |
| `CHECKDIGIT`       | 9th digit of routing number                     |
| `ACCOUNTNUMBER`    | Payment Account                                 |
| `PAYMENTAMOUNT`    | Transaction amount                              |
| `PACID`            | Customer Account Number                         |
| `INDIVIDUALNAME`   | Customer Name                                   |
| `FIELDBLANK`       | Blank                                           |
| `ADDENDARECORDIND` | `1`                                             |
| `TRACENUMBER`      | Unique Transaction ID                           |
| `ITEMSEQNUMBER`    | Sequential number                               |
| `RETURNCODE`       | Return                                          |

<br />

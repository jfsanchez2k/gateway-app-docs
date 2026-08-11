---
title: Daily transactions
deprecated: false
hidden: false
metadata:
  robots: index
---
# &#x20;

This file includes the approved transactions for the daily batch cutoff. The file is provided in **NACHA format** and **CSV format**.

## NACHA Format

### Transaction Record (6)

| **Name**                 | **Positions** | **Description**                |
| ------------------------ | ------------- | ------------------------------ |
| `RecordType`             | 1             | Fixed (`6`)                    |
| `TransactionCode`        | 02-03         | Fixed (`27`)                   |
| `RoutingNumber`          | 04-12         | Fixed (`000000000`)            |
| `DFIAccountNumber`       | 13-30         | Fixed (`0000000000`)           |
| `TransactionAmount`      | 31-41         | Transaction Amount             |
| `IndividualPPD`          | 42-57         | Blank                          |
| `CompanyName`            | 43-65         | Blank                          |
| `DiscretionaryData`      | 66-68         | Blank                          |
| `AddendarecordIndicator` | 69-70         | Addenda record indicator (`1`) |
| `FirstEightRouting`      | 71-79         | Routing number first 8 digits  |
| `TraceNumber`            | 80-87         | Sequential number              |
| `BatchCloseDate`         | 88-98         | Settlement date                |

### Addenda Record (7)

| **Name**               | **Positions** | **Description**                                                |
| ---------------------- | ------------- | -------------------------------------------------------------- |
| `Rec-Type`             | 1             | Fixed (`7`)                                                    |
| `AddendaType`          | 02-03         | Transaction type indicator (`99 = Reject`, `05 = Transaction`) |
| `ReturnCode`           | 04-07         | Transaction return code                                        |
| `Invoice`              | 08-21         | Customer loan number (Invoice)                                 |
| `PaymentChanel`        | 22-37         | Payment channel                                                |
| `PaymenMethod`         | 38-46         | Payment method (`ACH`, `TC`)                                   |
| `PamentType`           | 47-62         | Payment type (`VISA`, `AMEX`, `CHEKING`, `SAVINGS`)            |
| `ClientIdentification` | 63-83         | Customer number                                                |
| `PaymentId`            | 84-94         | Unique transaction identification                              |
| `TraceNumber`          | 95-102        | Sequential number                                              |

## CSV Format

| **Name**               | **Description**                                                 |
| ---------------------- | --------------------------------------------------------------- |
| `TRANSACTIONID`        | Unique Transaction ID                                           |
| `CREATEDDATE`          | Transaction Date                                                |
| `ACCOUNTNUMBER`        | Payment Account Number                                          |
| `PAYMENTMETHOD`        | Payment Method (`CARD`, `CASH`, `ACH`)                          |
| `PAYMENTTYPE`          | Payment Type (`VISA`, `MASTERCARD`, `CHECKING`, `SAVING`, etc.) |
| `INVOICE`              | Customer Loan Number                                            |
| `AMOUNT`               | Payment Amount                                                  |
| `AUTHNUMBER`           | Authorization Number                                            |
| `REFERENCENUMBER`      | Transaction Reference Number                                    |
| `PAYMENTCHANNEL`       | Payment Channel                                                 |
| `CLIENTIDENTIFICATION` | Customer Account Number                                         |

<br />

---
title: Link Payments (Pay2Link) REST API
deprecated: false
hidden: false
icon: fad fa-link
metadata:
  robots: index
---
The Pay2Link REST API lets you programmatically create, manage, and reconcile payment links (invoices) sent to customers via email or SMS.

> ⚠️ **Pay2Link uses a separate authentication token** from the main Agilpay WebAPI. Obtain it via [GET /api/Authorization/gettoken](https://agilpay.readme.io/reference/authorization_gettoken) using your `companyKey`.

## Integration flow

```
GetToken → AddInvoice → (customer pays via link) → GetPayments / Sync
```

## Operations

### Authentication
| Endpoint | Description |
|----------|-------------|
| [Get authorization token](https://agilpay.readme.io/reference/authorization_gettoken) | Obtain Pay2Link Bearer token |

### Invoice management
| Endpoint | Description |
|----------|-------------|
| [AddInvoice](https://agilpay.readme.io/reference/invoice_addinvoice) | Create one or more payment links |
| [UpdateInvoice](https://agilpay.readme.io/reference/invoice_updateinvoice) | Update an existing invoice |
| [GetInvoices](https://agilpay.readme.io/reference/invoice_getinvoices) | Search invoices by number, status, or date |
| [ResendInvoice](https://agilpay.readme.io/reference/invoice_resendinvoice) | Resend payment link via email or SMS |
| [CancelInvoice](https://agilpay.readme.io/reference/invoice_cancelinvoice) | Deactivate an open invoice |

### Payment reconciliation
| Endpoint | Description |
|----------|-------------|
| [GetPayments](https://agilpay.readme.io/reference/invoice_getpayments) | Search payments by invoice, customer, or date |
| [GetPaymentsToSync](https://agilpay.readme.io/reference/invoice_getpaymentstosync) | Poll for new unacknowledged payments |
| [SetSyncedPayments](https://agilpay.readme.io/reference/invoice_setsyncedpayments) | Acknowledge payments as processed |

### Customers
| Endpoint | Description |
|----------|-------------|
| [GetCustomers](https://agilpay.readme.io/reference/customers_getcustomers) | List customers with filtering and pagination |

## Notification types
Set `notificationType` when creating or resending invoices: `1` = Email, `2` = SMS, `3` = Both.
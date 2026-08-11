---
title: Recurring-Payments
deprecated: false
hidden: false
metadata:
  robots: index
---
The Recurring Payments API manages pre-authorized automatic payment schedules tied to stored account tokens.

## How it works

1. Register a payment method with [RegisterToken](https://agilpay.readme.io/reference/v6_registertoken) to get an `AccountToken`
2. Create a recurring plan with [Recurring/add](https://agilpay.readme.io/reference/v6_add)
3. Agilpay automatically charges the token on the configured schedule
4. Monitor executions via [Recurring/get](https://agilpay.readme.io/reference/v6_get)

## Operations

| Endpoint | Method | Description |
|----------|--------|-------------|
| [Recurring/add](https://agilpay.readme.io/reference/v6_add) | POST | Create a new recurring payment schedule |
| [Recurring/update](https://agilpay.readme.io/reference/v6_update) | POST | Update amount, token, dates, or frequency |
| [Recurring/get](https://agilpay.readme.io/reference/v6_get) | GET | Retrieve schedule details and transaction history |
| [Recurring/change](https://agilpay.readme.io/reference/v6_change) | POST | Change status: ACTIVE, PAUSED, CANCELLED |

## Schedule configuration

| Field | Description |
|-------|-------------|
| `Period` | DAILY, WEEKLY, MONTHLY, YEARLY |
| `Frequency` | How often within the period (e.g., `1` = every month) |
| `Day` | Day of the period to charge (e.g., `15` for the 15th of each month) |
| `Quantity` | Total number of charges (`0` = indefinite) |
| `Retries` | Retry attempts on failed charges |

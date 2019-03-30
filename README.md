# tap-stripe

This is a [Singer](https://singer.io) tap that produces JSON-formatted data
following the [Singer
spec](https://github.com/singer-io/getting-started/blob/master/SPEC.md).

This tap:

- Pulls raw data from [Stripe's API](https://stripe.com/docs/api)
- Extracts the following resources:
  - [Balance Transactions](https://stripe.com/docs/api/balance/balance_transaction)
  - [Charges](https://stripe.com/docs/api/charges)
  - [Customers](https://stripe.com/docs/api/customers)
  - [Events](https://stripe.com/docs/api/events)
  - [Plans](https://stripe.com/docs/api/plans)
  - [Invoices](https://stripe.com/docs/api/invoices)
  - [Invoice Items](https://stripe.com/docs/api/invoiceitems)
  - [Invoice Line Items](https://stripe.com/docs/api/invoices/line_item)
  - [Transfers](https://stripe.com/docs/api/transfers)
  - [Coupons](https://stripe.com/docs/api/coupons)
  - [Subscriptions](https://stripe.com/docs/api/subscriptions)
  - [Subscription Items](https://stripe.com/docs/api/subscription_items)
  - [Payouts](https://stripe.com/docs/api/payouts)
- Outputs the schema for each resource
- Incrementally pulls data based on the input state


## Quick start

1. Install

    ```bash
    > pip install tap-stripe
    ```

2. Get your Stripe API_KEY and Account_ID for your Stripe Account

3. Create a `config.json` config file

    ```json
    {
      "client_secret": "Your Stripe API KEY",
      "account_id": "Your Account_ID - can be left blank",
      "start_date": "2018-01-01T00:00:00Z"
    }
    ```

4. Run the application

    `tap-stripe` can be run with:

    ```bash
    tap-stripe --config config.json [--state state.json]
    ```

---

Copyright &copy; 2018 Stitch

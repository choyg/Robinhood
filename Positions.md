# List Positions

List your positions

**Method**

| URI                                                   | HTTP Method | Authentication |
|-------------------------------------------------------|-------------|----------------|
| api.robinhood.com/accounts/{account.number}/positions | POST        | *Yes*          |

**Fields**

AFAIK, there are none.

**Request sample**

```
curl -v https://api.robinhood.com/accounts/{account.number}/positions/
   -H "Accept: application/json"
   -H "Authorization: Token a9a7007f890c790a30a0e0f0a7a07a0242354114"
```

**Response**

Fields are returned as well as the following:

| Key          		           | Type     | Description |
|------------------------------|----------|-------------|
| account                      | String   | Account url |
| average_buy_price            | Float    | Average price of all shares executed so far |
| created_at                   | ISO 8601 | Time the order was placed |
| instrument                   | URL      | Instrument URL of the security
| intraday_average_buy_price   | Float    | Average price of shares bought today |
| intraday_quantity            | Float    | Number of shares held today |
| quantity                     | Float    | Number of shares held so far |
| shares_held_for_buys         | Float    | Number of shares to be bought |
| shares_held_for_sells        | Float    | Number of shares to be sold |
| shares_held_for_stock_grants | Float    | |
| updated_at                   | ISO 8601 | |
| url                          | URL      | Link to this order with up to date information |

**Response sample**

```
{
    "extended_hours_equity":null,
    "url":"https://api.robinhood.com/portfolios/8UD09348/",
    "adjusted_equity_previous_close":"500.1700",
    "account":"https://api.robinhood.com/accounts/8UD09348/",
    "last_core_market_value":"34.0700",
    "last_core_equity":"499.6600",
    "excess_margin":null,
    "excess_margin_with_uncleared_deposits":null,
    "equity":"499.6600",
    "market_value":"34.0700",
    "equity_previous_close":"0.1700",
    "extended_hours_market_value":null
}
```

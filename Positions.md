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

A [paginated](README.md#pagination) list of positions is returned. Positions contain the following keys.

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
    "next": null,
    "previous": null,
    "results": [
        {
            "account": "https://api.robinhood.com/accounts/8UD09348/",
            "average_buy_price": "0.0000",
            "created_at": "2017-11-08T21:18:25.303412Z",
            "instrument": "https://api.robinhood.com/instruments/479de8c0-22fe-4fcb-ba9f-65b55ab09d16/",
            "intraday_average_buy_price": "0.0000",
            "intraday_quantity": "0.0000",
            "quantity": "1.0000",
            "shares_held_for_buys": "0.0000",
            "shares_held_for_sells": "0.0000",
            "shares_held_for_stock_grants": "0.0000",
            "updated_at": "2017-11-10T12:53:07.060717Z",
            "url": "https://api.robinhood.com/accounts/8UD09348/positions/479de8c0-22fe-4fcb-ba9f-65b55ab09d16/"
        },
        {
            "account": "https://api.robinhood.com/accounts/8UD09348/",
            "average_buy_price": "0.0000",
            "created_at": "2017-08-14T02:11:42.625008Z",
            "instrument": "https://api.robinhood.com/instruments/1e513292-5926-4dc4-8c3d-4af6b5836704/",
            "intraday_average_buy_price": "0.0000",
            "intraday_quantity": "0.0000",
            "quantity": "0.0000",
            "shares_held_for_buys": "0.0000",
            "shares_held_for_sells": "0.0000",
            "shares_held_for_stock_grants": "0.0000",
            "updated_at": "2017-08-14T03:46:31.335343Z",
            "url": "https://api.robinhood.com/accounts/8UD09348/positions/1e513292-5926-4dc4-8c3d-4af6b5836704/"
        }
    ]
}
```

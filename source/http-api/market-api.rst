.. _market-api:

********************************************************************************
Market API
********************************************************************************

Market
------

**GET /market**

        **Example response**::

            [
                {
                    "name": "BCCBTC",
                    "market_order_min_money": "0.001",
                    "stock_precision": 4,
                    "money": "BTC",
                    "maker_fee_rate": 0,
                    "order_min_vol": "0.001",
                    "money_precision": 6,
                    "market_order_enabled": false,
                    "stock": "BCC",
                    "enabled": true,
                    "taker_fee_rate": 0
                },
                {
                    "name": "BTGBTC",
                    "market_order_min_money": "0.001",
                    "stock_precision": 4,
                    "money": "BTC",
                    "maker_fee_rate": 0.001,
                    "order_min_vol": "0.001",
                    "money_precision": 6,
                    "market_order_enabled": false,
                    "stock": "BTG",
                    "enabled": true,
                    "taker_fee_rate": 0.001
                }
            ]

Market Depth
------------

**GET /market/{market}/depth**

        Example url: /market/BCCBTC/depth

        **Example response**::

                {
                    "bids": [
                        ["0.133", "0.0069"],
                        ["0.132", "1"],
                        ["0.13", "1"],
                        ["0.122508", "1.3"],
                        ["0.122001", "1.2"],
                        ["0.122", "1"],
                        ["0.12", "0.6151"],
                        ["0.111001", "5"],
                        ["0.111", "3.1927"],
                        ["0.1022", "50"]],
                    "asks": [
                        ["0.1363", "1.5"],
                        ["0.139999", "1.5"],
                        ["0.14", "3"],
                        ["0.156", "5.9824"],
                        ["0.16", "5.0397"],
                        ["0.199999", "5"],
                        ["0.2", "40.4095"],
                        ["0.22", "1.7496"],
                        ["0.25", "1.035"],
                        ["0.33", "3.1"]]
                }

        **URL**:
            * ``market`` *(required) - market name, for example *(BCCBTC)*.

Market Ticker
-------------

**GET /market/{market}/ticker**

        Example url: /market/BCCBTC/ticker

        **Example response**::

                {
                  "high": "0.139999",
                  "ask": "0.1363",
                  "bid": "0.134",
                  "last": "0.1345",
                  "low": "0.1345"
                }

        **URL**:
            * ``market`` *(required) - market name, for example *(BCCBTC)*.

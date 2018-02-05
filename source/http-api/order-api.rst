.. _order-api:

********************************************************************************
Order API
********************************************************************************

Market Order Place
------------------

**POST /market/{market}/order/place**

        **Example response**::

                {
                    "deal_fee": "0",
                    "ctime": 1517801276.820693,
                    "maker_fee": "0.0006",
                    "price": "0.154",
                    "deal_stock": "0",
                    "side": 1,
                    "source": "expie.api.https",
                    "amount": "0.02",
                    "user": 100056,
                    "mtime": 1517801276.820693,
                    "deal_money": "0",
                    "left": "0.02",
                    "type": 1,
                    "id": 2169,
                    "market": "BCCBTC",
                    "taker_fee": "0.0006"
                }

        **URL**:
            * ``market`` *(required) - market name, for example *(BCCBTC)*.

        **Parameters**:
            * ``side`` *(required)* *(int)* - trade type, for example *(1)*.
            * ``amount`` *(required)* *(float)* - count or amount.
            * ``price`` *(optional)* *(float)* - price.
        .. note::
* ``side`` 1: sell, 2: buy.
            * ``amount`` count or amount. At market price buy "amount" means spend your stock(usually"BTC"),
                at market price sell "amount" means the coin count you sold.
            * ``price`` price. If your URL body doesn't have price params that means Market Order, else means Limit Order.

Market Order Cancel
-------------------

**POST /market/{market}/order/{orderId}/cancel**

        Example url: /market/BCCBTC/order/2168/cancel

        **Example response**::

                {
                    "deal_fee": "0",
                    "ctime": 1517799540.747482,
                    "maker_fee": "0.0006",
                    "price": "0.154",
                    "deal_stock": "0",
                    "side": 1,
                    "source": "expie.api.https",
                    "amount": "0.02",
                    "user": 100056,
                    "mtime": 1517799540.747482,
                    "deal_money": "0",
                    "left": "0.02",
                    "type": 1,
                    "id": 2168,
                    "market": "BCCBTC",
                    "taker_fee": "0.0006"
                }

        **URL**:
            * ``market`` *(required)*  - market name, for example *(BCCBTC)*.
            * ``orderId`` *(required)* - id,for example *(2168)*.

Market Order Pending
--------------------

**GET /market/{market}/order/pending**

        Example url: /market/BTGBTC/order/pending?limit=10&offset=0

        **Example response**::

                {
                    "records": [
                        {
                            "deal_fee": "0",
                            "ctime": 1517580449.685034,
                            "maker_fee": "0.001",
                            "price": "0.001254",
                            "deal_stock": "0",
                            "side": 2,      // 1: sell,2: buy
                            "source": "bitpie.client",
                            "amount": "30",
                            "user": 259285,
                            "mtime": 1517580449.685034,
                            "deal_money": "0",
                            "left": "30",
                            "type": 1,      // 1: limit order,2: market order
                            "id": 20321,
                            "market": "BTGBTC",
                            "taker_fee": "0.001"
                        }
                    ],
                    "total": 1,
                    "limit": 10,
                    "offset": 0
                }

        **URL**:
            * ``market`` *(required) - market name, for example *(BCCBTC)*.

        **Parameters**:
            * ``offset`` *(optional)* *(int)* - sinceId.
            * ``limit`` *(optional)* *(int)* - limit.

Market Order Details
--------------------

**GET /market/{market}/order/{orderId}/details**

        Example url: /market/BTGBTC/order/13479/details

        **Example response**::

                {
                    "records": [
                        {
                            "fee": "0.0010194",
                            "deal": "0.0161197722",
                            "price": "0.015813",
                            "amount": "1.0194",
                            "role": 1,
                            "user": 259285,
                            "time": 1517224387.037182,
                            "deal_order_id": 13506,
                            "id": 5288
                        }
                    ],
                    "limit": 20,
                    "offset": 0
                }

        **URL**:
              * ``market`` *(required)*  - market name, for example *(BTGBTC)*.
              * ``orderId`` *(required)* - id,for example *(2168)*.

Market Order Finished
---------------------

**GET /market/{market}/order/finished**

        Example url: /market/BCCBTC/order/finished?limit=10&offset=0

        **Example response**::

            {
                "records": [
                    {
                        "ctime": 1516689377.805243,
                        "maker_fee": "0",
                        "price": "0.151",
                        "deal_fee": "0",
                        "id": 187,
                        "source": "bitpie.client",
                        "amount": "0.001",
                        "ftime": 1516689386.619962,
                        "user": 116480,
                        "deal_stock": "0.001",
                        "deal_money": "0.000151",
                        "type": 1,
                        "side": 1,
                        "market": "BCCBTC",
                        "taker_fee": "0"
                    }
                ],
                "limit": 10,
                "offset": 0
            }

        **URL**:
            * ``market`` *(required) - market name, for example *(BCCBTC)*.

        **Parameters**:
            * ``offset`` *(optional)* *(int)* - sinceId.
            * ``limit`` *(optional)* *(int)* - limit.

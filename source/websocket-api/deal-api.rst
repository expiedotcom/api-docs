.. _deal-api:

********************************************************************************
Deal API
********************************************************************************

Acquire latest executed list
----------------------------

        **Example request**::

            {
                "method": "deals.query",
                "params": [
                    "BCCBTC",           //1.market: market name
                    10,                 //2.limit: amount limit
                    7561                //3.last_id: largest ID of last returned result
                ],
                "id": 1223
            }

        **Response**::

            {
              "error": null,
              "id": 1223,
              "result": []
            }

Latest order list subscription
------------------------------

        **Example request**::

            {
                "method": "deals.subscribe",
                    "params":[          #1. params: market list
                        "BCCBTC",
                        "BCDBTC"
                    ],
                "id": 1223
            }

        **Notify**::

            {
                "method": "deals.update",
                "params": [
                    "BCDBTC",           //1.market name
                    [                   //2.order list
                        {
                            "price": "0.000801",
                            "id": 6834,
                            "time": 1517370019.46558,
                            "amount": "10.5",
                            "type": "buy"
                        },
                        {
                            "price": "0.000801",
                            "id": 6833,
                            "time": 1517369971.09925,
                            "amount": "4.5",
                            "type": "sell"
                        }
                    ]
                ],
                "id": null
            }

Cancel subscription
-------------------

        **Example request**::

            {
                "method": "deals.unsubscribe",
                "params": [],
                "id": 1517466483
            }
        **Response**::

            {
              "error": null,
              "result": {
                "status": "success"
              },
              "id": 1517466483
            }

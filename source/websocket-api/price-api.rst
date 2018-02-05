.. _price-api:

********************************************************************************
Price API
********************************************************************************

Acquire latest price
--------------------

        **Example request**::

                {
                    "method": "price.query",
                    "params": [
                        "BCCBTC"                //1. market: String, market name
                    ],
                    "id": 1517466483
                }

        **Response**::

                {
                    "error": null,
                    "id": 1517466483,
                    "result": "0.14900000"
                }

Latest price subscription
-------------------------
        **Example request**::

                {
                    "method": "price.subscribe",
                    "params": [
                        "BCCBTC"                //1. market list
                    ],
                    "id": 1517466483
                }

        **notify**::

                {
                    "method": "price.update",
                    "params": [
                        "BCCBTC",
                        "0.149"
                    ],
                    "id": null
                }

Latest price unsubscribe
------------------------

        **Example request**::

                {
                    "method": "price.unsubscribe",
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

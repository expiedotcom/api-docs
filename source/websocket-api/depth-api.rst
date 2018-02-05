.. _depth-api:

********************************************************************************
Depth API
********************************************************************************

Depth query
-----------

        **Example request**::

                {
                  "method":"depth.query",
                  "params":[
                  "BCCBTC",           //1.market: market name
                  10,                 //2.limit: Count limit, Integer
                  "0"                 //3.interval: Merge, String e.g. "0" for no interval
                  ],
                  "id":1517465832
                }

        **Response**::

                {
                  "error": null,
                  "result": {
                    "asks": [          //Depth of Sell
                      [
                        "12.94",       //Sell out price
                        "0.1524"       //Sell out count
                      ]
                    ]
                  },
                  "id": 1517465832
                 }

Subscribe market depth
----------------------

        **Example request**::

                {
                "method":"depth.subscribe",
                  "params":[
                    "BCCBTC",           //1.market: market name
                    10,                 //2.limit: Count limit, Integer
                    "0"                 //3.interval: String, e.g. "0" for no interval markets
                  ],
                  "id": 1517465832
                }

        **Notify**::

                {
                  "method": "depth.update",
                  "params": [
                    true,                   //Boolean, true: for complete result, false: for update based on latest retrun result
                    {                       //Update info
                      "bids": [             //Depth of Buy
                        [
                            "0.21082",       //Buy in price
                            "0.0588"         //Buy in count
                        ]
                      ],
                      "asks": [              //Depth of Sell
                        [
                            "0.25082",       //Sell out price
                            "0.988"          //Sell in count
                        ]
                      ]
                    }
                    "BCCBTC"
                  ],
                  "id": null
                }

Unsubscribe depth
-----------------

        **Example request**::

                {
                    "method": "depth.unsubscribe",
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

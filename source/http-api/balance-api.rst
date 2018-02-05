.. _balance-api:

********************************************************************************
Balance API
********************************************************************************

Balance summery
---------------

**GET /balance/summery**

        **Example response**::

            [
                {
                    "coin_code": "BTC",
                    "available_amount": "0",
                    "balance": "0",
                    "ex_trading_amount": "0",
                    "ex_trading_amount_str": "0",
                    "pending_deposit_amount": "0",
                    "ex_available": "0",
                    "escrow_amount": "0",
                    "min_deposit": "0.001",
                    "pending_withdraw_amount": "0",
                    "pending_deposit_amount_str": "0",
                    "pending_withdraw_amount_str": "0",
                    "ex_freeze_str": "0",
                    "min_withdraw": "0.001",
                    "escrow_amount_str": "0",
                    "ex_available_str": "0",
                    "available_amount_str": "0",
                    "ex_freeze": "0",
                    "balance_str": "0"
                }
            ]

Balance history
---------------

**GET /balance/history** *(String: coin_code)* *(int: limit)* *(int: offset)*

        Example url: /balance/history?coin_code=BCC&limit=10&offset=0

        **Example response**::

                {
                    "records": [
                        {
                        "business": "deposit",
                            "detail": {
                                "timestamp_action_id": 1517749392,
                                "id": 85130
                            },
                                "asset": "BCC",
                                "time": 1517749392.541296,
                                "balance": "1",
                                "change": "0.9"
                            },
                            {
                        "business": "deposit",
                            "detail": {
                                "timestamp_action_id": 1517749197,
                                "id": 85128
                            },
                                "asset": "BCC",
                                "time": 1517749197.094249,
                                "balance": "0.1",
                                "change": "0.1"
                            }
                        ],
                    "limit": 10,
                    "offset": 0
                }

        **Parameters**:
            * ``coin_code`` *(required)* *(String)* - coinCode.
            * ``offset`` *(optional)* *(int)* - offset.
            * ``limit`` *(optional)* *(int)* - limit.

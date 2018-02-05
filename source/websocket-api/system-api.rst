.. _system-api:

********************************************************************************
System API
********************************************************************************

PING
----

        **Example request**::

            {
                "method": "server.ping",
                "params": [],
                "id": 1223
            }

        **Response**::

            {
              "error": null,
              "result": "pong",
              "id": 1223
            }

System Time
-----------

        **Example request**::

            {
              "method":"server.time",
              "params":[],
              "id": 1223
             }

        **Response**::

            {
              "error": null,
              "result": 1517455018,
              "id": 1223
            }


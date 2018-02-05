.. _general-usage:

********************************************************************************
General Usage
********************************************************************************

How to use Expie WebSocket?

Access Method
================================================================================

Link address for WebSocket: **wss://api.expie.com/ws**

Access Samples
================================================================================

WebSocket Client sends heartbeat:

::

            {
                "method": "server.ping",
                "params": [],
                "id": 1223
            }
Response:

::

            {
              "error": null,
              "result": "pong",
              "id": 1223
            }

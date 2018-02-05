.. _general-usage:

********************************************************************************
General Usage
********************************************************************************

How to use Expie API?

Access Method
================================================================================

Domain: **api.expie.com**

All API should be accessed with ``access-token`` (in HTTP header), and you can apply for your API access-token in Bitpie APP.

Access Samples
================================================================================

Python:

::

    domain = 'api.expie.com'
    url = 'https://' + domain
    access-token = 'e0b20185864172a0e209836e29d94be9fd2ca85c0a3ef4641f502d3c085820ea'
    request = urllib2.Request(url)
    request.add_header('access-token', access-token)

Curl:

::

    curl -H "access-token:e0b20185864172a0e209836e29d94be9fd2ca85c0a3ef4641f502d3c085820ea" https://api.expie.com/market


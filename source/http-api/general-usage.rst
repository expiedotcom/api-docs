.. _general-usage:

********************************************************************************
General Usage
********************************************************************************

How to use Expie API?

Access Method
================================================================================

Domain: **api.expie.com**

All API should be accessed with ``auth_token`` (in HTTP Authorization), and you can apply for your API auth_token in Bitpie APP.

Access Samples
================================================================================

Python:

::

    domain = 'api.expie.com'
    rootPath = '/v1'
    url = 'https://' + domain + rootPath + '/markets'
    Authorization = 'Bearer' + 'e0b20185864172a0e209836e29d94be9fd2ca85c0a3ef4641f502d3c085820ea'
    request = urllib2.Request(url)

Curl:

::

    curl -H "Authorization: Bearer e0b20185864172a0e209836e29d94be9fd2ca85c0a3ef4641f502d3c085820ea" https://api.expie.com/v1/markets


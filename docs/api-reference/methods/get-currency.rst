.. _get-currency:

List supported currency information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

    GET /v2/currencies

Gets information on supported monetary currencies.

This operation retrieves a list of supported monetary currencies.

Request
-------

The request has the following URI and header parameters.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - ``X-Auth-Token``
     - Header string *(Required)*
     - A valid authentication token.
   * - ``Content-type``
     - Header string
     - Value: ``application/json``.
   * - ``Accept``
     - Header string
     - Value: ``application/json``.
   * - ``{limit}``
     - String
     - The maximum number of items to return. This value should be ``100`` or
       less. The default value is ``100``.
   * - ``{marker}``
     - String
     - The starting point for the return data. This parameter is used to
       control pagination.

This operation does not accept a request body.

**Example request: header**

The following example shows the header information.

.. code::

   X-Auth-Token: f064c46a782c444cb4ba4b6434288f7c
   Content-Type: application/json
   Accept: application/json


Response
--------

The response has the following body parameters.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - currencies
     - Object
     - An info block that contains details about supported currencies.
   * - currencies.\ *currency*
     - Array
     - An info block that contains details about currencies.
   * - currencies.\ currency.\ *code*
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
   * - currencies.\ currency.\ *description*
     - String
     - The description of the currency.
   * - currencies.\ currency.\ *symbol*
     - String
     - The symbol for the currency.
   * - currencies.\ currency.\ *subdivision*
     - String
     - The subdivision of the currency.
   * - currencies.\ *link*
     - String
     - An info block that contains details about the links for the results.
   * - currencies.\ link.\ *href*
     - String
     - The URL for a set of results.
   * - currencies.\ link.\ *rel*
     - String
     - The relationship between the current information and the linked
       information.

**Example response**

The following example shows the response for the request.

.. code::

   Status Code: 200 OK
   Content-Length: 4543
   Content-Type: application/json
   Date: Wed, 03 Dec 2014 17:13:30 GMT
   Server: Jetty(8.0.y.z-SNAPSHOT)
   Via: 1.1 Repose (Repose/2.12)
   x-compute-request-id: req-7b7ffed2-9b1f-46a8-a478-315518d35387

   {
    "currencies": {
        "currency": [
            {
                "code": "AUD",
                "description": "Australian Dollar",
                "symbol": "\\u0041\\u0024",
                "subDivision": "cents"
            },
            {
                "code": "EUR",
                "description": "Euro",
                "symbol": "\\u20AC",
                "subDivision": "cents"
            },
            {
                "code": "HKD",
                "description": "Hong Kong Dollar",
                "symbol": "\\u0048\\u004B\\u0024",
                "subDivision": "cents"
            },
            {
                "code": "USD",
                "description": "US Dollar",
                "symbol": "\\u0024",
                "subDivision": "cents"
            },
            {
                "code": "GBP",
                "description": "Pound Sterling",
                "symbol": "\\u00A3",
                "subDivision": "pence"
            }
        ],
        "link": [
            {
                "href": "http://offer.api.rackspacecloud.com/v2/currencies?marker=1&limit=10",
                "rel": "next"
            },
            {
                "href": "http://offer.api.rackspacecloud.com/v2/currencies?marker=101&limit=10",
                "rel": "previous"
            }
          ]
        }
      }


Response codes
--------------

This operation can have the following response codes.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Code
     - Name
     - Description
   * - 200
     - Success
     - The request succeeded.
   * - 400
     - Error
     - A general error has occurred.
   * - 404
     - Not Found
     - The requested resource is not found.
   * - 405
     - Method Not Allowed
     - The method received in the request line is known by the origin server
       but is not supported by the target resource.
   * - 406
     - Not Acceptable
     - The value in the ``Accept`` header is not supported.
   * - 500
     - API Fault
     - The server encountered an unexpected condition that prevented it from
       fulfilling the request.

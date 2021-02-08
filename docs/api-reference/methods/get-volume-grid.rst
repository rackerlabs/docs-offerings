.. _get-volume-grid:

List volume grid
~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/volumeGrids/{volumeGridId}

Gets information on a specific volume grid.

This operation retrieves a volume grid.

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
   * - ``{volumeGridId}``
     - String *(Required)*
     - The ID for the volume grid. Example: ``STANDARD_USA_ONDEMAND_GRID_001``.

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
   * - volumeGrid
     - Object
     - An object that contains information about the volume grid.
   * - volumeGrid.\ *description*
     - String
     - The description of the volume grid.
   * - volumeGrid.\ *offerings*
     - Complex type
     - An info block that contains details about the offerings that are
       associated with the volume grid.
   * - volumeGrid.\ offerings.\ *offering*
     - Array
     - An array of offering codes.
   * - volumeGrid.\ offerings.\ offering.\ *offeringCode*
     - String
     - The code for the offering.
   * - volumeGrid.\ *volumeTiers*
     - Complex type
     - An info block that contains details about volume tiers.
   * - volumeGrid.\ volumeTiers.\ *volumeTier*
     - Complex type
     - An info block that contains details about a specific volume tier.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ *minAmount*
     - String
     - The minimum amount of the discount.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ *maxAmount*
     - String
     - The maximum amount of the discount.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ *discountPercentage*
     - String
     - The percentage of the discount.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ *tierIndex*
     - Integer
     - The index for the tier. This number is used to organize tiers.
   * - volumeGrid.\ *id*
     - String
     - The ID for the volume grid.
   * - volumeGrid.\ *geo*
     - String
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - volumeGrid.\ *currency*
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
   * - volumeGrid.\ *gridType*
     - String
     -
       - ``STANDARD``: Offers pre-defined discounts based on the length of the
         commitment. By default, only ``STANDARD`` grids are returned.
       - ``CUSTOM``: Offers a customized discount based on a customer's
         request.
   * - volumeGrid.\ *gridVersion*
     - String
     - The version of the volume grid.
   * - volumeGrid.\ *gridStartDate*
     - String
     - The date and time that the volume grid begins.
   * - volumeGrid.\ *gridEndDate*
     - String
     - The date and time that the volume grid ends.

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
      "volumeGrid": {
          "description": "Standard USA On Demand Grid for Commit Discounts",
          "offerings": {
              "offering": [
                  {
                      "offeringCode": "FSTGEN"
                  },
                  {
                      "offeringCode": "MFSTGEN"
                  },
                  {
                      "offeringCode": "NXTGEN"
                  },
                  {
                      "offeringCode": "MNXTGEN"
                  }
              ]
          },
          "volumeTiers": {
              "volumeTier": [
                  {
                      "minAmount": "0",
                      "maxAmount": "5000",
                      "discountPercentage": "0",
                      "tierIndex": 1
                  },
                  {
                      "minAmount": "5001",
                      "maxAmount": "10000",
                      "discountPercentage": "4",
                      "tierIndex": 2
                  },
                  {
                      "minAmount": "10001",
                      "maxAmount": "25000",
                      "discountPercentage": "8",
                      "tierIndex": 3
                  },
                  {
                      "minAmount": "25001",
                      "maxAmount": "50000",
                      "discountPercentage": "12",
                      "tierIndex": 4
                  },
                  {
                      "minAmount": "50001",
                      "maxAmount": "100000",
                      "discountPercentage": "16",
                      "tierIndex": 5
                  },
                  {
                      "minAmount": "100001",
                      "maxAmount": "200000",
                      "discountPercentage": "20",
                      "tierIndex": 6
                  },
                  {
                      "minAmount": "200001",
                      "discountPercentage": "24",
                      "tierIndex": 7
                  }
              ]
          },
          "id": "STANDARD_USA_ONDEMAND_GRID_001",
          "geo": "USA",
          "currency": "USD",
          "gridType": "STANDARD",
          "gridVersion": "1",
          "gridStartDate": "2013-05-30-05:00"
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

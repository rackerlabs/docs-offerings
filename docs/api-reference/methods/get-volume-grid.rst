.. _get-volume-grid:

List volume grid
~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/volumeGrids/{volumeGridId}

Gets information on a specific volume grid.

This operation retrieves a volume grid.

Request
-------

The request has the following query parameters.

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
     - Value: ``application/json`` or ``application/xml``.
   * - ``Accept``
     - Header string
     - Value: ``application/json`` or ``application/xml``.
   * - ``volumeGridId`` *(Required)*
     - String
     - The ID for the volume grid.

This operation does not accept a request body.

**Example Request: header**

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
   * - **volumeGrid**
     - Object
     - An object containing information about the volume grid.
   * - volumeGrid.\ **description**
     - String
     - The description of the volume grid. Example: ``Standard USA On Demand
       Grid for Commit Discounts``.
   * - volumeGrid.\ **offerings**
     - Complex type
     - An info block containing details about offerings.
   * - volumeGrid.\ offerings.\ **offering**
     - Array
     - An array of offering codes.
   * - volumeGrid.\ offerings.\ offering.\ **offeringCode**
     - String
     - A code for the offering. Example: ``FSTGEN``.
   * - volumeGrid.\ **volumeTiers**
     - Complex type
     - An info block containing details about volume tiers.
   * - volumeGrid.\ volumeTiers.\ **volumeTier**
     - Complex type
     - An info block containing details about a volume tier.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ **minAmount**
     - String
     - The minimum amount of the discount.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ **maxAmount**
     - String
     - The maximum amount of the discount.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ **discountPercentage**
     - String
     - The percentage of the discount.
   * - volumeGrid.\ volumeTiers.\ volumeTier.\ **tierIndex**
     - Integer
     - The index for the tier. This number is used to organize tiers.
   * - volumeGrid.\ **id**
     - String
     - The ID for the volume grid
   * - volumeGrid.\ **geo**
     - Geographical RegionType
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - volumeGrid.\ **currency**
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
       - ``HKD``: Hong Kong Dollar
   * - volumeGrid.\ **gridType**
     - String
     - The type of grid. By default only ``STANDARD`` grids are returned.
   * - volumeGrid.\ **gridVersion**
     - String
     - The version of the commit grid. Example: ``1``.
   * - volumeGrid.\ **gridStartDate**
     - String
     - The date and time that the commit grid begins. Example:
       ``2013-05-30-05:00``.
   * - volumeGrid.\ **gridEndDate**
     - String
     - The date and time that the commit grid ends. Example:
       ``2013-05-30-05:00``.

**Example response: JSON**

The following example shows the JSON response for the request.

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

**Example response: XML**

The following example shows the XML response for the request.

.. code::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <ns2:volumeGrid id="USACOMPUTECOMMITSTANDARDGRID_001" geo="USA" currency="USD"
    gridType="STANDARD" gridVersion="1" gridStartDate="2002-09-24-06:00" gridEndDate="2002-09-24-06:00" xmlns:ns2="http://offer.api.rackspacecloud.com/v2">
    <ns2:description>Standard US Volume Grid</ns2:description>
    <ns2:offerings>
        <ns2:offering offeringCode="NXTGEN" />
        <ns2:offering offeringCode="MNXTGEN"/>
        <ns2:offering offeringCode="FSTGEN"/>
        <ns2:offering offeringCode="MFSTGEN"/>
    </ns2:offerings>
    <ns2:volumeTiers>
        <ns2:volumeTier minAmount="0" maxAmount="5000" discountPercentage="12.00" tierIndex="1"/>
        <ns2:volumeTier minAmount="5001" maxAmount="10000" discountPercentage="14.00" tierIndex="2"/>
        <ns2:volumeTier minAmount="10001" maxAmount="25000" discountPercentage="16.00" tierIndex="3"/>
        <ns2:volumeTier minAmount="25001" maxAmount="50000" discountPercentage="18.00" tierIndex="4"/>
        <ns2:volumeTier minAmount="50001" maxAmount="100000" discountPercentage="20.00" tierIndex="5"/>
        <ns2:volumeTier minAmount="100001" maxAmount="200000" discountPercentage="22.00" tierIndex="6"/>
    </ns2:volumeTiers>
  </ns2:volumeGrid>

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

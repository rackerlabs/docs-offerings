.. _create-volume-grid:

Create volume grid
~~~~~~~~~~~~~~~~~~

.. code::

    POST /discountGrids/volumeGrids

Creates a volume grid.

This operation creates a volume grid.

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
     - A valid authentication token
   * - ``Content-type``
     - Header string
     - Value: ``application/json`` or ``application/xml``
   * - ``Accept``
     - Header string
     - Value: ``application/json`` or ``application/xml``

    The request has the following body parameters.

    .. list-table::
      :widths: 15 10 30
      :header-rows: 1

   * - ``volumeGrid`` *(Required)*
     - Object
     - An info block containing information about the commit grid.
   * - volumeGrid.\ *description*
     - String
     - A description of the commit grid.
   * - volumeGrid.\ *offerings*
     - Object
     - An object containing one or more ``offeringCode``.
   * - volumeGrid.\ *volumeTiers*
     - Object
     - An object containing information on any volume tiers.
   * - ``id``
     - String
     - The ID for the volume grid.
   * - ``geo``
     - String
     - This parameter is used to filter and retrieve products with only prices
       for specific geography where the Offering is available. Valid values
       are ``USA``, ``UK``, ``AUS`, and ``APAC``.
   * - ``currency``
     - String
     - This parameter is used to filter and retrieve products with only prices
       for specific currency. Valid values are ``USD`` and ``GBP``.
   * - ``gridType``
     - String
     - Valid values are ``STANDARD`` and ``PRESET``. By default only
       ``STANDARD`` grids are returned.
   * - ``gridVersion``
     - String
     - The version of the grid. Example: 1.
   * - ``gridStartDate``
     - String
     - The date and time that the grid begins.
   * - ``gridEndDate``
     - String
     - The date and time that the grid ends.

**Example Request: header**

The following example shows the header information.

.. code::

   X-Auth-Token: f064c46a782c444cb4ba4b6434288f7c
   Content-Type: application/json
   Accept: application/json

**Example Request: JSON**

.. code::

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

**Example Request: XML**

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


Response
--------

The response has the following body parameters.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - **images**\.[]
     - Array
     - An array of images in the list.
   * - images.\ **id**
     - String
     - The UUID of the image.
   * - images.\ **name**
     - String
     - The name of the image.
   * - images.\ **status**
     - String
     - The status of the image. For possible image statuses,
       see :ref:`Statuses <statuses>`.
   * - images.\ **visibility**
     - String
     - Specifies image visibility as ``public``, ``private``, or ``shared``.
   * - images.\ **size**
     - String
     - The size of the image in bytes.
   * - images.\ **checksum**
     - String
     - The checksum of this image.
   * - images.\ **self**
     - String
     - The link to the image.
   * - images.\ **file**
     - String
     - The image file.
   * - **first**
     - String
     - The URI for the first image in the list.
   * - **first**
     - String
     - The URI for the next image in the list.
   * - **last**
     - String
     - The URI for the last image in the list.

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
   * - 201
     - Created
     - The resource was created.
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
   * - 415
     - Unsupported Media Type
     - The payload type is not supported.
   * - 500
     - API Fault
     - The server encountered an unexpected condition that prevented it from
       fulfilling the request.

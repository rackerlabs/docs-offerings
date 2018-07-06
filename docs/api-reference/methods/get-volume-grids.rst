.. _get-volume-grids:

List volume grids
~~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/volumeGrids

Gets information on volume grids.

This operation retrieves a list of volume grids.

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
     - Value: ``application/json`` or ``application/xml``.
   * - ``Accept``
     - Header string
     - Value: ``application/json`` or ``application/xml``.
   * - ``{geo}``
     - String *(Required)*
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - ``{gridType}``
     - String
     -
       - ``STANDARD``: Offers pre-defined discounts based on the length of the
         commitment. By default only ``STANDARD`` grids are returned.
       - ``CUSTOM``: Offers a customized discount based on a customer's
         request.
   * - ``{currency}``
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro

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
   * - volumeGrids
     - Object
     - An object containing information about the volume grids.
   * - volumeGrids.\ *volumeGrid*
     - Object
     - An object containing information about a specific volume grid.
   * - volumeGrids.\ volumeGrid.\ *link*
     - Object
     - An info block that contains details about the link for the volume grid.
   * - volumeGrids.\ volumeGrid.\ link.\ *href*
     - String
     - The URL for the volume grid.
   * - volumeGrids.\ volumeGrid.\ link.\ *rel*
     - String
     - The relationship between the current document and the linked document.
   * - volumeGrids.\ volumeGrid.\ *id*
     - String
     - The ID for the volume grid.
   * - volumeGrids.\ volumeGrid.\ *geo*
     - Geographical RegionType
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - volumeGrids.\ volumeGrid.\ *currency*
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
       - ``HKD``: Hong Kong Dollar
   * - volumeGrids.\ volumeGrid.\ *gridType*
     - String
     - The type of grid. By default only ``STANDARD`` grids are returned.
   * - volumeGrids.\ volumeGrid.\ *gridVersion*
     - String
     - The version of the commit grid.
   * - volumeGrids.\ volumeGrid.\ *gridStartDate*
     - String
     - The date and time that the commit grid begins.
   * - volumeGrids.\ volumeGrid.\ *gridEndDate*
     - String
     - The date and time that the commit grid ends.
   * - volumeGrids.\ *link*
     - Object
     - An info block that contains details about the link for the volume grids.
   * - volumeGrids.\ link.\ *href*
     - String
     - The URL for the volume grids.
   * - volumeGrids.\ link.\ *rel*
     - String
     - The relationship between the current document and the linked document.

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
    "volumeGrids":{
        "volumeGrid":[{
                "link":{
                    "href":"https://test.offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids/STANDARD_AUS_VOLUME_GRID_001",
                    "rel":"self"
                },
                "id":"STANDARD_AUS_VOLUME_GRID_001",
                "geo":"AUS",
                "currency":"USD",
                "gridType":"STANDARD",
                "gridVersion":"1",
                "gridStartDate":"2013-05-30-05:00"
            },
            {
                "link":{
                    "href":"https://test.offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids/STANDARD_UK_VOLUME_GRID_001",
                    "rel":"self"
                },
                "id":"STANDARD_UK_VOLUME_GRID_001",
                "geo":"UK",
                "currency":"GBP",
                "gridType":"STANDARD",
                "gridVersion":"1",
                "gridStartDate":"2013-05-30-05:00"
            },
            {
                "link":{
                    "href":"https://test.offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids/STANDARD_USA_VOLUME_GRID_001",
                    "rel":"self"
                },
                "id":"STANDARD_USA_VOLUME_GRID_001",
                "geo":"USA",
                "currency":"USD",
                "gridType":"STANDARD",
                "gridVersion":"1",
                "gridStartDate":"2013-05-30-05:00"
            }
        ],
        "link":[{
                "href":"https://test.offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids?marker=0&limit=100",
                "rel": "next"
            },
            {
                "href":"https://test.offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids?marker=0&limit=100",
                "rel": "prev"
            }
          ]
        }
      }

**Example response: XML**

The following example shows the XML response for the request.

.. code::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <tns:volumeGrids xmlns:html="http://www.w3.org/1999/xhtml"
    xmlns:atom="http://www.w3.org/2005/Atom"
    xmlns:tns="http://offer.api.rackspacecloud.com/v2">
    <tns:volumeGrid id="USAVOLUMEGRID_001" geo="geo0" currency="USD" gridType="STANDARD" gridVersion="1" gridStartDate="2006-05-04"
        gridEndDate="2006-05-04">
        <atom:link href="https://offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids/A0001" rel="self"/>
    </tns:volumeGrid>
    <tns:volumeGrid id="id1" geo="geo1" currency="USD" gridType="PRESET" gridVersion="gridVersion1" gridStartDate="2006-05-04"
        gridEndDate="2006-05-04">
        <atom:link href="https://offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids/A0001" rel="self"/>
    </tns:volumeGrid>
    <atom:link
        href="https://offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids?marker=0&amp;limit=100"
        rel="next"/>
    <atom:link
        href="https://offer.api.rackspacecloud.com/v1/discountGrids/volumeGrids?marker=0&amp;limit=100"
        rel="prev"/>
  </tns:volumeGrids>

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

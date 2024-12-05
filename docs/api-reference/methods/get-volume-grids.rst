.. _get-volume-grids:

List volume grids
~~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/volumeGrids

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
     - Value: ``application/json``.
   * - ``Accept``
     - Header string
     - Value: ``application/json``.
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
         commitment. By default, only ``STANDARD`` grids are returned.
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
   * - volumeGrids
     - Object
     - An object that contains information about the volume grids.
   * - volumeGrids.\ *volumeGrid*
     - Object
     - An object that contains information about a specific volume grid.
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
   * - volumeGrids.\ volumeGrid.\ *gridType*
     - String
     -
     - ``STANDARD``: Offers pre-defined discounts based on the length of the
       commitment. By default, only ``STANDARD`` grids are returned.
     - ``CUSTOM``: Offers a customized discount based on a customer's
       request.
   * - volumeGrids.\ volumeGrid.\ *gridVersion*
     - String
     - The version of the volume grid.
   * - volumeGrids.\ volumeGrid.\ *gridStartDate*
     - String
     - The date and time that the volume grid begins.
   * - volumeGrids.\ volumeGrid.\ *gridEndDate*
     - String
     - The date and time that the volume grid ends.
   * - volumeGrids.\ *link*
     - Object
     - An info block that contains details about the links for the results.
   * - volumeGrids.\ link.\ *href*
     - String
     - The URL for the results.
   * - volumeGrids.\ link.\ *rel*
     - String
     - The relationship between the current document and the linked document.

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
      "volumeGrids": {
          "volumeGrid": [
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/volumeGrids/STANDARD_AUS_AUD_VOLUME_GRID_001"
                  },
                  "id": "STANDARD_AUS_AUD_VOLUME_GRID_001",
                  "geo": "AUS",
                  "currency": "AUD",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2015-06-26Z"
              },
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/volumeGrids/STANDARD_AUS_EUR_VOLUME_GRID_001"
                  },
                  "id": "STANDARD_AUS_EUR_VOLUME_GRID_001",
                  "geo": "AUS",
                  "currency": "EUR",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2015-06-25Z"
              },
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/volumeGrids/STANDARD_AUS_GBP_VOLUME_GRID_001"
                  },
                  "id": "STANDARD_AUS_GBP_VOLUME_GRID_001",
                  "geo": "AUS",
                  "currency": "GBP",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2015-06-25Z"
              },
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/volumeGrids/STANDARD_AUS_VOLUME_GRID_001"
                  },
                  "id": "STANDARD_AUS_VOLUME_GRID_001",
                  "geo": "AUS",
                  "currency": "USD",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2013-05-30Z",
                  "gridEndDate": "2015-06-19Z"
              }
          ],
          "link": []
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

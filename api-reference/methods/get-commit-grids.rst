.. _get-commit-grids:

List commit grids
~~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/commitGrids?geo={location}

Gets information on commit grids.

This operation retrieves a list of commit grids.

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
   * - commitGrids
     - Object
     - An object that contains information about the commit grids.
   * - commitGrids.\ *commitGrid*
     - Object
     - An object that contains information about a specific commit grid.
   * - commitGrids.\ commitGrid.\ *link*
     - Object
     - An info block that contains details about the link for the commit grid.
   * - commitGrids.\ commitGrid.\ link.\ *href*
     - String
     - The URL for the commit grid.
   * - commitGrids.\ commitGrid.\ link.\ *rel*
     - String
     - The relationship between the current information and the linked
       information.
   * - commitGrids.\ commitGrid.\ *id*
     - String
     - The ID for the commit grid.
   * - commitGrids.\ commitGrid.\ *geo*
     - String
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - commitGrids.\ commitGrid.\ *currency*
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
   * - commitGrids.\ commitGrid.\ *gridType*
     - String
     -
       - ``STANDARD``: Offers pre-defined discounts based on the length of the
           commitment. By default, only ``STANDARD`` grids are returned.
       - ``CUSTOM``: Offers a customized discount based on a customer's
           request.
   * - commitGrids.\ commitGrid.\ *gridVersion*
     - String
     - The version of the commit grid.
   * - commitGrids.\ commitGrid.\ *gridStartDate*
     - String
     - The date and time that the commit grid begins.
   * - commitGrids.\ commitGrid.\ *gridEndDate*
     - String
     - The date and time that the commit grid ends.
   * - commitGrids.\ *link*
     - Object
     - An info block that contains details about the links for the results.
   * - commitGrids.\ link.\ *href*
     - String
     - The URL for a set of results.
   * - commitGrids.\ link.\ *rel*
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
      "commitGrids": {
          "commitGrid": [
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/commitGrids/STANDARD_USA_AUD_COMMIT_GRID_001"
                  },
                  "id": "STANDARD_USA_AUD_COMMIT_GRID_001",
                  "geo": "USA",
                  "currency": "AUD",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2015-06-25Z"
              },
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/commitGrids/STANDARD_USA_COMMIT_GRID_001"
                  },
                  "id": "STANDARD_USA_COMMIT_GRID_001",
                  "geo": "USA",
                  "currency": "USD",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2013-05-30Z",
                  "gridEndDate": "2015-06-19Z"
              },
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/commitGrids/STANDARD_USA_EUR_COMMIT_GRID_001"
                  },
                  "id": "STANDARD_USA_EUR_COMMIT_GRID_001",
                  "geo": "USA",
                  "currency": "EUR",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2015-06-25Z"
              },
              {
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/discountGrids/commitGrids/STANDARD_USA_GBP_COMMIT_GRID_001"
                  },
                  "id": "STANDARD_USA_GBP_COMMIT_GRID_001",
                  "geo": "USA",
                  "currency": "GBP",
                  "gridType": "STANDARD",
                  "gridVersion": "1",
                  "gridStartDate": "2015-06-25Z"
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

.. _get-commit-grids:

List commit grids
~~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/commitGrids

Gets information on commit grids.

This operation retrieves a list of commit grids.

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
   * - ``geo`` *(Required)*
     - Geographical RegionType
     - Eaxmples include ``USA``, ``UK``, ``AUS``, and ``APAC``.
   * - ``gridType``
     - String
     - Valid values are ``STANDARD`` and ``PRESET``. By default only ``STANDARD`` grids are returned.
   * - ``currency``
     - String
     - This parameter is used to filter and retrieve products with only prices
       for specific currency. Valid values are ``USD``, ``GBP``, ``AUD``, and ``EUR``. By default only ``STANDARD`` grids are returned.

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
    "commitGrids": {
        "commitGrid": [
            {
                "link": {
                    "href": "https://test.offer.api.rackspacecloud.com/v1/discountGrids/commitGrids/STANDARD_AUS_COMMIT_GRID_001",
                    "rel":"self"
                },
                "id": "STANDARD_AUS_COMMIT_GRID_001",
                "geo": "AUS",
                "currency": "USD",
                "gridType": "STANDARD",
                "discountType": "COMMIT",
                "gridVersion": "1",
                "gridStartDate": "2013-05-30-05:00"
            },
            {
                "link": {
                    "href": "https://test.offer.api.rackspacecloud.com/v1/discountGrids/commitGrids/STANDARD_UK_COMMIT_GRID_001",
                    "rel":"self"
                },
                "id": "STANDARD_UK_COMMIT_GRID_001",
                "geo": "UK",
                "currency": "GBP",
                "gridType": "STANDARD",
                "discountType": "COMMIT",
                "gridVersion": "1",
                "gridStartDate": "2013-05-30-05:00"
            },
            {
                "link": {
                    "href": "https://test.offer.api.rackspacecloud.com/v1/discountGrids/commitGrids/STANDARD_USA_COMMIT_GRID_001",
                    "rel":"self"
                },
                "id": "STANDARD_USA_COMMIT_GRID_001",
                "geo": "USA",
                "currency": "USD",
                "gridType": "STANDARD",
                "gridVersion": "1",
                "gridStartDate": "2013-05-30-05:00"
            }
        ],
        "link": [
            {
                "href": "https://test.offer.api.rackspacecloud.com/v1/discountGrids/commitGrids?marker=0&limit=100",
                "rel":"next"
            },
            {
                "href": "https://test.offer.api.rackspacecloud.com/v1/discountGrids/commitGrids?marker=0&limit=100",
                "rel":"prev"
            }
          ]
        }
      }

**Example response: XML**

The following example shows the XML response for the request.

.. code::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <tns:commitGrids xmlns:html="http://www.w3.org/1999/xhtml"
    xmlns:atom="http://www.w3.org/2005/Atom"
    xmlns:tns="http://offer.api.rackspacecloud.com/v2">
    <tns:commitGrid id="USACOMPUTECOMMITSTANDARDGRID_001" geo="geo0" currency="USD" gridType="STANDARD" gridVersion="1" gridStartDate="2006-05-04"
        gridEndDate="2006-05-04">
        <atom:link href="https://offer.api.rackspacecloud.com/v1/discountGrids/commitGrids/A0001" rel="self"/>
    </tns:commitGrid>
    <tns:commitGrid id="id1" geo="geo1" currency="currency1" gridType="STANDARD" gridVersion="gridVersion1" gridStartDate="2006-05-04"
        gridEndDate="2006-05-04">
        <atom:link href="https://offer.api.rackspacecloud.com/v1/discountGrids/commitGrids/A0001" rel="self"/>
    </tns:commitGrid>
    <atom:link
        href="https://offer.api.rackspacecloud.com/v1/discountGrids/commitGrids?marker=0&amp;limit=100"
        rel="next"/>
    <atom:link
        href="https://offer.api.rackspacecloud.com/v1/discountGrids/commitGrids?marker=0&amp;limit=100"
        rel="prev"/>
  </tns:commitGrids>

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

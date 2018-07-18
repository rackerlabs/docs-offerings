.. _get-offerings:

List offerings
~~~~~~~~~~~~~~

.. code::

    GET /v2/offerings

This operation retrieves all of the Rackspace offerings that are available in
the product catalog.

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
   * - ``{lineOfBusiness}``
     - String
     - The Rackspace line of business that is associated with the offering.
       For example, a ``lineOfBusiness`` value of ``US_CLOUD`` returns the products for ``US_CLOUD``.
   * - ``{status}``
     - String
     -
       - ``ACTIVE``: Default
       - ``INACTIVE``: An offering becomes  ``INACTIVE`` when Rackspace
         introduces a new version of the offering. When an offering becomes
         ``INACTIVE``, all of the products that belong to that offering also
         become ``INACTIVE``.
   * - ``{limit}``
     - String
     - The maximum number of items to return. This value should be ``100`` or
       less. The default value is ``100``.
   * - ``{marker}``
     - String
     - The starting point for the return data. This parameter controls
       pagination.

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
   * - offerings
     - Array
     - An array of offerings.
   * - offerings.\ *offering*
     - Array
     - An info block that contains details about a specific offering.
   * - offerings.\ *offering*.\ *offeringCode*
     - String
     - A business identifier for the offering. This identifier remains
       consistent when a new version of the offering is introduced. Only
       one version of an ``offeringCode`` may have an ``ACTIVE`` status.
   * - offerings.\ *offering*.\ *offeringVersion*
     - Integer
     - The business version of the offering.
   * - offerings.\ *offering*.\ *name*
     - String
     - The name of the offering.
   * - offerings.\ offering.\ *description*
     - String
     - The description of the offering.
   * - offerings.\ offering.\ *lineOfBusinesses*
     - Complex type
     - An info block that contains details about the Rackspace lines of
       business that are associated with the offering.
   * - offerings.\ offering.\ lineOfBusinesses.\ *lineOfBusiness*
     - Object
     - Information on the Rackspace lines of business that are associated with
       the offering.
   * - offerings.\ offering.\ *link*
     - Object
     - An info block that contains details about the link for the offering.
   * - offerings.\ offering.\ link.\ *rel*
     - String
     - The relationship between the current information and the linked
       information.
   * - offerings.\ offering.\ link.\ *href*
     - String
     - The URL for the link.
   * - offerings.\ offering.\ link.\ *title*
     - String
     - The title of the link.
   * - offerings.\ offering.\ *status*
     - String
     - The status of the offering. Valid values are ``ACTIVE`` (default) and
       ``INACTIVE``. An offering becomes  ``INACTIVE`` when Rackspace
       introduces a new version of the offering.
   * - offerings.\ *offering*.\ *id*
     - String
     - The universally unique identifier (UUID) for the offering.
   * - offerings.\ *link*
     - Object
     - An info block that contains details about the link for the results.
   * - offerings.\ link.\ *rel*
     - String
     - The relationship between the current information and the linked
       information.
   * - offerings.\ link.\ *href*
     - String
     - The URL for a set of results.

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
      "offerings": {
          "offering": [
              {
                  "offeringCode": "DBAAS",
                  "offeringVersion": 2,
                  "name": "CLOUD DATABASES",
                  "description": "CLOUD DATABASES",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/fd2c2294-0498-3791-9df7-1d4ed883a939/products",
                      "title": "CLOUD DATABASES"
                  },
                  "status": "ACTIVE",
                  "id": "fd2c2294-0498-3791-9df7-1d4ed883a939"
              },
              {
                  "offeringCode": "CBS",
                  "offeringVersion": 2,
                  "name": "CLOUD BLOCK STORAGE",
                  "description": "CLOUD BLOCK STORAGE",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/a9b2e361-c7de-37e0-8bdb-40fb33ac1576/products",
                      "title": "CLOUD BLOCK STORAGE"
                  },
                  "status": "ACTIVE",
                  "id": "a9b2e361-c7de-37e0-8bdb-40fb33ac1576"
              },
              {
                  "offeringCode": "CLOUDBIGDATA",
                  "offeringVersion": 2,
                  "name": "CLOUD BIG DATA",
                  "description": "CLOUD BIG DATA",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/86af1b3c-682d-3114-9549-9a6e9ee12084/products",
                      "title": "CLOUD BIG DATA"
                  },
                  "status": "ACTIVE",
                  "id": "86af1b3c-682d-3114-9549-9a6e9ee12084"
              },
              {
                  "offeringCode": "RCDN",
                  "offeringVersion": 2,
                  "name": "RACKSPACE CDN",
                  "description": "RACKSPACE CDN",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/77d04f01-c000-32e9-aa6a-aac4ec3b5d35/products",
                      "title": "RACKSPACE CDN"
                  },
                  "status": "ACTIVE",
                  "id": "77d04f01-c000-32e9-aa6a-aac4ec3b5d35"
              },
              {
                  "offeringCode": "LBAAS",
                  "offeringVersion": 2,
                  "name": "CLOUD LOAD BALANCER",
                  "description": "CLOUD LOAD BALANCER",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/6d1e4a24-49df-3d67-88a5-0aa53e6eec23/products",
                      "title": "CLOUD LOAD BALANCER"
                  },
                  "status": "ACTIVE",
                  "id": "6d1e4a24-49df-3d67-88a5-0aa53e6eec23"
              },
              {
                  "offeringCode": "FSTGEN",
                  "offeringVersion": 2,
                  "name": "FIRST GENERATION CLOUD SERVERS",
                  "description": "FIRST GENERATION CLOUD SERVERS",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/6d02e6d4-f45f-3f65-b56b-d83ec803a6bb/products",
                      "title": "FIRST GENERATION CLOUD SERVERS"
                  },
                  "status": "ACTIVE",
                  "id": "6d02e6d4-f45f-3f65-b56b-d83ec803a6bb"
              },
              {
                  "offeringCode": "CBCKUP",
                  "offeringVersion": 2,
                  "name": "CLOUD BACKUP",
                  "description": "CLOUD BACKUP",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/41cb76aa-dd4d-3bd6-b305-e25f3fb3bae7/products",
                      "title": "CLOUD BACKUP"
                  },
                  "status": "ACTIVE",
                  "id": "41cb76aa-dd4d-3bd6-b305-e25f3fb3bae7"
              },
              {
                  "offeringCode": "CMNCLD",
                  "offeringVersion": 2,
                  "name": "COMMON CLOUD OFFERING",
                  "description": "COMMON CLOUD OFFERING",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/3a14712f-c617-3481-b397-174dfff1e41f/products",
                      "title": "COMMON CLOUD OFFERING"
                  },
                  "status": "ACTIVE",
                  "id": "3a14712f-c617-3481-b397-174dfff1e41f"
              },
              {
                  "offeringCode": "NXTGEN",
                  "offeringVersion": 2,
                  "name": "NEXT GENERATION CLOUD SERVERS",
                  "description": "NEXT GENERATION CLOUD SERVERS",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/387e19d3-d2bb-3310-96c7-8ea708239646/products",
                      "title": "NEXT GENERATION CLOUD SERVERS"
                  },
                  "status": "ACTIVE",
                  "id": "387e19d3-d2bb-3310-96c7-8ea708239646"
              },
              {
                  "offeringCode": "CSITES",
                  "offeringVersion": 2,
                  "name": "CLOUD SITES",
                  "description": "CLOUD SITES",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/361b9937-f217-3a8f-b6e8-27e294343c99/products",
                      "title": "CLOUD SITES"
                  },
                  "status": "ACTIVE",
                  "id": "361b9937-f217-3a8f-b6e8-27e294343c99"
              },
              {
                  "offeringCode": "CFILES",
                  "offeringVersion": 2,
                  "name": "CLOUD FILES",
                  "description": "CLOUD FILES",
                  "lineOfBusinesses": {
                      "lineOfBusiness": [
                          "UK_CLOUD",
                          "US_CLOUD"
                      ]
                  },
                  "link": {
                      "rel": "SELF",
                      "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/1099767e-99dc-3f62-a405-694ce681759c/products",
                      "title": "CLOUD FILES"
                  },
                  "status": "ACTIVE",
                  "id": "1099767e-99dc-3f62-a405-694ce681759c"
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

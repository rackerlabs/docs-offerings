.. _get-product:

List a product
~~~~~~~~~~~~~~

.. code::

    GET /v2/offerings/{offeringId}/products/{productId}

This operation retrieves a specific product.

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
   * - ``{offeringId}``
     - String *(Required)*
     - The ID for the offering. Example:
       ``fd2c2294-0498-3791-9df7-1d4ed883a939``.
   * - ``{productId}``
     - String *(Required)*
     - The ID for the product. Example:
       ``0a1239ca-19ae-39e7-a7a3-887dfcc8ea85``.

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
   * - product
     - Object
     - An info block that contains details about the product.
   * - product.\ *name*
     - String
     - The name of the product.
   * - product.\ *id*
     - String
     - The universally unique identifier (UUID) for the product.
   * - product.\ *description*
     - String
     - The description of the product.
   * - product.\ *productCode*
     - String
     - A business identifier for the product. This identifier remains
       consistent when a new version of the product is introduced. It is
       unique across all of the products within an offering.
   * - product.\ *productOfferingPrice*
     - Complex type
     - Provides pricing information specific to a product in an offering
       through a nested structure.
   * - product.\ productOfferingPrice.\ *description*
     - String
     - The description of the price.
   * - product.\ productOfferingPrice.\ *priceType*
     - String
     -
       - ``usage``: Utility pricing.
       - ``item``: One-time pricing.
       - ``subscription``: Recurring pricing.
   * - product.\ productOfferingPrice.\ *priceDetails*
     - Complex type
     - A collection that provides details about pricing for the product.
   * - product.\ productOfferingPrice.\ priceDetails.\ *priceCharacteristic*
     - Array
     - An array of JSON strings that contains a collection of characteristics
       that provide additional information about the price. Format is
       ``Characteristic key : Characteristic value``. This element is used to
       accommodate business-defined pricing drivers such as ``serviceLevel``
       (``INFRASTRUCTURE`` or ``MANAGED``), ``serviceType`` (``SYSOPS``,
       ``DEVOPS``, or ``LEGACY``), ``chargeType`` (``INFRASTRUCTURE`` or
       ``SUPPORT``), and other pricing qualifiers. These
       pricing qualifiers are present where applicable. For more information,
       see the "Service plan details" table on this page.
   * - product.\ productOfferingPrice.\ priceDetails.\ *prices*
     - Array
     - An info block that contains information about product prices.
   * - product.\ productOfferingPrice.\ priceDetails.\ prices.\ *unitOfMeasure*
     - String
     -
       - ``per hour``
       - ``per month``
       - ``per year``
       - ``per instance``
       - ``per request``
       - ``per compute cycle``
       - ``per transaction``
       - ``per GB``
       - ``per GB/month``
       - ``per instance/month``
       - ``per check/hour``
       - ``per CC``
       - ``per 100 MB``
       - ``per server/day``
       - ``per instance/hour``
       - ``per 100 MB/hour``
       - ``per 10000 MB``
   * - product.\ productOfferingPrice.\ priceDetails.\ prices.\ *price*
     - Complex type
     - An info block that contains information about a price.
   * - product.\ productOfferingPrice.\ priceDetails.\ prices.\ price.\ *amount*
     - String
     - The price of the product.
   * - product.\ productOfferingPrice.\ priceDetails.\ prices.\ price.\ *currency*
     - String
     - The monetary currency that is associated with the price.
   * - product.\ productOfferingPrice.\ priceDetails.\ prices.\ price.\ *geo*
     - String
     - The geographic region that is associated with the price.
   * - product.\ *productCharacteristic*
     - Array
     - An array of key-value pairs that contains info on the operating system
       and flavor that are associated with the product. This information is
       primarily used to configure information from external applications that
       drive product and pricing. Example: ``"name": "flavor_id", "value":"performance2-30"``.
   * - product.\ *status*
     - String
     -
       - ``ACTIVE``: Default
       - ``INACTIVE``: When an offering becomes ``INACTIVE``, all of the
         products that belong to that offering also become ``INACTIVE``.

**Service plan details**

The following table shows the service level and service type that is
associated with each Rackspace service plan.

.. list-table::
  :widths: 15 10 30
  :header-rows: 1

  * - Service plan
    - Service level
    - Service type
  * - Infrastructure
    - Infrastructure
    - Legacy
  * - Managed Cloud
    - Managed
    - Legacy
  * - Managed Infrastructure
    - Infrastructure
    - SysOps
  * - Managed Operations
    - Managed
    - SysOps
  * - DevOps
    - Managed
    - DevOps

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
      "product": {
          "name": "Windows - 30720 MB High Performance I/O 2 Server Instance",
          "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
          "description": "Windows - 30720 MB High Performance I/O 2 Server Instance",
          "productCode": "UPTIME_HIGH_IO_2_WIN_30720MB",
          "productOfferingPrice": {
              "description": "Windows - 30720 MB High Performance I/O 2 Server Instance Price",
              "priceType": "Usage",
              "priceDetails": [
                  {
                      "priceCharacteristic": [
                          {
                              "name": "serviceLevel",
                              "value": "MANAGED"
                          },
                          {
                              "name": "serviceType",
                              "value": "LEGACY"
                          },
                          {
                              "name": "chargeType",
                              "value": "INFRASTRUCTURE"
                          }
                      ],
                      "prices": [
                          {
                              "unitOfMeasure": "per Hour",
                              "price": [
                                  {
                                      "amount": "1.480",
                                      "currency": "GBP",
                                      "geo": "UK"
                                  },
                                  {
                                      "amount": "2.000",
                                      "currency": "USD",
                                      "geo": "USA"
                                  },
                                  {
                                      "amount": "2.000",
                                      "currency": "USD",
                                      "geo": "APAC"
                                  },
                                  {
                                      "amount": "2.000",
                                      "currency": "USD",
                                      "geo": "AUS"
                                  }
                              ]
                          }
                      ]
                  },
                  {
                      "priceCharacteristic": [
                          {
                              "name": "serviceLevel",
                              "value": "INFRASTRUCTURE"
                          },
                          {
                              "name": "serviceType",
                              "value": "LEGACY"
                          },
                          {
                              "name": "chargeType",
                              "value": "INFRASTRUCTURE"
                          }
                      ],
                      "prices": [
                          {
                              "unitOfMeasure": "per Hour",
                              "price": [
                                  {
                                      "amount": "1.180",
                                      "currency": "GBP",
                                      "geo": "UK"
                                  },
                                  {
                                      "amount": "1.600",
                                      "currency": "USD",
                                      "geo": "USA"
                                  },
                                  {
                                      "amount": "1.600",
                                      "currency": "USD",
                                      "geo": "APAC"
                                  },
                                  {
                                      "amount": "1.600",
                                      "currency": "USD",
                                      "geo": "AUS"
                                  }
                              ]
                          }
                      ]
                  }
              ]
          },
          "productCharacteristic": [
              {
                  "name": "os_type",
                  "value": "windows"
              },
              {
                  "name": "FLAVOR_ID",
                  "value": "performance2-30"
              }
          ],
          "status": "ACTIVE"
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

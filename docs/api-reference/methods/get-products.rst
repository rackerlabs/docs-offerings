.. _get-products:

List products
~~~~~~~~~~~~~

.. code::

    GET /v2/offerings/{offeringId}/products​

Gets the products for a Rackspace offering.

This operation retrieves all of the products that are associated with a
Rackspace offering.

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
       ``046b6c7f-0b8a-43b9-b35d-6489e6daee91``.
   * - ``{limit}``
     - String
     - The maximum number of items to return. The default value is ``100``.
       For this method, you may also set the value for this parameter to
       ``infinite``.
   * - ``{marker}``
     - String
     - The starting point for the return data. This parameter controls
       pagination.
   * - ``{serviceLevel}``
     - String
     -
       - ``INFRASTRUCTURE``
       - ``MANAGED``
   * - ``{serviceType}``
     - String
     -
       - ``SYSOPS``
       - ``LEGACY``
       - ``DEVOPS``
   * - ``{geo}``
     - String
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - ``{currency}``
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
   * - ``{unitOfMeasure}``
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
   * - products
     - Array
     - An array of products.
   * - products.\ *product*
     - Array
     - An info block that contains details about a specific product.
   * - products.\ product.\ *name*
     - String
     - The name of the product.
   * - products.\ product.\ *description*
     - String
     - The description of the product.
   * - products.\ product.\ *productOfferingPrice*
     - Complex type
     - Provides pricing information specific to a product in an offering
       through a nested structure.
   * - products.\ product.\ productOfferingPrice.\ *description*
     - String
     - A description of the product offering price.
   * - products.\ product.\ productOfferingPrice.\ *priceDetails*
     - Complex type
     - A collection that provides details specific to pricing for the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\
       *priceCharacteristic*
     - Array
     - An array of JSON strings that contains a collection of characteristics
       that provide additional information about the price. Format is
       ``Characteristic key : Characteristic value``. This element is used to
       accommodate business-defined pricing drivers such as ``serviceLevel``
       (``INFRASTRUCTURE`` or ``MANAGED``), ``serviceType`` (``SYSOPS``,
       ``DEVOPS``, or ``LEGACY``), ``chargeType`` (``INFRASTRUCTURE`` or
       ``SUPPORT``), and other pricing qualifiers. These
       pricing qualifiers are present where applicable. For more information, see the **Service plan details** table on this page.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ *prices*
     - Array
     - An info block that contains information about prices for the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       *unitOfMeasure*
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
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\
       prices.\ *price*
     - Complex type
     - An info block that contains information about a price for the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       price.\ *currency*
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       price.\ *amount*
     - String
     - The price of the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       price.\ *geo*
     - String
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - products.\ product.\ productOfferingPrice.\ *priceType*
     - String
     -
       - ``usage``: Utility pricing.
       - ``item``: One-time pricing.
       - ``subscription``: Recurring pricing.
   * - products.\ product.\ *productCharacteristic*
     - String
     - An array of key-value pairs that contains info on the operating system
       and flavor that are associated with the product. This information is
       primarily used to configure information from external applications that
       drive product and pricing.
       Example: ``"name": "flavor_id", "value":"performance2-30"``.
   * - products.\ product.\ *link*
     - Object
     - An info block that contains details about the link for the product.
   * - products.\ product.\ link.\ *rel*
     - String
     - The relationship between the current document and the linked document.
   * - products.\ product.\ link.\ *href*
     - String
     - The URL for the product.
   * - products.\ product.\ *id*
     - String
     - The universally unique identifier (UUID) for the product.
   * - products.\ product.\ *status*
     - String
     - The status of the product. The default is ``ACTIVE``. When an offering
       becomes ``INACTIVE``, all of the products that belong to that offering also become ``INACTIVE``.
   * - products.\ product.\ *productCode*
     - String
     - A business identifier for the product. This identifier remains
       consistent when a new version of the product is introduced. This identifier is unique across all of the products within an offering.
   * - products.\ product.\ *salesChannel*
     - String
     -
       - ``PUBLIC``: The product or plan is available to the public. In
         addition, if the value is blank, it is publicly available.
       - ``PRIVATE``: The product or plan is not available to the public.
   * - products.\ *link*
     - Object
     - An info block that contains details about the link for the results.
   * - products.\ *rel*
     - String
     - The relationship between the current document and the linked document.
   * - products.\ *href*
     - String
     - The URL for a set of results.

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

The following example shows the response for a request to retrieve the
Cloud Databases products for an offering. To view responses relating to other
types of products, see the
:ref:`Responses by product section <responses-by-product/index>`.

.. code::

   Status Code: 200 OK
   Content-Length: 4543
   Content-Type: application/json
   Date: Wed, 03 Dec 2014 17:13:30 GMT
   Server: Jetty(8.0.y.z-SNAPSHOT)
   Via: 1.1 Repose (Repose/2.12)
   x-compute-request-id: req-7b7ffed2-9b1f-46a8-a478-315518d35387


   {
    "products": {
        "product": [
            {
                "name": "Uptime - Hamysql - 98304 MB",
                "description": "Uptime - Hamysql - 98304 MB",
                "productOfferingPrice": {
                    "description": "Uptime - Hamysql - 98304 MB Price",
                    "priceDetails": [
                        {
                            "priceCharacteristic": [
                                {
                                    "name": "chargeType",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceLevel",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceType",
                                    "value": "LEGACY"
                                }
                            ],
                            "prices": [
                                {
                                    "unitOfMeasure": "per Hour",
                                    "price": [
                                        {
                                            "currency": "GBP",
                                            "amount": "4.4",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "5.75",
                                            "geo": "USA"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "priceCharacteristic": [
                                {
                                    "name": "chargeType",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceLevel",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceType",
                                    "value": "SYSOPS"
                                }
                            ],
                            "prices": [
                                {
                                    "unitOfMeasure": "per Hour",
                                    "price": [
                                        {
                                            "currency": "AUD",
                                            "amount": "8.964955",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": "6.078239",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": "4.4",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "7.171964",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "AUD",
                                            "amount": "7.1875",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": "4.873125",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": "3.527625",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "5.75",
                                            "geo": "USA"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "priceCharacteristic": [
                                {
                                    "name": "chargeType",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceLevel",
                                    "value": "MANAGED"
                                },
                                {
                                    "name": "serviceType",
                                    "value": "DEVOPS"
                                }
                            ],
                            "prices": [
                                {
                                    "unitOfMeasure": "per Hour",
                                    "price": [
                                        {
                                            "currency": "AUD",
                                            "amount": "8.964955",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": "6.078239",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": "4.4",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "7.171964",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "AUD",
                                            "amount": "7.1875",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": "4.873125",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": "3.527625",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "5.75",
                                            "geo": "USA"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "priceCharacteristic": [
                                {
                                    "name": "chargeType",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceLevel",
                                    "value": "MANAGED"
                                },
                                {
                                    "name": "serviceType",
                                    "value": "LEGACY"
                                }
                            ],
                            "prices": [
                                {
                                    "unitOfMeasure": "per Hour",
                                    "price": [
                                        {
                                            "currency": "GBP",
                                            "amount": "4.4",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "5.75",
                                            "geo": "USA"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "priceCharacteristic": [
                                {
                                    "name": "chargeType",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceLevel",
                                    "value": "MANAGED"
                                },
                                {
                                    "name": "serviceType",
                                    "value": "SYSOPS"
                                }
                            ],
                            "prices": [
                                {
                                    "unitOfMeasure": "per Hour",
                                    "price": [
                                        {
                                            "currency": "AUD",
                                            "amount": "8.964955",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": "6.078239",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": "4.4",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "7.171964",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "AUD",
                                            "amount": "7.1875",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": "4.873125",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": "3.527625",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": "5.75",
                                            "geo": "USA"
                                        }
                                    ]
                                }
                            ]
                        }
                    ],
                    "priceType": "Usage"
                },
                "productCharacteristic": [
                    {
                        "name": "db_type",
                        "value": "hamysql"
                    },
                    {
                        "name": "product_category",
                        "value": "UPTIME"
                    },
                    {
                        "name": "ram_in_mb",
                        "value": "98304 MB"
                    }
                ],
                "link": {
                    "rel": "SELF",
                    "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/fd2c2294-0498-3791-9df7-1d4ed883a939/products/0a1239ca-19ae-39e7-a7a3-887dfcc8ea85"
                },
                "id": "0a1239ca-19ae-39e7-a7a3-887dfcc8ea85",
                "status": "ACTIVE",
                "productCode": "UPTIME_hamysql_98304MB",
                "salesChannel": "PUBLIC"
            }
        ],
        "link": [
            {
                "rel": "NEXT",
                "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/fd2c2294-0498-3791-9df7-1d4ed883a939/products?marker=1&limit=1"
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

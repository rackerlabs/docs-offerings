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
   * - ``offeringId``
     - String
     - The ID for the offering. Example:
       ``046b6c7f-0b8a-43b9-b35d-6489e6daee91``.
   * - ``limit``
     - String
     - The maximum number of items to return. This parameter
       controls pagination. For example, a limit value of 50
       specifies that a maximum of 50 product offering items is returned.
   * - ``marker``
     - String
     - The starting point for the return data. This parameter controls
       pagination.
   * - ``serviceLevel``
     - String
     -
       - ``INFRASTRUCTURE``
       - ``MANAGED``
   * - ``serviceType``
     - String
     -
       - ``SYSOPS``
       - ``LEGACY``
       - ``DEVOPS``
   * - ``geo``
     - String
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - ``currency``
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
       - ``HKD``: Hong Kong Dollar
   * - ``unitOfMeasure``
     - String (enumerated)
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
   * - **products**\.[]
     - Array
     - An array of products.
   * - products.\ **product**
     - Array
     - An info block containing details about a product.
   * - products.\ product.\ **productOfferingPrice**
     - Complex type
     - Provides pricing information specific to a product in an offering
       through a nested structure.
   * - products.\ product.\ productOfferingPrice.\ **priceDetails**
     - Complex type
     - A collection that provides details specific to pricing for the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ **priceCharacteristic**
     - Array
     - An array of JSON strings containing a collection of characteristics
       that provide additional information about the price. Format is
       ``Characteristic key : Characteristic value``. This element is used to
       accommodate business-defined pricing drivers such as ``serviceLevel``,
       ``serviceType``, ``chargeType``, and other pricing qualifiers where
       applicable.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ **prices**
     - Array
     - An info block containing information about prices for the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       **price**
     - Complex type
     - An info block containing information about a price for the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       price.\ **amount**
     - String
     - The price the product.
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       price.\ **geo**
     - String
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\
       price.\ **currency**
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
       - ``HKD``: Hong Kong Dollar
   * - products.\ product.\ productOfferingPrice.\ priceDetails.\ prices.\ **unitOfMeasure**
     - String (enumerated)
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
   * - products.\ product.\ productOfferingPrice.\ **priceType**
     - String
     -
       - ``usage``: Utility pricing.
       - ``item``: One-time pricing.
       - ``subscription``: Recurring pricing.
   * - products.\ product.\ **id**
     - String
     - The universally unique identifier (UUID) for the product. Example:
       ``046b6c7f-0b8a-43b9-b35d-6489e6daee91``.
   * - products.\ product.\ **status**
     - String
     - The status of the product. The default is ``ACTIVE``. When an offering
       becomes ``INACTIVE``, all of the products that belong to that offering also become ``INACTIVE``.
   * - products.\ product.\ **productCode**
     - String (enumerated)
     - A business identifier for the product. This identifier remains
       consistent when a new version of the product is introduced. This identifier is unique across all of the products within an offering. Example: ``UPTIME_HIGH_IO_2_WIN_30720MB``.
   * - products.\ product.\ **productCharacteristic**
     - String
     - An array of key-value pairs that contains info on the operating system
       and flavor that are associated with the product. Format is
      ``Characteristic key : Characteristic value``. This information is
       primarily used to configure information from external applications that
       drive product and pricing. Example: ``"name": "flavor_id", "value":"performance2-30"``.
   * - products.\ product.\ **description**
     - String
     - A short, human-readable description of the product. Example: ``Windows -
       30720 MB High Performance I/O 2 Server Instance``.
   * - products.\ product.\ **name**
     - String
     - The name of the product. Example: ``Windows -
       30720 MB High Performance I/O 2 Server Instance``.
   * - products.\ **link**
     - Object
     - An info block that contains details about the link for the products
       that are associated with the offering.
   * - products.\ link.\ **href**
     - String
     - The URL for the products that are associated with the offering.
   * - commitGrids.\ commitGrid.\ link.\ **rel**
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
  "products": {
    "product": [
      {
        "productOfferingPrice": {
          "priceDetails": [
            {
              "priceCharacteristic": [
                {
                  "name": "serviceType",
                  "value": "INFRASTRUCTURE"
                },
                {
                  "name": "serviceLevel",
                  "value": "LEGACY"
                },
                {
                  "name": "chargeType",
                  "value": "INFRASTRUCTURE"
                }
              ],
              "prices": [
                {
                  "price": [
                    {
                      "amount": "1.6",
                      "geo": "USA",
                      "currency": "USD"
                    }
                  ],
                  "unitOfMeasure": "per Hour"
                }
              ]
            }
          ],
          "priceType": "Usage"
        },
        "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
        "status": "ACTIVE",
        "productCode": "UPTIME_HIGH_IO_2_WIN_30720MB",
        "productCharacteristic": [
          {
            "name": "os_type",
            "value": "windows"
          },
          {
            "name": "flavor_id",
            "value": "performance2-30"
          },
          {
            "name": "class",
            "value": "performance2"
          }
        ],
        "description": "Windows - 30720 MB High Performance I/O 2 Server Instance",
        "name": "Windows - 30720 MB High Performance I/O 2 Server Instance"
      }
    ],
    "link": [
      {
        "rel": "prev",
        "href": "http://offer.api.rackspacecloud.com/v2/offerings/046b6c7f/products?marker\u003d4\u0026amp;limit\u003d3"
      },
      {
        "rel": "next",
        "href": "http://offer.api.rackspacecloud.com/v2/offerings/046b6c7f/products?marker\u003d4\u0026amp;limit\u003d3"
      }
    ]
  }
}

**Example response: XML** MAYBE THIS SHOULD BE "REFERENCE" INSTEAD???

The following example shows the XML response for the request.

.. code::

  <?xml version="1.0" encoding="UTF-8"?>
  <ns3:products xmlns:atom="http://www.w3.org/2005/Atom" xmlns:ns3="http://offer.api.rackspacecloud.com/v2">
     <ns3:product id="046b6c7f-0b8a-43b9-b35d-6489e6daee91"
          productCode="UPTIME_HIGH_IO_2_WIN_30720MB" status="ACTIVE">
          <ns3:name>Windows - 30720 MB High Performance I/O 2 Server Instance</ns3:name>
          <ns3:description>Windows - 30720 MB High Performance I/O 2 Server Instance</ns3:description>
          <ns3:productOfferingPrice priceType="Usage">
               <ns3:priceDetails>
                    <ns3:priceCharacteristic name="serviceType" value="INFRASTRUCTURE"/>
                    <ns3:priceCharacteristic name="serviceLevel" value="LEGACY"/>
                    <ns3:priceCharacteristic name="chargeType" value="INFRASTRUCTURE"/>
                    <ns3:prices>
                         <ns3:unitOfMeasure>per Hour</ns3:unitOfMeasure>
                         <ns3:price amount="1.6" currency="USD" geo="USA"/>
                    </ns3:prices>
               </ns3:priceDetails>
          </ns3:productOfferingPrice>
          <ns3:productCharacteristic name="os_type" value="windows"/>
          <ns3:productCharacteristic name="flavor_id" value="performance2-30"/>
          <ns3:productCharacteristic name="class" value="performance2"/>
     </ns3:product>
     <atom:link
          href="http://offer.api.rackspacecloud.com/v2/offerings/046b6c7f/products?marker=4&amp;amp;limit=3" rel="prev"/>
     <atom:link
          href="http://offer.api.rackspacecloud.com/v2/offerings/046b6c7f/products?marker=4&amp;amp;limit=3" rel="next"/>
  </ns3:products>

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

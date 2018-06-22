.. _update-product:

Update a product
~~~~~~~~~~~~~~~~

.. code::

    PUT /offerings/{offeringId}/products/{productId}

Updates a product.

This operation updates a product.

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
   * - ``offeringId``
     - String
     - The ID for the offering.
    * - ``productId``
      - String
      - The ID for the product.

The request has the following body parameters.

.. list-table::
  :widths: 15 10 30
  :header-rows: 1

  * - Name
    - Type
    - Description
  * - product.\ *name*
    - String *(Required)*
    - The name of the product
  * - product.\ *id*
    - String
    - The ID for the product
  * - product.\ *description*
    - String
    - A description of the product
  * - product.\ *productCode*
    - String
    - The code for the product
  * - product.\ *productOfferingPrice*
    - Object
    - An info block that contains details about the offering price.
  * - product.\ *productCharacteristic*
    - Array
    - An array of key-value pairs that contains info on the operating system
      and flavor that are associated with the product.
  * - product.\ *status*
    - String
    - Whether the product is ``active`` or ``inactive``.

**Example Request: header**

The following example shows the header information.

.. code::

   X-Auth-Token: f064c46a782c444cb4ba4b6434288f7c
   Content-Type: application/json
   Accept: application/json

**Example Request: JSON**

.. code::

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

**Example Request: XML**

.. code::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <osl:product productCode="UPTIME_HIGH_IO_2_WIN_30720MB"
      status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91" xmlns:osl="http://offer.api.rackspacecloud.com/v2"
      xmlns:atom="http://www.w3.org/2005/Atom" xmlns:ns4="http://docs.openstack.org/common/api/v1.0"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <osl:name>Windows - 30720 MB High Performance I/O 2 Server Instance</osl:name>
      <osl:description>Windows - 30720 MB High Performance I/O 2 Server Instance</osl:description>
      <osl:productOfferingPrice priceType="Usage">
          <osl:priceDetails>
              <osl:priceCharacteristic name="serviceLevel"
                  value="MANAGED" />
              <osl:priceCharacteristic name="serviceType"
                  value="LEGACY" />
              <osl:priceCharacteristic name="chargeType"
                  value="INFRASTRUCTURE" />
              <osl:prices>
                  <osl:unitOfMeasure>per Hour</osl:unitOfMeasure>
                  <osl:price amount="1.480" currency="GBP" geo="UK" />
                  <osl:price amount="2.000" currency="USD" geo="USA" />
                  <osl:price amount="2.000" currency="USD" geo="APAC" />
                  <osl:price amount="2.000" currency="USD" geo="AUS" />
              </osl:prices>
          </osl:priceDetails>
          <osl:priceDetails>
              <osl:priceCharacteristic name="serviceLevel"
                  value="INFRASTRUCTURE" />
              <osl:priceCharacteristic name="serviceType"
                  value="LEGACY" />
              <osl:priceCharacteristic name="chargeType"
                  value="INFRASTRUCTURE" />
              <osl:prices>
                  <osl:unitOfMeasure>per Hour</osl:unitOfMeasure>
                  <osl:price amount="1.600" currency="GBP" geo="UK" />
                  <osl:price amount="1.600" currency="USD" geo="USA" />
                  <osl:price amount="1.600" currency="USD" geo="APAC" />
                  <osl:price amount="1.600" currency="USD" geo="AUS" />
              </osl:prices>
          </osl:priceDetails>
      </osl:productOfferingPrice>
      <osl:productCharacteristic name="os_type"
          value="windows" />
      <osl:productCharacteristic name="FLAVOR_ID"
          value="performance2-30" />
  </osl:product>

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

**Example response: XML**

The following example shows the XML response for the request.

.. code::

   <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
   <osl:product productCode="UPTIME_HIGH_IO_2_WIN_30720MB"
       status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91" xmlns:osl="http://offer.api.rackspacecloud.com/v2"
       xmlns:atom="http://www.w3.org/2005/Atom" xmlns:ns4="http://docs.openstack.org/common/api/v1.0"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
       <osl:name>Windows - 30720 MB High Performance I/O 2 Server Instance</osl:name>
       <osl:description>Windows - 30720 MB High Performance I/O 2 Server Instance</osl:description>
       <osl:productOfferingPrice priceType="Usage">
           <osl:priceDetails>
               <osl:priceCharacteristic name="serviceLevel"
                   value="MANAGED" />
               <osl:priceCharacteristic name="serviceType"
                   value="LEGACY" />
               <osl:priceCharacteristic name="chargeType"
                   value="INFRASTRUCTURE" />
               <osl:prices>
                   <osl:unitOfMeasure>per Hour</osl:unitOfMeasure>
                   <osl:price amount="1.480" currency="GBP" geo="UK" />
                   <osl:price amount="2.000" currency="USD" geo="USA" />
                   <osl:price amount="2.000" currency="USD" geo="APAC" />
                   <osl:price amount="2.000" currency="USD" geo="AUS" />
               </osl:prices>
           </osl:priceDetails>
           <osl:priceDetails>
               <osl:priceCharacteristic name="serviceLevel"
                   value="INFRASTRUCTURE" />
               <osl:priceCharacteristic name="serviceType"
                   value="LEGACY" />
               <osl:priceCharacteristic name="chargeType"
                   value="INFRASTRUCTURE" />
               <osl:prices>
                   <osl:unitOfMeasure>per Hour</osl:unitOfMeasure>
                   <osl:price amount="1.600" currency="GBP" geo="UK" />
                   <osl:price amount="1.600" currency="USD" geo="USA" />
                   <osl:price amount="1.600" currency="USD" geo="APAC" />
                   <osl:price amount="1.600" currency="USD" geo="AUS" />
               </osl:prices>
           </osl:priceDetails>
       </osl:productOfferingPrice>
       <osl:productCharacteristic name="os_type"
           value="windows" />
       <osl:productCharacteristic name="FLAVOR_ID"
           value="performance2-30" />
   </osl:product>

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
   * - 415
     - Unsupported Media Type
     - The payload type is not supported.
   * - 500
     - API Fault
     - The server encountered an unexpected condition that prevented it from
       fulfilling the request.

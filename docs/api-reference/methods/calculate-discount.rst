.. _calculate-discount:

Calculate a discount
~~~~~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/commitGrids/{commitGridId}/commitDiscountCalculation

Calculate a discount.

This operation calculates a discount by using a commit grid.

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
   * - ``commitGridId`` *(Required)*
     - String
     - The ID for the commit grid.

**Example Request: header**

The following example shows the header information.

.. code::

  X-Auth-Token: f064c46a782c444cb4ba4b6434288f7c
  Content-Type: application/json
  Accept: application/json

**Example request for a commit discount calculation request with prepay opted: JSON**

 .. code::

   {
     "commitDiscountCalculation": {
       "commitMonths": 6,
       "commitUsageAmountPerMonth": "8000",
       "isPrePayOpted": true
     }
   }

**Example request for a commit discount calculation request with prepay opted: XML**

 .. code::

   <?xml version="1.0" encoding="UTF-8"?>
     <ns3:commitDiscountCalculation xmlns:atom="http://www.w3.org/2005/Atom" xmlns:ns3="http://offer.api.rackspacecloud.com/v2">
       <ns3:commitUsageAmountPerMonth>8000</ns3:commitUsageAmountPerMonth>
       <ns3:isPrePayOpted>true</ns3:isPrePayOpted>
       <ns3:commitMonths>6</ns3:commitMonths>
     </ns3:commitDiscountCalculation>

**Example request for a commit discount calculation request with no prepay opted: JSON**

 .. code::

  {
    "commitDiscountCalculation": {
      "commitMonths": 6,
      "commitUsageAmountPerMonth": "8000",
      "isPrePayOpted": false
    }
  }

**Example request for a commit discount calculation request with no prepay opted: XML**

  .. code::

     <?xml version="1.0" encoding="UTF-8"?>
     <ns3:commitDiscountCalculation xmlns:atom="http://www.w3.org/2005/Atom" xmlns:ns3="http://offer.api.rackspacecloud.com/v2">
        <ns3:commitUsageAmountPerMonth>8000</ns3:commitUsageAmountPerMonth>
        <ns3:isPrePayOpted>false</ns3:isPrePayOpted>
        <ns3:commitMonths>6</ns3:commitMonths>
     </ns3:commitDiscountCalculation>

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

**Example response to a commit discount calculation request with prepay opted: JSON**

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
    "commitDiscountCalculation": {
      "commitMonths": 6,
      "commitPaymentAmount": "45000.00",
      "discountPercent": "12.00",
      "commitUsageAmountPerMonth": "80000.00",
      "isPrePayOpted": true
    }
  }

**Example response to a commit discount calculation request with prepay opted: XML**

The following example shows the XML response for the request.

.. code::

  <?xml version="1.0" encoding="UTF-8"?>
  <ns3:commitDiscountCalculation xmlns:atom="http://www.w3.org/2005/Atom" xmlns:ns3="http://offer.api.rackspacecloud.com/v2">
     <ns3:commitUsageAmountPerMonth>80000.00</ns3:commitUsageAmountPerMonth>
     <ns3:isPrePayOpted>true</ns3:isPrePayOpted>
     <ns3:commitMonths>6</ns3:commitMonths>
     <ns3:commitPaymentAmount>45000.00</ns3:commitPaymentAmount>
     <ns3:discountPercent>12.00</ns3:discountPercent>
  </ns3:commitDiscountCalculation>

**Example response to a commit discount calculation request with no prepay opted: JSON**

.. code::

   Status Code: 200 OK
   Content-Length: 4543
   Content-Type: application/json
   Date: Wed, 03 Dec 2014 17:13:30 GMT
   Server: Jetty(8.0.y.z-SNAPSHOT)
   Via: 1.1 Repose (Repose/2.12)
   x-compute-request-id: req-7b7ffed2-9b1f-46a8-a478-315518d35387

   {
      "commitDiscountCalculation": {
        "commitMonths": 6,
        "commitPaymentAmountPerMonth": "9000.00",
        "discountPercent": "12.00",
        "commitUsageAmountPerMonth": "8000.00",
        "isPrePayOpted": false
      }
    }

**Example response to a commit discount calculation request with no prepay opted: XML**

.. code::

   Status Code: 200 OK
   Content-Length: 4543
   Content-Type: application/json
   Date: Wed, 03 Dec 2014 17:13:30 GMT
   Server: Jetty(8.0.y.z-SNAPSHOT)
   Via: 1.1 Repose (Repose/2.12)
   x-compute-request-id: req-7b7ffed2-9b1f-46a8-a478-315518d35387

   <?xml version="1.0" encoding="UTF-8"?>
   <ns3:commitDiscountCalculation xmlns:atom="http://www.w3.org/2005/Atom" xmlns:ns3="http://offer.api.rackspacecloud.com/v2">
     <ns3:commitUsageAmountPerMonth>8000.00</ns3:commitUsageAmountPerMonth>
     <ns3:isPrePayOpted>false</ns3:isPrePayOpted>
     <ns3:commitMonths>6</ns3:commitMonths>
     <ns3:commitPaymentAmountPerMonth>9000.00</ns3:commitPaymentAmountPerMonth>
     <ns3:discountPercent>12.00</ns3:discountPercent>
   </ns3:commitDiscountCalculation>

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

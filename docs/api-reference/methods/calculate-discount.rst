.. _calculate-discount:

Calculate a discount
~~~~~~~~~~~~~~~~~~~~

.. code::

    POST /v2/discountGrids/commitGrids/{commitGridId}/commitDiscountCalculation

This operation calculates a discount by using a commit grid.

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
   * - ``{commitGridId}``
     - String *(Required)*
     - The ID for the commit grid. Example: ``STANDARD_AUS_COMMIT_GRID_001``.

The request has the following body parameters.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - commitDiscountCalculation
     - Object *(Required)*
     - An info block that contains information about the commit discount
       calculation.
   * - commitDiscountCalculation.\ *commitMonths*
     - Integer *(Required)*
     - The number of months of commitment that are required in order to
       receive the discount. Example: ``6``.
   * - commitDiscountCalculation.\ *commitUsageAmountPerMonth*
     - String *(Required)*
     - The amount of usage the customer may use during the commitment period.
       Example: ``8000``.
   * - commitDiscountCalculation.\ *isPrePayOpted*
     - Boolean *(Required)*
     - Whether prepayments are opted.

**Example request: header**

The following example shows the header information.

.. code::

  X-Auth-Token: f064c46a782c444cb4ba4b6434288f7c
  Content-Type: application/json
  Accept: application/json

**Example request for a commit discount calculation with prepay opted**

The following example shows what the request for a commit discount calculation with prepay opted looks like:

 .. code::

   {
     "commitDiscountCalculation": {
       "commitMonths": 6,
       "commitUsageAmountPerMonth": "8000",
       "isPrePayOpted": true
     }
   }

Response
--------

The response has the following body parameters.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Name
     - Type
     - Description
   * - commitDiscountCalculation
     - Object
     - An object that contains information about the commit discount
       calculation.
   * - commitDiscountCalculation.\ *commitMonths*
     - Integer
     - The number of months of commitment that are required in order to
       receive the discount.
   * - commitDiscountCalculation.\ *commitPaymentAmount*
     - String
     - The payment that is associated with the discount.
   * - commitDiscountCalculation.\ *discountPercent*
     - String
     - The percent of the discount.
   * - commitDiscountCalculation.\ *commitUsageAmountPerMonth*
     - String
     - The amount of usage the customer may use during the commitment period.
   * - commitDiscountCalculation.\ *isPrePayOpted*
     - Boolean
     - Whether prepayments are opted.

**Example response to a commit discount calculation request with prepay opted**

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
    "commitDiscountCalculation": {
      "commitMonths": 6,
      "commitPaymentAmount": "45000.00",
      "discountPercent": "12.00",
      "commitUsageAmountPerMonth": "80000.00",
      "isPrePayOpted": true
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
   * - 415
     - Unsupported Media Type
     - The payload type is not supported.
   * - 500
     - API Fault
     - The server encountered an unexpected condition that prevented it from
       fulfilling the request.

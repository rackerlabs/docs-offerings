.. _delete-volume-grid:

Delete a volume grid
~~~~~~~~~~~~~~~~~~~~

.. code::

    DELETE /v2/discountGrids/volumeGrids/{volumeGridId}

Deletes a volume grid.

This operation deletes a volume grid.

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
   * - ``volumeGridId``
     - String
     - The ID for the volume grid.

This operation does not accept a request body.

**Example Request: header**

The following example shows the header information.

.. code::

   X-Auth-Token: f064c46a782c444cb4ba4b6434288f7c
   Content-Type: application/json
   Accept: application/json

Response
--------

This operation does not return a response body.

Response codes
--------------

This operation can have the following response codes.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Code
     - Name
     - Description
   * - 204
     - No Content
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

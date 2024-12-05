.. _faults:

======
Faults
======

The fault objects in this section describe possible API operation errors. All
fault objects extend from the base fault, ``serviceFault``, for easier
exception handling  for languages that support it.

.. _faults-service:

serviceFault
~~~~~~~~~~~~

The ``serviceFault``, and by extension all other faults, includes ``message``
and ``details`` elements that contain strings that describe the nature of
the fault. It also contains a ``code`` attribute that represents the HTTP
response code. The ``code`` attribute of the fault is for the convenience of
the caller, who can retrieve the response code from the HTTP response headers
or directly from the fault object. Note that the ``serviceFault`` is not
returned directly; instead one of the faults based on it is returned.

.. _faults-badrequest:

badRequest
~~~~~~~~~~

The ``badRequest`` fault indicates that the data in the request object is
invalid. For example, a string was used in a parameter that accepts only an
integer. The fault wraps validation errors.

**Example: badRequest fault response**

.. code::

    {
      "badRequest": {
        "message": "Resource Not Found",
        "category": "example",
        "referenceCode": "afsgghasgahs12",
        "details": [
          {
            "faultCode": "REQUIRED",
            "resourceProperty": "resourceProperty0",
            "resourceName": "resourceName0"
          }
        ]
      }
    }

.. _faults-serviceunavailable:

serviceUnavailable
~~~~~~~~~~~~~~~~~~

The ``serviceUnavailable`` fault is returned when the service is unavailable,
such as when the service is undergoing maintenance.

**Example: serviceUnavailable fault response**

.. code::

    {
       "serviceUnavailable":
         {
            "code": 500,
            "message": "The Offer Service is currently not available."
         }
    }

.. _faults-unauthorized:

unauthorized
~~~~~~~~~~~~

The ``unauthorized`` fault is returned when you are not authorized to perform
an attempted operation.

**Example: unauthorized fault response**

.. code::

    {
      "Error" : {
          "code" : 401,
          "message" : "Unauthorized"
      }
    }

.. _faults-forbidden:

forbidden
~~~~~~~~~

The ``forbidden`` fault is returned when access to a resource or operation is
forbidden, regardless of authorization.

**Example: forbidden fault response**

.. code::

    {
      "Error" : {
          "code" : 403,
          "message" : "Access is forbidden."
      }
    }

.. _faults-itemnotfound:

itemNotFound
~~~~~~~~~~~~

The ``itemNotFound`` fault is returned when a requested resource is not found.

**Example: itemNotFound fault response**

.. code::

    {
      "notFound": {
      "message": "Product not found.",
      "referenceCode": "1d37a4e4-9e4d-45f5-b2ee-09957e92fb76"
      }
    }

.. _faults-methodnotallowed:

methodNotAllowed
~~~~~~~~~~~~~~~~

The ``methodNotAllowed`` fault is returned when the method is not allowed
for the resource that you are calling.

**Example: methodNotAllowed fault response**

.. code::

    {
      "methodNotAllowed": {
        "message": "The method you are attempting to use is not allowed for this resource.",
        "referenceCode": "1d37a4e4-9e4d-45f5-b2ee-09957e92fb76"
      }
    }

.. _faults-unsupportedmediatype:

unsupportedMediaType
~~~~~~~~~~~~~~~~~~~~

The ``unsupportedMediaType`` fault is returned when the payload type is not
supported.

**Example: unsupportedMediaType fault response**

.. code::

    {
      "unsupportedMediaType": {
        "message": "The payload type is not supported.",
        "referenceCode": "1d37a4e4-9e4d-45f5-b2ee-09957e92fb76"
      }
    }

.. _faults-notacceptable:

notAcceptable
~~~~~~~~~~~~~

The ``notAcceptable`` fault is returned when the value in the ``Accept``
header is not supported.

**Example: notAcceptable fault response**

.. code::

    {
      "notAcceptable": {
        "message": "The value in the ``Accept`` header is not supported.",
        "referenceCode": "1d37a4e4-9e4d-45f5-b2ee-09957e92fb76"
      }
    }

.. _faults:

======
Faults
======

API operations that return an error return one of the fault objects described
in this section. All fault objects extend from the base fault,
``serviceFault``, for easier exception handling  for languages that support it.

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

    <badRequest xmlns="https://offer.api.rackspacecloud.com/v2/" code="400">
        <message>Validation fault</message>
        <details>The object is not valid</details>
            <validationErrors>
                <message>Node IP is invalid. Please specify a valid IP.</message>
            </validationErrors>
    </badRequest>

.. _faults-serviceunavailable:

serviceUnavailable
~~~~~~~~~~~~~~~~~~

The ``serviceUnavailable`` fault is returned when the service is unavailable,
such as when the service is undergoing maintenance.

**Example: serviceUnavailable fault response**

.. code::

  <serviceUnavailable code="500" xmlns="https://offer.api.rackspacecloud.com/v2/">
      <message>The Offer Service is currently not available.</message>
  </serviceUnavailable>

.. _faults-unauthorized:

unauthorized
~~~~~~~~~~~~

The ``unauthorized`` fault is returned when you are not authorized to perform
an attempted operation.

**Example: unauthorized fault response**

.. code::

 <unauthorized code="404" xmlns="https://offer.api.rackspacecloud.com/v2/">
     <message>You are not authorized to execute this operation.</message>
 </unauthorized>

.. _faults-forbidden:

forbidden
~~~~~~~~~

The ``forbidden`` fault is returned when access to a resource or operation is
forbidden, regardless of authorization.

**Example: forbidden fault response**

.. code::

 <forbidden code="403" xmlns="https://offer.api.rackspacecloud.com/v2/">
    <message>Access is forbidden.</message>
 </forbidden>

.. _faults-itemnotfound:

itemNotFound
~~~~~~~~~~~~

The ``itemNotFound`` fault is returned when a requested resource is not found.

**Example: itemNotFound fault response**

.. code::

    <itemNotFound code="404" xmlns="https://offer.api.rackspacecloud.com/v2/">
        <message>Object not found.</message>
    </itemNotFound>

.. _faults-methodnotallowed:

methodNotAllowed
~~~~~~~~~~~~~~~~

The ``methodNotAllowed`` fault is returned when the operation is not allowed
for the resource that you are calling.

**Example: methodNotAllowed fault response**

.. code::

    <methodNotAllowed code="405" xmlns="https://offer.api.rackspacecloud.com/v2/">
        <message>The method you are attempting to use is not allowed for this resource.</message>
    </methodNotAllowed>

.. _faults-unsupportedmediatype:

unsupportedMediaType
~~~~~~~~~~~~~~~~~~~~

The ``unsupportedMediaType`` fault is returned when the payload type is not
supported.

**Example: unsupportedMediaType fault response**

.. code::

    <unsupportedMediaType code="415" xmlns="https://offer.api.rackspacecloud.com/v2/">
        <message>The payload type is not supported.</message>
    </unsupportedMediaType>

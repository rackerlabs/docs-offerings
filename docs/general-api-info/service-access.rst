.. _service-access:

========================
Service access endpoints
========================

The |api-service| can be accessed at https://offer.api.rackspace.com/.

Versions
~~~~~~~~

The Offer service API uses a URI versioning scheme. The first element of the
URI path contains the target version identifier: for example, in the URL
https://offer.api.rackspacecloud.com/v2/, the API version is 2.

All requests except for queries for the contract version must contain a target
version. Any feature or functionality change that would necessitate a break in
API compatibility will require a new version, which results in the URI version
being updated accordingly. When new API versions are released, older versions
will be marked as deprecated. Rackspace will work with developers and partners
to ensure that there is adequate time to migrate to the new version before
deprecated versions are discontinued.

**Note**: At this time, only version 2 of the Offer service API is publicly
available.

Example request with URI versioning
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   GET /v2/offerings HTTP/1.1
   Host: offer.api.rackspacecloud.com
   Accept: application/json
   X_AUTH_TOKEN: ab48a9efdfedb23ty3494

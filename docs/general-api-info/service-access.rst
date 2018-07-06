.. _service-access:

========================
Service access endpoints
========================

The |api-service| can be accessed at https://offer.api.rackspace.com/.

Versions
~~~~~~~~

The Offering API uses a URI versioning scheme. The first element of the URI
path contains the target version identifier: for example, in the URL
https://offer.api.rackspacecloud.com/v2/, the API version is 2.

All requests except for queries for the contract version must contain a target
version. Any feature or functionality change that would necessitate a break in
API compatibility will require a new version, which results in the URI version
being updated accordingly. When new API versions are released, older versions
will be marked as deprecated. Rackspace will work with developers and partners
to ensure that there is adequate time to migrate to the new version before
deprecated versions are discontinued.

Example request with URI versioning
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   GET /v2/offerings HTTP/1.1
   Host: offer.api.rackspacecloud.com
   Accept: application/xml
   X_AUTH_TOKEN: ab48a9efdfedb23ty3494

Your application can programmatically determine the available API contract
versions by performing a GET on the root URL (with the version and everything
to the right of it truncated) returned from the authentication system.

Example service profile request
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   GET HTTP/1.1
   Host: offer.api.rackspacecloud.com
   Accept: application/xml

This operation does not require a request body.

Normal Response Code(s): 200

Error Response Code(s): 400, 500, 503

Your application can programmatically determine the available API contract versions by performing a GET on the root URL (https://offer.api.rackspacecloud.com/).

Versions List Response: XML
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   <?xml version="2.0" encoding="UTF-8"?>

      <versions xmlns="http://docs.openstack.org/common/api/v1.0"
          xmlns:atom="http://www.w3.org/2005/Atom">
       <version id="v2" status="BETA"
                updated="2012-04-25T11:33:21-06:00">
           <atom:link rel="self"
                      href="https://offer.api.rackspacecloud.com/v2/"/>
       </version>
      </versions>

Versions List Response: JSON
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   {
       "versions": [
           {
               "id": "v2",
               "status": "BETA",
               "updated": "2009-10-09T11:30:00Z",
               "links": [
                   {
                       "rel": "self",
                       "href": "https://offer.api.rackspacecloud.com/v2/"
                   }
               ]
           }
        ]
   }

You can also obtain additional information about a contract version by
performing a GET on the base version's URL (for example,
https://offer.api.rackspace.com/v1).

Example version details request
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   GET HTTP/1.1
   Host: offer.api.rackspacecloud.com/v2
   Accept: application/xml

This operation does not require a request body.

Normal Response Code(s): 200

Error Response Code(s): 400, 500, 503

Example version details response: XML
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   <?xml version="1.0" encoding="UTF-8"?>
   <version xmlns="http://docs.openstack.org/common/api/v1.0" xmlns:atom="http://www.w3.org/2005/Atom" id="v2" status="BETA" updated="2012-04-25T11:33:21-06:00">
    <atom:link rel="describedby" type="application/pdf" href="http://docs-internal.rackspace.com/foundations/offeringdevguide/offeringdevguide.pdf"/>
    <atom:link rel="describedby" type="application/vnd.sun.wadl+xml" href="http://offer.api.rackspacecloud.com/v2/application.wadl"/>
   </version>

Example version details response: JSON
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code::

   {
       "version" : {
           "id" : "v2",
           "status" : "BETA",
           "updated" : "2012-04-25T11:33:21-06:00",
           "links": [
               {
                   "rel" : "describedby",
                   "type" : "application/pdf",
                   "href" : "http://docs-internal.rackspace.com/foundations/offeringdevguide/offeringdevguide.pdf"
               },
               {
                   "rel" : "describedby",
                   "type" : "application/vnd.sun.wadl+xml",
                   "href" : "https://offer.api.rackspacecloud.com/v2/application.wadl"
               }
            ]
         }
      }

The detailed version response contains pointers to both a human-readable and a
machine-processable description of the API service. The machine-processable
description is written in the Web Application Description Language (WADL).

.. note:: If there is a discrepancy between the two specifications, the WADL is authoritative as it contains the most accurate and up-to-date description of the API service.

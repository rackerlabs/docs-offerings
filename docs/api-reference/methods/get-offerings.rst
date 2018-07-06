.. _get-offerings:

List offerings
~~~~~~~~~~~~~~

.. code::

    GET /v2/offerings

Lists Rackspace offerings.

This operation retrieves all of the Rackspace offerings that are available in
the product catalog.

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
     - Value: ``application/json`` or ``application/xml``.
   * - ``Accept``
     - Header string
     - Value: ``application/json`` or ``application/xml``.
   * - ``{lineOfBusiness}``
     - String
     - The Rackspace line of business that is associated with the offering.
       For example, a ``lineOfBusiness`` value of ``US_CLOUD`` returns the products for ``US_CLOUD``.
   * - ``{status}``
     - String
     - Retrieves offerings with a given status. Valid values are ``ACTIVE``
       and ``INACTIVE``.
   * - ``{limit}``
     - String
     - The maximum number of items to return. This value should be ``100`` or
       less. The default value is ``100``.
   * - ``{marker}``
     - String
     - The starting point for the return data. This parameter controls
       pagination.

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
   * - offerings
     - Array
     - An array of offerings.
   * - offerings.\ *offering*
     - Array
     - An info block containing details about a specific offering.
   * - offerings.\ *offering*.\ *id*
     - String
     - The universally unique identifier (UUID) for the offering.
   * - offerings.\ *offering*.\ *offeringCode*
     - String
     - A business identifier for the offering. This identifier remains
       consistent when a new version of the offering is introduced. Only
       one version of an ``offeringCode`` may have an ``ACTIVE`` status.
   * - offerings.\ *offering*.\ *offeringVersion*
     - Integer
     - The business version of the offering.
   * - offerings.\ *offering*.\ *name*
     - String
     - The name of the offering.
   * - offerings.\ offering.\ *status*
     - String
     - The status of the offering. Valid values are ``ACTIVE`` (default) and
       ``INACTIVE``. An offering becomes  ``INACTIVE`` when Rackspace
       introduces a new version of the offering.
   * - offerings.\ offering.\ *description*
     - String
     - The description of the offering.
   * - offerings.\ offering.\ *lineOfBusinesses*
     - Complex type
     - An info block that contains details about the Rackspace lines of
       business that are associated with the offering.
   * - offerings.\ offering.\ lineOfBusinesses.\ *lineOfBusiness*
     - Object
     - Information on the Rackspace lines of business that are associated with
       the offering.
   * - offerings.\ offering.\ *link*
     - Object
     - An info block containing details about the link for the offering.
   * - offerings.\ offering.\ link\. *title*
     - String
     - The title of the link.
   * - offerings.\ offering.\ link\. *href*
     - String
     - The URL for the link.
   * - offerings.\ offering.\ link\. *rel*
     - String
     - The relationship between the current information and the linked
       information.
   * - offerings.\ *link*
     - Object
     - An info block containing details about the links for the results.
   * - offerings.\ link\. *href*
     - String
     - The URL for a set of results.
   * - offerings.\ link\. *rel*
     - String
     - The relationship between the current information and the linked
       information.

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
    "offerings": {
        "offering": [
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee91",
                "offeringCode": "NXTGEN",
                "offeringVersion": 1,
                "name": "NEXT GENERATION CLOUD SERVERS",
                "status": "ACTIVE",
                "description": "NEXT GENERATION CLOUD SERVERS",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "NEXT GENERATION CLOUD SERVERS",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee92",
                "offeringCode": "DBAAS",
                "offeringVersion": 1,
                "status": "ACTIVE",
                "name": "CLOUD DATABASES",
                "description": "CLOUD DATABASES",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "CLOUD DATABASES",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee92/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee93",
                "offeringCode": "MAAS",
                "offeringVersion": 1,
                "status": "ACTIVE",
                "name": "CLOUD MONITORING",
                "description": "CLOUD MONITORING",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "CLOUD MONITORING",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee93/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee94",
                "offeringCode": "CBS",
                "offeringVersion": 1,
                "status": "ACTIVE",
                "name": "CLOUD BLOCK STORAGE",
                "description": "CLOUD BLOCK STORAGE",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "CLOUD BLOCK STORAGE",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee94/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee95",
                "offeringCode": "CBCKUP",
                "offeringVersion": 1,
                "status": "ACTIVE",
                "name": "CLOUD BACKUP",
                "description": "CLOUD BACKUP",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "CLOUD BACKUP",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee95/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee96",
                "offeringCode": "FSTGEN",
                "offeringVersion": 1,
                "status": "ACTIVE",
                "name": "FIRST GENERATION CLOUD SERVERS",
                "description": "FIRST GENERATION CLOUD SERVERS",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "FIRST GENERATION CLOUD SERVERS",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee96/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "status": "ACTIVE",
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee97",
                "offeringCode": "LBAAS",
                "offeringVersion": 1,
                "name": "CLOUD LOAD BALANCER",
                "description": "CLOUD LOAD BALANCER",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "CLOUD LOAD BALANCER",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee97/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "status": "ACTIVE",
                "id": "986b6c7f-0b8a-43b9-b35d-6489e6daee97",
                "offeringCode": "LBAAS2.0",
                "offeringVersion": 1,
                "name": "CLOUD LOAD BALANCER 2.0",
                "description": "CLOUD LOAD BALANCER 2.0",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "CLOUD LOAD BALANCER 2.0",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee97/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "status": "ACTIVE",
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee98",
                "offeringCode": "CFILES",
                "offeringVersion": 1,
                "name": "CLOUD FILES",
                "description": "CLOUD FILES",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                },
                "link": [
                    {
                        "title": "CLOUD FILES",
                        "href": "https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee98/products",
                        "rel": "PRODUCTS"
                    }
                ]
            },
            {
                "name": "CLOUD SITES",
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee99",
                "offeringCode": "CSITES",
                "offeringVersion": 1,
                "description": "CLOUD SITES",
                "link": [
                    {
                        "title": "CLOUD SITES",
                        "rel": "PRODUCTS",
                        "href": "https://dev.offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee99/products"
                    }
                ],
                "status": "ACTIVE",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD"
                    ]
                }
            },
            {
                "name": "BIG DATA (HADOOP AS A SERVICE)",
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6dae100",
                "offeringCode": "BIGDATA",
                "offeringVersion": 1,
                "description": "BIG DATA (HADOOP AS A SERVICE)",
                "link": [
                    {
                        "title": "BIG DATA (HADOOP AS A SERVICE)",
                        "rel": "PRODUCTS",
                        "href": "https://dev.offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6dae100/products"
                    }
                ],
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                }
            },
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee93",
                "offeringCode": "NEWTON",
                "offeringVersion": 1,
                "name": "Newton",
                "description": "Newton",
                "status": "ACTIVE",
                "link": [
                    {
                        "title": "Newton",
                        "rel": "PRODUCTS",
                        "href": "https://dev.offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee93/products"
                    }
                ]
            },
            {
                "id": "046b6c7f-0b8a-43b9-b35d-6489e6daee93",
                "offeringCode": "CLOUDQUEUES",
                "offeringVersion": 1,
                "name": "CLOUD QUEUES",
                "description": "CLOUD QUEUES",
                "link": [
                    {
                        "title": "CLOUD QUEUES",
                        "rel": "PRODUCTS",
                        "href": "https://dev.offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee93/products"
                    }
                ],
                "status": "ACTIVE",
                "lineOfBusinesses": {
                    "lineOfBusiness": [
                        "US_CLOUD",
                        "UK_CLOUD"
                    ]
                }
            }
        ],
        "link": [
            {
                "href": "https://offer.api.rackspacecloud.com/v1/offerings?marker=0&limit=100",
                "rel": "self"
            },
            {
                "href": "https://offer.api.rackspacecloud.com/v1/offerings?marker=0&limit=100",
                "rel": "last"
            },
            {
                "href": "https://offer.api.rackspacecloud.com/v1/offerings?marker=0&limit=100",
                "rel": "first"
            }
        ]
    }
   }

**Example response: XML**

The following example shows the XML response for the request.

.. code::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <ns2:offerings xmlns:ns2="http://offer.api.rackspacecloud.com/v2"
     xmlns:ns3="http://www.w3.org/2005/Atom">
     <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>NXTGEN</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>NEXT GENERATION CLOUD SERVERS</ns2:name>
      <ns2:description>NEXT GENERATION CLOUD SERVERS</ns2:description>
      <ns2:lineOfBusinesses>
         <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
         <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="NEXT GENERATION CLOUD SERVERS" href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>DBAAS</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD DATABASES</ns2:name>
      <ns2:description>CLOUD DATABASES</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD DATABASES" href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>MAAS</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD MONITORING</ns2:name>
      <ns2:description>CLOUD MONITORING</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD MONITORING" href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>CBS</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD BLOCK STORAGE</ns2:name>
      <ns2:description>CLOUD BLOCK STORAGE</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD BLOCK STORAGE"
         href="https://offer.api.rackspacecloud.com/v1/offerings/16" rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>CBCKUP</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD BACKUP</ns2:name>
      <ns2:description>CLOUD BACKUP</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD BACKUP" href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>FSTGEN</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>FIRST GENERATION CLOUD SERVERS</ns2:name>
      <ns2:description>FIRST GENERATION CLOUD SERVERS</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="FIRST GENERATION CLOUD SERVERS"
         href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products" rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>LBAAS</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD LOAD BALANCER</ns2:name>
      <ns2:description>CLOUD LOAD BALANCER</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD LOAD BALANCER"
         href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products" rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="986b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>LBAAS2.0</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD LOAD BALANCER 2.0</ns2:name>
      <ns2:description>CLOUD LOAD BALANCER 2.0</ns2:description>
      <ns2:lineOfBusinesses>
          <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
          <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD LOAD BALANCER 2.0"
         href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products" rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>CFILES</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD FILES</ns2:name>
      <ns2:description>CLOUD FILES</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD FILES" href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>CSITES</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD SITES</ns2:name>
      <ns2:description>CLOUD SITES</ns2:description>
      <ns2:lineOfBusinesses>
         <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
         <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD SITES" href="https://test.offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>CLOUDBIGDATA</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>BIG DATA (HADOOP AS A SERVICE)</ns2:name>
      <ns2:description>BIG DATA (HADOOP AS A SERVICE)</ns2:description>
      <ns2:lineOfBusinesses>
         <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
         <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="BIG DATA (HADOOP AS A SERVICE)" href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="046b6c7f-0b8a-43b9-b35d-6489e6daee91">
      <ns2:offeringCode>NEWTON</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>Newton</ns2:name>
      <ns2:description>Newton</ns2:description>
      <ns2:lineOfBusinesses>
         <ns2:lineOfBusiness>DEDICATED</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="Newton" href="https://offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns2:offering status="ACTIVE" id="28">
      <ns2:offeringCode>CLOUDQUEUES</ns2:offeringCode>
      <ns2:offeringVersion>1</ns2:offeringVersion>
      <ns2:name>CLOUD QUEUES</ns2:name>
      <ns2:description>CLOUD QUEUES</ns2:description>
      <ns2:lineOfBusinesses>
       <ns2:lineOfBusiness>US_CLOUD</ns2:lineOfBusiness>
       <ns2:lineOfBusiness>UK_CLOUD</ns2:lineOfBusiness>
      </ns2:lineOfBusinesses>
      <ns3:link title="CLOUD QUEUES" href="https://dev.offer.api.rackspacecloud.com/v1/offerings/046b6c7f-0b8a-43b9-b35d-6489e6daee91/products"
         rel="self"/>
   </ns2:offering>
   <ns3:link href="https://offer.api.rackspacecloud.com/v1/offerings?marker=0&amp;limit=100"
      rel="self"/>
   <ns3:link href="https://offer.api.rackspacecloud.com/v1/offerings?marker=0&amp;limit=100"
      rel="self"/>
   <ns3:link href="https://offer.api.rackspacecloud.com/v1/offerings?marker=0&amp;limit=100"
      rel="last"/>
   <ns3:link href="https://offer.api.rackspacecloud.com/v1/offerings?marker=0&amp;limit=100"
      rel="first"/>
  </ns2:offerings>

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

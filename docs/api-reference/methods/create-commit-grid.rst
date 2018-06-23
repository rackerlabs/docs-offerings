.. _create-commit-grid:

Create commit grid
~~~~~~~~~~~~~~~~~~

.. code::

    POST /v2/discountGrids/commitGrids

Creates a commit grid.

This operation creates a commit grid.

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

    The request has the following body parameters.

    .. list-table::
      :widths: 15 10 30
      :header-rows: 1

   * - ``commitGrid`` *(Required)*
     - Object
     - An info block containing information about the commit grid.
   * - commitGrid.\ *description*
     - String
     - A description of the commit grid.
   * - commitGrid.\ *offerings*
     - Object
     - An object containing one or more ``offeringCode``.
   * - ``monthlyCommitTiers``
     - Object
     - An object containing information on any monthly commit tiers.
   * - ``prepayCommitTiers``
     - Object
     - An object containing information on any prepay commit tiers.
   * - ``id``
     - String
     - The ID for the commit grid.
   * - ``geo``
     - String
     - This parameter is used to filter and retrieve products with only prices
       for specific geography where the Offering is available. Valid values
       are ``USA``, ``UK``, ``AUS`, and ``APAC``.
   * - ``currency``
     - String
     - This parameter is used to filter and retrieve products with only prices
       for specific currency. Valid values are ``USD`` and ``GBP``.
   * - ``gridType``
     - String
     - Valid values are ``STANDARD`` and ``PRESET``. By default only
       ``STANDARD`` grids are returned.
   * - ``gridVersion``
     - String
     - The version of the grid. Example: 1.
   * - ``gridStartDate``
     - String
     - The date and time that the grid begins.
   * - ``gridEndDate``
     - String
     - The date and time that the grid ends.

**Example Request: header**

The following example shows the header information.

.. code::

   X-Auth-Token: f064c46a782c444cb4ba4b6434288f7c
   Content-Type: application/json
   Accept: application/json

**Example Request: JSON**

.. code::

  {
      "commitGrid": {
          "description": "Standard USA Commit Grid for Commit Discounts",
          "offerings": {
              "offering": [
                  {
                      "offeringCode": "NXTGEN"
                  },
                  {
                      "offeringCode": "MNXTGEN"
                  },
                  {
                      "offeringCode": "FSTGEN"
                  },
                  {
                      "offeringCode": "MFSTGEN"
                  },
                  {
                      "offeringCode": "CLOUDBIGDATA"
                  }
              ]
          },
          "monthlyCommitTiers": {
              "commitTier": [
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "5",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "10",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "15",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "20",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "25",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "0",
                      "maxAmount": "5000",
                      "tierIndex": 1
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "10",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "15",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "20",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "25",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "30",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "5001",
                      "maxAmount": "10000",
                      "tierIndex": 2
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "15",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "20",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "25",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "30",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "35",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "10001",
                      "maxAmount": "25000",
                      "tierIndex": 3
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "20",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "25",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "30",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "35",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "40",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "25001",
                      "maxAmount": "50000",
                      "tierIndex": 4
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "25",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "30",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "35",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "40",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "45",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "50001",
                      "maxAmount": "100000",
                      "tierIndex": 5
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "30",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "35",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "40",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "45",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "50",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "100001",
                      "maxAmount": "200000",
                      "tierIndex": 6
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "35",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "40",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "45",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "50",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "55",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "200001",
                      "tierIndex": 7
                  }
              ]
          },
          "prepayCommitTiers": {
              "commitTier": [
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "8",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "16",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "24",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "32",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "43",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "0",
                      "maxAmount": "5000",
                      "tierIndex": 1
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "13",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "21",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "29",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "37",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "48",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "5001",
                      "maxAmount": "10000",
                      "tierIndex": 2
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "18",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "26",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "34",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "42",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "53",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "10001",
                      "maxAmount": "25000",
                      "tierIndex": 3
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "23",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "31",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "39",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "47",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "58",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "25001",
                      "maxAmount": "50000",
                      "tierIndex": 4
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "28",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "36",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "44",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "52",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "63",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "50001",
                      "maxAmount": "100000",
                      "tierIndex": 5
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "33",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "41",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "49",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "57",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "68",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "100001",
                      "maxAmount": "200000",
                      "tierIndex": 6
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "38",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "46",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "54",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "62",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "73",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "200001",
                      "tierIndex": 7
                  }
              ]
          },
          "id": "STANDARD_USA_COMMIT_GRID_001",
          "geo": "USA",
          "currency": "USD",
          "gridType": "STANDARD",
          "gridVersion": "1",
          "gridStartDate": "05-30-2013-0500",
          "gridEndDate": null
      }
  }

**Example Request: XML**

.. code::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <ns2:commitGrid id="USACOMPUTECOMMITSTANDARDGRID_001" geo="USA" currency="USD"
      gridType="STANDARD" gridVersion="1" gridStartDate="2002-09-24-06:00" gridEndDate="2002-09-24-06:00" xmlns:ns2="http://offer.api.rackspacecloud.com/v2">
      <ns2:description>Standard US Grid for Compute Commit Discounts</ns2:description>
      <ns2:offerings>
          <ns2:offering offeringCode="NXTGEN" />
          <ns2:offering offeringCode="MNXTGEN"/>
          <ns2:offering offeringCode="FSTGEN"/>
          <ns2:offering offeringCode="MFSTGEN"/>
          <ns2:offering offeringCode="CLOUDBIGDATA"/>
      </ns2:offerings>
      <ns2:monthlyCommitTiers>
          <ns2:commitTier minAmount="0" maxAmount="5000" tierIndex="1">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="3" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="6" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="10" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="20" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="5001" maxAmount="10000" tierIndex="2">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="8" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="12" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="16" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="28" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="10001" maxAmount="25000" tierIndex="3">
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="3" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="16" discountPercentage="6" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="20" discountPercentage="10" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="32" discountPercentage="20" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="25001" maxAmount="50000" tierIndex="4">
              <ns2:commitTierItem tenureInMonths="16" discountPercentage="3" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="20" discountPercentage="6" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="24" discountPercentage="10" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="20" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="50001" maxAmount="100000" tierIndex="5">
              <ns2:commitTierItem tenureInMonths="20" discountPercentage="3" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="24" discountPercentage="6" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="28" discountPercentage="10" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="40" discountPercentage="20" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="100001" maxAmount="200000" tierIndex="6">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="3" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="6" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="10" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="20" itemIndex="4"/>
          </ns2:commitTier>
      </ns2:monthlyCommitTiers>
      <ns2:prepayCommitTiers>
          <ns2:commitTier minAmount="0" maxAmount="5000" tierIndex="1">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="8" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="16" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="25" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="50" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="5001" maxAmount="10000" tierIndex="2">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="13" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="22" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="31" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="58" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="10001" maxAmount="25000" tierIndex="3">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="17" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="26" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="35" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="62" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="25001" maxAmount="50000" tierIndex="4">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="21" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="30" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="39" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="66" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="50001" maxAmount="100000" tierIndex="5">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="25" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="34" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="43" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="70" itemIndex="4"/>
          </ns2:commitTier>
          <ns2:commitTier minAmount="100001" maxAmount="200000" tierIndex="6">
              <ns2:commitTierItem tenureInMonths="6" discountPercentage="30" itemIndex="1"/>
              <ns2:commitTierItem tenureInMonths="12" discountPercentage="40" itemIndex="2"/>
              <ns2:commitTierItem tenureInMonths="18" discountPercentage="50" itemIndex="3"/>
              <ns2:commitTierItem tenureInMonths="36" discountPercentage="80" itemIndex="4"/>
          </ns2:commitTier>
      </ns2:prepayCommitTiers>
  </ns2:commitGrid>



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
      "commitGrid": {
          "description": "Standard USA Commit Grid for Commit Discounts",
          "offerings": {
              "offering": [
                  {
                      "offeringCode": "NXTGEN"
                  },
                  {
                      "offeringCode": "MNXTGEN"
                  },
                  {
                      "offeringCode": "FSTGEN"
                  },
                  {
                      "offeringCode": "MFSTGEN"
                  },
                  {
                      "offeringCode": "CLOUDBIGDATA"
                  }
              ]
          },
          "monthlyCommitTiers": {
              "commitTier": [
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "5",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "10",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "15",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "20",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "25",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "0",
                      "maxAmount": "5000",
                      "tierIndex": 1
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "10",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "15",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "20",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "25",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "30",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "5001",
                      "maxAmount": "10000",
                      "tierIndex": 2
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "15",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "20",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "25",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "30",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "35",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "10001",
                      "maxAmount": "25000",
                      "tierIndex": 3
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "20",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "25",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "30",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "35",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "40",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "25001",
                      "maxAmount": "50000",
                      "tierIndex": 4
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "25",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "30",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "35",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "40",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "45",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "50001",
                      "maxAmount": "100000",
                      "tierIndex": 5
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "30",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "35",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "40",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "45",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "50",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "100001",
                      "maxAmount": "200000",
                      "tierIndex": 6
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "35",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "40",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "45",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "50",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "55",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "200001",
                      "tierIndex": 7
                  }
              ]
          },
          "prepayCommitTiers": {
              "commitTier": [
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "8",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "16",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "24",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "32",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "43",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "0",
                      "maxAmount": "5000",
                      "tierIndex": 1
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "13",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "21",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "29",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "37",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "48",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "5001",
                      "maxAmount": "10000",
                      "tierIndex": 2
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "18",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "26",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "34",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "42",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "53",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "10001",
                      "maxAmount": "25000",
                      "tierIndex": 3
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "23",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "31",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "39",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "47",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "58",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "25001",
                      "maxAmount": "50000",
                      "tierIndex": 4
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "28",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "36",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "44",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "52",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "63",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "50001",
                      "maxAmount": "100000",
                      "tierIndex": 5
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "33",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "41",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "49",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "57",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "68",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "100001",
                      "maxAmount": "200000",
                      "tierIndex": 6
                  },
                  {
                      "commitTierItem": [
                          {
                              "tenureInMonths": 6,
                              "discountPercentage": "38",
                              "itemIndex": 1
                          },
                          {
                              "tenureInMonths": 12,
                              "discountPercentage": "46",
                              "itemIndex": 2
                          },
                          {
                              "tenureInMonths": 18,
                              "discountPercentage": "54",
                              "itemIndex": 3
                          },
                          {
                              "tenureInMonths": 24,
                              "discountPercentage": "62",
                              "itemIndex": 4
                          },
                          {
                              "tenureInMonths": 36,
                              "discountPercentage": "73",
                              "itemIndex": 5
                          }
                      ],
                      "minAmount": "200001",
                      "tierIndex": 7
                  }
              ]
          },
          "id": "STANDARD_USA_COMMIT_GRID_001",
          "geo": "USA",
          "currency": "USD",
          "gridType": "STANDARD",
          "gridVersion": "1",
          "gridStartDate": "05-30-2013-0500",
          "gridEndDate": null
      }
  }

**Example response: XML**

The following example shows the XML response for the request.

.. code::

  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <ns2:commitGrid id="USACOMPUTECOMMITSTANDARDGRID_001" geo="USA" currency="USD"
    gridType="STANDARD" gridVersion="1" gridStartDate="2002-09-24-06:00" gridEndDate="2002-09-24-06:00" xmlns:ns2="http://offer.api.rackspacecloud.com/v2">
    <ns2:description>Standard US Grid for Compute Commit Discounts</ns2:description>
    <ns2:offerings>
        <ns2:offering offeringCode="NXTGEN" />
        <ns2:offering offeringCode="MNXTGEN"/>
        <ns2:offering offeringCode="FSTGEN"/>
        <ns2:offering offeringCode="MFSTGEN"/>
        <ns2:offering offeringCode="CLOUDBIGDATA"/>
    </ns2:offerings>
    <ns2:monthlyCommitTiers>
        <ns2:commitTier minAmount="0" maxAmount="5000" tierIndex="1">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="3" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="6" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="10" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="20" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="5001" maxAmount="10000" tierIndex="2">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="8" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="12" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="16" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="28" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="10001" maxAmount="25000" tierIndex="3">
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="3" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="16" discountPercentage="6" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="20" discountPercentage="10" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="32" discountPercentage="20" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="25001" maxAmount="50000" tierIndex="4">
            <ns2:commitTierItem tenureInMonths="16" discountPercentage="3" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="20" discountPercentage="6" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="24" discountPercentage="10" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="20" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="50001" maxAmount="100000" tierIndex="5">
            <ns2:commitTierItem tenureInMonths="20" discountPercentage="3" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="24" discountPercentage="6" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="28" discountPercentage="10" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="40" discountPercentage="20" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="100001" maxAmount="200000" tierIndex="6">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="3" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="6" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="10" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="20" itemIndex="4"/>
        </ns2:commitTier>
    </ns2:monthlyCommitTiers>
    <ns2:prepayCommitTiers>
        <ns2:commitTier minAmount="0" maxAmount="5000" tierIndex="1">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="8" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="16" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="25" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="50" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="5001" maxAmount="10000" tierIndex="2">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="13" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="22" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="31" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="58" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="10001" maxAmount="25000" tierIndex="3">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="17" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="26" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="35" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="62" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="25001" maxAmount="50000" tierIndex="4">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="21" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="30" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="39" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="66" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="50001" maxAmount="100000" tierIndex="5">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="25" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="34" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="43" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="70" itemIndex="4"/>
        </ns2:commitTier>
        <ns2:commitTier minAmount="100001" maxAmount="200000" tierIndex="6">
            <ns2:commitTierItem tenureInMonths="6" discountPercentage="30" itemIndex="1"/>
            <ns2:commitTierItem tenureInMonths="12" discountPercentage="40" itemIndex="2"/>
            <ns2:commitTierItem tenureInMonths="18" discountPercentage="50" itemIndex="3"/>
            <ns2:commitTierItem tenureInMonths="36" discountPercentage="80" itemIndex="4"/>
        </ns2:commitTier>
    </ns2:prepayCommitTiers>
  </ns2:commitGrid>

Response codes
--------------

This operation can have the following response codes.

.. list-table::
   :widths: 15 10 30
   :header-rows: 1

   * - Code
     - Name
     - Description
   * - 201
     - Created
     - The resource was created.
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

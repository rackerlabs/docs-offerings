.. _get-commit-grid:

List commit grid
~~~~~~~~~~~~~~~~

.. code::

    GET /v2/discountGrids/commitGrids/{commitGridId}

Gets information on a specific commit grid.

This operation retrieves a commit grid.

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

This operation does not accept a request body.

**Example request: header**

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
   * - commitGrid
     - Object
     - An object that contains information about the commit grid.
   * - commitGrid.\ *description*
     - String
     - A description of the commit grid.
   * - commitGrid.\ *offerings*
     - Object
     - An object that contains one or more offerings.
   * - commitGrid.\ offerings.\ *offering*
     - Array
     - An array that contains one or more offering codes.
   * - commitGrid.\ offerings.\ offering.\ *offeringCode*
     - String
     - The code for the offering.
   * - commitGrid.\ *monthlyCommitTiers*
     - Object
     - An info block that contains details about any monthly commit tiers.
   * - commitGrid.\ monthlyCommitTiers.\ *commitTier*
     - Object
     - An info block that contains details about the commit tier.
   * - commitGrid.\ monthlyCommitTiers.\ commitTier.\ *commitTierItem*
     - Array
     - An info block that contains options for the commit tier.
   * - commitGrid.\ monthlyCommitTiers.\ commitTier.\ commitTierItem.\
       *tenureInMonths*
     - Integer
     - The number of months to which the customer must commit.
   * - commitGrid.\ monthlyCommitTiers.\ commitTier.\ commitTierItem.\
       *discountPercentage*
     - String
     - The discount percentage that is associated with the option.
   * - commitGrid.\ monthlyCommitTiers.\ commitTier.\ commitTierItem.\
       *itemIndex*
     - Integer
     - The index that is associated with the option.
   * - commitGrid.\ monthlyCommitTiers.\ commitTier.\ *minAmount*
     - String
     - The minimum amount of the discount.
   * - commitGrid.\ monthlyCommitTiers.\ commitTier.\ *maxAmount*
     - String
     - The maximum amount of the discount.
   * - commitGrid.\ monthlyCommitTiers.\ commitTier.\ *tierIndex*
     - Integer
     - The index that is associated with the tier.
   * - commitGrid.\ *prepayCommitTiers*
     - Object
     - An info block that contains details about any prepay commit tiers.
   * - commitGrid.\ prepayCommitTiers.\ *commitTier*
     - Object
     - An info block that contains details about the commit tier.
   * - commitGrid.\ prepayCommitTiers.\ commitTier.\ *commitTierItem*
     - Array
     - An info block that contains options for the commit tier.
   * - commitGrid.\ prepayCommitTiers.\ commitTier.\ commitTierItem.\
       *tenureInMonths*
     - Integer
     - The number of months to which the customer must commit.
   * - commitGrid.\ prepayCommitTiers.\ commitTier.\ commitTierItem.\
       *discountPercentage*
     - String
     - The discount percentage that is associated with the option.
   * - commitGrid.\ prepayCommitTiers.\ commitTier.\ commitTierItem.\
       *itemIndex*
     - Integer
     - The index that is associated with the option.
   * - commitGrid.\ prepayCommitTiers.\ commitTier.\ *minAmount*
     - String
     - The minimum amount of the discount.
   * - commitGrid.\ prepayCommitTiers.\ commitTier.\ *maxAmount*
     - String
     - The maximum amount of the discount.
   * - commitGrid.\ prepayCommitTiers.\ commitTier.\ *tierIndex*
     - Integer
     - The index that is associated with the tier.
   * - commitGrid.\ *id*
     - String
     - The ID for the commit grid.
   * - commitGrid.\ *geo*
     - String
     -
       - ``USA``: United States
       - ``UK``: United Kingdom
       - ``AUS``: Australia
       - ``APAC``: Asia-Pacific
   * - commitGrid.\ *currency*
     - String
     -
       - ``USD``: United States Dollar
       - ``GBP``: British Pound Sterling
       - ``AUD``: Australian Dollar
       - ``EUR``: Euro
   * - commitGrid.\ *gridType*
     - String
     -
       - ``STANDARD``: Offers pre-defined discounts based on the length of the
         commitment. By default, only ``STANDARD`` grids are returned.
       - ``CUSTOM``: Offers a customized discount based on a customer's
         request.
   * - commitGrid.\ *gridVersion*
     - String
     - The version of the commit grid. Example: ``1``.
   * - commitGrid.\ *gridStartDate*
     - String
     - The date and time that the commit grid begins.
   * - commitGrid.\ *gridEndDate*
     - String
     - The date and time that the commit grid ends.

**Example response**

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

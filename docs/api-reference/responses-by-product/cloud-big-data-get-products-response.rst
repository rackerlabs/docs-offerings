.. _cloud-big-data-get-products-response:

====================================
Cloud Big Data get products response
====================================

The following example shows the response for a request to retrieve the
Cloud Big Data products that are associated with an offering.

.. code::

  {
    "products": {
        "product": [
            {
                "name": "Uptime - Hadoop1-4 - 4096 MB",
                "description": "Uptime - Hadoop1-4 - 4096 MB",
                "productOfferingPrice": {
                    "description": "Uptime - Hadoop1-4 - 4096 MB Price",
                    "priceDetails": [
                        {
                            "priceCharacteristic": [
                                {
                                    "name": "chargeType",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceLevel",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceType",
                                    "value": "LEGACY"
                                }
                            ],
                            "prices": [
                                {
                                    "unitOfMeasure": "per Instance/per Hour",
                                    "price": [
                                        {
                                            "currency": "GBP",
                                            "amount": ".1401",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": ".18",
                                            "geo": "USA"
                                        }
                                    ]
                                }
                            ]
                        },
                        .
                        .
                        .
                        {
                            "priceCharacteristic": [
                                {
                                    "name": "chargeType",
                                    "value": "INFRASTRUCTURE"
                                },
                                {
                                    "name": "serviceLevel",
                                    "value": "MANAGED"
                                },
                                {
                                    "name": "serviceType",
                                    "value": "SYSOPS"
                                }
                            ],
                            "prices": [
                                {
                                    "unitOfMeasure": "per Instance/per Hour",
                                    "price": [
                                        {
                                            "currency": "AUD",
                                            "amount": ".2853",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": ".1934",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": ".1401",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": ".2282",
                                            "geo": "UK"
                                        },
                                        {
                                            "currency": "AUD",
                                            "amount": ".225",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "EUR",
                                            "amount": ".1526",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "GBP",
                                            "amount": ".1105",
                                            "geo": "USA"
                                        },
                                        {
                                            "currency": "USD",
                                            "amount": ".18",
                                            "geo": "USA"
                                        }
                                    ]
                                }
                            ]
                        }
                    ],
                    "priceType": "Usage"
                },
                "productCharacteristic": [
                    {
                        "name": "flavor_id",
                        "value": "hadoop1-4"
                    },
                    {
                        "name": "product_category",
                        "value": "UPTIME"
                    },
                    {
                        "name": "ram_in_mb",
                        "value": "4096 MB"
                    }
                ],
                "link": {
                    "rel": "SELF",
                    "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/86af1b3c-682d-3114-9549-9a6e9ee12084/products/0ef22b0b-b494-31d2-aab5-a77418da7d55"
                },
                "id": "0ef22b0b-b494-31d2-aab5-a77418da7d55",
                "status": "ACTIVE",
                "productCode": "UPTIME_hadoop1-4_4096MB",
                "salesChannel": "PUBLIC"
            }
        ],
        "link": [
            {
                "rel": "NEXT",
                "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/86af1b3c-682d-3114-9549-9a6e9ee12084/products?marker=1&limit=1"
            }
        ]
      }
    }

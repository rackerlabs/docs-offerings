.. _cloud-bs-get-products-response:

=========================================
Cloud Block Storage get products response
=========================================

The following example shows the response for a request to retrieve the
Rackspace Cloud Block Storage products that are associated with an offering.

.. code::

  {
     "products": {
         "product": [
             {
                 "name": "Storage - SNAPSHOTS",
                 "description": "Storage - SNAPSHOTS",
                 "productOfferingPrice": {
                     "description": "Storage - SNAPSHOTS Price",
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
                                     "unitOfMeasure": "per GB/per Hour",
                                     "price": [
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000096",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000137",
                                             "geo": "USA"
                                         }
                                     ]
                                 }
                             ]
                         },
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
                                     "value": "SYSOPS"
                                 }
                             ],
                             "prices": [
                                 {
                                     "unitOfMeasure": "per GB/per Hour",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001798",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001219",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000882",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001798",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001219",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000882",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001956",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001326",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000096",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001565",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001713",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001161",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000084",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000137",
                                             "geo": "USA"
                                         }
                                     ]
                                 }
                             ]
                         },
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
                                     "value": "DEVOPS"
                                 }
                             ],
                             "prices": [
                                 {
                                     "unitOfMeasure": "per GB/per Hour",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001798",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001219",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000882",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001798",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001219",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000882",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001956",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001326",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000096",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001565",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001713",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001161",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000084",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000137",
                                             "geo": "USA"
                                         }
                                     ]
                                 }
                             ]
                         },
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
                                     "value": "LEGACY"
                                 }
                             ],
                             "prices": [
                                 {
                                     "unitOfMeasure": "per GB/per Hour",
                                     "price": [
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000096",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000137",
                                             "geo": "USA"
                                         }
                                     ]
                                 }
                             ]
                         },
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
                                     "unitOfMeasure": "per GB/per Hour",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001798",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001219",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000882",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001798",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001219",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000882",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001438",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001956",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001326",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000096",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0001565",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0001713",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0001161",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000084",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000137",
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
                         "name": "product_category",
                         "value": "STORAGE"
                     },
                     {
                         "name": "volume_type",
                         "value": "SNAPSHOTS"
                     }
                 ],
                 "link": {
                     "rel": "SELF",
                     "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/a9b2e361-c7de-37e0-8bdb-40fb33ac1576/products/36c91c84-12b6-3817-a811-417b2c745ba2"
                 },
                 "id": "36c91c84-12b6-3817-a811-417b2c745ba2",
                 "status": "ACTIVE",
                 "productCode": "STORAGE_SNAPSHOTS",
                 "salesChannel": "PUBLIC"
             }
         ],
         "link": [
             {
                 "rel": "NEXT",
                 "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/a9b2e361-c7de-37e0-8bdb-40fb33ac1576/products?marker=1&limit=1"
             }
         ]
      }
    }

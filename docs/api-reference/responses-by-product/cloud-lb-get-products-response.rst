.. _cloud-lb-get-products-response:

==========================================
Cloud Load Balancers get products response
==========================================

The following example shows the response for a request to retrieve the
Rackspace loud Load Balancers products that are associated with an offering.

.. code::

  {
     "products": {
         "product": [
             {
                 "name": "Uptime - BASE",
                 "description": "Uptime - BASE",
                 "productOfferingPrice": {
                     "description": "Uptime - BASE Price",
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
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".01",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".015",
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
                                     "unitOfMeasure": "per Instance/per Hour",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".0213",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0144",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0104",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0213",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0144",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0104",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0204",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0138",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".01",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0163",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0188",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0127",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0092",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".015",
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
                                     "unitOfMeasure": "per Instance/per Hour",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".0213",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0144",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0104",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0213",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0144",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0104",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0204",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0138",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".01",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0163",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0188",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0127",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0092",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".015",
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
                                     "unitOfMeasure": "per Instance/per Hour",
                                     "price": [
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".01",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".015",
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
                                     "unitOfMeasure": "per Instance/per Hour",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".0213",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0144",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0104",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0213",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0144",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0104",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".017",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0204",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0138",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".01",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0163",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0188",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".0127",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0092",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".015",
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
                         "value": "UPTIME"
                     },
                     {
                         "name": "sub_product_code",
                         "value": "BASE"
                     }
                 ],
                 "link": {
                     "rel": "SELF",
                     "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/6d1e4a24-49df-3d67-88a5-0aa53e6eec23/products/195652c0-0b4d-3989-ba5a-c814410387bb"
                 },
                 "id": "195652c0-0b4d-3989-ba5a-c814410387bb",
                 "status": "ACTIVE",
                 "productCode": "UPTIME_BASE",
                 "salesChannel": "PUBLIC"
             }
         ],
         "link": [
             {
                 "rel": "NEXT",
                 "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/6d1e4a24-49df-3d67-88a5-0aa53e6eec23/products?marker=1&limit=1"
             }
         ]
      }
    }

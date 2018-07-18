.. _cloud-backup-offering-get-products-response:

==================================
Cloud Backup get products response
==================================

The following example shows the response for a request to retrieve the
Cloud Backup products that are associated with an offering.

.. code::

  {
     "products": {
         "product": [
             {
                 "name": "Storage License",
                 "description": "Storage License",
                 "productOfferingPrice": {
                     "description": "Storage License Price",
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
                                     "unitOfMeasure": "per Server/per Day",
                                     "price": [
                                         {
                                             "currency": "USD",
                                             "amount": ".36",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".36",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".263",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".329",
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
                                     "unitOfMeasure": "per Server/per Day",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".45",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".3051",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".2209",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".36",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".45",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".3051",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".2209",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".36",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".5359",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".3633",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".263",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".4287",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".4113",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".2788",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".2018",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".329",
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
                                     "unitOfMeasure": "per Server/per Day",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": "0",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "0",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "0",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "0",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "0",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "0",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "0",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "0",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "0",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "0",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "0",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "0",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "0",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "0",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "0",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "0",
                                             "geo": "USA"
                                         }
                                     ]
                                 }
                             ]
                         }
                     ],
                     "priceType": "License"
                 },
                 "productCharacteristic": [
                     {
                         "name": "product_category",
                         "value": "STORAGE_LICENSE"
                     }
                 ],
                 "link": {
                     "rel": "SELF",
                     "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/41cb76aa-dd4d-3bd6-b305-e25f3fb3bae7/products/7584faf3-8da8-36db-a003-a59cfe8f7397"
                 },
                 "id": "7584faf3-8da8-36db-a003-a59cfe8f7397",
                 "status": "ACTIVE",
                 "productCode": "STORAGE_LICENSE",
                 "salesChannel": "PUBLIC"
             }
         ],
         "link": []
      }
    }

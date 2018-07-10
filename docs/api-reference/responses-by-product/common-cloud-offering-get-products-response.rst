.. _common-cloud-offering-get-products-response:

===========================================
Common Cloud offering get products response
===========================================

The following example shows the response for a request to retrieve the
Common Cloud Backup products that are associated with an offering.

.. code::

  {
     "products": {
         "product": [
             {
                 "name": "Minimum Support Charge",
                 "description": "Minimum Support Charge",
                 "productOfferingPrice": {
                     "description": "Minimum Support Charge Price",
                     "priceDetails": [
                         {
                             "priceCharacteristic": [
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
                                     "unitOfMeasure": "per Month",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": "62.5",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "42.375",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "30.675",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "50",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "62.5",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "42.375",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "30.675",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "50",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "71.313",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "48.35",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "35",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "57.05",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "62.5",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "42.375",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "30.675",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "50",
                                             "geo": "USA"
                                         }
                                     ]
                                 }
                             ]
                         },
                         {
                             "priceCharacteristic": [
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
                                     "unitOfMeasure": "per Month",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": "625",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "423.75",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "306.75",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "500",
                                             "geo": "APAC"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "625",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "423.75",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "306.75",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "500",
                                             "geo": "AUS"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "713.121",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "483.496",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "350",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "570.497",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": "625",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": "423.75",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": "306.75",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": "500",
                                             "geo": "USA"
                                         }
                                     ]
                                 }
                             ]
                         }
                     ],
                     "priceType": "Service"
                 },
                 "productCharacteristic": [
                     {
                         "name": "product_category",
                         "value": "MINIMUM_SUPPORT_CHARGE"
                     }
                 ],
                 "link": {
                     "rel": "SELF",
                     "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/3a14712f-c617-3481-b397-174dfff1e41f/products/15ccd805-aed9-3d68-a85a-b5e9ad258e96"
                 },
                 "id": "15ccd805-aed9-3d68-a85a-b5e9ad258e96",
                 "status": "ACTIVE",
                 "productCode": "MINIMUM_SUPPORT_CHARGE",
                 "salesChannel": "PUBLIC"
             }
         ],
         "link": [
             {
                 "rel": "NEXT",
                 "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/3a14712f-c617-3481-b397-174dfff1e41f/products?marker=1&limit=1"
             }
         ]
      }
    }

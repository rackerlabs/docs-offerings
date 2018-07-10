.. _cloud-sites-offering-get-products-response:

=================================
Cloud Sites get products response
=================================

The following example shows the response for a request to retrieve the
Cloud Sites products that are associated with an offering.

.. code::

    {
       "products": {
           "product": [
               {
                   "name": "Domain Renewal",
                   "description": "Domain Renewal",
                   "productOfferingPrice": {
                       "description": "Domain Renewal Price",
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
                                       "unitOfMeasure": "per Year",
                                       "price": [
                                           {
                                               "currency": "USD",
                                               "amount": "10",
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
                                       "unitOfMeasure": "per Year",
                                       "price": [
                                           {
                                               "currency": "AUD",
                                               "amount": "12.5",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": "8.475",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": "6.135",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": "10",
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
                                       "unitOfMeasure": "per Year",
                                       "price": [
                                           {
                                               "currency": "AUD",
                                               "amount": "12.5",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": "8.475",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": "6.135",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": "10",
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
                                       "unitOfMeasure": "per Year",
                                       "price": [
                                           {
                                               "currency": "USD",
                                               "amount": "10",
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
                                       "unitOfMeasure": "per Year",
                                       "price": [
                                           {
                                               "currency": "AUD",
                                               "amount": "12.5",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": "8.475",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": "6.135",
                                               "geo": "USA"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": "10",
                                               "geo": "USA"
                                           }
                                       ]
                                   }
                               ]
                           }
                       ],
                       "priceType": "Item"
                   },
                   "productCharacteristic": [
                       {
                           "name": "product_category",
                           "value": "DOMAIN_RENEWAL"
                       }
                   ],
                   "link": {
                       "rel": "SELF",
                       "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/361b9937-f217-3a8f-b6e8-27e294343c99/products/12beb0d0-8145-3a96-853f-66b4031ee29b"
                   },
                   "id": "12beb0d0-8145-3a96-853f-66b4031ee29b",
                   "status": "ACTIVE",
                   "productCode": "DOMAIN_RENEWAL",
                   "salesChannel": "PUBLIC"
               }
           ],
           "link": [
               {
                   "rel": "NEXT",
                   "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/361b9937-f217-3a8f-b6e8-27e294343c99/products?marker=1&limit=1"
               }
           ]
        }
      }

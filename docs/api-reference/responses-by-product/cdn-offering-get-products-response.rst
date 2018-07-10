.. _cdn-offering-get-products-response:

===================================
Rackspace CDN get products response
===================================

The following example shows the response for a request to retrieve the
Rackspace Content Delivery Network (CDN) products that are associated with an
offering.

.. code::

  {
     "products": {
         "product": [
             {
                 "name": "Requests - HTTPS",
                 "description": "Requests - HTTPS",
                 "productOfferingPrice": {
                     "description": "Requests - HTTPS Price",
                     "priceDetails": [
                         {
                             "priceCharacteristic": [
                                 {
                                     "name": "chargeType",
                                     "value": "INFRASTRUCTURE"
                                 },
                                 {
                                     "name": "edgeLocation",
                                     "value": "APAC"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "APAC"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "APAC"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "APAC"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "APAC"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "AUS"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".00000125",
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
                                     "name": "edgeLocation",
                                     "value": "AUS"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001563",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001059",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000767",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".00000125",
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
                                     "name": "edgeLocation",
                                     "value": "AUS"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001563",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001059",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000767",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".00000125",
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
                                     "name": "edgeLocation",
                                     "value": "AUS"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".00000125",
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
                                     "name": "edgeLocation",
                                     "value": "AUS"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001563",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001059",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000767",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".00000125",
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
                                     "name": "edgeLocation",
                                     "value": "EMEA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "EMEA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "EMEA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "EMEA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "EMEA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "IND"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "IND"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "IND"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "IND"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "IND"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "JPN"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "JPN"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "JPN"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "JPN"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "JPN"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001834",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001243",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000009",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001467",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".0000015",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001017",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000736",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000012",
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
                                     "name": "edgeLocation",
                                     "value": "NA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000007",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001",
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
                                     "name": "edgeLocation",
                                     "value": "NA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001426",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000000967",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000007",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001141",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000125",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000000848",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000614",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001",
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
                                     "name": "edgeLocation",
                                     "value": "NA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001426",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000000967",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000007",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001141",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000125",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000000848",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000614",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001",
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
                                     "name": "edgeLocation",
                                     "value": "NA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000007",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001",
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
                                     "name": "edgeLocation",
                                     "value": "NA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".000001426",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000000967",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000007",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001141",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000125",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000000848",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".000000614",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000001",
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
                                     "name": "edgeLocation",
                                     "value": "SA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000016",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000022",
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
                                     "name": "edgeLocation",
                                     "value": "SA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000326",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".00000221",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000016",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000002608",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000275",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001865",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".00000135",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000022",
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
                                     "name": "edgeLocation",
                                     "value": "SA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000326",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".00000221",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000016",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000002608",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000275",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001865",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".00000135",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000022",
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
                                     "name": "edgeLocation",
                                     "value": "SA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000016",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000022",
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
                                     "name": "edgeLocation",
                                     "value": "SA"
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
                                     "unitOfMeasure": "per Request",
                                     "price": [
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000326",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".00000221",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".0000016",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".000002608",
                                             "geo": "UK"
                                         },
                                         {
                                             "currency": "AUD",
                                             "amount": ".00000275",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "EUR",
                                             "amount": ".000001865",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "GBP",
                                             "amount": ".00000135",
                                             "geo": "USA"
                                         },
                                         {
                                             "currency": "USD",
                                             "amount": ".0000022",
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
                         "value": "REQUESTS"
                     },
                     {
                         "name": "sub_product_code",
                         "value": "HTTPS"
                     }
                 ],
                 "link": {
                     "rel": "SELF",
                     "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/77d04f01-c000-32e9-aa6a-aac4ec3b5d35/products/1b912dc1-4b25-39d3-b782-62b7daef874b"
                 },
                 "id": "1b912dc1-4b25-39d3-b782-62b7daef874b",
                 "status": "ACTIVE",
                 "productCode": "REQUESTS_HTTPS",
                 "salesChannel": "PUBLIC"
             }
         ],
         "link": [
             {
                 "rel": "NEXT",
                 "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/77d04f01-c000-32e9-aa6a-aac4ec3b5d35/products?marker=1&limit=1"
             }
         ]
      }
    }

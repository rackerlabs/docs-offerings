.. _cloud-files-get-products-response:

=================================
Cloud Files get products response
=================================

The following example shows the response for a request to retrieve the
Rackspace Cloud Files products that are associated with an offering.

.. code::

    {
       "products": {
           "product": [
               {
                   "name": "Storage",
                   "description": "Storage",
                   "productOfferingPrice": {
                       "description": "Storage Price",
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
                                       "unitOfMeasure": "per GB/per Month",
                                       "price": [
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".07",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".065",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".06",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".055",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".052",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".048",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".07",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
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
                                       "unitOfMeasure": "per GB/per Month",
                                       "price": [
                                           {
                                               "currency": "AUD",
                                               "amount": ".1313",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1188",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".089",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0805",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0644",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0583",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1313",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1188",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".089",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0805",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0644",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0583",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1426",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1324",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1223",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".112",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".106",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0978",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0967",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0898",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0829",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0759",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0719",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0663",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".07",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".065",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".06",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".055",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".052",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".048",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1141",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1059",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0978",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0896",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0848",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0782",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".125",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0875",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0848",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0593",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0614",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0429",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".07",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
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
                                       "unitOfMeasure": "per GB/per Month",
                                       "price": [
                                           {
                                               "currency": "AUD",
                                               "amount": ".1313",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1188",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".089",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0805",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0644",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0583",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1313",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1188",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".089",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0805",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0644",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0583",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1426",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1324",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1223",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".112",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".106",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0978",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0967",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0898",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0829",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0759",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0719",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0663",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".07",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".065",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".06",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".055",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".052",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".048",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1141",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1059",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0978",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0896",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0848",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0782",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".125",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0875",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0848",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0593",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0614",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0429",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".07",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
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
                                       "unitOfMeasure": "per GB/per Month",
                                       "price": [
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".07",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".065",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".06",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".055",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".052",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".048",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".07",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
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
                                       "unitOfMeasure": "per GB/per Month",
                                       "price": [
                                           {
                                               "currency": "AUD",
                                               "amount": ".1313",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1188",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".089",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0805",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0644",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0583",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "APAC",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "APAC",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "APAC",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "APAC",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "APAC",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "APAC",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1313",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1188",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".089",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0805",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0644",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0583",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".105",
                                               "geo": "AUS",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".095",
                                               "geo": "AUS",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "AUS",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "AUS",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "AUS",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "AUS",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1426",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1324",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1223",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".112",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".106",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0978",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0967",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0898",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0829",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0759",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0719",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0663",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".07",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".065",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".06",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".055",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".052",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".048",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1141",
                                               "geo": "UK",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1059",
                                               "geo": "UK",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0978",
                                               "geo": "UK",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0896",
                                               "geo": "UK",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0848",
                                               "geo": "UK",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".0782",
                                               "geo": "UK",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".125",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1125",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1063",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0938",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "AUD",
                                               "amount": ".0875",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0848",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0763",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".072",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0678",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0636",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "EUR",
                                               "amount": ".0593",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0614",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0552",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0521",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0491",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".046",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "GBP",
                                               "amount": ".0429",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".1",
                                               "geo": "USA",
                                               "tierMin": "1",
                                               "tierMax": "1",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".09",
                                               "geo": "USA",
                                               "tierMin": "2",
                                               "tierMax": "50",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".085",
                                               "geo": "USA",
                                               "tierMin": "51",
                                               "tierMax": "200",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".08",
                                               "geo": "USA",
                                               "tierMin": "201",
                                               "tierMax": "500",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".075",
                                               "geo": "USA",
                                               "tierMin": "501",
                                               "tierMax": "1024",
                                               "tierUnit": "TB"
                                           },
                                           {
                                               "currency": "USD",
                                               "amount": ".07",
                                               "geo": "USA",
                                               "tierMin": "1025",
                                               "tierUnit": "TB"
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
                       }
                   ],
                   "link": {
                       "rel": "SELF",
                       "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/1099767e-99dc-3f62-a405-694ce681759c/products/2b137f49-562d-3027-926e-71de2faaac7d"
                   },
                   "id": "2b137f49-562d-3027-926e-71de2faaac7d",
                   "status": "ACTIVE",
                   "productCode": "STORAGE",
                   "salesChannel": "PUBLIC"
               }
           ],
           "link": [
               {
                   "rel": "NEXT",
                   "href": "https://staging.offer.api.rackspacecloud.com/v2/offerings/1099767e-99dc-3f62-a405-694ce681759c/products?marker=1&limit=1"
               }
           ]
        }
      }

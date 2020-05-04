.. _cloud-files-get-products-response:

=================================
Cloud Files get products response
=================================

The following example shows the response for a request to retrieve the
Cloud Files products that are associated with an offering.

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
                                           .
                                           .
                                           .
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
                                           .
                                           .
                                           .
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

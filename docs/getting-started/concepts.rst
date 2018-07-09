.. _concepts:

==================
|service| concepts
==================

To use the |api-service| effectively, you should understand several key
concepts.

.. COMMENT: The following concepts are provided as examples only. Replace
   them with relevant information for your product, and provide as many
   concepts as needed.

.. _concept-offering:

Offering
~~~~~~~~
An offering is a configuration of products that a user can purchase for a
certain price. It is a collection of products, product characteristics, and
product prices.

.. _concept-product:

Product
~~~~~~~
A product is a tangible or intangible item that is sold to a customer.

.. _concept-product-characteristic:

Product characteristic
~~~~~~~~~~~~~~~~~~~~~~
A product characteristic provides additional information about a product. It
follows the format ``Characteristic key : Characteristic value``. Product
characteristics are mainly intended to be used to configure information from
external applications that drive product configuration.

.. _concept-commit-grid:

Commit grid
~~~~~~~~~~~

A commit grid is a matrix that indicates the discounts that are available per
offering and length of commitment.

Rackspace commit grids can be classified into the following types.

Standard commit grid
####################

A standard commit grid offers pre-defined discounts based on the length of the
customer's commitment. By default, Rackspace applies a standard commit grid to
new accounts.

Custom commit grid
##################

A custom commit grid offers customized discounts based on a customer's
request. A payload for the custom commit grid is created and posted to the
Offer Service with a unique ID. A customer account that is associated with a
specific geographic region (such as USA or UK) can have only one
commit grid applied to it.

.. _concept-volume-grid:

Volume Grid
~~~~~~~~~~~

A volume grid is a matrix that indicates the discounts that can be applied
based on the volume of cloud services usage. A volume grid is only used when
an overflow occurs, such as when a customer exceeds the monthly maximum amount
(``maxAmount``) that is associated with the commitment.

Rackspace has the following types of volume discount grids:

Standard volume grid
####################

A standard volume grid offers pre-defined discounts based on the volume of
cloud services usage. If an overflow occurs, Rackspace applies a standard
volume grid to the account by default.

Custom volume grid
##################

A custom volume grid offers customized volume discounts. Custom volume grids
are further classified into the following types:

* **Preset grid**: Offers customized volume discounts.

* **Zero-preset grid**: No discount is applied to the account. This scenario
  occurs only when a customer waives a volume discount in favor of a better
  custom commit grid discount.

.. _behavior-api:

=========================
API behavior and statuses
=========================

.. COMMENT: Adapt this topic to provide information that is relevant for your
   product.


The Offer API is considered to be asynchronous because mutable
operations (that is, POST, PUT, and DELETE) are often queued up and then
handled accordingly. All successful asynchronous API operations have a normal
response code of 202.

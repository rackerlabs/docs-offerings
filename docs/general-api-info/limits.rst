.. _limits:

======
Limits
======


All accounts, by default, have a preconfigured set of thresholds, or *limits*,
to manage capacity and prevent abuse of the system. The Offer API recognizes
*rate limits*. Rate limits are thresholds that are reset after a certain
amount of time passes. The rate limit for the Offer API is 100.

.. note::

    If the default limit is too low for your particular application,
    contact Rackspace Cloud support to request an increase. All requests
    require reasonable justification.

.. _Repose service: http://www.openrepose.org

.. _api-info-limits-ratelimits:

If you exceed this limit, a ``413 (Rate Control)`` HTTP  response is returned
with a ``Retry-After`` header to notify the client when it can  attempt to try
again.

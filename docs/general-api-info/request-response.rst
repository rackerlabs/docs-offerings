.. _req-resp-types:

==========================
Request and response types
==========================

The Offer service API supports JSON data serialization format.

The request format is specified by using the ``Content-Type`` header and is
required for operations that have a request body.

The response format can be specified in requests either by using the ``Accept``
header or by adding a ``.json`` extension to the request URI. A
response can be serialized by using a format that is different from the
request. If conflicting formats are specified by using both an ``Accept``
header and a query extension, the query extension takes precedence.

If no response format is specified, JSON is the default.

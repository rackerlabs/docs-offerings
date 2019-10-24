.. _authenticate-to-cloud:

===================================
Authenticate to the Rackspace Cloud
===================================

Whether you use cURL, a REST client, or a command-line client (CLI) to send
requests to the |api-service|, you need an authentication token to include in
the ``X-Auth-Token`` header of each request. You get a token by submitting an
authentication request with valid account credentials to the Rackspace Cloud
Identity API service.

To access the Authentication service, you must know whether your account is
US-based or UK-based.

US-based accounts authenticate through the following endpoint:

.. code::

       https://identity.api.rackspacecloud.com/v2.0

UK-based accounts authenticate through the following endpoint:

.. code::

       https://lon.identity.api.rackspacecloud.com/v2.0/

Your account may be based in either the US or the UK. The location that is
associated with your account is not determined by your physical location but
by the location of the Rackspace retail site which was used to create your
account.

If your account was created through https://www.rackspacecloud.com, it is a US-based account.

If your account was created through https://www.rackspace.co.uk, it is a UK-based account.

If you are unsure how your account was created, use the Rackspace contact
information at either site to ask for help.

With a valid token, you can send API requests to any of the API service
endpoints that you are authorized to use. The authentication response includes
a token expiration date. When a token expires, you can send another
authentication request to get a new one.


.. note::
     For more information about authentication tokens, see the following
     topics in the Identity developer documentation.

     - :rax-devdocs:`Authentication token operations
       <cloud-identity/v2/api-reference/token-operations/#authentication-token>`

        The examples in the Getting Started Guide show how to authenticate by
        using username and API key credentials,
        which is a more secure way to communicate with API services.
        The authentication token operations reference describes other types
        of credentials that you can use for authentication.

     - :rax-devdocs:`Manage tokens and token expiration
       <cloud-identity/v2/getting-started/manage-auth-tokens/#manage-authentication-tokens>`

.. include:: ../common-gs/auth-using-curl.rst

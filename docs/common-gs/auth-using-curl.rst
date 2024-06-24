.. _authenticate-using-curl:

Follow these steps to authenticate to the Rackspace Cloud by
:ref:`using cURL <how-curl-commands-work>`.

- :ref:`Send an authentication request <send-auth-req-curl>`
- :ref:`Review the authentication response <review-auth-resp>`
- :ref:`Configure environment variables <configure-environment-variables>`

.. important::

   The cURL examples in this guide are provided for reference only. Because
   the use of cURL has environmental dependencies, copying and pasting the
   examples might not work in your environment.

.. _send-auth-req-curl:

Send an authentication request
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

From a command prompt, send a **POST tokens** request to the Rackspace Cloud
Identity service.  Include your username and :ref:`API key <get-credentials>`,
as shown in the following example.

.. include:: ../common-gs/samples/auth-req-curl.rst


.. _review-auth-resp:

Review the authentication response
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If your credentials are valid, the Identity service returns an authentication
response that includes the following information:

 - An authentication token.
 - A service catalog with information about the services that you can access.

   **Note**: The response to the authentication request only includes
   endpoints for products and does not include the endpoint for the Offer
   Service API.

 - User information and role assignments.


.. note::
    For detailed information about the authentication response, see the
    :rax-devdocs:`Annotated authentication request and response
    <cloud-identity/v2/general-api-info/authentication-info/sample-auth-req-response/#annotated-auth-req-resp>`
    in the Identity API documentation.


In the following example, the ellipsis (...)  represents other service
endpoints, which are not shown. The values shown in this and other examples
vary because the information returned is specific to your account.

**Example: Authentication response**

.. include:: ../common-gs/samples/auth-resp-json.rst


If the request was successful, it returns the following values that you need to
include when you make service requests to the Rackspace product API:

token ID
    The token ID value is required to confirm your identity each
    time you access the service. Include it in the ``X-Auth-Token`` header
    for each API request.

    The ``expires`` attribute indicates the date and time that the token will
    expire, unless it is revoked before the expiration. To get a new token,
    submit another authentication request. For more information, see
    :rax-devdocs:`Manage tokens and token expiration
    <cloud-identity/v2/getting-started/manage-auth-tokens/#manage-authentication-tokens>`.

tenant ID
    The tenant ID provides your account number. For most Rackspace Cloud
    service APIs, the tenant ID is appended to the API endpoint in the service
    catalog automatically. For Rackspace Cloud services, the tenant ID has the
    same value as the tenant name.

If the request failed, review the response message and
the following error message descriptions to determine next steps.

- If you see the following error message, review the authentication request
  for syntax or coding errors. If you are using cURL, see
  :ref:`Using cURL <how-curl-commands-work>`.

  .. code::

     400 Invalid request body: unable to parse Auth data. Please review XML or
     JSON formatting

- If you see the following error message, verify the authentication credentials
  submitted in the authentication request. If necessary, contact your Rackspace
  Cloud Administrator or Rackspace Support to get valid credentials.

  .. code::

     401 Unable to authenticate user with credentials provided.

..  note::
       For additional information about authentication errors, see the
       :rax-dev:`Identity API Reference documentation
       <docs/cloud-identity/v2/developer-guide/#token-operations>`.

.. _configure-environment-variables:

Configure environment variables
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To make it easier to include the token ID, tenant ID, and other
values in API requests, use the ``export`` command to create environment
variables that can be substituted for the actual values.

.. include:: ../common-gs/using-env-variables.rst

**Create environment variables**

#. In the ``token`` section of the authentication response, copy the
   token ``id`` and tenant ``id`` values from the token object. The
   following example shows example values only.

      .. include:: ../common-gs/samples/auth-token-object.rst

#. Export the token ID to an environment variable
   that can be supplied in the ``X-Auth-Token`` header required in each
   API request.

   .. code::

       $ export AUTH_TOKEN="token-id"

   Replace ``token-id`` with the authentication token ``id`` value returned
   in the authentication response.

#. Export the tenant ID to an environment variable that can be supplied in
   requests that require you to specify a tenant ID or tenant name.

   .. code::

       $ export TENANT_ID="tenant-id"

   Replace ``tenant-id`` with the token ``id`` value returned
   in the authentication response.

#. The ``service catalog`` section of the authentication response does not
   include the endpoint for the Offer service API. To get the endpoint, go to
   the top of this page and copy the URL for the version and region that you
   want to access.

#. Export the URL to an environment variable, as shown in the following
   example:

   .. code::

        $ export API_ENDPOINT="URL"


   Replace ``URL`` with the URL that is listed for your region at the top of
   this page.

Usage
=====

Quickstart
------------

To be able to use Datatruck's OpenAPI you should create tokens from your dashboard. Go to your dashboard and create token 
with appropriate scopes and expiration. Expiration and scopes are optional as well as description for your token, 

but remember name is required. 

.. image:: token_create.jpg


Once you create your token, token is displayed only once so make sure you copy it 


to somewhere else. You can always regenerate the token or delete. Once you regenerate, previous token will stop working. 


.. image:: token_list.jpg


Datatruck uses the API Key Token HTTP authentication scheme. In order to use the authentication token, include it in the Authorization header in your HTTP request:

.. code-block:: shell

    curl --request GET \
  --url https://dashboard.datatruck.io/api/v1/openapi/orders \
  --header 'Authorization: Token cc92174571ac12f386e5657b187d39bb210f3270a837730125ed4029a448877e' \
  --header 'Content-Type: application/json'

The Datatruck API returns JSON-encoded responses (It is list of loads):


.. literalinclude:: order.json
  :language: JSON

Thank you, we are developing Postman OpenAPI collection..

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

.. code-block:: json
[
	{
		"id": 2489,
		"load_id": "T-111QT34XS",
		"shipment_id": "DT-002489",
		"status": "dispatched",
		"load_pay": 148.17,
		"total_miles": 574.31,
		"created_datetime": "2023-10-11T13:42:54.456045Z",
		"created_by__full_name": "Super Admin",
		"total_other_pay": 122.0,
		"total_pay": 270.17,
		"per_mile_revenue": 0.26,
		"tags": [],
		"dispatcher__full_name": " ",
		"customer__company_name": "string",
		"mc_number__company_name": "Updated Test Mc Number",
		"office__office_name": null,
		"pickup_appointment_time": "2023-10-08T20:00:00Z",
		"delivery_appointment_time": "2023-10-11T23:14:00Z",
		"pickup_time": "2023-10-08T20:00:00Z",
		"delivery_time": "2023-10-11T23:14:00Z",
		"trip": {
			"id": 1913,
			"status": "assigned",
			"trip_id": "TR-002489-01",
			"mile": 574.31,
			"empty_mile": 0.0,
			"total_load_pay": 148.17,
			"carrier__name": null,
			"driver__full_name": "awefas fasdfads",
			"team_driver__full_name": " ",
			"truck__unit_number": "fasdfawefadsfasdf",
			"pickup": {
				"id": 1348,
				"company": "DWA9",
				"address1": "3711 142nd Ave E, Sumner, WA 98390, USA",
				"city": "Sumner",
				"state": "Washington",
				"zip_code": "98390"
			},
			"delivery": {
				"id": 1348,
				"company": "DWA9",
				"address1": "3711 142nd Ave E, Sumner, WA 98390, USA",
				"city": "Sumner",
				"state": "Washington",
				"zip_code": "98390"
			},
			"settlement": null
		},
		"batch_orders": null
	},
    ...
]

Thank you, we are developing Postman OpenAPI collection.
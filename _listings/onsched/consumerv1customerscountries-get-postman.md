{
  "info": {
    "name": "OnSched Returns a list of country objects",
    "_postman_id": "d7be9572-4fcf-41e2-9045-f0a494cb4295",
    "description": "Returns a list of countries with the associated country code. Country codes are based on the 2 character ANSI standard.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Customers",
      "item": [
        {
          "id": "0659442e-93d5-4b02-879e-62ab495eac21",
          "name": "ConsumerV1CustomersCountriesGet",
          "request": {
            "url": "http://api.onsched.com/consumer/v1/customers/countries",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of countries with the associated country code. Country codes are based on the 2 character ANSI standard."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fe4a927f-7cc9-486b-804b-86c8cd63d738"
            }
          ]
        }
      ]
    }
  ]
}
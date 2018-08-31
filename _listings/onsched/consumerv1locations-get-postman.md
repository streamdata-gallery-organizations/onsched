{
  "info": {
    "name": "OnSched Returns a list of business locations.",
    "_postman_id": "4ce845e3-323e-498b-a773-b863ddd999ea",
    "description": "Use this api end point if you have multiple business locations in your company.\r\nThe results are returned in pages. Use the offset and limit parameters to control the page start and size. Default offset is 0, and limit is 20.\r\nUse the other query parameters to optionally filter the results list.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Locations",
      "item": [
        {
          "id": "2917ae10-ed1a-4ccb-b632-f9cad3e6b306",
          "name": "ConsumerV1LocationsGet",
          "request": {
            "url": "http://api.onsched.com/consumer/v1/locations?limit=%7B%7D&name=%7B%7D&offset=%7B%7D",
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
            "description": "Use this api end point if you have multiple business locations in your company.\r\nThe results are returned in pages. Use the offset and limit parameters to control the page start and size. Default offset is 0, and limit is 20.\r\nUse the other query parameters to optionally filter the results list."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c60181c-4f46-45fa-88da-982ea47efcda"
            }
          ]
        }
      ]
    }
  ]
}
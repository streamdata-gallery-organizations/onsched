{
  "info": {
    "name": "OnSched Returns a business location object.",
    "_postman_id": "04932eb3-e619-46b5-9475-58012a94fe88",
    "description": "The result returned is a single location object. An id is required to find the location. Find location id's using the GET consumer/v1/locations end point,",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Locations",
      "item": [
        {
          "id": "47cf83a7-995a-4d01-a4a0-9b18abb7b1f5",
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
              "id": "22d5b4c1-06c4-4f81-a620-2147afa50dcb"
            }
          ]
        },
        {
          "id": "ffa4519a-cf00-4ee6-9d15-6a011d5c00cd",
          "name": "ConsumerV1LocationsByIdGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.onsched.com",
              "path": [
                "consumer/v1/locations/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "The result returned is a single location object. An id is required to find the location. Find location id's using the GET consumer/v1/locations end point,"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58055e82-5846-41da-a3ef-78112a1d3e56"
            }
          ]
        }
      ]
    }
  ]
}
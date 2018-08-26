{
  "info": {
    "name": "OnSched Returns a list of customers.",
    "_postman_id": "05802f3d-0c43-4df4-8a02-f98737c58cb8",
    "description": "The results are returned in pages. Use the offset and limit parameters to control the page start and size. Default offset is 0, and limit is 20.\r\nUse the other query parameters to optionally filter the results list.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Customers",
      "item": [
        {
          "id": "2b864ba9-d169-416c-b36f-58ff386f84c4",
          "name": "ConsumerV1CustomersGet",
          "request": {
            "url": "http://api.onsched.com/consumer/v1/customers?deleted=%7B%7D&email=%7B%7D&groupId=%7B%7D&lastname=%7B%7D&limit=%7B%7D&locationId=%7B%7D&offset=%7B%7D",
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
            "description": "The results are returned in pages. Use the offset and limit parameters to control the page start and size. Default offset is 0, and limit is 20.\r\nUse the other query parameters to optionally filter the results list."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "95f94757-760e-4120-bbb9-4c635bed91eb"
            }
          ]
        }
      ]
    }
  ]
}
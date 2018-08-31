{
  "info": {
    "name": "OnSched Returns a list of appointments.",
    "_postman_id": "d4df90e4-f662-4c4c-9335-37045921f0b7",
    "description": "The results are returned in pages. Use the offset and limit parameters to control the page start and size. Default offset is 0, and limit is 20.\r\nUse the other query parameters to optionally filter the results list.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Appointments",
      "item": [
        {
          "id": "3e515613-a4be-4cdb-b25b-18a10256acfd",
          "name": "ConsumerV1AppointmentsGet",
          "request": {
            "url": "http://api.onsched.com/consumer/v1/appointments?customerId=%7B%7D&email=%7B%7D&limit=%7B%7D&locationId=%7B%7D&offset=%7B%7D&resourceId=%7B%7D&serviceId=%7B%7D&status=%7B%7D",
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
              "id": "3a0b2458-a8b8-4d26-bf82-6a2a96df4db7"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "OnSched Returns a list of available days.",
    "_postman_id": "9681fad4-2ed9-42bb-8e2c-15d781740e44",
    "description": "This end point is used to show day level availability. For example if the business is closed, or there is a public holiday.\r\n\r\nDay level availability is a good way to restrict your choices of dates in your app and improve usability.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Availability",
      "item": [
        {
          "id": "0f8bb8a3-44c5-423d-947c-94af5c53b309",
          "name": "ConsumerV1AvailabilityByServiceIdByStartDateByEndDateGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.onsched.com",
              "path": [
                "consumer/v1/availability/:serviceId/:startDate/:endDate"
              ],
              "query": [
                {
                  "key": "dayAvailability",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "duration",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "endTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "firstDayAvailable",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "locationId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "resourceGroupId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "resourceId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "resourceIds",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "tzOffset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "endDate",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "serviceId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "startDate",
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
            "description": "Choose your search criteria carefully. Availability is an expensive call. If you search availability for all resources\r\nthen you should only do so for a single date. If you decide to search availability for multiple dates you should only do so\r\nfor a specific resource by specifying the optional resourceId parameter.\r\n\r\nStart and End times are specified as military times e.g. 800 = 8:00am, 2230 = 10:30pm. \r\nYou will only see availability within the boundary of your business start and end times.\r\n\r\ndayAvailability will return day availablility for the number of days requested from the start date.\r\n\r\nfirstDayAvailable only works with day availability. If set to true it will look for the first day available within the range specified\r\nby the dayAvailability parameter. The two parameters together can be a clever way to display availability for a week or month.\r\nTip - pass in the beginning of the week or month, and available times are displayed for the first available date if exists.\r\n\r\nYou should only specify the duration parameter if you let your customers choose the duration of the appointment. e.g. from a list.\r\n\r\nThe tz parameter allows you to select a suitable timezone for the customer to book in. Your app should be timezone aware if you \r\nuse this option. The requested timezone is specified as an offset(plus or minus) from GMT time."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b23591f4-a6aa-4c7a-a9fc-b60f20bd5b63"
            }
          ]
        },
        {
          "id": "74b014ae-7d45-49f0-8903-6e55e1d59183",
          "name": "ConsumerV1AvailabilityByServiceIdByStartDateByEndDateDaysGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.onsched.com",
              "path": [
                "consumer/v1/availability/:serviceId/:startDate/:endDate/days"
              ],
              "query": [
                {
                  "key": "locationId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "resourceId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "tzOffset",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "endDate",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "serviceId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "startDate",
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
            "description": "This end point is used to show day level availability. For example if the business is closed, or there is a public holiday.\r\n\r\nDay level availability is a good way to restrict your choices of dates in your app and improve usability."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3892b602-9349-465d-b24d-6a2f3dc39873"
            }
          ]
        }
      ]
    }
  ]
}
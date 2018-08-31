{
  "info": {
    "name": "OnSched Returns a list of unavailable times.",
    "_postman_id": "11bcbfdc-eb7f-4b92-bd7d-c73f507055b6",
    "description": "This endpoint is used to show unavailable times and provides information why the timeslot is unavailable.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Availability",
      "item": [
        {
          "id": "3692b1bc-3628-485b-a2b3-8107cc3af01f",
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
              "id": "04432185-ea64-4783-9748-ccecceec0849"
            }
          ]
        },
        {
          "id": "bbf8405b-c472-42cd-bbc9-39b90aab4a94",
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
              "id": "5a9c0acd-f578-40ab-81f1-b8a6590a2711"
            }
          ]
        },
        {
          "id": "74826b7f-0f07-4775-81c0-f406f5159b41",
          "name": "ConsumerV1AvailabilityByServiceIdByStartDateByEndDateUnavailableGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.onsched.com",
              "path": [
                "consumer/v1/availability/:serviceId/:startDate/:endDate/unavailable"
              ],
              "query": [
                {
                  "key": "duration",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
            "description": "This endpoint is used to show unavailable times and provides information why the timeslot is unavailable."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9bf0b4c9-fbf3-45f5-ad7c-54c86311bb88"
            }
          ]
        }
      ]
    }
  ]
}
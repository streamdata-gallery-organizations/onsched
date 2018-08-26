---
name: OnSched
x-slug: onsched
description: Build secure and scalable custom apps for Online Booking. Our flexible
  API provides many options for availability and booking. OnSched is an API first
  booking software that allows you to bring your design to life by creating your own
  booking flow. Using our robust API you can customize the interaction between your
  consumers and vendors while we do all the leg work behind the scenes. Want to offer
  online booking to your vendors? Ask about our white labelling solutions and rebrand
  our software as your own.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
x-kinRank: "7"
x-alexaRank: ""
tags: OnSched
created: "2018-08-26"
modified: "2018-08-26"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/apis.md
specificationVersion: "0.14"
apis:
- name: OnSched API - Returns a list of appointments.
  x-api-slug: consumerv1appointments-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointments-get-openapi.md
- name: OnSched API - Returns a list of available times.
  x-api-slug: consumerv1availabilityserviceidstartdateenddate-get
  description: "Choose your search criteria carefully. Availability is an expensive
    call. If you search availability for all resources\r\nthen you should only do
    so for a single date. If you decide to search availability for multiple dates
    you should only do so\r\nfor a specific resource by specifying the optional resourceId
    parameter.\r\n\r\nStart and End times are specified as military times e.g. 800
    = 8:00am, 2230 = 10:30pm. \r\nYou will only see availability within the boundary
    of your business start and end times.\r\n\r\ndayAvailability will return day availablility
    for the number of days requested from the start date.\r\n\r\nfirstDayAvailable
    only works with day availability. If set to true it will look for the first day
    available within the range specified\r\nby the dayAvailability parameter. The
    two parameters together can be a clever way to display availability for a week
    or month.\r\nTip - pass in the beginning of the week or month, and available times
    are displayed for the first available date if exists.\r\n\r\nYou should only specify
    the duration parameter if you let your customers choose the duration of the appointment.
    e.g. from a list.\r\n\r\nThe tz parameter allows you to select a suitable timezone
    for the customer to book in. Your app should be timezone aware if you \r\nuse
    this option. The requested timezone is specified as an offset(plus or minus) from
    GMT time."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1availabilityserviceidstartdateenddate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1availabilityserviceidstartdateenddate-get-openapi.md
- name: OnSched API - Returns a list of available days.
  x-api-slug: consumerv1availabilityserviceidstartdateenddatedays-get
  description: "This end point is used to show day level availability. For example
    if the business is closed, or there is a public holiday.\r\n\r\nDay level availability
    is a good way to restrict your choices of dates in your app and improve usability."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1availabilityserviceidstartdateenddatedays-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1availabilityserviceidstartdateenddatedays-get-openapi.md
- name: OnSched API - Returns a list of unavailable times.
  x-api-slug: consumerv1availabilityserviceidstartdateenddateunavailable-get
  description: This endpoint is used to show unavailable times and provides information
    why the timeslot is unavailable.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1availabilityserviceidstartdateenddateunavailable-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1availabilityserviceidstartdateenddateunavailable-get-openapi.md
- name: OnSched API - Returns a list of customers.
  x-api-slug: consumerv1customers-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customers-get-openapi.md
- name: OnSched API - Returns a list of country objects
  x-api-slug: consumerv1customerscountries-get
  description: Returns a list of countries with the associated country code. Country
    codes are based on the 2 character ANSI standard.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customerscountries-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customerscountries-get-openapi.md
- name: OnSched API - Returns a list of business locations.
  x-api-slug: consumerv1locations-get
  description: "Use this api end point if you have multiple business locations in
    your company.\r\nThe results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1locations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1locations-get-openapi.md
- name: OnSched API - Returns a business location object.
  x-api-slug: consumerv1locationsid-get
  description: The result returned is a single location object. An id is required
    to find the location. Find location id's using the GET consumer/v1/locations end
    point,
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1locationsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1locationsid-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://onenote.api.gallery.streamdata.io
- type: x-api-stack
  url: http://onsched.stack.network
- type: x-documentation
  url: https://www.onsched.com/api/docs/
- type: x-pricing
  url: https://www.onsched.com/index.html#self-service
- type: x-website
  url: http://www.onsched.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---
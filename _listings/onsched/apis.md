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
created: "2018-08-30"
modified: "2018-08-30"
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
- name: OnSched API - Returns an appointment object
  x-api-slug: consumerv1appointments-post
  description: "This end point creates a new appointment in an Initial \"IN\" status.
    \r\n\r\nA valid serviceId is required. Use GET consumer/v1/services to retrieve
    a list of your services.\r\n\r\nA valid resourceId is required if your calendar
    is a resource based calendar. Use consumer/v1/resources to retrieve a list of
    your resources.\r\n\r\nStartDateTime and EndDateTime are required. Use the ISO
    8601 format for DateTime Timezone. e.g. 2016-10-30T9:00:00-5:00"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointments-post-openapi.md
- name: OnSched API - Returns an appointment object.
  x-api-slug: consumerv1appointmentsid-get
  description: "The result returned is a single appointment object. A valid id is
    required to find the appointment. \r\n\r\nFind appointment id's using the GET
    consumer/v1/appointments end point."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointmentsid-get-openapi.md
- name: OnSched API - Returns an appointment object
  x-api-slug: consumerv1appointmentsid-delete
  description: "This end point deletes a booking. Only appointments in a \"IN\" initial
    status can be deleted.\r\nPast dated appointments cannot be cancelled.\r\n\r\nA
    valid appointment id is required. Use the appointmentId returned from GET /consumer/v1/appointments"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointmentsid-delete-openapi.md
- name: OnSched API - Returns an appointment object
  x-api-slug: consumerv1appointmentsidbook-put
  description: "This end point completes a new booking. Only appointments in the \"IN\"
    initial status can be booked.\r\nby saving all the relevant details of the booking.\r\n\r\nA
    valid appointment id is required. Use the appointmentId returned from POST /consumer/v1/appointments\r\n\r\nTo
    update appointment custom field values, use the GET /consumer/v1/appointments/customfields
    information\r\nto understand your definitions of custom fields and what key and
    values to update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointmentsidbook-put-openapi.md
- name: OnSched API - Returns an appointment object
  x-api-slug: consumerv1appointmentsidcancel-put
  description: "This end point cancels a booking or reservation. Only appointments
    in a \"BK\" booked, or \"RS\" reserved status can be cancelled.\r\nPast dated
    appointments cannot be cancelled.\r\n\r\nA valid appointment id is required. Use
    the appointmentId returned from POST /consumer/v1/appointments"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointmentsidcancel-put-openapi.md
- name: OnSched API - Returns an appointment object
  x-api-slug: consumerv1appointmentsidreschedule-put
  description: "This end point reschedules a booking. Only appointments in a \"BK\"
    booked status can be rescheduled.\r\nPast dated appointments cannot be cancelled.\r\n\r\nA
    valid appointment id is required. Use the appointmentId returned from GET /consumer/v1/appointments.\r\n\r\nThe
    serviceId and resourceId are optional. If you want your users to change the resource
    or service on a reschedule\r\nyou will have to use the regular availability endpoint
    rather than the reschedule availability end point.\r\n\r\nUse the GET /consumer/v1/availability/{id}/reschedule
    endpoint to display a list of available times\r\nfor the end user to choose from
    to reschedule the original appointment."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointmentsidreschedule-put-openapi.md
- name: OnSched API - Returns a list of appointment custom field definitions
  x-api-slug: consumerv1appointmentscustomfields-get
  description: "This end point returns your Appointment custom field definitions.\r\n\r\nAppointment
    custom fields are different than Customer custom fields. Appointment custom fields
    are\r\nstored with each appointment. They are used when the information collected
    during the booking is specific\r\nto a particular visit.\r\n\r\nUse the field,
    and type to determine how to update field values\r\nin PUT /consumer/v1/appointments/{id}/book"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointmentscustomfields-get-openapi.md
- name: 'OnSched API - '
  x-api-slug: consumerv1appointmentsbookingfields-get
  description: ""
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1appointmentsbookingfields-get-openapi.md
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
- name: OnSched API - Returns a list of available times.
  x-api-slug: consumerv1availabilityappointmentidreschedule-get
  description: "This end point is used to find availability for the purpose of rescheduling
    an appointment.\r\nAvailability defaults to the serviceId, resourceId and timezone
    from the original appointment.\r\nAfter choosing from the availability, you can
    call the appointment reschedule endpoint."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1availabilityappointmentidreschedule-get-openapi.md
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
- name: OnSched API - Creates a new customer object.
  x-api-slug: consumerv1customers-post
  description: "Use this endpoint to create a new customer. If not specified the business
    location id defaults to the first location in the company.\r\nEmail Address and
    a lastname are required for creating a new customer."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customers-post-openapi.md
- name: OnSched API - Returns a customer object.
  x-api-slug: consumerv1customersid-get
  description: "The result returned is a single customer object. An id is required
    to find the customer. Find customer id's using either the GET consumer/v1/customers
    end point,\r\nor the GET consumer/v1/appointments end point. A customer object
    is automatically created with the first booking if it doesn't already exist."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersid-get-openapi.md
- name: OnSched API - Updates a customer object.
  x-api-slug: consumerv1customersid-put
  description: "Use this endpoint to update customer information. If not specified
    the business location id defaults to the first location in the company.\r\nBlank
    fields are not changed"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersid-put-openapi.md
- name: OnSched API - Deletes a customer subscription object.
  x-api-slug: consumerv1customersid-delete
  description: Deletes a customer subscription object.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersid-delete-openapi.md
- name: OnSched API - Returns a list of customField objects
  x-api-slug: consumerv1customerscustomfields-get
  description: "This end point returns your Customer custom field definitions.\r\n\r\nCustomer
    custom fields are different than Appointment custom fields. Appointment custom
    fields are\r\nstored with each appointment. They are used when the information
    collected during the booking is specific\r\nto a particular visit, where as Customer
    custom fields are stored with the customer profile. \r\n\r\nUse the key field,
    and type to determine how to update field values\r\nin POST /consumer/v1/customers
    and PUT /consumer/v1/customers/{id}"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customerscustomfields-get-openapi.md
- name: OnSched API - Returns a list of lead questions
  x-api-slug: consumerv1customersregistrationfields-get
  description: "This end point returns your Customer Registration fields.\r\n\r\nCustomer
    custom fields are different than Appointment custom fields. Appointment custom
    fields are\r\nstored with each appointment. They are used when the information
    collected during the booking is specific\r\nto a particular visit, where as Customer
    custom fields are stored with the customer profile."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersregistrationfields-get-openapi.md
- name: OnSched API - Returns a list of customers.
  x-api-slug: consumerv1customersplans-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersplans-get-openapi.md
- name: OnSched API - Returns a customer object.
  x-api-slug: consumerv1customersplansid-get
  description: "The result returned is a single customer object. An id is required
    to find the customer. Find customer id's using either the GET consumer/v1/customers
    end point,\r\nor the GET consumer/v1/appointments end point. A customer object
    is automatically created with the first booking if it doesn't already exist."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersplansid-get-openapi.md
- name: OnSched API - Returns a list of customer booking limits.
  x-api-slug: consumerv1customersidplanlimitsserviceidresourceiddatetimetz-get
  description: "The result returned is list of limit rules as defined by the subscribed
    customer plan along with Booking Counts/Minutes\r\nThe results indicate the remaining
    bookings count / minutes. Use the results in your app to determine if the customer
    should continue booking.\r\nYou can enforce Limits in periods: Daily,Weekly,Monthly
    and for maximum total limits. Maximum total limits is based on six months prior
    to\r\nthe DateTimeTz and six months after the DateTimeTz. Daily, Weekly and Monthly
    limits are based on the calculated period relative to the\r\nsubscription plan
    start. Daily,Weekly and Monthly limits can be setup on a per interval basis e.g.
    to biweekly, or daily every 10 days.\r\nSee customer plans setup in the Portal
    for more information.\r\nAll parameters are required. If resourceId is not applicable
    for a non-resource calendar, pass zero.\r\nFormat of the dateTimeTz field is 2018-10-30T10:00-5:00"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersidplanlimitsserviceidresourceiddatetimetz-get-openapi.md
- name: OnSched API - Returns a list of customer subscriptions.
  x-api-slug: consumerv1customerssubscriptions-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customerssubscriptions-get-openapi.md
- name: OnSched API - Returns a customer subscription object.
  x-api-slug: consumerv1customersidsubscriptions-get
  description: The result returned is a single customer subscription object. A customer
    can only be subsribed to a single Customer Plan
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersidsubscriptions-get-openapi.md
- name: OnSched API - Creates a new customer subscription object.
  x-api-slug: consumerv1customersidsubscriptions-post
  description: Use this endpoint to create a new customer subscription.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersidsubscriptions-post-openapi.md
- name: OnSched API - Returns a customer subscription object.
  x-api-slug: consumerv1customerssubscriptionsid-get
  description: The result returned is a single customer subscription object.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customerssubscriptionsid-get-openapi.md
- name: OnSched API - Updates a customer subscription object.
  x-api-slug: consumerv1customerssubscriptionsid-put
  description: Use this endpoint to update customer subscription information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customerssubscriptionsid-put-openapi.md
- name: OnSched API - Deletes a list of lead questions
  x-api-slug: consumerv1customerssubscriptionsid-delete
  description: Deletes a list of lead questions
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customerssubscriptionsid-delete-openapi.md
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
- name: OnSched API - Returns a list of state objects
  x-api-slug: consumerv1customersstates-get
  description: "Returns a list of states with the associated state code and country.
    \r\n\r\nContact us if states for your countries of operation are not currently
    loaded."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1customersstates-get-openapi.md
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
- name: OnSched API - Returns a list of resources.
  x-api-slug: consumerv1resources-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1resources-get-openapi.md
- name: OnSched API - Returns a resource object.
  x-api-slug: consumerv1resourcesid-get
  description: "The result returned is a single resource object. An id is required
    to find the resource. Find customer id's using either the GET consumer/v1/resources
    end point,\r\nor the GET consumer/v1/appointments end point."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1resourcesid-get-openapi.md
- name: OnSched API - Returns a list of resource services.
  x-api-slug: consumerv1resourcesidservices-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list.\r\nResource
    services are used to explicitly define the services that can be booked for a resource.
    If no resource services are defined then by\r\ndefault all services can be booked
    for the resource."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1resourcesidservices-get-openapi.md
- name: OnSched API - Returns a list of service groups.
  x-api-slug: consumerv1servicegroups-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1servicegroups-get-openapi.md
- name: OnSched API - Returns a serviceGroup object.
  x-api-slug: consumerv1servicegroupsid-get
  description: "The result returned is a single serviceGroup object. An id is required
    to find the serviceGroup. Find serviceGroup id's using \r\nthe GET consumer/v1/servicegroups
    end point,"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1servicegroupsid-get-openapi.md
- name: OnSched API - Returns a list of services.
  x-api-slug: consumerv1services-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1services-get-openapi.md
- name: OnSched API - Returns a service object.
  x-api-slug: consumerv1servicesid-get
  description: "The result returned is a single service object. An id is required
    to find the service. Find service id's using either the GET consumer/v1/service
    end point,\r\nor the GET consumer/v1/appointments end point."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1servicesid-get-openapi.md
- name: OnSched API - Returns a list of resources.
  x-api-slug: consumerv1servicesidresources-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1servicesidresources-get-openapi.md
- name: OnSched API - Returns a list of customers.
  x-api-slug: consumerv1settings-get
  description: "The results are returned in pages. Use the offset and limit parameters
    to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
    the other query parameters to optionally filter the results list."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/onsched-logo.png
  humanURL: http://www.onsched.com
  baseURL: https://api.onsched.com//
  tags: API Provider, Bookings, Profiles, Schedules, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/onsched/master/_listings/onsched/consumerv1settings-get-openapi.md
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
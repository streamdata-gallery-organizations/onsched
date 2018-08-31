---
swagger: "2.0"
x-collection-name: OnSched
x-complete: 0
info:
  title: OnSched Returns a customer object.
  description: "The result returned is a single customer object. An id is required
    to find the customer. Find customer id's using either the GET consumer/v1/customers
    end point,\r\nor the GET consumer/v1/appointments end point. A customer object
    is automatically created with the first booking if it doesn't already exist."
  termsOfService: None
  contact:
    name: OnSched.com
    url: https://onsched.com
    email: info@onsched.com
  version: 1.0.0
host: api.onsched.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /consumer/v1/appointments:
    get:
      summary: Returns a list of appointments.
      description: "The results are returned in pages. Use the offset and limit parameters
        to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
        the other query parameters to optionally filter the results list."
      operationId: ConsumerV1AppointmentsGet
      x-api-path-slug: consumerv1appointments-get
      parameters:
      - in: query
        name: customerId
        description: Filter appointments by customer
      - in: query
        name: email
        description: Filter appointments by email address
      - in: query
        name: limit
        description: Page limit, default 20
      - in: query
        name: locationId
        description: The id of the business location
      - in: query
        name: offset
        description: Starting row of page, default 0
      - in: query
        name: resourceId
        description: Filter appointments by resource
      - in: query
        name: serviceId
        description: Filter appointments by service
      - in: query
        name: status
        description: 'Filter appointments by status: IN, BK, CN, RE, RS'
      responses:
        200:
          description: OK
      tags:
      - Appointments
    post:
      summary: Returns an appointment object
      description: "This end point creates a new appointment in an Initial \"IN\"
        status. \r\n\r\nA valid serviceId is required. Use GET consumer/v1/services
        to retrieve a list of your services.\r\n\r\nA valid resourceId is required
        if your calendar is a resource based calendar. Use consumer/v1/resources to
        retrieve a list of your resources.\r\n\r\nStartDateTime and EndDateTime are
        required. Use the ISO 8601 format for DateTime Timezone. e.g. 2016-10-30T9:00:00-5:00"
      operationId: ConsumerV1AppointmentsPost
      x-api-path-slug: consumerv1appointments-post
      parameters:
      - in: body
        name: appointmentIM
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Appointments
  /consumer/v1/appointments/{id}:
    get:
      summary: Returns an appointment object.
      description: "The result returned is a single appointment object. A valid id
        is required to find the appointment. \r\n\r\nFind appointment id's using the
        GET consumer/v1/appointments end point."
      operationId: ConsumerV1AppointmentsByIdGet
      x-api-path-slug: consumerv1appointmentsid-get
      parameters:
      - in: path
        name: id
        description: The id of the appointment object
      responses:
        200:
          description: OK
      tags:
      - Appointments
    delete:
      summary: Returns an appointment object
      description: "This end point deletes a booking. Only appointments in a \"IN\"
        initial status can be deleted.\r\nPast dated appointments cannot be cancelled.\r\n\r\nA
        valid appointment id is required. Use the appointmentId returned from GET
        /consumer/v1/appointments"
      operationId: ConsumerV1AppointmentsByIdDelete
      x-api-path-slug: consumerv1appointmentsid-delete
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Appointments
  /consumer/v1/appointments/{id}/book:
    put:
      summary: Returns an appointment object
      description: "This end point completes a new booking. Only appointments in the
        \"IN\" initial status can be booked.\r\nby saving all the relevant details
        of the booking.\r\n\r\nA valid appointment id is required. Use the appointmentId
        returned from POST /consumer/v1/appointments\r\n\r\nTo update appointment
        custom field values, use the GET /consumer/v1/appointments/customfields information\r\nto
        understand your definitions of custom fields and what key and values to update."
      operationId: ConsumerV1AppointmentsByIdBookPut
      x-api-path-slug: consumerv1appointmentsidbook-put
      parameters:
      - in: body
        name: appointmentBookModel
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Appointments
      - Book
  /consumer/v1/appointments/{id}/cancel:
    put:
      summary: Returns an appointment object
      description: "This end point cancels a booking or reservation. Only appointments
        in a \"BK\" booked, or \"RS\" reserved status can be cancelled.\r\nPast dated
        appointments cannot be cancelled.\r\n\r\nA valid appointment id is required.
        Use the appointmentId returned from POST /consumer/v1/appointments"
      operationId: ConsumerV1AppointmentsByIdCancelPut
      x-api-path-slug: consumerv1appointmentsidcancel-put
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Appointments
      - Cancel
  /consumer/v1/appointments/{id}/reschedule:
    put:
      summary: Returns an appointment object
      description: "This end point reschedules a booking. Only appointments in a \"BK\"
        booked status can be rescheduled.\r\nPast dated appointments cannot be cancelled.\r\n\r\nA
        valid appointment id is required. Use the appointmentId returned from GET
        /consumer/v1/appointments.\r\n\r\nThe serviceId and resourceId are optional.
        If you want your users to change the resource or service on a reschedule\r\nyou
        will have to use the regular availability endpoint rather than the reschedule
        availability end point.\r\n\r\nUse the GET /consumer/v1/availability/{id}/reschedule
        endpoint to display a list of available times\r\nfor the end user to choose
        from to reschedule the original appointment."
      operationId: ConsumerV1AppointmentsByIdReschedulePut
      x-api-path-slug: consumerv1appointmentsidreschedule-put
      parameters:
      - in: body
        name: appointmentRM
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: appointment id
      responses:
        200:
          description: OK
      tags:
      - Appointments
      - Reschedule
  /consumer/v1/appointments/customfields:
    get:
      summary: Returns a list of appointment custom field definitions
      description: "This end point returns your Appointment custom field definitions.\r\n\r\nAppointment
        custom fields are different than Customer custom fields. Appointment custom
        fields are\r\nstored with each appointment. They are used when the information
        collected during the booking is specific\r\nto a particular visit.\r\n\r\nUse
        the field, and type to determine how to update field values\r\nin PUT /consumer/v1/appointments/{id}/book"
      operationId: ConsumerV1AppointmentsCustomfieldsGet
      x-api-path-slug: consumerv1appointmentscustomfields-get
      parameters:
      - in: query
        name: locationId
        description: The id of the business location
      responses:
        200:
          description: OK
      tags:
      - Appointments
      - Customfields
  /consumer/v1/appointments/bookingfields:
    get:
      summary: ""
      description: ""
      operationId: ConsumerV1AppointmentsBookingfieldsGet
      x-api-path-slug: consumerv1appointmentsbookingfields-get
      parameters:
      - in: query
        name: locationId
      responses:
        200:
          description: OK
      tags:
      - Appointments
      - Bookingfields
  /consumer/v1/availability/{serviceId}/{startDate}/{endDate}:
    get:
      summary: Returns a list of available times.
      description: "Choose your search criteria carefully. Availability is an expensive
        call. If you search availability for all resources\r\nthen you should only
        do so for a single date. If you decide to search availability for multiple
        dates you should only do so\r\nfor a specific resource by specifying the optional
        resourceId parameter.\r\n\r\nStart and End times are specified as military
        times e.g. 800 = 8:00am, 2230 = 10:30pm. \r\nYou will only see availability
        within the boundary of your business start and end times.\r\n\r\ndayAvailability
        will return day availablility for the number of days requested from the start
        date.\r\n\r\nfirstDayAvailable only works with day availability. If set to
        true it will look for the first day available within the range specified\r\nby
        the dayAvailability parameter. The two parameters together can be a clever
        way to display availability for a week or month.\r\nTip - pass in the beginning
        of the week or month, and available times are displayed for the first available
        date if exists.\r\n\r\nYou should only specify the duration parameter if you
        let your customers choose the duration of the appointment. e.g. from a list.\r\n\r\nThe
        tz parameter allows you to select a suitable timezone for the customer to
        book in. Your app should be timezone aware if you \r\nuse this option. The
        requested timezone is specified as an offset(plus or minus) from GMT time."
      operationId: ConsumerV1AvailabilityByServiceIdByStartDateByEndDateGet
      x-api-path-slug: consumerv1availabilityserviceidstartdateenddate-get
      parameters:
      - in: query
        name: dayAvailability
        description: Return day availability for number of days specified
      - in: query
        name: duration
        description: Duration of the service if different than the default
      - in: path
        name: endDate
        description: End Date for availability search
      - in: query
        name: endTime
        description: End Time for availability search
      - in: query
        name: firstDayAvailable
        description: Return available times for the first available day
      - in: query
        name: locationId
        description: The id of the business location
      - in: query
        name: resourceGroupId
        description: Resource Group Id for availability search
      - in: query
        name: resourceId
        description: Resource Id for availability search
      - in: query
        name: resourceIds
        description: Comma separated Resource Ids for availability search
      - in: path
        name: serviceId
        description: Service Id for availability search
      - in: path
        name: startDate
        description: Start Date for availability search
      - in: query
        name: startTime
        description: Start Time for availability search
      - in: query
        name: tzOffset
        description: Request timezone offset to view availability
      responses:
        200:
          description: OK
      tags:
      - Availability
      - ServiceId
      - StartDate
      - EndDate
  /consumer/v1/availability/{serviceId}/{startDate}/{endDate}/days:
    get:
      summary: Returns a list of available days.
      description: "This end point is used to show day level availability. For example
        if the business is closed, or there is a public holiday.\r\n\r\nDay level
        availability is a good way to restrict your choices of dates in your app and
        improve usability."
      operationId: ConsumerV1AvailabilityByServiceIdByStartDateByEndDateDaysGet
      x-api-path-slug: consumerv1availabilityserviceidstartdateenddatedays-get
      parameters:
      - in: path
        name: endDate
        description: End Date for availability search
      - in: query
        name: locationId
        description: The id of the business location
      - in: query
        name: resourceId
        description: Resource Id to filter on
      - in: path
        name: serviceId
        description: Service Id for availability search
      - in: path
        name: startDate
        description: Start Date for availability search
      - in: query
        name: tzOffset
        description: Request timezone offset to view availability
      responses:
        200:
          description: OK
      tags:
      - Availability
      - ServiceId
      - StartDate
      - EndDate
      - Days
  /consumer/v1/availability/{serviceId}/{startDate}/{endDate}/unavailable:
    get:
      summary: Returns a list of unavailable times.
      description: This endpoint is used to show unavailable times and provides information
        why the timeslot is unavailable.
      operationId: ConsumerV1AvailabilityByServiceIdByStartDateByEndDateUnavailableGet
      x-api-path-slug: consumerv1availabilityserviceidstartdateenddateunavailable-get
      parameters:
      - in: query
        name: duration
        description: Duration of the service if different than the default
      - in: path
        name: endDate
        description: End Date for unavailable time search
      - in: query
        name: locationId
        description: The id of the business location
      - in: query
        name: resourceId
        description: Resource Id to filter on
      - in: path
        name: serviceId
        description: Service Id for availability search
      - in: path
        name: startDate
        description: Start Date for unavailable time search
      - in: query
        name: tzOffset
        description: Request timezone offset to view unavailable times
      responses:
        200:
          description: OK
      tags:
      - Availability
      - ServiceId
      - StartDate
      - EndDate
      - Unavailable
  /consumer/v1/availability/{appointmentId}/reschedule:
    get:
      summary: Returns a list of available times.
      description: "This end point is used to find availability for the purpose of
        rescheduling an appointment.\r\nAvailability defaults to the serviceId, resourceId
        and timezone from the original appointment.\r\nAfter choosing from the availability,
        you can call the appointment reschedule endpoint."
      operationId: ConsumerV1AvailabilityByAppointmentIdRescheduleGet
      x-api-path-slug: consumerv1availabilityappointmentidreschedule-get
      parameters:
      - in: path
        name: appointmentId
        description: Appointment Id of the original appointment being rescheduled
      - in: query
        name: tzOffset
        description: Request timezone offset to view availability
      responses:
        200:
          description: OK
      tags:
      - Availability
      - AppointmentId
      - Reschedule
  /consumer/v1/customers:
    get:
      summary: Returns a list of customers.
      description: "The results are returned in pages. Use the offset and limit parameters
        to control the page start and size. Default offset is 0, and limit is 20.\r\nUse
        the other query parameters to optionally filter the results list."
      operationId: ConsumerV1CustomersGet
      x-api-path-slug: consumerv1customers-get
      parameters:
      - in: query
        name: deleted
        description: Filter customers by deleted status
      - in: query
        name: email
        description: Filter customers by email address
      - in: query
        name: groupId
        description: Filter customers by group
      - in: query
        name: lastname
        description: Search customers by lastname
      - in: query
        name: limit
        description: Page limit, default 20
      - in: query
        name: locationId
        description: The id of the business location
      - in: query
        name: offset
        description: Starting row of page, default 0
      responses:
        200:
          description: OK
      tags:
      - Customers
    post:
      summary: Creates a new customer object.
      description: "Use this endpoint to create a new customer. If not specified the
        business location id defaults to the first location in the company.\r\nEmail
        Address and a lastname are required for creating a new customer."
      operationId: ConsumerV1CustomersPost
      x-api-path-slug: consumerv1customers-post
      parameters:
      - in: body
        name: customerIM
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Customers
  /consumer/v1/customers/{id}:
    get:
      summary: Returns a customer object.
      description: "The result returned is a single customer object. An id is required
        to find the customer. Find customer id's using either the GET consumer/v1/customers
        end point,\r\nor the GET consumer/v1/appointments end point. A customer object
        is automatically created with the first booking if it doesn't already exist."
      operationId: ConsumerV1CustomersByIdGet
      x-api-path-slug: consumerv1customersid-get
      parameters:
      - in: path
        name: id
        description: The id of the customer object
      responses:
        200:
          description: OK
      tags:
      - Customers
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
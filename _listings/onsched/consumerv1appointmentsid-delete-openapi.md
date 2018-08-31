---
swagger: "2.0"
x-collection-name: OnSched
x-complete: 0
info:
  title: OnSched Returns an appointment object
  description: "This end point deletes a booking. Only appointments in a \"IN\" initial
    status can be deleted.\r\nPast dated appointments cannot be cancelled.\r\n\r\nA
    valid appointment id is required. Use the appointmentId returned from GET /consumer/v1/appointments"
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
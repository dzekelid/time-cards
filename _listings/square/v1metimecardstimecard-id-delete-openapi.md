---
swagger: "2.0"
x-collection-name: Square
x-complete: 0
info:
  title: Square Connect API Deletes a timecard. Deleted timecards are still accessible
    from Connect API endpoints, but the value of their deleted field is set to true.
    See Handling deleted timecards for more information.
  description: Deletes a timecard. Deleted timecards are still accessible from Connect
    API endpoints, but the value of their deleted field is set to true. See Handling
    deleted timecards for more information.
  termsOfService: https://connect.squareup.com/tos
  contact:
    name: Square Developer Platform
    url: https://squareup.com/developers
    email: developers@squareup.com
  version: "2.0"
host: connect.squareup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/me/timecards:
    get:
      summary: Provides summary information for all of a business's employee timecards.
      description: Provides summary information for all of a business's employee timecards.
      operationId: ListTimecards
      x-api-path-slug: v1metimecards-get
      parameters:
      - in: query
        name: batch_token
        description: A pagination cursor to retrieve the next set of results for youroriginal
          query to the endpoint
      - in: query
        name: begin_clockin_time
        description: If filtering results by their clockin_time field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: begin_clockout_time
        description: If filtering results by their clockout_time field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: begin_updated_at
        description: If filtering results by their updated_at field, the beginning
          of the requested reporting period, in ISO 8601 format
      - in: query
        name: deleted
        description: If true, only deleted timecards are returned
      - in: query
        name: employee_id
        description: If provided, the endpoint returns only timecards for the employee
          with the specified ID
      - in: query
        name: end_clockin_time
        description: If filtering results by their clockin_time field, the end of
          the requested reporting period, in ISO 8601 format
      - in: query
        name: end_clockout_time
        description: If filtering results by their clockout_time field, the end of
          the requested reporting period, in ISO 8601 format
      - in: query
        name: end_updated_at
        description: If filtering results by their updated_at field, the end of the
          requested reporting period, in ISO 8601 format
      - in: query
        name: limit
        description: The maximum integer number of employee entities to return in
          a single response
      - in: query
        name: order
        description: The order in which timecards are listed in the response, based
          on their created_at field
      responses:
        200:
          description: OK
      tags:
      - Provides
      - Summary
      - Information
      - Of
      - Businesss
      - Employee
      - Timecards
    post:
      summary: Creates a timecard for an employee. Each timecard corresponds to a
        single shift.
      description: Creates a timecard for an employee. Each timecard corresponds to
        a single shift.
      operationId: CreateTimecard
      x-api-path-slug: v1metimecards-post
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Timecardan
      - Employee
      - ""
      - Each
      - Timecard
      - Corresponds
      - To
      - Single
      - Shift
  /v1/me/timecards/{timecard_id}:
    delete:
      summary: Deletes a timecard. Deleted timecards are still accessible from Connect
        API endpoints, but the value of their deleted field is set to true. See Handling
        deleted timecards for more information.
      description: Deletes a timecard. Deleted timecards are still accessible from
        Connect API endpoints, but the value of their deleted field is set to true.
        See Handling deleted timecards for more information.
      operationId: DeleteTimecard
      x-api-path-slug: v1metimecardstimecard-id-delete
      parameters:
      - in: path
        name: timecard_id
        description: The ID of the timecard to delete
      responses:
        200:
          description: OK
      tags:
      - S
      - Timecard
      - ""
      - D
      - Timecards
      - Are
      - Still
      - Accessible
      - From
      - Connect
      - Endpoints
      - ""
      - But
      - Value
      - Of
      - Their
      - Deleted
      - Field
      - Is
      - Set
      - To
      - "True"
      - ""
      - See
      - Handling
      - Deleted
      - Timecardsmore
      - Information
    put:
      summary: Modifies a timecard's details. This creates an API_EDIT event for the
        timecard. You can view a timecard's event history with the List Timecard Events
        endpoint.
      description: Modifies a timecard's details. This creates an API_EDIT event for
        the timecard. You can view a timecard's event history with the List Timecard
        Events endpoint.
      operationId: UpdateTimecard
      x-api-path-slug: v1metimecardstimecard-id-put
      parameters:
      - in: body
        name: body
        description: An object containing the fields to POST for the request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: timecard_id
        description: TThe ID of the timecard to modify
      responses:
        200:
          description: OK
      tags:
      - Modifies
      - Timecards
      - Details
      - ""
      - This
      - Creates
      - EDIT
      - Eventthe
      - Timecard
      - ""
      - You
      - Can
      - View
      - Timecards
      - Event
      - History
      - List
      - Timecard
      - Events
      - Endpoint
    get:
      summary: Provides the details for a single timecard.
      description: Provides the details for a single timecard.
      operationId: RetrieveTimecard
      x-api-path-slug: v1metimecardstimecard-id-get
      parameters:
      - in: path
        name: timecard_id
        description: The timecards ID
      responses:
        200:
          description: OK
      tags:
      - Provides
      - Detailsa
      - Single
      - Timecard
  /v1/me/timecards/{timecard_id}/events:
    get:
      summary: Provides summary information for all events associated with a particular
        timecard.
      description: Provides summary information for all events associated with a particular
        timecard.
      operationId: ListTimecardEvents
      x-api-path-slug: v1metimecardstimecard-idevents-get
      parameters:
      - in: path
        name: timecard_id
        description: The ID of the timecard to list events for
      responses:
        200:
          description: OK
      tags:
      - Provides
      - Summary
      - Information
      - Events
      - Associated
      - Particular
      - Timecard
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
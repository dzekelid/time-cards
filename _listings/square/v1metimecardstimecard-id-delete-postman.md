{
  "info": {
    "name": "Square Connect API Deletes a timecard. Deleted timecards are still accessible from Connect API endpoints, but the value of their deleted field is set to true. See Handling deleted timecards for more information.",
    "_postman_id": "19651680-3e16-4194-ae64-521cfee49d95",
    "description": "Deletes a timecard. Deleted timecards are still accessible from Connect API endpoints, but the value of their deleted field is set to true. See Handling deleted timecards for more information.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "S",
      "item": [
        {
          "id": "411a927f-ce22-4077-808d-eed6f5acc524",
          "name": "DeleteTimecard",
          "request": {
            "url": {
              "protocol": "http",
              "host": "connect.squareup.com",
              "path": [
                "v1/me/timecards/:timecard_id"
              ],
              "variable": [
                {
                  "id": "timecard_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a timecard. Deleted timecards are still accessible from Connect API endpoints, but the value of their deleted field is set to true. See Handling deleted timecards for more information."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e4be91c9-1c69-4de5-a4dd-f523ef1d216f"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "reverb Post My Negotiations Decline",
    "_postman_id": "dde5a839-5dad-4eed-8605-a18269546528",
    "description": "Post my negotiations decline.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "My",
      "item": [
        {
          "id": "5b37dd6c-c43a-4c39-aa32-b810ea501949",
          "name": "postMyNegotiationsDecline",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.reverb.com",
              "path": [
                "api",
                "my/negotiations/:id/decline"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Post my negotiations decline."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b8af8991-631c-46c3-abfc-67f2f83f4a22"
            }
          ]
        }
      ]
    }
  ]
}
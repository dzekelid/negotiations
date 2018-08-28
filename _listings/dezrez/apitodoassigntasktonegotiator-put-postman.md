{
  "info": {
    "name": "Dezrez Assign a task to a negotiator by its Id.",
    "_postman_id": "73fc3356-07e6-4be7-938c-a3be9a94e658",
    "description": "Assign a task to a negotiator by its id..",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assign",
      "item": [
        {
          "id": "cab407e2-b704-4ab5-9b5c-75813626ea02",
          "name": "DefaultToDo_AssignLeadsToOwningNegotiatorsBytoDoId",
          "request": {
            "url": "http://api.dezrez.com/api/todo/assignleadstoowningnegotiators?toDoId=%7B%7D",
            "method": "PUT",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Assign inboundlead todos to the owning negotiators of the property.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b1e64d1c-38cc-4ad5-bd6d-0d355fa63afd"
            }
          ]
        },
        {
          "id": "f798d4e7-27ba-428b-8632-61104b1e5035",
          "name": "DefaultToDo_AssignTaskToNegotiatorBytaskIdBynegotiatorId",
          "request": {
            "url": "http://api.dezrez.com/api/todo/assigntasktonegotiator?negotiatorId=%7B%7D&taskId=%7B%7D",
            "method": "PUT",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Assign a task to a negotiator by its id.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f8172a2a-cabc-4c52-8981-17fb149ff0fb"
            }
          ]
        }
      ]
    }
  ]
}
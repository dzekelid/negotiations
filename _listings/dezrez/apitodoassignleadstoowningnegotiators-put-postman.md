{
  "info": {
    "name": "Dezrez Assign InboundLead Todos to the owning Negotiators of the property.",
    "_postman_id": "e615574f-7268-4b74-97f6-dc2194dd5c80",
    "description": "Assign inboundlead todos to the owning negotiators of the property..",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Assign",
      "item": [
        {
          "id": "9c3ccb0e-bc9b-453e-97bc-06625ebe75b7",
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
              "id": "3ac90264-9675-4a0b-9bd5-515bc8b7eb6f"
            }
          ]
        }
      ]
    }
  ]
}
{
  "info": {
    "name": "Google Play Get State Keys",
    "_postman_id": "bea507f2-a0cc-426c-94c2-617b0da45a8b",
    "description": "Lists all the states keys, and optionally the state data.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application State",
      "item": [
        {
          "id": "e34feece-072c-45ff-a6cd-9401b7839b7e",
          "name": "appstate.states.list",
          "request": {
            "url": "http://example.com/api/states?includeData=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all the states keys, and optionally the state data."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bf9791c4-508d-4939-9654-74a105141c34"
            }
          ]
        }
      ]
    }
  ]
}
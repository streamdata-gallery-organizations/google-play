{
  "info": {
    "name": "Google Play Delete State Key",
    "_postman_id": "572f1536-3098-41b0-bea9-7728fc270670",
    "description": "Deletes a key and the data associated with it. The key is removed and no longer counts against the key quota. Note that since this method is not safe in the face of concurrent modifications, it should only be used for development and testing purposes. Invoking this method in shipping code can result in data loss and data corruption.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application State",
      "item": [
        {
          "id": "77308d81-a3c2-4ced-abe5-4f013b87a98f",
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
              "id": "ce4d1f4c-0e4e-4146-9573-e699918c6fe2"
            }
          ]
        },
        {
          "id": "d03da12d-e409-4f49-beee-7f1b9aa1bce5",
          "name": "appstate.states.delete",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "states/:stateKey"
              ],
              "variable": [
                {
                  "id": "stateKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a key and the data associated with it. The key is removed and no longer counts against the key quota. Note that since this method is not safe in the face of concurrent modifications, it should only be used for development and testing purposes. Invoking this method in shipping code can result in data loss and data corruption."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "68afc114-c95b-4ddc-803d-5bd86e04ada2"
            }
          ]
        }
      ]
    }
  ]
}
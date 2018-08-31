{
  "info": {
    "name": "Google Play Get State Key",
    "_postman_id": "95419992-28fc-4032-ac76-78b498c49b90",
    "description": "Retrieves the data corresponding to the passed key. If the key does not exist on the server, an HTTP 404 will be returned.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application State",
      "item": [
        {
          "id": "3b12a745-c529-4116-a93e-2890a5e51ef2",
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
              "id": "832f985a-e17a-491c-80f5-d59fd560d625"
            }
          ]
        },
        {
          "id": "24db8157-117b-4633-b1ca-f4e52cf8be7a",
          "name": "appstate.states.get",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the data corresponding to the passed key. If the key does not exist on the server, an HTTP 404 will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a9e32652-e3e2-4388-b1b2-28acb1b68a2c"
            }
          ]
        },
        {
          "id": "819056c6-efc2-45c0-a6cb-9a27d031ba47",
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
              "id": "684a1f0c-8b96-4104-b143-5228beb3707d"
            }
          ]
        }
      ]
    }
  ]
}
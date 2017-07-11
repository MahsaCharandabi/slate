# Tasks

## The task object

> Definition:

```curl

```
> Example Request:

```curl

```
> Example Response:

```json

```

## Create a task

> Definition:

```curl
POST http://echon.io/v1/tasks
```
> Example Request:

```curl
curl -X POST \
  http://echon.io/v1/tasks \
  -H 'authorization: bearer 1208d53e433242edb1e8f45d351506a7gbNMGn45TNxNsv2x9cPYvRTgvTiVUh9Idnju1BJQCbkhjAri9u2xlFbFVtMs0g9WoWLrUscPPvOIX6aECKWJ6luN5tLeKlXKnitsIsJOvwR78QDz56VItGgZDapKrIGSyvSVkaePYnUOPVZKOQ9dBd4yogIp2j3yUw0aLuJ9bTFhJ93TjrKKA0xrJEGbpLZUlHTAyJ9VlJPdXT4JbL7GLBMo1tVgrCd6' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: c45095c4-34a3-5555-2b7a-b307c7b0659b' \
  -d 'organizationId=6ab965cb-a242-4b9f-a868-0a946a2c3cf5&creatorOperatorId=d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34&title=Send a copy of contract to customer.'
```
> Example Response:

```json
{
    "id": "7db5823a-19c4-4a56-be32-3af5e8d39f90",
    "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
    "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "customerId": null,
    "departmentId": null,
    "operatorId": null,
    "title": "Send a copy of contract to customer.",
    "description": null,
    "dueDate": null,
    "taskDoneTimelineEventId": null,
    "done": false,
    "priority": 1
}
```

## Retrieve a task

> Definition:

```curl
GET http://echon.io/v1/tasks/{TASK_ID}
```
> Example Request:

```curl
curl -X GET \
  http://echon.io/v1/tasks/c5729313-94c6-4ef6-87aa-68b500381e48 \
  -H 'authorization: bearer de0890b96e9a4e09a55a290e51efe99dBqAp6volwZySaiNDgY3muwkOPKP7XgrVfvRvzD6MEBUDOi4aJEhbH9ajdo6l6dSnfttR5Jz3mLySzqBxM74vt1rJYtFltK5NMeG4jClTHVsvHQM0JTtPDj97UoIM7GGV9GpOtRjUPXGfL5tUShqzD6gGSSgpvGJPvxuhlgzr0t2AztVG5nRb8a1DwUdVypICNt2WjU6x8PT2gml1PQl8guUtJAR16yd6' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: e7c2d4ef-f220-8f7b-a3b7-af7e5f84b5d4' \
  -d 'identity=&contacts=&type=corporate'
```
> Example Response:

```json
{
    "id": "c5729313-94c6-4ef6-87aa-68b500381e48",
    "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
    "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "customerId": null,
    "departmentId": null,
    "operatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "title": "ارسال مرسوله",
    "description": "",
    "dueDate": null,
    "taskDoneTimelineEventId": null,
    "done": false,
    "priority": 1
}
```

## Check a task completed

> Definition:

```curl

```
> Example Request:

```curl

```
> Example Response:

```json

```

## Undo a task complete

> Definition:

```curl

```
> Example Request:

```curl

```
> Example Response:

```json

```

## Update dueDate of a task

> Definition:

```curl

```
> Example Request:

```curl

```
> Example Response:

```json

```

## Update assignee of a task

> Definition:

```curl

```
> Example Request:

```curl

```
> Example Response:

```json

```

## Update details of a task

> Definition:

```curl

```
> Example Request:

```curl

```
> Example Response:

```json

```


## List all tasks of an organization
> Definition

```curl
GET http://echon.io/v1/tasks?scope=organization
```

> Example Request

```curl
curl -X GET \
  'http://echon.io/v1/tasks?scope=organization' \
  -H 'authorization: bearer 48ea35ed61524b86b1fba663a24d3457xR24U5bly1xuartnBz1vrnz7MVpIfZbUxZQ4wnB15CKrhhJwGUE6DfZv21GNKN108EY4unimrEMDJ4qSKqNwCV55M1qfvJ8Cy4EN1dRMAwGIQQ8YWBnyTOP4Wk8zyRWHi2Q4snt0KpHOdSJHgydiHwsXTx4ckD8S7ENo5P8dkzkp1ZkKittQqX2nrw6IeVkmBj9f9p3OLjcsQWVROrjgA6EsoO6VBkU1' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 3ff83cbf-188a-bb62-c693-a4c532cc7038' \
  -d 'identity=&contacts=&type=corporate'
```

> Example Response

```json
[
  {
      "id": "9c24e53c-8403-45a2-bcd6-2e33607d30ce",
      "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
      "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
      "customerId": null,
      "departmentId": null,
      "operatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
      "title": "ارسال مرسوله۲",
      "description": "",
      "dueDate": null,
      "taskDoneTimelineEventId": null,
      "done": false,
      "priority": 2
  },
  {
      "id": "c5729313-94c6-4ef6-87aa-68b500381e48",
      "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
      "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
      "customerId": null,
      "departmentId": null,
      "operatorId": null,
      "title": "ارسال مرسوله",
      "description": "",
      "dueDate": null,
      "taskDoneTimelineEventId": null,
      "done": false,
      "priority": 1
  }
]

```

## List all tasks of an operator

> Definition:

```curl
GET http://echon.io/v1/tasks?scope=operator
```

> Example Request:

```curl
curl -X GET \
  'http://echon.io/v1/tasks?scope=operator' \
  -H 'authorization: bearer 48ea35ed61524b86b1fba663a24d3457xR24U5bly1xuartnBz1vrnz7MVpIfZbUxZQ4wnB15CKrhhJwGUE6DfZv21GNKN108EY4unimrEMDJ4qSKqNwCV55M1qfvJ8Cy4EN1dRMAwGIQQ8YWBnyTOP4Wk8zyRWHi2Q4snt0KpHOdSJHgydiHwsXTx4ckD8S7ENo5P8dkzkp1ZkKittQqX2nrw6IeVkmBj9f9p3OLjcsQWVROrjgA6EsoO6VBkU1' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/x-www-form-urlencoded' \
  -H 'postman-token: 8d0325c1-af2f-ff00-a888-dc972ff90653' \
  -d 'identity=&contacts=&type=corporate'
```

> Example Response:

```json
[
  {
    "id": "9c24e53c-8403-45a2-bcd6-2e33607d30ce",
    "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
    "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "customerId": null,
    "departmentId": null,
    "operatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "title": "ارسال مرسوله۲",
    "description": "",
    "dueDate": null,
    "taskDoneTimelineEventId": null,
    "done": false,
    "priority": 2
  },
  {
    "id": "c5729313-94c6-4ef6-87aa-68b500381e48",
    "organizationId": "6ab965cb-a242-4b9f-a868-0a946a2c3cf5",
    "creatorOperatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "customerId": null,
    "departmentId": null,
    "operatorId": "d08bcb06-5c2b-4cb1-b6de-e3afb7d3ae34",
    "title": "ارسال مرسوله",
    "description": "",
    "dueDate": null,
    "taskDoneTimelineEventId": null,
    "done": false,
    "priority": 1
  }
]
```

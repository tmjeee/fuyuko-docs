---
description: Get job details by it's id
---

# GET-job-details-by-id

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/job/:jobId/details/:lastLogId" %}
{% api-method-summary %}
Get job details
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="jobId" type="number" required=true %}
Job Id
{% endapi-method-parameter %}

{% api-method-parameter name="lastLogId" type="string" %}
Job's last Log Id to starts it's log off.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "job": {
        "id": 1,
        "name": "BulkEditJob-05bb9170-8ded-4fb7-9023-6fff52804a32",
        "description": "Bulk Edit Job (05bb9170-8ded-4fb7-9023-6fff52804a32) for viewId 1",
        "status": "ENABLED",
        "creationDate": "2020-03-16T03:57:23.000Z",
        "progress": "COMPLETED",
        "lastUpdate": "2020-03-16T03:57:23.000Z"
    },
    "logs": [
        {
            "id": 1,
            "level": "INFO",
            "message": "Start running bulk edit job (jobId: 1)",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 2,
            "level": "INFO",
            "message": "Working on item 1",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 3,
            "level": "INFO",
            "message": "Changed attribute 2 for item 1 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 4,
            "level": "INFO",
            "message": "Working on item 2",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 5,
            "level": "INFO",
            "message": "Changed attribute 2 for item 2 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 6,
            "level": "INFO",
            "message": "Working on item 4",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 7,
            "level": "INFO",
            "message": "Changed attribute 2 for item 4 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 8,
            "level": "INFO",
            "message": "Working on item 7",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 9,
            "level": "INFO",
            "message": "Changed attribute 2 for item 7 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 10,
            "level": "INFO",
            "message": "Working on item 5",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 11,
            "level": "INFO",
            "message": "Working on item 8",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 12,
            "level": "INFO",
            "message": "Changed attribute 2 for item 5 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 13,
            "level": "INFO",
            "message": "Changed attribute 2 for item 8 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 14,
            "level": "INFO",
            "message": "Working on item 9",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 15,
            "level": "INFO",
            "message": "Changed attribute 2 for item 9 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 16,
            "level": "INFO",
            "message": "Working on item 6",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 17,
            "level": "INFO",
            "message": "Changed attribute 2 for item 6 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 18,
            "level": "INFO",
            "message": "Working on item 3",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 19,
            "level": "INFO",
            "message": "Changed attribute 2 for item 3 to [object Object]",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        },
        {
            "id": 20,
            "level": "INFO",
            "message": "Done running bulk edit job (jobId: 1)",
            "creationDate": "2020-03-16T03:57:23.000Z",
            "lastUpdate": "2020-03-16T03:57:23.000Z"
        }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




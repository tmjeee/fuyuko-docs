---
description: Get all data export artifacts
---

# GET-all-data-export-artifacts

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/data-export-artifacts" %}
{% api-method-summary %}
Get all data export artifacts
{% endapi-method-summary %}

{% api-method-description %}
Get all export artifacts.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token
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
  "payload": [
    {
        "view": {
            "id": 2,
            "name": "Test View 2",
            "description": "Test View 2 Description",
            "creationDate": "2020-03-23T06:51:24.000Z",
            "lastUpdate": "2020-03-23T06:51:24.000Z"
        },
        "id": 5,
        "name": "price-data-export-job-3566e567-e601-434e-9807-7cfcf0c36cf6",
        "type": "PRICE",
        "creationDate": "2020-03-25T09:43:29.000Z",
        "lastUpdate": "2020-03-25T09:43:29.000Z",
        "fileName": "price-data-export-job-3566e567-e601-434e-9807-7cfcf0c36cf6",
        "mimeType": "text/csv",
        "size": 549
    },
    {
        "view": {
            "id": 2,
            "name": "Test View 2",
            "description": "Test View 2 Description",
            "creationDate": "2020-03-23T06:51:24.000Z",
            "lastUpdate": "2020-03-23T06:51:24.000Z"
        },
        "id": 4,
        "name": "item-data-export-job-dba4a4fd-74df-4968-ac70-e658617da3ba",
        "type": "ITEM",
        "creationDate": "2020-03-25T09:40:08.000Z",
        "lastUpdate": "2020-03-25T09:40:08.000Z",
        "fileName": "item-data-export-job-dba4a4fd-74df-4968-ac70-e658617da3ba",
        "mimeType": "text/csv",
        "size": 525
    },
    {
        "view": {
            "id": 2,
            "name": "Test View 2",
            "description": "Test View 2 Description",
            "creationDate": "2020-03-23T06:51:24.000Z",
            "lastUpdate": "2020-03-23T06:51:24.000Z"
        },
        "id": 3,
        "name": "attribute-data-export-job-97e7ab1a-9f7d-4142-a476-1f5062df9cb4",
        "type": "ATTRIBUTE",
        "creationDate": "2020-03-25T09:36:18.000Z",
        "lastUpdate": "2020-03-25T09:36:18.000Z",
        "fileName": "attribute-data-export-job-97e7ab1a-9f7d-4142-a476-1f5062df9cb4",
        "mimeType": "text/csv",
        "size": 922
    },
    {
        "view": {
            "id": 1,
            "name": "Test View 1",
            "description": "Test View 1 Description",
            "creationDate": "2020-03-23T06:51:24.000Z",
            "lastUpdate": "2020-03-23T06:51:24.000Z"
        },
        "id": 2,
        "name": "item-data-export-job-f7085552-a20f-465e-83a7-7d69e8cf4ad2",
        "type": "ITEM",
        "creationDate": "2020-03-23T11:59:07.000Z",
        "lastUpdate": "2020-03-23T11:59:07.000Z",
        "fileName": "item-data-export-job-f7085552-a20f-465e-83a7-7d69e8cf4ad2",
        "mimeType": "text/csv",
        "size": 549
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




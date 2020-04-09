---
description: Schedule Item data export
---

# POST-schedule-item-data-export

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/export/items" %}
{% api-method-summary %}
Schedule item data export
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="string" required=true %}
View Id
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
    "id": 7,
    "name": "item-data-export-job-dba4a4fd-74df-4968-ac70-e658617da3ba",
    "description": "item-data-export-job-dba4a4fd-74df-4968-ac70-e658617da3ba description",
    "creationDate": "2020-03-25T09:40:08.000Z",
    "lastUpdate": "2020-03-25T09:40:08.000Z",
    "status": "ENABLED",
    "progress": "SCHEDULED"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




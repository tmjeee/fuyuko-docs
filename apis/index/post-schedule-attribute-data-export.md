---
description: Schedule attribute data export
---

# POST-schedule-attribute-data-export

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/export/attributes" %}
{% api-method-summary %}
Schedule attribute data export
{% endapi-method-summary %}

{% api-method-description %}
Schedule attribute data export.
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
    "id": 6,
    "name": "attribute-data-export-job-97e7ab1a-9f7d-4142-a476-1f5062df9cb4",
    "description": "attribute-data-export-job-97e7ab1a-9f7d-4142-a476-1f5062df9cb4 description",
    "creationDate": "2020-03-25T09:36:18.000Z",
    "lastUpdate": "2020-03-25T09:36:18.000Z",
    "status": "ENABLED",
    "progress": "SCHEDULED"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




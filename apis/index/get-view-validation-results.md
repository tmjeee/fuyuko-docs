---
description: Get view validation results
---

# GET-view-validation-result

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/validation/:validationId" %}
{% api-method-summary %}
Get view validation result
{% endapi-method-summary %}

{% api-method-description %}
Get View's validation result.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="validationId" type="number" required=true %}
Validation Id
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
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "id": 1,
    "viewId": 1,
    "name": "test view1 vaslidation",
    "description": "asdsdsd",
    "progress": "COMPLETED",
    "creationDate": "2020-03-25T13:42:20.000Z",
    "lastUpdate": "2020-03-25T13:42:22.000Z",
    "logResult": {
        "batchFirstValidationLogId": 31495,
        "batchLastValidationLogId": 31594,
        "batchTotal": 30972,
        "progress": "COMPLETED",
        "max": 31594,
        "min": 623,
        "batchSize": 100,
        "batchHasMoreAfter": false,
        "batchHasMoreBefore": true,
        "logs": [
            {
                "id": 1,
                "level": "INFO",
                "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Running Predefined Rules validations for viewId 1 validationId 1",
                "creationDate": "2020-03-25T13:42:20.000Z"
            },
            {
                "id": 2,
                "level": "INFO",
                "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved validation for validationId 1",
                "creationDate": "2020-03-25T13:42:20.000Z"
            },
            ...
        ]
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




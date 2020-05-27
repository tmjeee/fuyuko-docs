---
description: Get rule by view
---

# GET-rule-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/rule/:ruleId" %}
{% api-method-summary %}
Get rule by view
{% endapi-method-summary %}

{% api-method-description %}
Get rules in a view.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="ruleId" type="number" required=true %}
Rule Id
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
    "id": 1,
    "name": "Rule #1",
    "status": "ENABLED",
    "description": "Rule #1 Description",
    "validateClauses": [
        {
            "id": 1,
            "attributeId": 1,
            "attributeName": "string attribute",
            "attributeType": "string",
            "operator": "eq",
            "condition": [
                {
                    "type": "string",
                    "value": "val string 1"
                },
                {
                    "type": "string",
                    "value": "val string 2"
                }
            ]
        }
    ],
    "whenClauses": [
        {
            "id": 1,
            "attributeId": 2,
            "attributeName": "text attribute",
            "attributeType": "text",
            "operator": "not eq",
            "condition": [
                {
                    "type": "text",
                    "value": "val text 1"
                },
                {
                    "type": "text",
                    "value": "val text 2"
                }
            ]
        }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




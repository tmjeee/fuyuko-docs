# GET-pricing-structures-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/pricingStructures" %}
{% api-method-summary %}
Get Pricing Structures By View
{% endapi-method-summary %}

{% api-method-description %}
Get all pricing structures in a view.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View ID
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
    "message": "Pricing Structures retrieved",
    "payload": [
        {
            "id": 1,
            "viewId": 1,
            "lastUpdate": "2020-04-16T00:37:09.000Z",
            "description": "Pricing Structure #1 Description",
            "creationDate": "2020-04-16T00:37:09.000Z",
            "name": "Pricing Structure #1"
        },
        {
            "id": 2,
            "viewId": 1,
            "lastUpdate": "2020-04-16T00:37:09.000Z",
            "description": "Pricing Structure #2 Description",
            "creationDate": "2020-04-16T00:37:09.000Z",
            "name": "Pricing Structure #2"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




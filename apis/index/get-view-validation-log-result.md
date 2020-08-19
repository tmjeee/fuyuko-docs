# GET-view-validation-log-result

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/validation/:validationId/order/:order/limit/:limit" %}
{% api-method-summary %}
Get view validation log result
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=false %}
viewId
{% endapi-method-parameter %}

{% api-method-parameter name="validationId" type="number" required=false %}
validationId
{% endapi-method-parameter %}

{% api-method-parameter name="validationLogId" type="number" required=false %}
validationLogId
{% endapi-method-parameter %}

{% api-method-parameter name="order" type="string" required=false %}
"before" or "after"
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" %}
limit
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
JWT authentication token
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
    "message": "Validation log result retrieved",
    "payload": {
        "batchFirstValidationLogId": 124411,
        "batchLastValidationLogId": 124510,
        "batchTotal": 30972,
        "progress": "COMPLETED",
        "max": 124510,
        "min": 93539,
        "batchSize": 100,
        "batchHasMoreAfter": false,
        "batchHasMoreBefore": true,
        "logs": [
            {
                "id": 124411,
                "level": "INFO",
                "message": "[validationId=5]\n             [itemId=2076]\n             [attributeId=31] \n             - Validated current ValidateClause result is [true] overall ValidateClause result is [true] for ValidateClause 17 \n                           (attributeId 31 attributeName Year \n                           validateClause condition  \n                           op not empty \n                           against itemValueTypes )\n                           for itemId 2076 against ruleId 17 in viewId 5",
                "creationDate": "2020-08-18T12:54:16.000Z"
            },
            ...
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




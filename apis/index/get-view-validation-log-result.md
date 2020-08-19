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
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




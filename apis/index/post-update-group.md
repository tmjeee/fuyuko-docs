# POST-update-group

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/group" %}
{% api-method-summary %}
Add or Update Group
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
Group Id, -1 for new group, otherwise group Id of group for update
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Group name
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
Group description
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "Group xxxxx-gggg-group updated"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




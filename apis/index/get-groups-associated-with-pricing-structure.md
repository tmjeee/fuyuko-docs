# GET-groups-associated-with-pricing-structure

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricing-structure/:pricingStrcutureId/groups-associated/:groupName" %}
{% api-method-summary %}
Get Groups associated with pricing structure
{% endapi-method-summary %}

{% api-method-description %}
Get groups linked to a pricing structure.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pricingStructureId" type="number" required=true %}
Pricing Structure Id
{% endapi-method-parameter %}

{% api-method-parameter name="groupName" type="string" %}
Group Name to search for
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
    "message": "successfully retrieved group",
    "payload": [
        {
            "id": 3,
            "name": "ADMIN Group",
            "isSystem": 1,
            "description": "Group with VIEW & EDIT & PARTNER & ADMIN roles",
            "status": "ENABLED",
            "roles": [
                {
                    "id": 1,
                    "name": "VIEW",
                    "description": "VIEW Role"
                },
                {
                    "id": 2,
                    "name": "EDIT",
                    "description": "EDIT Role"
                },
                {
                    "id": 3,
                    "name": "ADMIN",
                    "description": "ADMIN Role"
                },
                {
                    "id": 4,
                    "name": "PARTNER",
                    "description": "PARTNER Role"
                }
            ]
        },
        {
            "id": 4,
            "name": "PARTNER Group",
            "isSystem": 1,
            "description": "Group with PARTNER role",
            "status": "ENABLED",
            "roles": [
                {
                    "id": 4,
                    "name": "PARTNER",
                    "description": "PARTNER Role"
                }
            ]
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




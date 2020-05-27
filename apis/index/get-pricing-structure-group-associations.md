# GET-pricing-structure-group-associations

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricing-structure/:pricingStructureId/groups-not-associated/:groupName?" %}
{% api-method-summary %}
Get pricing structure group associations
{% endapi-method-summary %}

{% api-method-description %}
Get all groups not yet linked to the given pricing structure.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pricingStructureId" type="number" required=false %}
Pricing Structure Id
{% endapi-method-parameter %}

{% api-method-parameter name="groupName" type="string" %}
Group Name.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-token" type="string" required=true %}
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
    "message": "Groups retrieved",
    "payload": [
        {
            "id": 1,
            "name": "VIEW Group",
            "isSystem": 1,
            "description": "Group with VIEW role",
            "status": "ENABLED",
            "roles": [
                {
                    "id": 1,
                    "name": "VIEW",
                    "description": "VIEW Role"
                }
            ]
        },
        {
            "id": 2,
            "name": "EDIT Group",
            "isSystem": 1,
            "description": "Group with VIEW & EDIT roles",
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




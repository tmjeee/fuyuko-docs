---
description: Get all views
---

# GET-all-views

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/views" %}
{% api-method-summary %}
Get all views
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
[
    {
        "id": 1,
        "name": "Test View 1",
        "description": "Test View 1 Description"
    },
    {
        "id": 2,
        "name": "Test View 2",
        "description": "Test View 2 Description"
    },
    {
        "id": 3,
        "name": "Test View 3",
        "description": "Test View 3 Description"
    },
    {
        "id": 4,
        "name": "New-View-0.23649599024793466",
        "description": "New-View-Description-0.23649599024793466"
    },
    {
        "id": 5,
        "name": "New-View-0.9753762348113788",
        "description": "New-View-Description-0.9753762348113788"
    },
    {
        "id": 6,
        "name": "New-View-0.9077122422241255",
        "description": "New-View-Description-0.9077122422241255"
    },
    {
        "id": 7,
        "name": "New-View-0.736771295411397",
        "description": "New-View-Description-0.736771295411397"
    },
    {
        "id": 8,
        "name": "New-View-0.7751256193543219",
        "description": "New-View-Description-0.7751256193543219"
    },
    {
        "id": 9,
        "name": "New-View-0.09638445508894677",
        "description": "New-View-Description-0.09638445508894677"
    },
    {
        "id": 10,
        "name": "New-View-0.02445412004006009",
        "description": "New-View-Description-0.02445412004006009"
    },
    {
        "id": 11,
        "name": "New-View-0.09191582807824394",
        "description": "New-View-Description-0.09191582807824394"
    },
    {
        "id": 12,
        "name": "New-View-0.06696982855338085",
        "description": "New-View-Description-0.06696982855338085"
    },
    {
        "id": 13,
        "name": "New-View-0.7660559639898912",
        "description": "New-View-Description-0.7660559639898912"
    },
    {
        "id": 14,
        "name": "New-View-0.06874715648042895",
        "description": "New-View-Description-0.06874715648042895"
    },
    {
        "id": 15,
        "name": "New-View-0.46098176194973717",
        "description": "New-View-Description-0.46098176194973717"
    },
    {
        "id": 16,
        "name": "New-View-0.08293311415741833",
        "description": "New-View-Description-0.08293311415741833"
    },
    {
        "id": 17,
        "name": "New-View-0.5906412979238049",
        "description": "New-View-Description-0.5906412979238049"
    },
    {
        "id": 18,
        "name": "New-View-0.5258947395742362",
        "description": "New-View-Description-0.5258947395742362"
    },
    {
        "id": 19,
        "name": "New-View-0.25806540459259275",
        "description": "New-View-Description-0.25806540459259275"
    },
    {
        "id": 20,
        "name": "New-View-0.4237902471805617",
        "description": "New-View-Description-0.4237902471805617"
    },
    {
        "id": 21,
        "name": "New-View-0.6531376567226985",
        "description": "New-View-Description-0.6531376567226985"
    },
    {
        "id": 22,
        "name": "New-View-0.6257760059175559",
        "description": "New-View-Description-0.6257760059175559"
    },
    {
        "id": 23,
        "name": "New-View-0.04405645311160722",
        "description": "New-View-Description-0.04405645311160722"
    },
    {
        "id": 24,
        "name": "New-View-0.002344071179352314",
        "description": "New-View-Description-0.002344071179352314"
    },
    {
        "id": 25,
        "name": "New-View-0.09631125741213298",
        "description": "New-View-Description-0.09631125741213298"
    },
    {
        "id": 26,
        "name": "New-View-0.14146560943889375",
        "description": "New-View-Description-0.14146560943889375"
    },
    {
        "id": 27,
        "name": "New-View-0.1765078988889044",
        "description": "New-View-Description-0.1765078988889044"
    },
    {
        "id": 28,
        "name": "New-View-0.8045126907229381",
        "description": "New-View-Description-0.8045126907229381"
    },
    {
        "id": 29,
        "name": "New-View-0.31603594555136105",
        "description": "New-View-Description-0.31603594555136105"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




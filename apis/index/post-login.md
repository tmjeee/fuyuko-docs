---
description: Login to application
---

# POST-login

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/login" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
Username
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
Password
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
    "jwtToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoxLCJ1c2VybmFtZSI6ImN5cHJlc3MiLCJmaXJzdE5hbWUiOiJjeXByZXNzIiwibGFzdE5hbWUiOiJqZWUiLCJ0aGVtZSI6ImRlZXBwdXJwbGVfYW1iZXJfbGlnaHQiLCJlbWFpbCI6InRtamVlZUBnbWFpbC5jb20iLCJncm91cHMiOlt7ImlkIjoxLCJuYW1lIjoiVklFVyBHcm91cCIsImRlc2NyaXB0aW9uIjoiR3JvdXAgd2l0aCBWSUVXIHJvbGUiLCJzdGF0dXMiOiJFTkFCTEVEIiwicm9sZXMiOlt7ImlkIjoxLCJuYW1lIjoiVklFVyIsImRlc2NyaXB0aW9uIjoiVklFVyBSb2xlIn1dfSx7ImlkIjoyLCJuYW1lIjoiRURJVCBHcm91cCIsImRlc2NyaXB0aW9uIjoiR3JvdXAgd2l0aCBWSUVXICYgRURJVCByb2xlIiwic3RhdHVzIjoiRU5BQkxFRCIsInJvbGVzIjpbeyJpZCI6MiwibmFtZSI6IkVESVQiLCJkZXNjcmlwdGlvbiI6IkVESVQgUm9sZSJ9XX0seyJpZCI6MywibmFtZSI6IkFETUlOIEdyb3VwIiwiZGVzY3JpcHRpb24iOiJHcm91cCB3aXRoIFZJRVcgJiBFRElUICYgUEFSVE5FUiAmIEFETUlOIHJvbGUiLCJzdGF0dXMiOiJFTkFCTEVEIiwicm9sZXMiOlt7ImlkIjozLCJuYW1lIjoiQURNSU4iLCJkZXNjcmlwdGlvbiI6IkFETUlOIFJvbGUifV19LHsiaWQiOjQsIm5hbWUiOiJQQVJUTkVSIEdyb3VwIiwiZGVzY3JpcHRpb24iOiJHcm91cCB3aXRoIFBBUlRORVIgcm9sZSIsInN0YXR1cyI6IkVOQUJMRUQiLCJyb2xlcyI6W3siaWQiOjQsIm5hbWUiOiJQQVJUTkVSIiwiZGVzY3JpcHRpb24iOiJQQVJUTkVSIFJvbGUifV19XX0sImlhdCI6MTU4Mzk4NzU1NiwiZXhwIjoxNTgzOTkxMTU2fQ.hZD9qusN9hac9Kc8auHUXHbsmoM6hKarnRj8HRD000c",
    "status": "SUCCESS",
    "message": "Successfully logged in",
    "user": {
        "id": 1,
        "username": "cypress",
        "firstName": "cypress",
        "lastName": "jee",
        "theme": "deeppurple_amber_light",
        "email": "tmjeee@gmail.com",
        "groups": [
            {
                "id": 1,
                "name": "VIEW Group",
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
                "description": "Group with VIEW & EDIT role",
                "status": "ENABLED",
                "roles": [
                    {
                        "id": 2,
                        "name": "EDIT",
                        "description": "EDIT Role"
                    }
                ]
            },
            {
                "id": 3,
                "name": "ADMIN Group",
                "description": "Group with VIEW & EDIT & PARTNER & ADMIN role",
                "status": "ENABLED",
                "roles": [
                    {
                        "id": 3,
                        "name": "ADMIN",
                        "description": "ADMIN Role"
                    }
                ]
            },
            {
                "id": 4,
                "name": "PARTNER Group",
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
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




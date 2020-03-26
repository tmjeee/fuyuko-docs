---
description: Common response across all endpoints
---

# Common response

### 400 - Bad Request

General error due to bad client request.

```text
{
    "context": "default",
    "errors": [
        {
            "msg": "User with either username invitation1 or email invitation1@gmail.com already exists",
            "location": "",
            "param": "",
            "value": ""
        }
    ]
}
```

```text
{
    "context": "default",
    "errors": [
        {
            "msg": "Invalid value",
            "param": "username",
            "location": "body"
        }
    ]
}
```

### 401 - Unauthorized

Unauthorized, due to bad access token

```text
{
    "context": "default",
    "errors": [
        {
            "msg": "TokenExpiredError jwt expired",
            "location": "Security",
            "param": "jwtToken",
            "value": ""
        }
    ]
}
```

### 403 - Unauthenticated

Request do not have the right permission.

```text
{
    "context": "default",
    "errors": [
        {
            "msg": "",
            "location": "",
            "param": "",
            "value": "Security"
        }
    ]
}
```

### 500 - Internal Server Error

Internal error from the server

```text

```


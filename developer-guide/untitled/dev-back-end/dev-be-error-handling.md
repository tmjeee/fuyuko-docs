# Dev - BE - Error handling

## Handling Error

All routing errors handling are done by `catchErrorMiddleware` in `src/route/v1/common-middleware.ts`.

It handles the following exceptions :-

### ClientError

This will result in **Http status 400** being returned, `ApiErrorContext` to be exact, with the mesage of `ClientError` wrapped in it.

```text
{
  "context": "...",
  "errors": [
     "msg": "....",
     "location": "....",
     "param": "....",
     "value": "...."
  ]
}
```

### Other Errors

Other errors or exception, apart from `ClientError`, will result in **Http Status 500** being returned, `ApiErrorContext` to be exact. 

```text
{
  "context": "...",
  "errors": [
     "msg": "....",
     "location": "....",
     "param": "....",
     "value": "...."
  ]
}
```


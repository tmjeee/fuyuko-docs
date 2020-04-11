# DEV - BE - REST End Point Route

## Location

Located in `src/route` directory and is versioned eg.

* `src/route/v1`, will be the **version 1** of the REST end point routes
* `src/route/v2`, which do not exists as of this writting, will be the **version 2** of the REST end point routes

## Script naming convention

Typically named as follows

```text
<HTTP_methd>-<short_description_of_route_function>.route.ts
```

## Script structure

Typical REST end point route script looks as follows 

```text

const httpAction: any[] = [
    // express-validator validation checks 
    // for path, body etc. variables
    [                                                    // (1)
       param('pathVariable1').exists().isNumeric(),
       param('pathVariable2').exists()
    ],
    validateMiddlewareFn,                                // (2)
    validateJwtMiddlewareFn,                             // (3)
    v([vFnHasAnyUserRoles([ROLE_VIEW])], aFnAnyTrue)     // (4)
];

const reg = (router: Router, registry: Registry) => {
    const p = `/path/:var1/another-path/:var2`;          // (5)
    registry.addItem('GET', p);                          // (6)
    router.get(p, ...httpActions);                       // (7)
}

export default reg;
```

### Point \(1\)

\`\`[`express-validator`](https://express-validator.github.io/) validation checks for variables validity in `path`, `body`, `query parameters` etc.

### Point \(2\)

`validateMiddlewareFn` is a middleware located in `src/route/v1/common-middleware.ts` to run [`express-validator`](https://express-validator.github.io/)'s validations.

### Point \(3\)

`validateJwtMiddlewareFn` is a middleware located in `src/route/v1/common-middleware.ts` to validate jwt token passed in through http header.

### Point \(4\)

```text
v([vFnHasAnyUserRoles([ROLE_VIEW])], aFnAnyTrue)
```

`v(...)` is a function located in src/route/v1/common-middleware.ts to validate a user role, by accepting the following parameters

* an array of `validation function factory functions` as first argument
* an `aggregation function`, as second argument, to aggregate the result of validation functions in first argument

{% hint style="info" %}
Note that all `validation function factory functions` begins with `vFn` prefix
{% endhint %}

{% hint style="info" %}
Note that all `agregation function` begins with `aFn` prefix
{% endhint %}

`validation function factory functions` available are :

| `validation function factory functions` | Description |
| :--- | :--- |
| `vFnHasNoneUserRoles(roleNames: string[])` | Return true when the logged in user has none of the given roles passed in as argument, else false |
| `vFnIsSelf(userId: number)` | Return true when the userId passed in as agument is the current logged in user, else false |
| `vFnHasAnyUserRoles(roleNames: string[])` | Return true when the logged in user has any of the given roles passed in as argument, else false |
| `vFnHasAllUserRoles(roleNames: string[])` | Return true when the logged in user has all of the given roles passed in as argument, else false |

`aggregation functions` available are :

| `agregation functions` |  |
| :--- | :--- |
| aFnAllTrue | Return true if all of the `validation functions` return true, else false |
| aFnAllFalse | Return true if all of the `validation functions` return false, else false |
| aFnAnyTrue | Return true if any of the `validation functions` return true, else false |
| aFnAnyFalse | Return true if any of the `validation functions` return false, else false |

#### Examples

With `v([vFnIsSelf(someUserId), vFnHasAnyUserRoles([ROLE_ADMIN, ROLE_VIEW])], aFnAllTrue)`, the validation will pass only when all of the followings are true, identified by `aggregation function` `aFnAllTrue`

* current logged in user id is `someUserId`, identified by `validation function factory function` `vFnIsSelf(someUserId)`
* current logged in user has either `ROLE_ADMIN` or `ROLE_VIEW`, identified by `validation function factory function` `vFnHasAnyUserRoles([ROLE_ADMIN, ROLE_VIEW])`

### Point \(5\)

URI path for this end point.

### Point \(6\)

Add this end point to the registry

### Point \(7\)

Add this end point to ExpressJs route

{% hint style="info" %}
Note: both `point(6)` and `point (7)` must match, ie. both uses the same HTTP Method.
{% endhint %}

## Registering script

Routing script needs to be register in `src/route/v1/v1-app-router.ts` as follows

```text
import registerGetMyCustomScriptRoute 
     from '<path-to>/GET-my-custom-script.route.ts';     // (1)

....

registerGetMyCustomScriptRoute(                          // (2)
     v1AppRouter,                                        // (3)
     registry                                            // (4)
);

```

### Point \(1\)

import the route script

### Point \(2\)

call the route script to register itself

### Point \(3\)

pass in the `ExpressJS` Router to the route script itself as the first argument

### Point \(4\)

pass in a `Registry` object to the route script as the second argument. This `Registry` object merely register the path so that it can print out a hierarchical layout of enpoints when requested \(during application startup\)


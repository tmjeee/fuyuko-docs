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

### Point \(2\)

### Point \(3\)

### Point \(4\)

### Point \(5\)

### Point \(6\)

### Point \(7\)

## Registering script

Routing script needs to be register in `src/route/v1/v1-app-router.ts` as follows

```text

```


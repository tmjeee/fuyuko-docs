# Dev - FE - Service

## Directory Structure

```text
+ src/
   + service/
      + activation-service/
         ...
      + app-notification-service/
         ...
      + attribute-service/
         ...
      + auth-service/
         ...
      ...
```

## Characteristics

* Make call to BE through `HttpClient`
* Used by `Layout` or `Page` components only.
* Most service are application wide scoped apart from the followings:
  * `DashboardWidgetService` located in `src/service/dashboard-service` which is scoped to `WidgetContainerComponent`, see [dashboard documentation](dev-fe-dashboard-and-widgets.md) for more info,
* Resides in a folder in `src/service/` directory. 
* Services of similar nature can lie inside same directory under `src/service/`




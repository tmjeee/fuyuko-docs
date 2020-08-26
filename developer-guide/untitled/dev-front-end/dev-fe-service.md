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
* Most service are application wide scoped, exceptional ones are listed in the section that follows.
* Resides in a folder in `src/service/` directory. 
* Services of similar nature can lie inside same directory under `src/service/`

Following are some special services:

### DashboardWidgetService

* Located in `src/service/dashboard-service`
* Scoped to `WidgetContainerComponent`, see [dashboard documentation](dev-fe-dashboard-and-widgets.md) for more info.

### ViewService

* `init()` when user login, where a default view will be chosen
* `destroy()` when user logout
* Allow view changes to be persistent and observable for current user throughout his session with the application.

### ThemeService

* `setTheme(...)` when user login 
* allow user theme changed to be observable through `observer()`

### SettingsService

* `init()` when user login, to load user's settings
* `destroy()` when user logout
* allowed users cached settings to be retrieved.

### AuthService

* Allows listening to `login` and `logout` events, when the occurred.

### GlobalCommunicationService

* Where inter- components events, thorugh `Observables` / `Subjects` takes place.
* Allow user's avatar changes to be observed and triggered.


# Dev - FE - Layout

## Directory structure

Following is the directory structure for layouts

```text
+ src/
   + app/
      + layout/
         + dashboard-layout/
            - ...
         + gen-layout/
            - ...
         + import-export-gen-layout/
            - ...
         + login-layout/
            - ...
         + partner-layout/
            - ...
         + user-gen-layout/
            - ...
         + view-gen-layout/
            - ...
```

## Characteristics

* [Layout components](dev-fe-layout.md) are angular components, that decide how `<router-outlet>` are layouted eg. side navigation, sub-side navigation, help menu etc.
* In rare cases it might require services to be injected
* It is the main components wrapping [page components](dev-fe-page.md) which in order wrapped [components](dev-fe-component.md)

### dashboard-layout

![](../../../.gitbook/assets/dashboard-layout.png)

### gen-layout

![](../../../.gitbook/assets/gen-layout.png)

### import-export-gen-layout

![](../../../.gitbook/assets/import-export-layout.png)

### login-layout

![](../../../.gitbook/assets/login-layout.png)

### partner-layout

![](../../../.gitbook/assets/partner-layout.png)

### user-gen-layout

![](../../../.gitbook/assets/user-gen-layout.png)

### view-gen-layout

![](../../../.gitbook/assets/view-gen-layout.png)


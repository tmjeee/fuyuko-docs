# Dev - FE - Component

## Directory Structure

```text
+ src/
   + component/
      + attribute-table-component/
      + avatar-component/
      + carousel-component/
      + dashboard-component/
      ...
```

## Characteristics

* Should **not** access any service
* Dumb, obtain data / information from page component through `@Input()`
* Communicate interaction / changes to page component through 
  * `@Ouput()` events
  * `@Input()` callback functions
* Reusability
* Each component directory is an angular module by itself and can encompass many related components.


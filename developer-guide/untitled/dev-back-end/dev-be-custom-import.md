# Dev - BE - Custom Import

## Location

Located in `src/custom-import` directory. Custom export scripts need to be dump in `src/custom-import/custom-import-scripts` directory.

## Script naming convension

Typically named `<semver-version-format>-<short-description-of-custom-import-function>.ts`

## Directory Structure

```text
+ src/
  + custom-import/
     + custom-import-scripts/
        - 0.0.1-sample-custom-import-1.ts
        - 0.0.2-sample-custom-import-1.ts
```

* custom import script should be located in `src/custom-import/custom-import-scripts/`
* adding new custom import to the directory will need a restart of the back-end server so synchronisation can take place.
* removing a custom import would require removing it from the directory and doing a restart of the back-end server for synchronisation to take place.
* Upon synchronisation, custom imports will be avialable in the application.

{% hint style="warning" %}
Warning

Removing and existing custom import script, will result in all it's information being lost
{% endhint %}


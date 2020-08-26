# Dev - BE - Custom Export

## Location

Located in `src/custom-export` directory. Custom export scripts need to be dump in `src/custom-export/custom-export-scripts` directory.

## Script naming convension

Typically named `<semver-version-format>-<short-description-of-custom-export-function>.ts`

## Directory Structure

```text
+ src/
  + custom-export/
     + custom-export-scripts/
        - 0.0.1-sample-custom-export-1.ts
        - 0.0.2-sample-custom-export-2.ts
```

* custom export script should be located in `src/custom-export/custom-export-scripts/`
* adding new custom export to the directory will need a restart of the back-end server so synchronisation can take place.
* removing a custom export would require removing it from the directory and doing a restart of the back-end server for synchronisation to take place.
* Upon synchronisation, custom exports will be avialable in the application.

{% hint style="warning" %}
Warning

Removing and existing custom export script, will result in all it's information being lost
{% endhint %}

## Synchronisation

Upon startup, the application will try to synchronise the custom export scripts with the information it had in the database based on the following conditions:

1. If a custom export script, identified by it's **file** **name** exists in `src/custom-export/custom-export-scripts` directory but do not exists in application database, one will be **created**
2. If a custom export script, identifed by its **file name** do not exists in `src/custom-export/custom-export-scripts` directory but exists in application database, the one in application database will be **wipe out**.
3. If a custom export script, identified by its **file name** exists in `src/custom-export/custom-export-scripts` directory and also exists in application database, **no action is required**, they are in sync.

## Script Structure

The name of the custom export would be the **filename** of the custom rule script.

If you were to write a custom export script , you would need to follow this structure.

 Typical custom export script would look as follows :

```text
const scriptName: string = `0.0.1-sample-custom-import-1`;

export const description = (): string => {                              // (1)
    // return the description of this custom export
    return `${scriptName} description`;
}


export const inputs = (): ExportScriptInput[] => {                      // (2)
   // return the input(s) required to collect information
   // the custom export here
}

export const validate  = (v: View,                                      // (3)
                          values: ExportScriptInputValue[]): 
                          {valid: boolean, 
                           messages: NewNotification[]} => {
   // call 1: validate input
   // implement custom export input(s) validation logic here
}

export const preview = (view: View,                                     // (4)
                        inputValues: ExportScriptInputValue[], 
                        ctx: CustomExportContext): 
                        ExportScriptPreview => {
   // call 2: do preview
   // implement custom export preview logic here 
}

export const action = (view: View,                                     // (5)
                       inputValues: ExportScriptInputValue[], 
                       preview: ImportScriptPreview, 
                       ctx: CustomExportContext, 
                       log: (logMessage: LogMessage) => void) : 
                       CustomExportJob => {
   // call 3: do actual custom export work
   // implement actual custom export work here
}
```

It would require :

### `description(): string` function

returns a description of this custom export

### `inputs(): ExportScriptInput[]` function

return the input\(s\) to collect information required for this custom export. It will be converted to UI Inputs when in a HTML forms with HTML inputs in custom export wizard 

### `validate(v: View, values: ExportScriptInputValue[]): {valid: boolean, messages: NewNotification[]}` function

perform validation on input\(s\) values

### `preview(v: View, inputValues: ExportScriptInputValue[], ctx: CustomExportContext): ExportScriptPreview` function

perform a custom export preview, returning result in tablular format encapsulated by `ExportScriptPreview` object.

### `action(view: View, inputValues: ExportScriptInputValue[], ctx: CustomExportContext): CustomExportJob` function

perform the actual custom export, encapsulating the task in `run()` function in `CustomExportJob`


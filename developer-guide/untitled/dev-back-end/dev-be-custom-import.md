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

## Synchronisation

Upon startup, the application will try to synchronise the custom import scripts with the information it had in the database based on the following conditions:

1. If a custom import script, identified by it's **file** **name** exists in `src/custom-import/custom-import-scripts` directory but do not exists in application database, one will be **created**
2. If a custom import script, identifed by its **file name** do not exists in `src/custom-import/custom-import-scripts` directory but exists in application database, the one in application database will be **wipe out**.
3. If a custom import script, identified by its **file name** exists in `src/custom-import/custom-import-scripts` directory and also exists in application database, **no action is required**, they are in sync.

## Script Structure

The name of the custom export would be the **filename** of the custom rule script.

If you were to write a custom import script , you would need to follow this structure.

 Typical custom import script would look as follows :

```text
const scriptName: string = `0.0.1-sample-custom-import-1`;

export const description = (): string => {
    return `${scriptName} description`;
}

export const inputs = (): ImportScriptInput[] => {
  // return inputs for custom import
}

export const validate  = (v: View, 
                          values: ImportScriptInputValue[]): 
                          {valid: boolean, 
                           messages: NewNotification[]} => {
  // validate inputs for custom import
}

export const preview = (view: View, 
                        inputValues: ImportScriptInputValue[], 
                        ctx: CustomImportContext): 
                        ImportScriptPreview => {
  // return a preview for cutom import
}

export const action = (view: View, 
                       inputValues: ImportScriptInputValue[], 
                       preview: ImportScriptPreview, 
                       ctx: CustomImportContext, 
                       log: (logMessage: LogMessage) => void) : 
                       CustomImportJob => {
  // do actual custom import
}
```

It would require :

### `description(): string` function

returns a description of this custom import

### `inputs(): ImportScriptInput[]` function

return the input\(s\) to collect information required for this custom import. It will be converted to UI Inputs when in a HTML forms with HTML inputs in custom import wizard 

### `validate(v: View, values: ImportScriptInputValue[]): {valid: boolean, messages: NewNotification[]}` function

perform validation on input\(s\) values

### `preview(v: View, inputValues: ImportScriptInputValue[], ctx: CustomImportContext): ImportScriptPreview` function

perform a custom import preview, returning result in tablular format encapsulated by `ImportSriptPreview` object.

### `action(view: View, inputValues: ImportScriptInputValue[], ctx: CustomImportContext): CustomImportJob` function

perform the actual custom import, encapsulating the task in `run()` function in `CustomImportJob`


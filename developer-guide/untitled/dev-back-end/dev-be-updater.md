# Dev - BE - Updater

Located at `src/updater`, this package run update scripts upon BE application startup.

## Configuration

Located in `src/config/config.json`, following are the properties that govern updater

```text
{
  ...
  "updater-run": true,
  "updater-profiles": ["CORE", "TEST-DATA"]  
  ...
}
```

### `updater-run` property

To turn updater on or off. No updater scripts will be run if turn off.

### `updater-profiles` property

Updater scripts are grouped by profiles, only those scripts that are in this listed profiles are allowed to run.

## Directory Structure

Following is a typical directory structure for `src/updater`

```text
+ src/
   + updater/
      + scripts/
          - 0.0.1-create-tables.ts
          - 0.0.2-create-core-data.ts
          - 0.0.3-create-sample-users-data.ts
          - 0.0.4-create-sample-test-data.ts
```

* Scripts should be located in `src/updater/scripts/` folder
* Scripts are run in order dictated by semver syntax, eg if ther are only 2 scripts \(`0.0.1-script.ts` and `0.0.2-script.ts`\), `0.0.1-script.ts` will run before `0.0.2-script.ts`
* Scripts will run once only \(regardless of how many times the application is started\) as it will registered itself upon first run.
* Script only runs when has a profile defined in `updater-profiles` properties located in `src/config/config.json`.

## Profile

 Each script can have many profiles. But they need to match with the updater's profile \(defined by `updater-profiles` property in the configuration\) in order for it to be executed, if it has not yet being executed before.

## Writing a custom updater script

Writing a custom updater script would require:

* creating a script file that follows `<semver-version-format>-<name of script>.ts` format
* the script file needs to be located in `src/updater/scripts` folder
* the script file needs to contain
  * a `profiles` property that returns an array of profile \(string\) it supports
  * a `update()` function where the operations related to it's update should be performed

 Example,

```text
// an example of an update script ts file

// profiles that this script supports
export const profiles = ['MY_PROFILE'];

// function to call to perform an update
export const update = async () => {
   // code for this script actual update operation
   ...
} 
```

{% hint style="info" %}
The '`MY_PROFILE`' will need to present in updater's profile as well in order for the script to run

```
 "updater-profiles": [ ..., "MY_PROFILE" ]  
```
{% endhint %}




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

 


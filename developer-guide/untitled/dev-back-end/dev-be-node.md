# Dev - BE - Node

## NPM \(package.json\)

Following are the targets in `package.json`

| Target name | Description |
| :--- | :--- |
| tsc | Compile typescripts |
| copy | Copy models code into BE |
| exec | Copy models, compile typescripts and run BE REST APIs server |
| build | Copy models and compile typescripts |
| test | Run jasmine tests |

## Application main entry point

`app.tsc` located in `src/` directory, is the main script that starts up the application, it does roughly the followings

* wires up all the REST APIs routes using `ExpressJS` 
* run [updater](dev-be-updater.md)
* sync [custom rules](dev-be-custom-rule.md)
* sync [custom exports](dev-be-custom-export.md)
* sync [custom imports](dev-be-custom-import.md)
* start up `ExpressJS` at configured port

Typical startup would look as follow in the console 

```text
> node --max-old-space-size=8192 -- src/app.js


         ______                 _                 
        |  ____|               | |                
        | |__ _   _ _   _ _   _| | _____          
        |  __| | | | | | | | | | |/ / _ \         
 _ _ _  | |  | |_| | |_| | |_| |   < (_) |  _ _ _ 
(_|_|_) |_|   \__,_|\__, |\__,_|_|\_\___/  (_|_|_)
                     __/ |                        
                    |___/     1.0.0-beta                    
    
    
body-parser deprecated undefined extended: provide extended option src/app.js:27:27
[04-11-2020 07:01:34 am] - INFO - URL Mappings :-
  api
    /v1
      GET - /heartbeat
      POST - /activate-invitation/:code
      POST - /self-register/approve/:selfRegistrationId
      POST - /create-invitation
      GET - /user/:userId/avatar
      GET - /user/:userId/avatar-info
      GET - /global/avatar/:avatarName
      GET - /global/avatars
      GET - /invitations/:code
      POST - /login
      POST - /logout
      POST - /self-register
      POST - /user/:userId/avatar
      POST - /user
      GET - /user/:userId
      GET - /groups
      GET - /group/:groupId
      GET - /groups/no-role/:roleName/:groupName?
      GET - /groups/with-role/:roleName
      DELETE - /group/:groupId/role/:roleName
      POST - /group/:groupId/role/:roleName
      GET - /users/not-in-group/:groupId/:username?
      GET - /users/in-group/:groupId
      POST - /group/:groupId/add-user/:userId
      DELETE - /group/:groupId/remove-user/:userId
      GET - /self-registers
      DELETE - /self-register/:selfRegistrationId
      GET - /users/status/:status
      DELETE - /user/:userId
      POST - /user/:userId/status/:status
      GET - /roles
      GET - /views
      POST - /views/update
      DELETE - /views/delete
      GET - /attributes/view/:viewId
      GET - /attributes/view/:viewId/search/:attribute?
      POST - /attributes/update
      POST - /attribute/:attributeId/state/:state
      GET - /view/:viewId/items
      GET - /item/image/:itemImageId
      GET - /item/image/primary/:itemId
      POST - /view/:viewId/items/update
      POST - /view/:viewId/items/status/:status
      GET - /view/:viewId/rules
      POST - /view/:viewId/rule/:ruleId/status/:status
      POST - /view/:viewId/rules
      GET - /pricingStructures
      GET - /pricingStructuresWithItems/:pricingStructureId
      POST - /pricingStructure/:pricingStructureId/status/:status
      POST - /pricingStructures
      POST - /view/:viewId/preview-bulk-edit
      POST - /view/:viewId/bulk-edit
      GET - /jobs
      GET - /job/:jobId/details/:lastLogId?
      GET - /job/:jobId/details
      GET - /job/:jobId
      POST - /view/:viewId/import/attributes
      POST - /view/:viewId/import/items
      POST - /view/:viewId/import/prices
      POST - /view/:viewId/import/attributes/preview
      POST - /view/:viewId/import/items/preview
      POST - /view/:viewId/import/prices/preview
      POST - /view/:viewId/export/attributes/preview
      POST - /view/:viewId/export/items/preview
      POST - /view/:viewId/export/pricingStructure/:pricingStructureId/prices/preview
      POST - /view/:viewId/export/attributes
      POST - /view/:viewId/export/items
      POST - /view/:viewId/export/pricingStructure/:pricingStructureId/prices
      GET - /export/:exportDataId/file
      POST - /user/:userId/dashboard/save
      GET - /user/:userId/dashboard
      POST - /user/:userId/dashboard-widget-instance-data
      GET - /user/:userId/dashboard-widget-instance/:dashboardWidgetInstanceId
      GET - /user/:userId/partner-pricing-structures
      GET - /pricingStructure/:pricingStructureId/pricedItems
      GET - /group/:groupName/search
      GET - /search/status/:status/user/:username?
      GET - /search/self-registration/:username?
      GET - /view/:viewId/rule/:ruleId
      GET - /attribute/:attributeId/view/:viewId
      GET - /view/:viewId/items/:itemIds
      GET - /view/:viewId/validations
      GET - /view/:viewId/validation/:validationId
      POST - /view/:viewId/validation
      GET - /view/:viewId
      GET - /user/:userId/settings
      POST - /user/:userId/settings
      GET - /custom-rules
      GET - /view/:viewId/custom-rules
      POST - /view/:viewId/custom-rules
      POST - /view/:viewId/custom-rules/:customRuleId/status/:status
      DELETE - /view/:viewId/custom-rules
      GET - /user/:userId/notifications
      POST - /user/:userId/notification
      POST - /view/:viewId/attributes/add
      GET - /view/:viewId/searchType/:searchType/search/:search?
      DELETE - /view/:viewId/validation/:validationId
      GET - /data-export/:dataExportId
      GET - /pricingStructure/:pricingStructureId
      GET - /data-export-artifacts
      DELETE - /data-export-artifact/:dataExportArtifactId
      POST - /item/:itemId/image
      DELETE - /item/:itemId/image/:itemImageId
      POST - /item/:itemId/image/:itemImageId/mark-primary
      GET - /help/:helpPostfix
      GET - /custom-imports
      POST - /view/:viewId/custom-import/:customImportId/validate-input
      POST - /view/:viewId/custom-import/:customImportId/preview
      POST - /view/:viewId/custom-import/:customImportId/submit-job
      GET - /custom-exports
      POST - /view/:viewId/custom-export/:customExportId/validate-input
      POST - /view/:viewId/custom-export/:customExportId/preview
      POST - /view/:viewId/custom-export/:customExportId/submit-job

[04-11-2020 07:01:34 am] - INFO - Fuyuko API started listening at port 8888
[04-11-2020 07:01:34 am] - INFO - running db updater
[04-11-2020 07:01:34 am] - INFO - ** Running updater, profiles found [CORE, TEST-DATA]
[04-11-2020 07:01:34 am] - INFO - script /home/tmjee/cockpit/code/fuyuko/be/src/updater/scripts/0.0.1-create-tables.js has already been executed before, skip execution
[04-11-2020 07:01:34 am] - INFO - script /home/tmjee/cockpit/code/fuyuko/be/src/updater/scripts/0.0.2-create-core-data.js has already been executed before, skip execution
[04-11-2020 07:01:34 am] - INFO - script /home/tmjee/cockpit/code/fuyuko/be/src/updater/scripts/0.0.3-create-sample-users-data.js has already been executed before, skip execution
[04-11-2020 07:01:34 am] - INFO - script /home/tmjee/cockpit/code/fuyuko/be/src/updater/scripts/0.0.4-create-sample-test-data.js has already been executed before, skip execution
[04-11-2020 07:01:34 am] - INFO - done with db updater
[04-11-2020 07:01:34 am] - INFO - running custom rule sync
[04-11-2020 07:01:34 am] - INFO - Running custom rule sync ...
[04-11-2020 07:01:34 am] - INFO - Custom rules script forward sync, files to db
[04-11-2020 07:01:34 am] - INFO - Rule file 0.0.1-sample-rule-1.js already registered before
[04-11-2020 07:01:34 am] - INFO - Rule file 0.0.2-sample-rule-2.js already registered before
[04-11-2020 07:01:34 am] - INFO - Custom rules script reverse sync, db to files
[04-11-2020 07:01:34 am] - INFO - Db rule registry 0.0.1-sample-rule-1.js is in sync with rule script, no action required
[04-11-2020 07:01:34 am] - INFO - Db rule registry 0.0.2-sample-rule-2.js is in sync with rule script, no action required
[04-11-2020 07:01:34 am] - INFO - Done custom rule sync
[04-11-2020 07:01:34 am] - INFO - done with custom rule sync
[04-11-2020 07:01:34 am] - INFO - running custom import sync
[04-11-2020 07:01:34 am] - INFO - Running custom import script sync ...
[04-11-2020 07:01:34 am] - INFO - Custom import scripts forward sync, files to db
[04-11-2020 07:01:34 am] - INFO - Custom import script file 0.0.1-sample-custom-import-1.js already registered before
[04-11-2020 07:01:34 am] - INFO - Custom import script reverse sync, db to files
[04-11-2020 07:01:34 am] - INFO - Db custom import registry 0.0.1-sample-custom-import-1.js is in sync with custom import script, no action required
[04-11-2020 07:01:34 am] - INFO - Db custom import registry 0.0.2-sample-custom-import-2.js is in sync with custom import script, no action required
[04-11-2020 07:01:34 am] - INFO - Done custom import script sync
[04-11-2020 07:01:34 am] - INFO - Custom import script file 0.0.2-sample-custom-import-2.js already registered before
[04-11-2020 07:01:34 am] - INFO - Custom import script reverse sync, db to files
[04-11-2020 07:01:34 am] - INFO - Db custom import registry 0.0.1-sample-custom-import-1.js is in sync with custom import script, no action required
[04-11-2020 07:01:34 am] - INFO - Db custom import registry 0.0.2-sample-custom-import-2.js is in sync with custom import script, no action required
[04-11-2020 07:01:34 am] - INFO - Done custom import script sync
[04-11-2020 07:01:34 am] - INFO - done with custom import sync
[04-11-2020 07:01:34 am] - INFO - running custom export sync
[04-11-2020 07:01:34 am] - INFO - Running custom export script sync ...
[04-11-2020 07:01:34 am] - INFO - Custom export scripts forward sync, files to db
[04-11-2020 07:01:34 am] - INFO - Custom export script file 0.0.1-sample-custom-export-1.js already registered before
[04-11-2020 07:01:34 am] - INFO - Custom export script reverse sync, db to files
[04-11-2020 07:01:34 am] - INFO - Db custom export registry 0.0.1-sample-custom-export-1.js is in sync with custom export script, no action required
[04-11-2020 07:01:34 am] - INFO - Db custom export registry 0.0.2-sample-custom-export-2.js is in sync with custom export script, no action required
[04-11-2020 07:01:34 am] - INFO - Done custom export script sync
[04-11-2020 07:01:34 am] - INFO - Custom export script file 0.0.2-sample-custom-export-2.js already registered before
[04-11-2020 07:01:34 am] - INFO - Custom export script reverse sync, db to files
[04-11-2020 07:01:34 am] - INFO - Db custom export registry 0.0.1-sample-custom-export-1.js is in sync with custom export script, no action required
[04-11-2020 07:01:34 am] - INFO - Db custom export registry 0.0.2-sample-custom-export-2.js is in sync with custom export script, no action required
[04-11-2020 07:01:34 am] - INFO - Done custom export script sync
[04-11-2020 07:01:34 am] - INFO - done with custom export sync
[04-11-2020 07:01:34 am] - INFO - Fuyuko ready for operation !!!
```


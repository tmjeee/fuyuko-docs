# Docker Compose

## Requirements

Assuming that you have [Docker](https://docs.docker.com) and [Docker Compose](https://docs.docker.com/compose/) installed.

## Starting

To start Fuyuko with docker compose, navigate into `<fuyuko-root>/docker-compose/` directory and run the following command

```text
# we are at <fuyuko-root>/docker-compose/
$> docker-compose up
```

This will build docker images for `fuyuko-db`, `fuyuko-be` and `fuyuko-fe` and create and run their resepective containers. Following is a sample of logs when `docker-compose up` is executed.

```text
Starting dockercompose_db_1 ... 
Starting dockercompose_db_1 ... done
Starting dockercompose_be_1 ... 
Starting dockercompose_be_1 ... done
Recreating dockercompose_fe_1 ... 
Recreating dockercompose_fe_1 ... done
Attaching to dockercompose_db_1, dockercompose_be_1, dockercompose_fe_1
db_1  | 2020-07-21 12:23:46+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 1:10.1.45+maria-1~bionic started.
db_1  | 2020-07-21 12:23:47+00:00 [Note] [Entrypoint]: Switching to dedicated user 'mysql'
be_1  | mysqladmin: connect to server at 'db' failed
be_1  | error: 'Can't connect to MySQL server on 'db' (111 "Connection refused")'
db_1  | 2020-07-21 12:23:47+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 1:10.1.45+maria-1~bionic started.
be_1  | Check that mysqld is running on db and that the port is 3306.
be_1  | You can check this by doing 'telnet db 3306'
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] mysqld (mysqld 10.1.45-MariaDB-1~bionic) starting as process 1 ...
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Using mutexes to ref count buffer pool pages
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: The InnoDB memory heap is disabled
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Mutexes and rw_locks use GCC atomic builtins
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: GCC builtin __atomic_thread_fence() is used for memory barrier
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Compressed tables use zlib 1.2.11
be_1  | Mariadb is unavailable - sleeping
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Using Linux native AIO
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Using SSE crc32 instructions
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Initializing buffer pool, size = 256.0M
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Completed initialization of buffer pool
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Highest supported file format is Barracuda.
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: The log sequence number 1616727 in ibdata file do not match the log sequence number 10825026 in the ib_logfiles!
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Restoring possible half-written data pages from the doublewrite buffer...
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: 128 rollback segment(s) are active.
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB: Waiting for purge to start
db_1  | 2020-07-21 12:23:47 140235146762240 [Note] InnoDB:  Percona XtraDB (http://www.percona.com) 5.6.47-87.0 started; log sequence number 10825026
db_1  | 2020-07-21 12:23:48 140234180261632 [Note] InnoDB: Dumping buffer pool(s) not yet started
db_1  | 2020-07-21 12:23:48 140235146762240 [Note] Plugin 'FEEDBACK' is disabled.
db_1  | 2020-07-21 12:23:48 140235146762240 [Note] Recovering after a crash using tc.log
db_1  | 2020-07-21 12:23:48 140235146762240 [Note] Starting crash recovery...
db_1  | 2020-07-21 12:23:48 140235146762240 [Note] Crash recovery finished.
db_1  | 2020-07-21 12:23:48 140235146762240 [Note] Server socket created on IP: '::'.
db_1  | 2020-07-21 12:23:48 140235146762240 [Warning] 'proxies_priv' entry '@% root@d15dc84b26a0' ignored in --skip-name-resolve mode.
db_1  | 2020-07-21 12:23:48 140235146762240 [Note] mysqld: ready for connections.
db_1  | Version: '10.1.45-MariaDB-1~bionic'  socket: '/var/run/mysqld/mysqld.sock'  port: 3306  mariadb.org binary distribution
be_1  | mysqld is alive
be_1  | Mariadb is up - execute -- node src/app.js --db-host=db --db-port=3306
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - process argv --db-host=db
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - WARN - failed to JSON parse value db for overriding property db-host using value as is
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - Command line arguments db-host=db will override the one in config.json
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - process argv --db-port=3306
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - Command line arguments db-port=3306 will override the one in config.json
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - Run Timezoner
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - Timezone set to Australia/Sydney, Today's date time with locale is Tue Jul 21 2020 12:23:48 GMT+0000 (Coordinated Universal Time)
be_1  | Tue, 21 Jul 2020 12:23:48 GMT body-parser deprecated undefined extended: provide extended option at src/app.js:32:27
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - URL Mappings :-
be_1  |   api
be_1  |     /v1
be_1  |       GET - /heartbeat
be_1  |       POST - /activate-invitation/:code
be_1  |       POST - /self-register/approve/:selfRegistrationId
be_1  |       POST - /create-invitation
be_1  |       GET - /user/:userId/avatar
be_1  |       GET - /user/:userId/avatar-info
be_1  |       GET - /global/avatar/:avatarName
be_1  |       GET - /global/avatars
be_1  |       GET - /invitations/:code
be_1  |       POST - /login
be_1  |       POST - /logout
be_1  |       POST - /self-register
be_1  |       POST - /user/:userId/avatar
be_1  |       POST - /user
be_1  |       GET - /user/:userId
be_1  |       GET - /groups
be_1  |       GET - /group/:groupId
be_1  |       GET - /groups/no-role/:roleName/:groupName?
be_1  |       GET - /groups/with-role/:roleName
be_1  |       DELETE - /group/:groupId/role/:roleName
be_1  |       POST - /group/:groupId/role/:roleName
be_1  |       GET - /users/not-in-group/:groupId/:username?
be_1  |       GET - /users/in-group/:groupId
be_1  |       POST - /group/:groupId/add-user/:userId
be_1  |       DELETE - /group/:groupId/remove-user/:userId
be_1  |       GET - /self-registers
be_1  |       DELETE - /self-register/:selfRegistrationId
be_1  |       GET - /users/status/:status
be_1  |       DELETE - /user/:userId
be_1  |       POST - /user/:userId/status/:status
be_1  |       GET - /roles
be_1  |       GET - /views
be_1  |       POST - /views/update
be_1  |       DELETE - /views/delete
be_1  |       GET - /attributes/view/:viewId
be_1  |       GET - /attributes/view/:viewId/search/:attribute?
be_1  |       POST - /attributes/update
be_1  |       POST - /attribute/:attributeId/state/:state
be_1  |       GET - /view/:viewId/items
be_1  |       GET - /item/image/:itemImageId
be_1  |       GET - /item/image/primary/:itemId
be_1  |       POST - /view/:viewId/items/update
be_1  |       POST - /view/:viewId/items/status/:status
be_1  |       GET - /view/:viewId/rules
be_1  |       POST - /view/:viewId/rule/:ruleId/status/:status
be_1  |       POST - /view/:viewId/rules
be_1  |       GET - /pricingStructures
be_1  |       GET - /pricingStructuresWithItems/:pricingStructureId
be_1  |       POST - /pricingStructure/:pricingStructureId/status/:status
be_1  |       POST - /pricingStructures
be_1  |       POST - /view/:viewId/preview-bulk-edit
be_1  |       POST - /view/:viewId/bulk-edit
be_1  |       GET - /jobs
be_1  |       GET - /job/:jobId/details/:lastLogId?
be_1  |       GET - /job/:jobId/details
be_1  |       GET - /job/:jobId
be_1  |       POST - /view/:viewId/import/attributes
be_1  |       POST - /view/:viewId/import/items
be_1  |       POST - /view/:viewId/import/prices
be_1  |       POST - /view/:viewId/import/attributes/preview
be_1  |       POST - /view/:viewId/import/items/preview
be_1  |       POST - /view/:viewId/import/prices/preview
be_1  |       POST - /view/:viewId/export/attributes/preview
be_1  |       POST - /view/:viewId/export/items/preview
be_1  |       POST - /view/:viewId/export/pricingStructure/:pricingStructureId/prices/preview
be_1  |       POST - /view/:viewId/export/attributes
be_1  |       POST - /view/:viewId/export/items
be_1  |       POST - /view/:viewId/export/pricingStructure/:pricingStructureId/prices
be_1  |       POST - /user/:userId/dashboard/save
be_1  |       GET - /user/:userId/dashboard
be_1  |       POST - /user/:userId/dashboard-widget-instance-data
be_1  |       GET - /user/:userId/dashboard-widget-instance/:dashboardWidgetInstanceId
be_1  |       GET - /user/:userId/partner-pricing-structures
be_1  |       GET - /pricingStructure/:pricingStructureId/pricedItems
be_1  |       GET - /group/:groupName/search
be_1  |       GET - /search/status/:status/user/:username?
be_1  |       GET - /search/self-registration/:username?
be_1  |       GET - /view/:viewId/rule/:ruleId
be_1  |       GET - /attribute/:attributeId/view/:viewId
be_1  |       GET - /view/:viewId/items/:itemIds
be_1  |       GET - /view/:viewId/validations
be_1  |       GET - /view/:viewId/validation/:validationId
be_1  |       POST - /view/:viewId/validation
be_1  |       GET - /view/:viewId
be_1  |       GET - /user/:userId/settings
be_1  |       POST - /user/:userId/settings
be_1  |       GET - /custom-rules
be_1  |       GET - /view/:viewId/custom-rules
be_1  |       POST - /view/:viewId/custom-rules
be_1  |       POST - /view/:viewId/custom-rules/:customRuleId/status/:status
be_1  |       DELETE - /view/:viewId/custom-rules
be_1  |       GET - /user/:userId/notifications
be_1  |       POST - /user/:userId/notification
be_1  |       POST - /view/:viewId/attributes/add
be_1  |       GET - /view/:viewId/searchType/:searchType/search/:search?
be_1  |       DELETE - /view/:viewId/validation/:validationId
be_1  |       GET - /data-export/:dataExportId
be_1  |       GET - /pricingStructure/:pricingStructureId
be_1  |       GET - /data-export-artifacts
be_1  |       DELETE - /data-export-artifact/:dataExportArtifactId
be_1  |       POST - /item/:itemId/image
be_1  |       DELETE - /item/:itemId/image/:itemImageId
be_1  |       POST - /item/:itemId/image/:itemImageId/mark-primary
be_1  |       GET - /help/:helpPostfix
be_1  |       GET - /custom-imports
be_1  |       POST - /view/:viewId/custom-import/:customImportId/validate-input
be_1  |       POST - /view/:viewId/custom-import/:customImportId/preview
be_1  |       POST - /view/:viewId/custom-import/:customImportId/submit-job
be_1  |       GET - /custom-exports
be_1  |       POST - /view/:viewId/custom-export/:customExportId/validate-input
be_1  |       POST - /view/:viewId/custom-export/:customExportId/preview
be_1  |       POST - /view/:viewId/custom-export/:customExportId/submit-job
be_1  |       GET - /view/:viewId/pricingStructures
be_1  |       POST - /group
be_1  |       DELETE - /groups
be_1  |       GET - /pricing-structure-group-associations
be_1  |       GET - /pricing-structure/:pricingStructureId/groups-not-associated/:groupName?
be_1  |       POST - /pricing-structure/:pricingStructureId/group/:groupId/link
be_1  |       POST - /pricing-structure/:pricingStructureId/group/:groupId/unlink
be_1  |       GET - /pricing-structure/:pricingStructureId/groups-associated/:groupName?
be_1  |       GET - /view/:viewId/categories
be_1  |       DELETE - /view/:viewId/category/:categoryId
be_1  |       GET - /view/:viewId/categories-with-items
be_1  |       GET - /view/:viewId/category/:categoryId/items
be_1  |       POST - /view/:viewId/add-category
be_1  |       POST - /view/:viewId/update-category
be_1  |       POST - /view/:viewId/category/:categoryId/item/:itemId
be_1  |       DELETE - /view/:viewId/category/:categoryId/item/:itemId
be_1  |       GET - /view/:viewId/category/:categoryId/category-simple-items-in-category
be_1  |       GET - /view/:viewId/category/:categoryId/category-simple-items-not-in-category
be_1  |       POST - /forgot-password/code/:code/validity
be_1  |       POST - /forgot-password/code/:code/reset
be_1  |       POST - /forgot-password
be_1  |       GET - /custom-bulk-edits
be_1  |       POST - /view/:viewId/custom-bulk-edit/:customBulkEditId/preview
be_1  |       POST - /view/:viewId/custom-bulk-edit/:customBulkEditId/submit-job
be_1  |       POST - /view/:viewId/custom-bulk-edit/:customBulkEditId/validate-input
be_1  |       GET - /audit-log
be_1  |       GET - /view/:viewId/user/:userId/favourite-items
be_1  |       GET - /view/:viewId/user/:userId/favourite-item-ids
be_1  |       POST - /view/:viewId/user/:userId/add-favourite-items
be_1  |       DELETE - /view/:viewId/user/:userId/remove-favourite-items
be_1  |       GET - /view/:viewId/user/:userId/searchType/:searchType/search/:search?
be_1  | 
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - running db updater
be_1  | [07-21-2020 12:23:48 pm] - [<unknown>] - INFO - ** Running updater, profiles found [CORE, TEST-DATA]
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - script /usr/src/fuyuko/src/updater/scripts/0.0.1-create-tables.js has already been executed before, skip execution
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - script /usr/src/fuyuko/src/updater/scripts/0.0.2-create-core-data.js has already been executed before, skip execution
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - script /usr/src/fuyuko/src/updater/scripts/0.0.3-create-sample-users-data.js has already been executed before, skip execution
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - script /usr/src/fuyuko/src/updater/scripts/0.0.4-create-sample-test-data.js has already been executed before, skip execution
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - script /usr/src/fuyuko/src/updater/scripts/0.0.5-create-sample-cars-data.js profiles [CARS-DATA] does not match updater's profiles [CORE, TEST-DATA], skip execution
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - script /usr/src/fuyuko/src/updater/scripts/0.0.6-create-sample-leefahmee-data.js profiles [LEEFAHMEE-DATA] does not match updater's profiles [CORE, TEST-DATA], skip execution
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - done with db updater
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - running custom rule sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Running custom rule sync ...
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom rules script forward sync, files to db
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Rule file 0.0.1-sample-rule-1.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Rule file 0.0.2-sample-rule-2.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom rules script reverse sync, db to files
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db rule registry 0.0.1-sample-rule-1.js is in sync with rule script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db rule registry 0.0.2-sample-rule-2.js is in sync with rule script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Done custom rule sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - done with custom rule sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - running custom import sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Running custom import script sync ...
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom import scripts forward sync, files to db
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom import script file 0.0.1-sample-custom-import-1.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom import script reverse sync, db to files
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom import registry 0.0.1-sample-custom-import-1.js is in sync with custom import script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom import registry 0.0.2-sample-custom-import-2.js is in sync with custom import script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Done custom import script sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom import script file 0.0.2-sample-custom-import-2.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom import script reverse sync, db to files
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom import registry 0.0.1-sample-custom-import-1.js is in sync with custom import script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom import registry 0.0.2-sample-custom-import-2.js is in sync with custom import script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Done custom import script sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - done with custom import sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - running custom export sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Running custom export script sync ...
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom export scripts forward sync, files to db
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom export script file 0.0.1-sample-custom-export-1.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom export script reverse sync, db to files
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom export registry 0.0.1-sample-custom-export-1.js is in sync with custom export script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom export registry 0.0.2-sample-custom-export-2.js is in sync with custom export script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Done custom export script sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom export script file 0.0.2-sample-custom-export-2.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom export script reverse sync, db to files
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom export registry 0.0.1-sample-custom-export-1.js is in sync with custom export script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom export registry 0.0.2-sample-custom-export-2.js is in sync with custom export script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Done custom export script sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - done with custom export sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - running custom bulk edit sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Running custom bulk edit script sync ...
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom bulk edit scripts forward sync, files to db
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom bulk edit script file 0.0.1-sample-custom-bulk-edit-1.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom bulk edit script reverse sync, db to files
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom bulk edit registry 0.0.1-sample-custom-bulk-edit-1.js is in sync with custom bulk edit script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom bulk edit registry 0.0.2-sample-custom-bulk-edit-2.js is in sync with custom bulk edit script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Done custom bulk edit script sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom bulk edit script file 0.0.2-sample-custom-bulk-edit-2.js already registered before
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Custom bulk edit script reverse sync, db to files
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom bulk edit registry 0.0.1-sample-custom-bulk-edit-1.js is in sync with custom bulk edit script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Db custom bulk edit registry 0.0.2-sample-custom-bulk-edit-2.js is in sync with custom bulk edit script, no action required
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Done custom bulk edit script sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - done with custom bulk edit sync
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - registrying global event subscription
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - importing event subscription registry file /usr/src/fuyuko/src/service/event/custom-events-subscription/0.0.1-sample-event-subscription.js
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - importing event subscription registry file /usr/src/fuyuko/src/service/event/custom-events-subscription/1.0.0-audit-event-subscription.js
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - done with global event subscription
be_1  | 
be_1  |          ______                 _                 
be_1  |         |  ____|               | |                
be_1  |         | |__ _   _ _   _ _   _| | _____          
be_1  |         |  __| | | | | | | | | | |/ / _ \         
be_1  |  _ _ _  | |  | |_| | |_| | |_| |   < (_) |  _ _ _ 
be_1  | (_|_|_) |_|   \__,_|\__, |\__,_|_|\_\___/  (_|_|_)
be_1  |                      __/ |                        
be_1  |                     |___/     1.0.0-beta                    
be_1  |     
be_1  |     
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Fuyuko ready for operation !!!
be_1  | [07-21-2020 12:23:49 pm] - [<unknown>] - INFO - Fuyuko API started listening at port 8888

```

### DB

The database can be accessed using the following info :

| Property | Value |
| :--- | :--- |
| DB Host | localhost |
| Port | 3307 |
| DB Name | fuyuko |

### BE

Back end can be accessed using the following info, eg `http://localhost:8888/api/v1/heartbeat`:

| Property | Value |
| :--- | :--- |
| Host | localhost |
| Port | 8888 |

### FE

Front end can be access using the following info, eg. `http://localhost/`:

| Property | Value |
| :--- | :--- |
| Host | localhost |
| Port | 80 |

## Removing

To clean up allt the images and containers created run the following command 

```text
# assuming we are at <fuyuko-root>/docker-compose/ directory
$> docker-compose down
```

Following is the logs when `docker-compose down` is executed

```text
Removing dockercompose_fe_1 ... done
Removing dockercompose_be_1 ... done
Removing dockercompose_db_1 ... done
Removing network dockercompose_appnetwork
```


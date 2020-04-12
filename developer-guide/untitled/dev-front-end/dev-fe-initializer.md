# DEV - FE - Initializer

App initializer lies as a const function in `src/app/app.module.ts`, it gets called when the application starts up, registered as an `APP_INITIALIZER` provider in `app.module.ts`.

It does :

* Custom `init()` of services that needs it, happens when user login
* Custom `destroy()` of services that needs it, happens when user logout.




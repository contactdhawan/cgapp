# Cgapp

## Create a Angular app with routing (Unsecured)
1. Create a app `ng new cgapp --routing`
1. Delete app.component.html content and just keep `<router-outlet></router-outlet>`
1. Create a component `ng g c home`
1. Update `app.routing.module.ts` file to display Home component on default path
```
{
    path: '',
    component: HomeComponent
  }
```
1. Run `ng serve` and it should bring angular app

## Configuartion needed for MSAL
1. Using [Sample App](https://github.com/AzureAD/microsoft-authentication-library-for-js/blob/dev/samples/msal-angular-v2-samples/angular11-sample-app), update package.json file to include msal dependencies :-
```
"@azure/msal-angular": "^2.0.0-beta.2",
    "@azure/msal-browser": "^2.13.0",
```
1. Break app and run `npm install`
1. Run `ng serve` and application still be unsecured.
1. Update `app.routing.module.ts` and add auth Gaurd
```
 canActivate: [MsalGuard]
```

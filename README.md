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



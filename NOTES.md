## [Angular Router](https://angular.io/guide/router-tutorial-toh)

### Register Router & Routes

- import RouterModule from **@angular/router**
- Define an array of routes name _appRoutes_ & pass them in to the RouterModulkel.forRoot() method.

```
Registering the RouterModule.forRoot() in the AppModule imports array makes the Router service available everywhere in the application.
```

- Add the Router OutLet in app.component.html
  : The router outlet serves as a placeholder where the routed components are rendered.

- Add WildCard Route

  `{ path: '**', component: PageNotFoundComponent }`

- Add a Default Redirect Route

`{ path: '', redirectTo: '/heroes', pathMatch: 'full' },`

### Refactor the routing configuration into a routing module

- Create a file app-routing-module & follow the steps of **Register Router & Routes**

- Exports the RoduterModule:
  - By re-exporting the RouterModule here, the components declared in AppModule have access to router directives such as RouterLink and RouterOutlet else it will throw error **router-outlet' is not a known element:**

#Custom

First step: npm install -g @angular/cli

ng new <project_name> --style=scss --routing
(Routing flag will help us in creating routing file app-routing.module.ts, scss will make use of sass)

For material design we can also use "ng add @angular/material"

Now open the <project_name> folder in vs code(code .)

To run the project, simply use "ng serve -o"

We can generate our own components from CLI using "ng genereate component <component_name>" or "ng g c <name>"
(It will update app.module.ts and will create html,scss,.ts and spec files)

Main/Index component is app.component.html

We can embed one component into another using the selector defined in <name>.component.ts file


Now after editing style.scss, component's css, we can provide the routes in app-routing.module.ts by importing our components and editing Routes = [];


Now we want to fetch a list of users from public API, for that we will create a service by using Angular cli 
"ng generate service <service_name>". This will create test file and a service file(.spec.ts and .ts resp).
If we have a reusable code to be accessed between multiple components, then we can create service for it.When it comes to fetch result from public API/accessing the DB etc then we create a service file.
If we fant to fetch the result from a API, then we can use, angular6 internal http client.


After adding the service, we need to add http client module in app.module.ts
import { HttpClientModule } from '@angular/common/http';

Services cant be used all alone, they can be used by a component, so inside one component.ts file we will import the service and Observable(to hold data) . Now we need to call the service.
We can import ActivatedRoute for urls like /id

After the service call we will change the html of the component.

For adding animations we use npm i @angular/animations@latest --save
Now import in app module.

For deployment , run ng build (dist folder will be created)
For production deployment, run ng build --prod


In dist folder, open index.html and change <base href="/"> to: <base href="./">


# Ng6

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.1.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

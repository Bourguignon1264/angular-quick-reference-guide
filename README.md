# Angular Quick Reference Guide

## Installation and Setup:

1. Install Node.js (https://nodejs.org/)
2. Install Angular CLI: `npm install -g @angular/cli`
3. Create a new project: `ng new my-app`
4. Start the development server: `cd my-app`, `ng serve`

## Basic Concepts:

1. Components: Building blocks of an Angular app
2. Modules: Organize components, services, and other code
3. Templates: Define the UI layout and structure
4. Directives: Control DOM behavior
5. Services: Share data and logic across components
6. Dependency Injection: Manage dependencies in a modular way

## Components:

1. Create a new component: `ng generate component my-component`
2. Component decorator: `@Component`
3. Component template: Inline (`template`) or external (`templateUrl`)
4. Component styles: Inline (`styles`) or external (`styleUrls`)

## Data Binding:

1. Interpolation: `{{ variable }}`
2. Property binding: `[property]="expression"`
3. Event binding: `(event)="handlerMethod($event)"`
4. Two-way binding: `[(ngModel)]="variable"`

## Directives:

1. Structural directives: Manipulate the DOM structure
    * `*ngIf`: Conditionally display content (`<div *ngIf="condition">`)
    * `*ngFor`: Loop over a collection (`<div *ngFor="let item of items">`)
2. Attribute directives: Change appearance or behavior
    * `ngStyle`: Apply styles dynamically (`[ngStyle]="{'property': value}"`)
    * `ngClass`: Apply CSS classes dynamically (`[ngClass]="{'class': condition}"`)

## Services and Dependency Injection:

1. Create a new service: `ng generate service my-service`
2. Service decorator: `@Injectable`
3. Inject a service: Add to the constructor: `constructor(private myService: MyService) { }`
4. Use `providedIn: root` for app-wide services

## Routing:

1. Import `RouterModule` and `Routes` from `@angular/router`
2. Define routes: `const routes: Routes = [{ path: 'route', component: MyComponent }]`
3. Add `RouterModule.forRoot(routes)` to `@NgModule.imports`
4. Use `<router-outlet>` in the template for navigation
5. Navigate with `routerLink`: `<a routerLink="/route">`

## Forms:

1. Template-driven forms: Require `FormsModule`
    * Use `[(ngModel)]` for two-way binding
    * Use `#ref="ngModel"` for template reference
2. Reactive forms: Require `ReactiveFormsModule`
    * Use `FormBuilder` to create form controls
    * Use `FormGroup` and `FormControl` for form structure

## HTTP and Observables:

1. Import `HttpClientModule` from `@angular/common/http`
2. Inject `HttpClient` in a service: `constructor(private http: HttpClient) { }`
3. Use `.get()`, `.post()`, `.put()`, or `.delete()` for HTTP requests
4. Subscribe to observables: `.subscribe(data => { }, error => { })`

## Angular Best Practices:

1. Organize code in feature modules
2. Use lazy loading for better performance
3. Employ a shared module for common components
4. Write unit tests with Jasmine and Karma
5. Optimize for production with Ahead-of-Time (AOT) compilation: `ng build --prod`
6. Follow Angular Style Guide (https://angular.io/guide/styleguide)
7. Use Angular Material for a consistent UI design (https://material.angular.io/)
8. Keep templates clean and modular by utilizing pipes
9. Leverage Angular's built-in directives and avoid direct DOM manipulation
10. Utilize RxJS operators for more efficient handling of observables

This Angular quick reference guide provides a concise overview of the essential concepts and techniques to kick-start your journey with Angular. Use this cheat sheet as a starting point and gradually expand your knowledge by diving deeper into each topic, exploring the official Angular documentation, and practicing with hands-on examples.


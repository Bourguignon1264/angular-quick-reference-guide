Angular Quick Reference Guide

1. **Installation and Setup:**
   a. Install Node.js (https://nodejs.org/)
   b. Install Angular CLI: `npm install -g @angular/cli`
   c. Create a new project: `ng new my-app`
   d. Start the development server: `cd my-app`, `ng serve`

2. **Basic Concepts:**
   a. Components: Building blocks of an Angular app
   b. Modules: Organize components, services, and other code
   c. Templates: Define the UI layout and structure
   d. Directives: Control DOM behavior
   e. Services: Share data and logic across components
   f. Dependency Injection: Manage dependencies in a modular way

3. **Components:**
   a. Create a new component: `ng generate component my-component`
   b. Component decorator: `@Component`
   c. Component template: Inline (`template`) or external (`templateUrl`)
   d. Component styles: Inline (`styles`) or external (`styleUrls`)

4. **Data Binding:**
   a. Interpolation: `{{ variable }}`
   b. Property binding: `[property]="expression"`
   c. Event binding: `(event)="handlerMethod($event)"`
   d. Two-way binding: `[(ngModel)]="variable"`

5. **Directives:**
   a. Structural directives: Manipulate the DOM structure
      - *ngIf: Conditionally display content (`<div *ngIf="condition">`)
      - *ngFor: Loop over a collection (`<div *ngFor="let item of items">`)
   b. Attribute directives: Change appearance or behavior
      - ngStyle: Apply styles dynamically (`[ngStyle]="{'property': value}"`)
      - ngClass: Apply CSS classes dynamically (`[ngClass]="{'class': condition}"`)

6. **Services and Dependency Injection:**
   a. Create a new service: `ng generate service my-service`
   b. Service decorator: `@Injectable`
   c. Inject a service: Add to the constructor: `constructor(private myService: MyService) { }`
   d. Use providedIn: `root` for app-wide services

7. **Routing:**
   a. Import `RouterModule` and `Routes` from `@angular/router`
   b. Define routes: `const routes: Routes = [{ path: 'route', component: MyComponent }]`
   c. Add `RouterModule.forRoot(routes)` to `@NgModule.imports`
   d. Use `<router-outlet>` in the template for navigation
   e. Navigate with `routerLink`: `<a routerLink="/route">`

8. **Forms:**
   a. Template-driven forms: Require `FormsModule`
      - Use `[(ngModel)]` for two-way binding
      - Use `#ref="ngModel"` for template reference
   b

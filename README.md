Angular Quick Reference Guide
Installation and Setup:

    Install Node.js (https://nodejs.org/)
    Install Angular CLI: npm install -g @angular/cli
    Create a new project: ng new my-app
    Start the development server: cd my-app, ng serve

Basic Concepts:

    Components: Building blocks of an Angular app
    Modules: Organize components, services, and other code
    Templates: Define the UI layout and structure
    Directives: Control DOM behavior
    Services: Share data and logic across components
    Dependency Injection: Manage dependencies in a modular way

Components:

    Create a new component: ng generate component my-component
    Component decorator: @Component
    Component template: Inline (template) or external (templateUrl)
    Component styles: Inline (styles) or external (styleUrls)

Data Binding:

    Interpolation: {{ variable }}
    Property binding: [property]="expression"
    Event binding: (event)="handlerMethod($event)"
    Two-way binding: [(ngModel)]="variable"

Directives:

    Structural directives: Manipulate the DOM structure
        *ngIf: Conditionally display content (<div *ngIf="condition">)
        *ngFor: Loop over a collection (<div *ngFor="let item of items">)
    Attribute directives: Change appearance or behavior
        ngStyle: Apply styles dynamically ([ngStyle]="{'property': value}")
        ngClass: Apply CSS classes dynamically ([ngClass]="{'class': condition}")

Services and Dependency Injection:

    Create a new service: ng generate service my-service
    Service decorator: @Injectable
    Inject a service: Add to the constructor: constructor(private myService: MyService) { }
    Use providedIn: root for app-wide services

Routing:

    Import RouterModule and Routes from @angular/router
    Define routes: const routes: Routes = [{ path: 'route', component: MyComponent }]
    Add RouterModule.forRoot(routes) to @NgModule.imports
    Use <router-outlet> in the template for navigation
    Navigate with routerLink: <a routerLink="/route">

Forms:

    Template-driven forms: Require FormsModule
        Use [(ngModel)] for two-way binding
        Use #ref="ngModel" for template reference
    Reactive forms: Require ReactiveFormsModule
        Use FormBuilder to create form controls
        Use FormGroup and FormControl for form structure

HTTP and Observables:

    Import HttpClientModule from @angular/common/http
    Inject HttpClient in a service: constructor(private http: HttpClient) { }
    Use .get(), .post(), .put(), or .delete() for HTTP requests
    Subscribe to observables: .subscribe(data => { }, error => { })

Angular Best Practices:

    Organize code in feature modules
    Use lazy loading for better performance
    Employ a shared module for common components
    Write unit tests with Jasmine and Karma
    Optimize for production with Angular CLI build options.

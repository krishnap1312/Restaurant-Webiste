Here is the complete markdown file answering all your Angular-related questions:

```markdown
# Angular Interview Questions and Answers

### 1. **What is Angular, and how does it differ from AngularJS?**
   Angular is a platform and framework for building client-side applications using HTML, CSS, and TypeScript. Angular is a complete rewrite of AngularJS, improving performance, modularity, and modern development practices. Angular uses TypeScript, while AngularJS was based on JavaScript. 

### 2. **Explain the core architecture of Angular.**
   Angular's architecture is based on:
   - **Components**: Building blocks of UI.
   - **Modules**: Containers for related components and services.
   - **Directives**: Custom HTML attributes used to manipulate DOM.
   - **Services**: Singleton objects used to share code and data across components.
   - **Dependency Injection**: Design pattern used for injecting dependencies into components and services.

### 3. **What is a component in Angular, and how do you create one?**
   A component is a core building block that controls a section of the UI. It consists of:
   - HTML template
   - TypeScript class
   - CSS styles
   To create one, use:
   ```bash
   ng generate component component-name
   ```

### 4. **What are Angular directives? Name the types of directives.**
   Directives are instructions in the DOM. Types:
   - **Structural Directives**: Modify DOM structure (e.g., `*ngIf`, `*ngFor`).
   - **Attribute Directives**: Modify element behavior or appearance (e.g., `ngClass`, `ngStyle`).

### 5. **What is data binding in Angular? Explain the different types.**
   Data binding is the communication between the component and the DOM. Types:
   - **Interpolation**: `{{ value }}`
   - **Property binding**: `[property]="value"`
   - **Event binding**: `(event)="handler"`
   - **Two-way binding**: `[(ngModel)]="value"`

### 6. **What is a template in Angular?**
   A template defines the HTML structure of the view and includes Angular-specific syntax to bind data.

### 7. **Explain what two-way data binding is and how it’s achieved in Angular.**
   Two-way data binding allows synchronization between the model and the view. It is achieved using `[(ngModel)]="property"`.

### 8. **What is dependency injection in Angular?**
   Dependency Injection (DI) is a design pattern in Angular to inject services or objects into components and other services. This allows better modularity and easier testing.

### 9. **How do you use the Angular CLI to create a new project?**
   Use the following command:
   ```bash
   ng new project-name
   ```

### 10. **What is a module in Angular?**
   A module is a container that groups related components, services, and directives. The root module is `AppModule`.

### 11. **What are Angular services, and how are they used?**
   Services are classes that provide functionality across components, such as data retrieval or logging. They are injected via DI.

### 12. **Explain the role of the @NgModule decorator.**
   `@NgModule` is a decorator that defines an Angular module by configuring metadata for components, services, and other providers.

### 13. **What is routing in Angular?**
   Routing allows navigation between different views or components based on URL. The `RouterModule` is used to configure routes.

### 14. **How do you set up routing between different components in Angular?**
   In `app.module.ts`, import `RouterModule` and configure routes:
   ```typescript
   const routes: Routes = [
     { path: 'home', component: HomeComponent },
     { path: 'about', component: AboutComponent }
   ];
   ```

### 15. **What is the difference between constructor and ngOnInit() in Angular?**
   - **Constructor**: Initializes class members, injected services, but doesn’t have access to Angular bindings.
   - **ngOnInit()**: Lifecycle hook called after component initialization, where binding to template occurs.

### 16. **What is interpolation in Angular?**
   Interpolation allows embedding expressions inside `{{ }}` in templates to display dynamic data.

### 17. **What is a pipe in Angular?**
   Pipes transform data in templates. Example: `{{ date | date:'short' }}`.

### 18. **How do you define a custom pipe in Angular?**
   Use `@Pipe` decorator and implement `transform` method:
   ```typescript
   @Pipe({name: 'customPipe'})
   export class CustomPipe implements PipeTransform {
     transform(value: string): string {
       return value.toUpperCase();
     }
   }
   ```

### 19. **What is ngIf and ngFor in Angular?**
   - `ngIf`: Conditionally includes a template.
   - `ngFor`: Iterates over a collection and creates a template for each item.

### 20. **What is an observable in Angular, and how does it work with data streams?**
   Observables are data streams that allow async data handling. They are used in services like `HttpClient` to handle API responses.

### 21. **What is the purpose of the package.json file in an Angular project?**
   `package.json` lists dependencies, scripts, and configurations for the Angular project.

### 22. **How do you make HTTP requests in Angular?**
   Use the `HttpClient` service for making HTTP requests:
   ```typescript
   this.http.get('api/url').subscribe(response => console.log(response));
   ```

### 23. **What is Angular’s HttpClient module?**
   `HttpClient` is a built-in service for making HTTP requests in Angular and is part of `HttpClientModule`.

### 24. **How do you use the ngModel directive in Angular forms?**
   `ngModel` binds form inputs to component properties for two-way data binding.

### 25. **Explain the difference between template-driven forms and reactive forms.**
   - **Template-driven forms**: Defined using directives in the template.
   - **Reactive forms**: Defined programmatically using `FormGroup` and `FormControl`.

### 26. **What is the Angular Router, and how does it work?**
   The Angular Router is a service for navigating between views or pages based on URL paths.

### 27. **What is lazy loading in Angular?**
   Lazy loading is a technique where Angular modules are loaded only when needed, improving app performance.

### 28. **What is the purpose of the ng-content directive?**
   `ng-content` allows insertion of content from a parent component into a child component.

### 29. **Explain the purpose of Angular’s @Input() and @Output() decorators.**
   - `@Input()`: Allows data to be passed from a parent to a child component.
   - `@Output()`: Emits events from the child to the parent component.

### 30. **What is the role of the app.module.ts file in an Angular application?**
   It defines the root module of the application and registers all necessary components, services, and other modules.

### 31. **How do you handle errors in Angular applications?**
   You can handle errors using `catchError` in RxJS or by providing an error handler service globally using `ErrorHandler`.

### 32. **What are structural directives? Give examples.**
   Structural directives alter the DOM structure. Examples: `*ngIf`, `*ngFor`, `*ngSwitch`.

### 33. **What is an Angular service, and why would you use it?**
   Services are used for business logic and data management, and they are singleton instances shared across components.

### 34. **What is the purpose of @Injectable() in Angular?**
   `@Injectable()` marks a class as available for DI, allowing Angular to inject it wherever needed.

### 35. **How does Angular handle browser events?**
   Angular handles browser events via event binding: `(event)="handler()"`.

### 36. **What is ngClass and ngStyle in Angular?**
   - `ngClass`: Dynamically adds/removes CSS classes.
   - `ngStyle`: Dynamically applies inline styles.

### 37. **What is change detection in Angular?**
   Change detection is the process by which Angular updates the view in response to data changes.

### 38. **What is the Angular lifecycle, and what are the key lifecycle hooks?**
   Angular lifecycle hooks control how a component is initialized, updated, and destroyed. Key hooks:
   - `ngOnInit()`
   - `ngOnChanges()`
   - `ngOnDestroy()`

### 39. **Explain how you would pass data between parent and child components.**
   Use `@Input()` to pass data from parent to child and `@Output()` to emit events from child to parent.

### 40. **What is a guard in Angular routing, and what are its types?**
   Guards control access to routes:
   - `CanActivate`: Controls access to a route.
   - `CanDeactivate`: Checks before leaving a route.
   - `Resolve`: Pre-fetches route data.

### 41. **How do you handle forms in Angular?**
   You can handle forms using template-driven or reactive forms depending on complexity.

### 42. **What is the difference between observable.subscribe() and observable.toPromise() in Angular?**
   - `subscribe()`: Used to listen to observable data streams.
   - `toPromise()`: Converts observable into a promise and resolves

 it.

### 43. **What is the purpose of the angular.json file?**
   `angular.json` contains configurations for the project, such as build and serve settings.

### 44. **How do you implement navigation in an Angular app using the routerLink directive?**
   Use `routerLink` for internal navigation:
   ```html
   <a [routerLink]="['/path']">Go to path</a>
   ```

### 45. **What is zone.js in Angular?**
   Zone.js is a library that Angular uses to track and detect asynchronous tasks and trigger change detection.

### 46. **Explain the use of the async pipe in Angular templates.**
   `async` pipe automatically subscribes to an observable and renders the latest emitted value.

### 47. **What is the role of polyfills in Angular?**
   Polyfills allow Angular to support older browsers by emulating modern browser features.

### 48. **What are template reference variables in Angular?**
   Template reference variables are used to access a DOM element or a directive in a template.

### 49. **What is a single-page application (SPA), and how does Angular fit into this concept?**
   An SPA dynamically updates the page content without reloading the page. Angular supports SPAs with its routing system.

### 50. **How do you install third-party libraries in an Angular application?**
   Use npm to install third-party libraries:
   ```bash
   npm install library-name
   ```
```

This markdown file includes answers to all your Angular-related questions.
```

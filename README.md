# Angular Learning Path (v15+)

This modular, hands-on curriculum is organized into progressive weekly modules (inspired by the Full Stack Open style). Each module introduces key Angular concepts with practical projects and free resources. Learners should have basic HTML/CSS/JavaScript knowledge; Angular uses TypeScript (a quick TS tutorial is recommended). Primary focus is on Angular (latest version), with optional light backend integration (e.g. Firebase or simple Node/Express). Each module lists **resources** (official docs, videos, tutorials) and **project ideas** to reinforce learning.

## Module 1: Introduction & Setup

**Topics:** Angular overview, project structure, Node.js/TypeScript setup, Angular CLI, creating your first app, components concept, development server.

* **Angular CLI & Workspace** – Install Node.js and use the Angular CLI (`ng new`) to scaffold a workspace and run `ng serve`. The Angular CLI “is a command-line interface tool which allows you to scaffold, develop, test, deploy, and maintain Angular applications”. It gets your project up and running in under a minute.
* **Components & Modules (intro)** – Each Angular app is a tree of components (with HTML templates, CSS, and TypeScript classes) and NgModules. Components keep code modular and testable.
* **TypeScript Basics** – Review TypeScript syntax (classes, typing) via a free tutorial, since Angular code is written in TS.
* **Resources:**

  * **Official Angular Getting Started** – The Angular “Get Started” guide (angular.dev) covers installation of the CLI and creating a new app.
  * **Angular CLI Guide (docs)** – Official CLI overview explains creating workspaces and basic commands.
  * **YouTube – Academind “Setup with Angular CLI”** – Maximilian Schwarzmüller’s free playlist covers CLI setup (see Academind Getting Started with Angular).
  * **Video Tutorial – freeCodeCamp Crash Course** – (e.g. Beau Carnes’ “Learn Angular” video) provides a fast-paced introduction.
  * **Interactive Try-Angular** – Use StackBlitz or Angular’s online playground (see *Try it now!* via angular.dev) to experiment without installing.
* **Projects:**

  * **“Hello Angular” app** – Use the CLI to create a new project, modify the default AppComponent template, and serve it locally.
  * **Tic-Tac-Toe game (beginner)** – Build a simple Tic-Tac-Toe component. (Fireship’s Angular course even includes a Tic-Tac-Toe project.) This exercises components and templates.
  * **Basic To-Do List** – Create a small component-based to-do list (hard-coded items) to practice Angular binding and component structure.

## Module 2: Components, Templates, and Data Binding

**Topics:** Component architecture, @Component decorator, templates (interpolation, property/event binding), data binding (one-way vs two-way), @Input/@Output for parent-child communication, structural directives (`*ngIf`, `*ngFor`), pipes.

* **Components & Templates** – Build and nest components. Each component consists of a TypeScript class (logic) and HTML template (view). Templates use data binding to display component data. Angular’s component model and dependency injection help keep code modular and testable.
* **Data Binding** – Learn interpolation (`{{}}`), property binding (`[src]`), and event binding (`(click)`). Angular supports one-way data binding (for read-only data) and two-way binding (`[(ngModel)]`) for form inputs.
* **Directives and Pipes** – Use structural directives like `*ngIf`/`*ngFor` to control the DOM. Use built-in pipes (date, uppercase, etc.) to format data.
* **Resources:**

  * **Angular Official Docs – Components & Templates** – The Angular “Components” guide (angular.dev/guide/components) and “Templates” guide cover how to write components and bind data.
  * **Angular Tutorial (Tour of Heroes)** – The official tutorial’s early steps teach components and data binding (see *“Tour of Heroes”* introduction).
  * **Academind Series** – Maximilian’s free videos “Components & Modules” and “Lists, Events & Databinding” from the Getting Started playlist.
  * **freeCodeCamp – Angular Basics** – Free crash course video on components and binding.
* **Projects:**

  * **Product or Contact List** – Create a component that displays a list of items (e.g. products, contacts) using `*ngFor`. Use interpolation to show item properties and buttons to interact.
  * **Nested Components** – Build a parent-child component pair (e.g. *UserListComponent* and *UserDetailComponent*) and pass data via @Input and @Output. Practice event binding (click events) to select an item.

## Module 3: Services, Dependency Injection & HTTP

**Topics:** Angular services, dependency injection (DI), Injectable services, singleton data stores. Using the `HttpClient` to fetch data from APIs (REST or Firebase). Async data with RxJS Observables.

* **Services & DI** – Create injectable services (`@Injectable`) to share data or logic across components. Angular’s dependency injection system lets you provide a service at the module or component level. For example, a `DataService` can fetch or store app data.
* **HttpClient** – Use `@angular/common/http`’s `HttpClient` service to communicate with a back end via HTTP. Most front-end apps need server communication; Angular provides an `HttpClient` API for this. Learn GET/POST requests, and handle asynchronous responses with Observables.
* **Async & Observables** – HTTP calls return RxJS Observables. Learn basic RxJS (subscribe, map, etc.) to process data. In reactive forms (next module) you’ll also use Observables.
* **Resources:**

  * **Angular Official Docs – Services & HTTP** – The “Dependency Injection” guide (angular.dev/guide/dependency-injection) and “HTTP Client” guide explain services and HTTP calls.
  * **Angular HTTP & Firebase Codelab** – Google’s free Codelab *“Building a web app with Angular and Firebase”* walks through using Angular Material, adding Firebase/Firestore, and deploying. It teaches using the CLI and services to build a Kanban board.
  * **Academind / Codevolution** – Search for “Angular HTTP tutorial” (Academind has free videos on services and HttpClient).
  * **freeCodeCamp** – Any Angular course covering fetching data (e.g. using JSONPlaceholder API).
* **Projects:**

  * **API Data App** – Build a component that fetches and displays data from a public API. Examples: a list of GitHub users, a weather widget (fetch from OpenWeatherMap), or posts from JSONPlaceholder.
  * **Firebase or Node Backend** – (Optional) Use Firebase (Firestore) or set up a simple Node/Express JSON server to serve data. For example, adapt the Kanban Codelab to practice reading/writing to Firestore.
  * **Service Demo** – Turn one of your earlier projects (e.g. To-Do list) into a service-backed app: store the to-dos in a service, and fetch them in the component using `HttpClient`.

## Module 4: Routing & Navigation

**Topics:** Angular Router for single-page apps. Configuring routes, `<router-outlet>`, navigation links (`routerLink`), route parameters, nested routes, lazy loading feature modules, and route guards (basic intro).

* **Angular Router** – Set up client-side routes so your app can have multiple views (pages). Define routes in a routing module and use `<router-outlet>` in the template. Angular’s router “provides a feature-rich navigation toolkit, including support for route guards, data resolution, lazy-loading, and much more”.
* **Navigation & Params** – Create navigation menus with `[routerLink]`. Learn to read route parameters or query parameters in a component. Protect routes with basic guard (e.g. only show a route if a user is logged in).
* **Resources:**

  * **Angular Official Docs – Routing & Navigation** – The Angular Router documentation (angular.dev/guide/router) and tutorial (the router section of Tour of Heroes) explain basic routing.
  * **Academind / Fireship** – Free video tutorials on Angular routing. For example, Fireship’s Angular tutorial covers adding Router.
  * **freeCodeCamp Crash Course** – Many full-course videos include a section on routing.
* **Projects:**

  * **Multi-Page App** – Turn a previous project into a multi-route app. For example, create *Home*, *Items*, *About* components and navigate between them. Pass an item ID in the URL and fetch that item’s details on a detail view.
  * **Lazy-Loaded Feature** – (Advanced) Create an Angular feature module and configure it to load lazily when its route is accessed. For example, a separate *AdminModule* that is lazy-loaded.
  * **Route Guard Example** – If you implemented a login form, protect certain routes using a simple guard that checks an “isLoggedIn” flag.

## Module 5: Forms & Validation

**Topics:** Template-driven forms vs Reactive forms, form controls (`FormGroup`, `FormControl`), validation (built-in validators, custom validators), handling form events, form styling.

* **Template-driven Forms** – Use Angular directives (`ngModel`) in your template-driven form for simple scenarios.
* **Reactive Forms** – Learn the model-driven approach: define a `FormGroup` and `FormControl`s in your component. Angular’s reactive forms “provide a model-driven approach to handling form inputs” and are built on observable streams. Reactive forms give you synchronous access to form data and easier validation logic.
* **Validation** – Implement built-in validators (e.g. required, email) and display validation messages in the template. Explore Angular’s async validators if needed.
* **Resources:**

  * **Angular Official Docs – Forms** – The Reactive Forms guide (angular.dev/guide/forms/reactive-forms) and Template-driven Forms guide cover both approaches.
  * **Angular Overview – Forms** – As noted, “Angular’s forms module provides a standardized system for form participation and validation”.
  * **Tutorials** – Academind and freeCodeCamp have tutorials on building forms in Angular (Reactive Forms crash courses, etc.).
* **Projects:**

  * **User Input Form** – Create a form for user input (e.g. registration or contact form). Use reactive forms, apply validation, and display validation feedback.
  * **Search/Filter Form** – Add a search input to a component from Module 2/3 and use it to filter displayed items in real time (use reactive form `valueChanges` Observable for live filtering).

## Module 6: Angular Material & Styling

**Topics:** Angular Material component library, CDK, theming, layout. Using Material components (buttons, toolbar, cards, forms, tables, dialogs), and responsive design (Flex Layout or CSS).

* **Angular Material** – Install `@angular/material` via `ng add`. Learn core Material components (toolbar, menu, cards, form fields, snack-bars, etc.) and theming. The Component Dev Kit (CDK) provides utilities (accessibility, drag-and-drop, overlays). The Google codelab teaches this in context: “How to use Angular Material and the CDK”.
* **Styling** – Use Angular’s recommended styling: component-scoped styles or global themes. Incorporate SCSS or CSS frameworks if desired.
* **Resources:**

  * **Angular Material Docs** – Official docs (material.angular.io) have a Getting Started guide and component documentation.
  * **Tutorials (Fireship/Academind)** –

    * Fireship “Meet Angular Material” and “Material Schematics” chapters outline how to add Material to your app.
    * Google’s codelab *Kanban* shows adding a Material toolbar and icons.
  * **freeCodeCamp / YouTube** – Many Angular courses include a segment on Angular Material UI.
* **Projects:**

  * **Material Dashboard** – Refactor a previous project (e.g. the item list) to use Angular Material components: add a `mat-toolbar` navigation, display items in `mat-card` or `mat-table`, and style with Angular Material theme.
  * **Dialog & Form** – Use a Material Dialog or `MatDialog` to implement a popup form (e.g. “Add Item” dialog).
  * **Responsive Layout** – Practice using Flex Layout or CSS Grid with Material components to ensure the app looks good on mobile and desktop.

## Module 7: RxJS & Advanced Data Management

**Topics:** Introduction to RxJS Observables in Angular. Common operators (`map`, `filter`, `switchMap` etc.), Subjects and BehaviorSubjects, state management basics (service + Observables).

* **Observables in Angular** – Angular’s APIs (HttpClient, Forms, Router events) return RxJS Observables. Practice subscribing to Observables and using operators. For example, HTTP calls return Observables you can `subscribe()` to get data.
* **Reactive Patterns** – Use `Subject` or `BehaviorSubject` in a service to maintain app state (e.g. a current user or settings). Components subscribe to these Observables for updates. This mimics simple state management without a full library.
* **Resources:**

  * **RxJS Documentation** – The official RxJS docs (rxjs.dev) and Angular’s “Using RxJS with Angular” guide cover Observable basics.
  * **Tutorials** –

    * Academic courses on RxJS (e.g. official “RxJS in 100 seconds” by Fireship on YouTube).
    * Articles or videos on “Angular + RxJS”, many freeCodeCamp articles and YouTube channels (Academind, Fireship) have intros.
* **Projects:**

  * **Live Search Feature** – Enhance a list component with a live search box. Use `FormControl.valueChanges` (an Observable) with `debounceTime` and `filter` to update the list as the user types.
  * **Data Stream** – Build a component that displays data from an Observable source (e.g. a clock or timer using `interval()`, or live stock prices from a public API if available).
  * **Shared State Service** – Create a simple “current selection” service using a `BehaviorSubject`. For example, clicking an item in one component updates the service, and another component (on a different route) subscribes and displays details of the selected item.

## Module 8: Testing & Deployment

**Topics:** Unit testing with Jasmine/Karma (or Jest), end-to-end testing (Protractor/Cypress intro). Building and deploying: using Angular CLI (`ng build`/`ng deploy`), hosting (GitHub Pages, Firebase, Netlify, etc.).

* **Unit Testing Basics** – Learn to write basic unit tests for components and services. Angular projects include Jasmine/Karma setup by default. Write a simple spec for a component method or service.
* **End-to-End (E2E) Testing** – (Overview) Angular CLI sets up Protractor for E2E testing. You can also use Cypress as an alternative. Try writing one E2E test (e.g. check navigation flow).
* **Deployment** – Use the Angular CLI to build a production bundle (`ng build --prod`). Then deploy to a static hosting. The Google codelab shows deploying to Firebase Hosting with a single command. You can also deploy to GitHub Pages (`ng deploy --base-href`) or Netlify (drag-and-drop build output).
* **Resources:**

  * **Angular Official Docs – Testing** – The Angular Testing guide (angular.dev/guide/testing) covers unit and integration tests.
  * **Tutorials** – Medium posts and video tutorials exist for “Angular testing tutorial”.
  * **Deployment Guides** –

    * Angular CLI Command Reference (docs) for `ng deploy`.
    * Free guides for Firebase Hosting or GitHub Pages (e.g. use the `angular-cli-ghpages` tool for GitHub Pages).
    * The Firebase codelab mentions deployment: at the end it shows deploying the Kanban app to Firebase Hosting.
* **Projects:**

  * **Add Tests** – Pick one small feature from earlier modules (e.g. a form validation method or a utility service) and write a few Jasmine unit tests for it.
  * **Deploy an App** – Take a completed project (for example, your Angular Material dashboard or Kanban) and deploy it. For Firebase: run `ng add @angular/fire` and `ng deploy --hosting`. For GitHub Pages: install `angular-cli-ghpages` and deploy. Ensure the deployed app loads correctly.

## Final Project: Full-Featured Angular App

Combine everything you’ve learned into one larger project. Choose a real-world app idea that integrates components, routing, services, forms, and UI components. Examples:

* **Kanban/Task Manager** – Build a Trello-like board. Use Angular Material cards, drag-and-drop (CDK), a Firebase or mock backend for tasks, multiple routes (e.g. board list, board detail), and reactive forms to create/edit tasks. (Google’s tutorial builds a Kanban with Angular + Firestore.)
* **E-Commerce Store** – Develop a small store app. Components for product listing, product details, and cart. Use routing for product pages, services/HTTP to fetch products, a form for checkout, and Material design for a polished UI.
* **Blog or News App** – Create a blog reader. Use HTTP to fetch posts, router for individual post pages, a form for creating new posts (stored in Firebase or local storage), and Material for layout (cards, navigation).

Your final project should demonstrate:

* A well-structured Angular app with multiple components and modules.
* Routing between views.
* Data fetching via HttpClient (or Firebase) and use of Observables.
* Reactive forms with validation (e.g. login or data entry forms).
* Angular Material UI components and responsive layout.
* At least basic unit tests on one component or service.
* Deployed live (e.g. Firebase Hosting or GitHub Pages) for a real-world feel.

For inspiration, see Google’s Angular+Firebase Kanban codelab, which culminates in a working PWA deployed online. Use all the documentation and tutorials from earlier modules as references when building your project.

**Citations:** Key concepts are drawn from Angular’s official documentation and tutorials. Each resource above is free and authoritative (Angular docs, Google Codelabs, and well-known tutorial channels).


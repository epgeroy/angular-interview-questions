# Angular Interview Questions

A complete guideline to prepare for angular interviews. Also, you can use these questions to verify your expertise in angular. 



## Table of Contents
* [Assess Your Skill Level](#assess-your-skill-level)
* [Know the Interviewer](#know-the-interviewer)
* [Novice Level Questions](#novice-level)
    * [Familiarity to Basic Terminology](#familiarity-to-basic-terminology)
    * [Ability to Build Simple App](#ability-to-build-simple-app-questions)
    * [Understanding Basic Concepts](#understanding-basic-concepts-questions)
* [Intermediate Level Questions](#intermediate-level)
    * [Essential Terminology](#essential-terminology-questions)
    * [Comfortability to Build Medium Size App](#comfortability-to-build-medium-size-app-questions)
    * [Core Concepts Understandability](#core-concepts-understandability-questions)
* [Expert Level Questions](#expert-level)
    * [Performance and Edge Case Related Terminology](#performance-and-edge-case-related-terminology)
    * [Master a Large App](#master-a-large-app)
    * [Rock star and Fighter for angular](#rockstar-and-fighter-for-angular-questions)
* [Coding Test Question](#coding-test)
    * [Fetch Data and Display User Profile](#fetch-data-and-display-user-profile)
    * [Persistent Todo List](#persistent-todo-list)
    * [Student Registration System](#student-registration-system)
* [Side Things Related Questions](#side-things-related-questions)
    * [rxjs](#rxjs)
    * [TypeScript](#typescript)
    * [angular-cli](#angular-cli)
    * [others](#others)
* [Note from God](#note-from-god)



## Assess Your Skill Level
The most important step is knowing how you compare to other job seekers. Pinpoint areas where you are weaker, and spend the time necessary to make improvements. Google is your friend.

* **Novice** - You can create an Angular app using angular-cli or other popular project seeds, you have a basic understanding of components, modules, pipes, services, etc. If you don't have a clue what I am talking about, watch this [video](https://www.youtube.com/watch?v=rOr1r1rSZQ8) and get up to speed.
* **Intermediate** - You have a fully functional app that is deployed somewhere and/or published code in github, and you are comfortable with routing, authorization, feature modules, architecture, style guide, etc.
* **Expert** - You have mastered lazy loading, AOT, custom directives, deployment configuration, extending core features, etc.
* **Everyone Else** - You are either angular blind or an angular rock star. 


## Know the Interviewer
Do yourself a favor—Google the interviewer. Look at his/her Linkedin profile. Check his/her youtube videos, crappy old blog that hasn't been updated in years, and github profile. After your research, try to put the interviewer in one of the following categories:
1. Lazy interviewers wil ask about terminology. Sometimes they just Google and ask questions from there. If your interviewer is older and out of touch with the current development landscape, there is a greater chance that he/she will ask questions related to terminology.
2. More modest and nicer interviewers will be interested in what you know and whether you can get the job done. For this kind of interviewer look at the How category questions (I'm unsure what you are trying to say here)
3. Experienced interviewers (those who have been senior developers for a long time and have recently updated blogs and videos) want to know that you can think critically, and he will be interested in your process for decision making. These interviewers love to prove you wrong. One important tip: don't try to prove them wrong.

Researching relevant team members on LinkedIn and github can be useful as well.

## Novice Level

At this level an interviewer wants to know whether the interviewee is a coachable self-learner. Hence, he/she might ask questions about basic terminology, your ability to build a simple app, and your comprehension of basic concepts.  


### Familiarity of Basic Terminology
1. What are the differences between AngularJS (angular 1.x) and Angular (Angular 2.x and beyond)?
    1. Mobile driven, mobile support was keept in mind while writing the framework.

    2. Component based, the idea of controller does not exist anymore, only components, those can be smart components or dumb components.

    3. Performance, Angular is to 5 times faster than AngularJS.

    4. Languaje support, Angular support many languajes, been TypeScript the most popular among them.

2. What is a component? Why would you use it?

    Components are the most basic building block of an UI in an Angular application. An Angular application is a tree of Angular components. Angular components are a subset of directives. Unlike directives, components always have a template and only one component can be instantiated per an element in a template.

3. What is the minimum definition of a component?

    The absolute minimal configuration for a @Component in angular is a template. Both template properties are set to optional because you have to define either template or templateUrl.

4. What is a module, and what does it contain?

    Every Angular app has at least one NgModule class, the root module, conventionally named AppModule. Is a piece of code that contains Components, Directives, Services, Values and Functions.

5. What is a service, and when will you use it?
    It's a component like object used to comunicate between interfaces and smart components.

6. What is a promise? Explain it laymen's terms.

    It's an object that represents a not yet avaidable value, but it will be in near future. It allows to write asynchronus code in a synchronus way.

7. What are the lifecycle hooks for components and directives?

    1. ngOnChanges(): Respond when Angular (re)sets data-bound input properties. The method receives a SimpleChanges object of current and previous property values.

    2. ngOnInit(): Initialize the directive/component after Angular first displays the data-bound properties and sets the directive/component's input properties.

    3. ngDoCheck(): Detect and act upon changes that Angular can't or won't detect on its own.

    4. ngAfterContentInit(): Respond after Angular projects external content into the component's view. A component-only hook.

    5. ngAfterContentChecked(): Respond after Angular checks the content projected into the component. A component-only hook.

    6. ngAfterViewInit(): Respond after Angular initializes the component's views and child views. A component-only hook.

    7. ngAfterViewChecked(): Respond after Angular checks the component's views and child views. A component-only hook.

    8. ngOnDestroy(): Cleanup just before Angular destroys the directive/component. Unsubscribe Observables and detach event handlers to avoid memory leaks. Called just before Angular destroys the directive/component.

8. What are pipes? Give me an example.

    Pipes are presentation formatters used to format a value in a convenient way for the presentation i.e. | uppercase formatts the input string into an uppercased string.

9. What are the differences between reactive forms and template driven forms?

    Template driven forms are:

        1. Easy to use

        2. Similar to AngularJS

        3. Two way data binding

        4. Automatically tracks form and input element state
    
    Reactive forms are:

        1. More flexible, used in more complex scenarios

        2. Inmuttable data model

        3. Reactive transformation

        4. Easily add input elements dynamically

        5. Easier to unit test

10. What is a dumb, or presentation, component? What are the benefits of using dumb components?

    A dumb component is a component with no inyections, is a component whos only responsability is to present data. A benefit is modularity, a dumb component is not aware of who is providing the data, so it can be used to present data using distincts way for fetching it.



### Ability to Build Simple App
1. How do components communicate with each other?

    Using angular dependency injector.

2. How would you use http to load data from server?

    I will use it from a Component, injecting the HttpClient module, then calling the convenient functon for the convenient HTTP request configuration, passing the url as parameter and then subscribing a delegate function for processing the return value.

3. How do you create routes?

    Routes are defined by convention in the app-routing.module.ts file. This are declared in the Routes array form. The basic way to declare a route is defining a path and a component, a route path can contain route parameters used as values in the component and wildcards. Also a Route object have several optional values such as: title, redirectTo, pathMatch, etc.

4. How can you get the current state of a route?

    After the end of each successful navigation lifecycle, the router builds a tree of ActivatedRoute objects that make up the current state of the router. You can access the current RouterState from anywhere in the application using the Router service and the routerState property.

Each ActivatedRoute in the RouterState provides methods to traverse up and down the route tree to get information from parent, child and sibling routes.

5. How do you create two-way data binding?

    In Angular, two-way binding is denoted by [()], descriptively referred to as a "banana in a box". This syntax is a shortcut for defining both property binding (from the component to the view) and event binding (from the view to the component), thereby providing two-way binding.

6. How do you load external modules?

    Most o the time, installing it using npm or algunlar cli, scafolded code and webpack will do most of the work, therefore some modules are aplication wide and are grouped in the so called Shared Module.[REVIEW]

7. How would you display form validation errors?

    Angular provides @angular/forms module, with this module features an angular application can have form validation rules using the FormBuilder, FormControl and Validators.[REVIEW]

8. Which lifecycle hook would you use to unsubscribe an observable?

    ngOnDestroy if needed.

9. How are services injected to your application?

    Using the @Injectable decorator.

10. How would you create route parameters and access them from a component?

    Route parameters are defined in the Routes[] configuration array in the same field that the path value, using :<variable_name> sintax. This values are extracted in components using the ActivatedRoute component from @angular/router module and accessed in a dictionary form via .snapshot.paramMap.get('variable_name')

### Basic Concepts
1. Why would you use Angular instead of another framework, e.g., React?

    1. Low Decision Fatigue

        Since Angular is a framework, it provides significantly more opinions and functionality out of the box. With React, you typically pull a number of other libraries off the shelf to build a real app. You’ll likely want libraries for routing, enforcing unidirectional flows, web API calls, testing, dependency management, and so on. The number of decisions is pretty overwhelming. This is why React has so many starter kits (I’ve published two).
        Angular offers more opinions out of the box, which helps you get started more quickly without feeling intimidated by decisions. This enforced consistency also helps new hires feel at home more quickly and makes switching developers between teams more practical.

    2. TypeScript

        Sure, TypeScript isn’t loved by all, but Angular 2’s opinionated take on which flavor of JavaScript to use is a big win. React examples across the web are frustratingly inconsistent — it’s presented in ES5 and ES6 in roughly equal numbers, and it currently offers three different ways to declare components. This creates confusion for newcomers. (Angular also embraces decorators instead of extends — many would consider this a plus as well).
        While Angular 2 doesn’t require TypeScript, the Angular core team certainly embraces it and defaults to using TypeScript in documentation. This means related examples and open source projects are more likely to feel familiar and consistent. Angular already provides clear examples that show how to utilize the TypeScript compiler. (though admittedly, not everyone is embracing TypeScript yet, but I suspect shortly after launch it’ll become the de facto standard). This consistency should help avoid the confusion and decision overload that comes with getting started with React.
    
    3. Reduced Churn

        2015 was the year of JavaScript fatigue. Although React itself is expected to be quite stable with version 15 coming soon, React’s ecosystem has churned at a rapid pace, particularly around the long list of Flux flavors and routing. So anything you write in React today may feel out of date or require breaking changes in the future if you lean on one of many related libraries.
        In contrast, Angular 2 is a careful, methodical reinvention of a mature, comprehensive framework. So Angular is less likely to churn in painful ways after release. And as a full framework, when you choose Angular, you can trust a single team to make careful decisions about the future. In React, it’s your responsibility to herd a bunch of disparate, fast-moving, open-source libraries into a comprehensive whole that plays well together. It’s time-consuming, frustrating, and a never-ending job.
    
    4. Broad Tooling Support

        As you’ll see below, I consider React’s JSX a big win. However, you need to select tooling that supports JSX. React has become so popular that tooling support is rarely a problem today, but new tooling such as IDEs and linters are unlikely to support JSX on day one. Angular 2’s templates store markup in a string or in separate HTML files, so it doesn’t require special tooling support (though it appears tooling to intelligently parse Angular’s string templates is on the way).
    
    5. Web Component Friendly
        Angular 2’s design embraces the web component’s standard.

    [FROM https://medium.freecodecamp.org/angular-2-versus-react-there-will-be-blood-66595faafd51]

2. What is the difference between an observable and a promise?

    Often Observable is preferred over Promise because it provides the features of Promise and more. With Observable it doesn't matter if you want to handle 0, 1, or multiple events. You can utilize the same API in each case.
    Observable also has the advantage over Promise to be cancelable. If the result of an HTTP request to a server or some other expensive async operation isn't needed anymore, the Subscription of an Observable allows to cancel the subscription, while a Promise will eventually call the success or failed callback even when you don't need the notification or the result it provides anymore.
    Observable provides operators like map, forEach, reduce, ... similar to an array
    There are also powerful operators like retry(), or replay(), ... that are often quite handy.
    [FROM https://stackoverflow.com/questions/37364973/angular-promise-vs-observable]

3. What is the difference between a component and a directive?

    Components are a subset of Directives and handles a template
    Directives add behaviour to an existing DOM element or an existing component instance. A component, rather than adding/modifying behaviour, actually creates its own view (hierarchy of DOM elements) with attached behaviour.
    [FROM https://stackoverflow.com/questions/32680244/directive-v-s-component-in-angular]

4. Why would you use typescript aka benefits of typescript?

    TypeScript adds clarity and scalability to JavaScript.
    1. Is purely object-oriented programming    
    2. Can be used for client-side and server-side development alike
    3. Offers a “compiler” that can convert to JavaScript-equivalent code
    4. Has an API for DOM manipulation
    5. Has a namespace concept by defining a “Module”

5. Why different life cycle hooks are needed for a component/directive?

    Directive and component instances have a lifecycle as Angular creates, updates, and destroys them. So developers can tap into key moments in that lifecycle by implementing one or more of the lifecycle hook interfaces in the Angular core library.
    [FROM https://angular.io/guide/lifecycle-hooks]

6. Why does angular use rxjs?

    In RxJS, you represent asynchronous data streams using observable sequences or also just called observables. Observables are very flexible and can be used using push or pull patterns.
    When using the push pattern, we subscribe to the source stream and react to new data as soon as is made available (emitted).
    When using the pull pattern, we are using the same operations but synchronously. This happens when using Arrays, Generators or Iterables.
    [FROM https://medium.com/google-developer-experts/angular-introduction-to-reactive-extensions-rxjs-a86a7430a61f]

7. What is the purpose of using zone.js?

    A zone is an execution context that persists across async tasks, and allows the creator of the zone to observe and control execution of the code within the zone.
    I think that the main purpose of using zonejs in Angular is to know when to render.
    Frameworks, such as Angular, need to know when all of the application work has completed and perform DOM update before the host environment performs the pixel rendering. In practice this means that the framework is interested when the main task and the associated micro tasks have executed but before the VM hands over the control to the host.

8. What is the difference between ngOnInit() and the constructor() of a component?

    ngOnInit() is a lifecylce hook used for initialize the directive/component after Angular first displays the data-bound properties and sets the directive/component's input properties. The Constructor is a default method of the class that is executed when the class is instantiated and ensures proper initialization of fields in the class and its subclasses.

9. When will ngOnInit() be called? How would you make use of ngOnInit()?

    Better used for custom initialization logic after your directive's data-bound properties have been initialized.

10. What are the benefits of using formBuilder?

    More testable code. The FormGroup and FormControl classes provide an API that allows to build UIs using a completely different programming style known as Functional Reactive Programming.

[Answers link coming soon]


## Intermediate Level

To be in the intermediate level, you have to build at least one medium sized angular app. You have to have familiarity with routing, https, different built process, unit test, etc. here are the questions you could expect.



### Essential Terminology Questions
1. How will you protect a route for authorized user only?

    Implementing CanActivate and CanActivateChild and passing the implementation to the route like:
    
    { path: 'home', component: HomeComponent,  canActivate: [AppRouteGuard] },

    { path: 'users', component: UsersComponent, data: { permission: 'Manage.Users' }, canActivate: [AppRouteGuard] },

2. What is a custom pipe and how will you use it?

    A custom pipe is a user defined pipe used when the angular built in pipes don't meet the needed requirements. It's used in the same way as built in pipes but only declared in app.module.ts if is an application-wide feature.

3. What is a structural directive?

    Structural directives are some kind of "complicated directives". The two most common structural directives are ngIf and ngFor, they use the asterisk syntactic sugar. When using this directives Angular will wrap the host element with a template tag.

4. What is the difference between RouterModule.forRoot() vs RouterModule.forChild()? Why is it important?

    
5. What is the difference between a module's forRoot() and forChild() methods and why do you need it?

    forRoot() static method is used to inject components with the app root injector, ergo, all the providers specified with forRoot() will be available for the entire applications. forChild() static method is used to inject components with a child injector, therefore providers specified will only be avaidable for injections inside this lazy-loaded module.

6. What's the difference between dirty, touched, and pristine on a form element?

    @property {boolean} $untouched True if control has not lost focus yet.

    @property {boolean} $touched True if control has lost focus.

    @property {boolean} $pristine True if user has not interacted with the control yet.

    @property {boolean} $dirty True if user has already interacted with the control.

7. What is an async pipe? What kind of data can be used with async pipe?

    The async pipe subscribes to an Observable or Promise and returns the latest value it has emitted. When a new value is emitted, the async pipe marks the component to be checked for changes. When the component gets destroyed, the async pipe unsubscribes automatically to avoid potential memory leaks.

8. What is injectable? Give me some example.

    @Injectable() lets Angular know that a class can be used with the dependency injector. @Injectable() is not strictly required if the class has other Angular decorators on it or does not have any dependencies. What is important is that any class that is going to be injected with Angular is decorated. However, best practice is to decorate injectables with @Injectable(), as it makes more sense to the reader.

9. What is a pure pipe?

    Angular executes a pure pipe only when it detects a pure change to the input value. A pure change is either a change to a primitive input value (String, Number, Boolean, Symbol) or a changed object reference (Date, Array, Function, Object).

    There are two categories of pipes: pure and impure. Pipes are pure by default. Angular ignores changes within (composite) objects. It won't call a pure pipe if you change an input month, add to an input array, or update an input object property.

10. How will you create two-way data binding in Angular?

    Angular offers a special two-way data binding syntax, [(x)]. The [(x)] syntax combines the brackets of property binding, [x], with the parentheses of event binding, (x).

### Comfortability to Build Medium Size App Questions
1. How do components communicate with each other?
2. How do you decide to create a new NgModule?

    The app lacks clear boundaries between  functionalitys. That lack of clarity makes it harder to assign development responsibilities to different teams.

3. How will you inject custom header in your http call?
4. How do you identify a structural directive in html?
5. How would you select a custom component to style it?
6. How would you select all the child components' elements?
7. How would you cache an observable data?
8. How would you save data from a form control?
9. How Event Emitters works in Angular?
10. How do you mock a service to inject in a unit test?



### Core Concepts Understandability Questions
1. Tell me about feature module and shared module?
2. What would you not put in a shared module?
3. Why angular uses decorator?
4. What is async validation and how is it done?
5. Why do you need type definitions?
6. Which components will be notified when an event is emitted?
7. Why would you export from ngModule?
8. Why is it bad if SharedModule provides a service to a lazy loaded module?
9. Can you explain the difference between ActivatedRoute and RouterState?
10. Which service will you put in the module and why?



[Answers link coming soon]



## Expert Level

You are a Rockstar in angular. You can teach other. You can lead a team of angular developers.

### Performance and Edge case Related Terminology
1. What is a factory Component?
2. What is lazy loading and why will you use it?
3. What is Ahead of time (AOT) compilation and why will you use it?
4. What are some of the Angular Style Guide suggestions you follow on your code? Why?
5. What is wildcard state?
6. How do you put animation between two states?
7. What would be a good use for NgZone service?
8. How would you protect a component being activated through the router?
9. How would you insert an embedded view from a prepared TemplateRef?
10. What is attribute directive and why will you use it?

### Master a Large App
1. How will you intercept http to inject header to each http call?
2. How would you create a component to display error messages throughout your application?
3. How will you parallelize multiple observable call?
4. How will you put one async call before another?
5. How can you use web worker in angular app?
6. What tools would you use to find a performance issue in your code?
7. What are some ways you may improve your website's scrolling performance?
8. Explain the difference between layout, painting and compositing.
9. How can you cancel a router navigation?
10. How would you animate routing?
11. How would you cancel a promise on which you are waiting?


### Rockstar and Fighter for Angular Questions
1. When does a lazy loaded module is loaded?
2. Why angular uses url segment?
3. How will you make angular app secure?
4. How will you localize numbers currencies and dates?
5. What is the best way to use translation in your app?
6. How will you setup different environment build differently for your app?
7. How will you use scss or css preprocessing with your application?
8. How will you optimize image/svg in your angular app?
9. How would you make sure an api call that needs to be called only once but with multiple conditions? Example: if you need to get some data in multiple routes but, once you get it, you can reuse it in the routes that needs it, therefor no need to make another call to your backend apis.
10. If you need to respond to two different Observable/Subject with one callback function, how would you do it? (ex: if you need to change the url through route parameters and with prev/next buttons).




[Answers link coming soon]

## Coding Test
Sometimes interviewer gives real coding test. Most of us suck on those and feel ashamed of ourselves and then continue to work in the current job. I don't want you to saty in that miserable job. Hence, take the following coding challenges and master them. 

### Fetch Data and Display User Profile

This test has three level
1. Level 1: I am giving you an api https://api.github.com/search/users?q=eric This api takes a query parameter name "q" and passes query string to server. Server returns bunch of users. Now I want you to create a input text box and button so that you can type anything on the text box and hit on the button to retrieve data from the given api. Upon retrieval display total_count and first 10 users in the search result. Detail instruction about this test is available [here](https://github.com/khan4019/github-profile-search)
2. Level 2: Convert each user profile as a router link so that upon clicking on each user profile you will navigate to a route that has "login" property in the route. Pass user.login as route parameter. Create a separate component where you will read the route parameter and then fetch data for that user  by using this api https://api.github.com/users/eric . Please Notice that last part of this api is the user.login (the route parameter that you have passed). Finally display user image and few other information in the component
3. Level 3: use any charting framework that you can find and then create a simple bar chart to display number of followers of first 10 users


This coding test will judge your ability to use services, component, routing, data visualization, external module, observables, etc.

[Sample code link coming soon] 

### Persistent Todo List
This test has three levels
1. Level 1:  Implement a simple todo list where you can add items, mark as done
2. Level 2: Now create few categories of todo list and make it persistence in the browser
3. Level 3: Now use firebase (serverless database) to make todo list persistence across multiple devices

This coding test will judge whether you can pass data and events between components. Also, whether you are leveraging directives and understand difference between component and directives.


[Sample code link coming soon]

### Student Registration System
This test has three levels
1. Level-1: Design a system where students can login to register different courses 
2. Level-2: Add a feature so that faculties on each course can view how many students registered on the courses
3. Level-3: (I need a shower. will add text here after I clean up myself) 

This coding test will judge your understanding of architecture for a large application. Your ability to think and implement module, lazy loading, asset management etc.

[Sample code link coming soon]

## Side Things Related Questions

### rxjs
3. Why unsubscribing is important?
1. What is the difference between map and flatmap?
2. Whare are the different ways you can create an Observable?
4. What is forkJoin, zip, share?
5. Difference between hot and cold observables.

### TypeScript
1. How would you debug a typescript file?
2. How do you implement interface in typescript?
3. How would you call base class constructor from child class in typescript?
4. What is typescript language service?
5. How to declare a custom type?
6. what are some disadvantages of typescirpt? answers [here](https://www.codeproject.com/Articles/1071285/Latest-TypeScript-Interview-Questions-for-Beginner) 

### angular-cli
1. Why would you use angular cli?
2. How would you run unit test? 
3. How do you create application to use scss?
4. How to inject base href?
5. How would you extract webpack config from angular cli project?


### Others
1. What is the use of codelyzer?
2. Will you use Angular Material2?
4. How would you set different config in different deployment server?
5. What do you know about ES6?
6. What is ngUpgrage? Do you know how you can run angularJS and angular side by side?

[Answers link coming soon]


## Contributors
* [That JS Dude](https://github.com/khan4019)
* [Jesse M. Holmes](https://github.com/wolfhoundjesse)
* And you?
___________


Few questions are inspired by [Yonet](https://github.com/Yonet/Angular-Interview-Questions), [codeProject](https://www.codeproject.com/Articles/1169073/Angular-Interview-Questions)
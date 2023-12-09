## Angular

### What is Angular ?

Angular is a TypeScript-based, open-source framework for building single-page web applications (SPAs). It's a popular choice for developers due to its robust features, extensive documentation, and large community.

### what is open-source ?

Open-source development allows anyone to view the source code, contribute to its development, and report bugs. This transparency fosters a strong community around Angular, where developers can learn from each other, share knowledge, and collaborate on improvements.

    for eg : 
    if i am developing some application for my users and making it public such that anyone can see the code and can use it, if they want can give me feedbacks and report bugs so that by this means developers can engage other developers and can get good insight about the application.

- Open-source development allows for a more rapid pace of innovation. Bug fixes, improvements, and new features can be implemented and released quickly,

### What is a framework ?

Suppose we want to build a house, basic materials that is needed to build a house are `bricks` , `cement`, `steel` , `labour`.

now building a house can be done in 2 ways:

- if a person himself takes responsibilty of everything
- if he delegated the work to someone else (in this case a professional developer) who will look after all the things.


same is with like framework -> a framework is a complete package, it is a collection of tools and everything needed to build a complete thing.

What angular provides : 

`angular routing`, `compiler` ,`security`, `angular-forms`, `karma and jasmine frameworks for testing`.


### is Angular not a js framework ?

No! Though we know that Only browsers can understand javascript only.
but angular is a typescript based.

Angular was first launched in 2010, by that time it was built using javascript only, but due t few limitations nd more features of typescript in 2016 angular developers came up with new version of angular which was angular 2+, which was complete revamp of angular, and this time they used typescript.


### But Browsers can only understand Javascript how angular application which is in typescipt run on browsers ?

Typescript is a language by microsoft. it is a superset of javascript, means it is built on javascript using its all features and adding its own features.

Typescript is compiled into javascript. thats how angular application works.
   
    Typescript code -----ts compiler ----> javascript code

### Typescript Language and how it is different from javascript ?

- Features

        1. Static Typing: Statically typed, meaning types are checked during compilation, catching errors early
        2. Type Inference: Can infer types from variable assignments and function parameters.
        3. Interfaces:Supports classes and inheritance with improved syntax.
        4. Decorators:Allows attaching metadata to declarations for code generation, configuration, and other purposes.
        5. Private and protected members:Supports access modifiers like private and protected for greater control over object member visibility.
        6.  Advanced object-oriented features:
        7. Build tooling integration:Compiles TypeScript code to JavaScript, supporting various build tools and configuration options.

### What is Single page application 

Before coming to Single page application consider we have to build a ecommerce website which sells apparels of `mens`, `womens`, `kids`.

#### - SPA : A single-page application (SPA) is a web app that loads a single HTML page and then updates the content dynamically without reloading the entire page. This is different from traditional web applications, which load a new page every time the user clicks a link or submits a form.
---

### How to install Angular ?

Here's how to install Angular on different operating systems:

**1. Install Node.js:**

Angular requires Node.js to run. You can download and install the latest version from the official website: [https://nodejs.org/en/download](https://nodejs.org/en/download)

**2. Install Angular CLI:**

Once Node.js is installed, open a terminal and run the following command to install the Angular CLI globally:

```
npm install -g @angular/cli
```

This will install the Angular CLI globally on your system. You can use the `ng` command to access Angular CLI commands.

**3. Create a new Angular project:**

Run the following command to create a new Angular project named `my-app`:

```
ng new my-app
```

This will create a new directory called `my-app` with the basic structure for an Angular application.

**4. Start the development server:**

Navigate to the project directory and run the following command to start the development server:

```
cd my-app
ng serve
```

This will start a development server on port 4200. You can access the application in your web browser by navigating to [https://locall.host/4200/](https://locall.host/4200/).


### How do i check node js , npm and angular are installed properly ?

#### to check node js installed properly check node version using

- node -v 

#### to check version of npm check 
- npm -v 

#### to check version of angular use 
- ng version


### why do we need node js and what is npm ?

node js is a javascript runtime. 

    now what is javascript runtime 
    - as we all know only browsers had the power to run the javascript because browsers only had the javascript engines. 

    and javascript was only limited to frontend applications.

    but as the software system evolved many companies started building and developing a new and better javascript engine, their own engine which could run javascript. 


Node js is also one of them. it can run our javascript.

## But ??? Angular is not in js it is typescript based so why do we need node js here?

- Benefits of NODE js

    1. node js comes up with node package manager (NPM).NPM allows you to install and manage the various dependencies required by your Angular project.
    2. we need angular cli for angular related stuff, it needs node js to run. 
    3. Node allows you to spin up a lightweight web server to host your application locally in your system.


### what is angular cli ?

In the download process,we download three things 
1. node js 
2. npm 
3. angular-cli

`we didnt downloaded angular, we downloaded angular-cli ??`

The Angular CLI (Command Line Interface) is a powerful tool that plays a vital role in Angular development. It provides a set of commands that you can use to automate various tasks, such as:

**Project creation and management:**

* Create new Angular projects.
* Add, remove, and update components, services, directives, and other features.
* Generate boilerplate code for various elements.
* Manage dependencies with NPM.

**Development and testing:**

* Start and stop the development server for local testing.
* Run unit and end-to-end tests.
* Lint your code for errors and stylistic consistency.
* Build and deploy your application for production.

**Code scaffolding and generation:**

* Generate boilerplate code for components, services, pipes, and other common Angular elements.
* Quickly create basic structure for new features in your application.

**Version management:**

* Update Angular versions and other dependencies.
* Upgrade your application to newer versions of Angular with minimal effort.

**Here are some of the key reasons why the Angular CLI is essential for Angular development:**

* **Improved productivity:** Repetitive tasks can be automated, saving you time and effort.
* **Reduced errors:** Consistent code generation and boilerplate reduces the risk of manual errors.
* **Better development workflow:** Streamlines development process, making it easier to manage projects.
* **Enhanced code quality:** Enforces best practices and improves code maintainability.
* **Standardized project structure:** Ensures consistency across projects and teams.
* **Faster build times:** Optimizes build process for production deployments.
* **Community support:** Extensive documentation and community resources available.

**In summary, the Angular CLI is an indispensable tool for any Angular developer.** It provides a comprehensive set of features that simplify and accelerate the development process, while also promoting consistent and high-quality code. Learning and mastering the Angular CLI will significantly enhance your productivity and overall development experience with Angular.


### how to create angular application ?

*To create angular application we need to use command ng generate <project-name>*

**ng generate new-app**

The `ng new` command in the Angular CLI serves a crucial role in initializing and setting up new Angular projects. It performs several key tasks to get you started with development:

**1. Creates a New Project Directory:**

The command creates a new directory for your project with a standard structure recommended by the Angular team. This structure includes folders for components, services, directives, assets, and other essential elements.

**2. Generates Initial Project Files:**

It generates the essential files like `package.json`, `tsconfig.json`, `angular.json`, and others that define your project configuration, dependencies, and build settings.

**3. Installs Dependencies:**

The command automatically installs all necessary dependencies for your project, including the Angular framework itself, libraries, and other tools required for development.

**4. Sets Up Routing:**

It configures basic routing for your application, allowing you to define navigation between different views and components.

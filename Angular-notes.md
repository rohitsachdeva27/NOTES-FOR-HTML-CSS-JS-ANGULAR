
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

consider the theoretical design of website like below

<img width="886" alt="Screenshot 2023-12-09 at 3 38 12 PM" src="https://github.com/rohitsachdeva27/NOTES-FOR-HTML-CSS-JS-ANGULAR/assets/82018198/c00d224b-c9ab-4360-b6ac-d243f639ad64">


we know this is web applications contains all these elements

<img width="886" alt="Screenshot 2023-12-09 at 3 38 12 PM" src="https://github.com/rohitsachdeva27/NOTES-FOR-HTML-CSS-JS-ANGULAR/assets/82018198/af774c68-f11a-4dcc-a7f6-3ff4cc745c1a">


consider we have developed a website using html and css only.

in this case we would have developed 3 html pages like:

1. mens.html
2. womens.html
3. kids.html

and initialy a page where we will show some home content and 3 links 

when user will click on `men` then we will open a new page mens.html

## in case of mens.html we would have to have header and footer.
## same in womens.html page also we will have header and footer.
## same in kids html page we will have header and footer.

there is no way to re-use the functionality which is common.

- in normal applications there are individual pages for a different section or functionality.

#### - SPA : A single-page application (SPA) is a web app that loads a single HTML page and then updates the content dynamically without reloading the entire page. This is different from traditional web applications, which load a new page every time the user clicks a link or submits a form.







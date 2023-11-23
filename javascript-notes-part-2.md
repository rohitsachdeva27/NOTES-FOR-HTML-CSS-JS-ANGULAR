
## FAQ

## what is return value of function ?
Return values are just what they sound like — the values that a function returns when it completes.Some functions don't return a significant value, but others do.

## Strings in javascript and what are the methods appliable on strings ?
In JavaScript, strings are a data type used to represent sequences of characters. JavaScript provides a wide range of methods and properties that you can use to work with strings. Here's an overview of some common string methods in JavaScript:

1. **String Length:**
   - `length`: Returns the number of characters in a string.

   ```javascript
   const str = "Hello, World!";
   console.log(str.length); // Outputs: 13
   ```

   if string has whitespace , the length property counts whitespaces as 1 character.
   
        str = "Hello ";
        str.length -> 6

2. **String Access:**

   - You can access individual characters in a string using bracket notation.
   - strings are treated as sequences of characters, and they have a numeric index associated with each character
  
   ```javascript
   const str = "Hello";
   console.log(str[1]); // Outputs: "e"
   ```

3. **String Concatenation:**
   - `concat()`: Combines two or more strings and returns a new string.

   ```javascript
   const str1 = "Hello";
   const str2 = "World";
   const combined = str1.concat(", ", str2);
   console.log(combined); // Outputs: "Hello, World"
   ```

4. **Substring:**
   - `substring()`: Returns a part of the string between two indices.

syntax: 

        text_string.substring(start,?end);
        where end index is optional.

   ```javascript
   const str = "Hello, World!";
   const substr = str.substring(0, 5);
   console.log(substr); // Outputs: "Hello"
   ```

5. **String Search and Replace:**
   - `indexOf()`: Returns the index of the first occurrence of a specified substring. it returns index as index-1.
   - `lastIndexOf()`: Returns the index of the last occurrence of a specified substring.
   - `replace()`: Replaces a specified substring with another string.

   ```javascript
   const str = "Hello, World!";
   console.log(str.indexOf("World")); // Outputs: 7
   console.log(str.replace("World", "Universe")); // Outputs: "Hello, Universe!"
   ```

6. **String Case Modification:**
   - `toUpperCase()`: Converts the string to uppercase.
   - `toLowerCase()`: Converts the string to lowercase.

   ```javascript
   const str = "Hello, World!";
   console.log(str.toUpperCase()); // Outputs: "HELLO, WORLD!"
   ```

7. **Trimming Whitespace:**
   - `trim()`: Removes leading and trailing whitespace from a string.

   ```javascript
   const str = "   Hello, World!   ";
   console.log(str.trim()); // Outputs: "Hello, World!"
   ```

8. **String Splitting:**
   - `split()`: Splits a string into an array of substrings based on a specified delimiter.

   ```javascript
   const str = "apple,banana,cherry";
   const fruits = str.split(",");
   console.log(fruits); // Outputs: ["apple", "banana", "cherry"]
   ```

9. **String Conversion:**
   - `toString()`: Converts various data types to a string.

   ```javascript
   const num = 42;
   const str = num.toString();
   console.log(str); // Outputs: "42"
   ```

These are just a few examples of the many methods available for working with strings in JavaScript. Strings are a fundamental part of JavaScript, and these methods can help you manipulate and manage text data effectively.

 10. **String replace**
We can replace the contents inside the string using .replace method.

      let str = "Welcome to the js";
      str.replace("js","javascript");
      output => 'Welcome to the javascript'

11. **ReplaceAll**
it is used to replace all characters in the string.
      let str = "Welcome to the js tutorial, js is dynamic language";
      str.replace("js","javascript");
      output => 'Welcome to the javascript,js is dynamic language';

      Whereas ReplaceAll
       str.replaceAll("js","javascript");
      output => Welcome to the javascript,javascript is dynamic language.


### what are js objects ?

An object is a complex data type that represents a collection of key-value pairs, where keys are strings (or symbols in modern JavaScript) and values can be of any data type.

**How Can we create objects in js** 
- Object literal 

      The simplest way to create an object is using object literal notation. You define an object with curly braces and specify its properties and values.

      const person = {
      name: "John",
      age: 30,
      };

- Contructor function 

      You can create objects using constructor functions. These functions act as blueprints for creating multiple instances of objects with the same properties and methods.

   1. Using object literals is fine when you only need to create one object, but if you have to create more than one, as in the previous section, they're seriously inadequate.

a) first way of making it reusable is creating a function. 
inside function - create a obj and initialize prperties and methods.

      function createPerson(name) {
      const obj = {};
      obj.name = name;
      obj.introduceSelf = function () {
         console.log(`Hi! I'm ${this.name}.`);
      };
      return obj;
      }

b) this works fine but is a bit long-winded: we have to create an empty object, initialize it, and return it. A better way is to use a constructor. A constructor is just a function called using the new keyword. When you call a constructor, it will:

      function Person(name) {
      this.name = name;
         this.introduceSelf = function () {
            console.log(`Hi! I'm ${this.name}.`);
         };
      }


      const salva = new Person("Salva");
      salva.name;

- Object.create()

       The Object.create() static method creates a new object, using an existing object as the prototype of the newly created object.

            const person = {
               isHuman: false,

               printIntroduction: function () {
                  console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
                  },
               };

      const me = Object.create(person);

      me.name = 'Matthew'; // "name" is a property set on "me", but not on "person"
      me.isHuman = true; // Inherited properties can be overwritten

      me.printIntroduction();
      // Expected output: "My name is Matthew. Am I human? true"

   
   ### Object. create method returns a new object with the specified prototype object and properties.



## What are various Object methods ?

- ### Object.assign 


        let obj1 = {a:1,b:2};
        let obj2 = {c:3,a:4};

        syntax: 

        Object.assign(target_object,source_object);

        // here we want to copy all the properties or say we want to merge the properties of obj2 in obj1.

        Object.assign(obj1,obj2) // target obj is obj1 and source obj2 is source object 
        console.log(Object.assign(obj1,obj2));
        // . output => {a: 4, b: 2, c: 3}

        here we can see on merging or copying the object a value is updated to 4 this is because object.assign behaves like below

        {a:1,b:2} <- {c:3,a:4}  // the values flow from right to left so when merging or copying will start 
         1. first c value will be copied in object obj1
                {a:1,b:2,c:3} 
        2. a will be copied , but obj1 still has the obj1 already so a will be replaced with the new value from the obj2.a
                {a:4,b:2,c:3}

- ### Object.keys()
Object.keys is a static method available on Object , which returns the collection or array of keys of an object.


      const obj1= {
      name:'john',
      age:28,
      height:162
      }

      to get the array of keys we can do : 
      Object.entries(obj1) -> ["name","age","height"]

   - ### Object.values()

   - ### The Object.values() static method returns an array of a given object's own enumerable string-keyed property values.


         const object1 = {
            a: 'somestring',
            b: 42,
            c: false,
         };

         console.log(Object.values(object1));
         // Expected output: Array ["somestring", 42, false]

- ###  Object.entries()

#### an object is a collection of key and value pairs, Object.entries convert each key value pair as an array object where first element is key and second is value.

      const obj ={
         name : 'john',
         age:30
      }

      the first pair of key and value is 
       a) key : name 
          value : 'john'
       b) key : age
          value : 30 

      Object.entries will create a array of key and value pairs 

       like first pair will be 
       ["name","john"] 
       ["age",30]

       and will return as [["name","john"],["age",30]]

#### Each key-value pair is an array with two elements: the first element is the property key (which is always a string), and the second element is the property value.

- ### Object.hasOwnProperty()

#### The hasOwnProperty() method of Object instances returns a boolean indicating whether this object has the specified property as its own property (as opposed to inheriting 

         const object1 = {};
         object1.property1 = 42;

         console.log(object1.hasOwnProperty('property1'));
         // Expected output: true

         console.log(object1.hasOwnProperty('toString'));
         // Expected output: false

         console.log(object1.hasOwnProperty('hasOwnProperty'));
         // Expected output: false

### similar method is there which is static mehthod as Object.hasOwn(object,property)

- ## Object.groupBy()

### The Object.groupBy() static method groups the elements of a given iterable according to the string values returned by a provided callback function. The returned object has separate properties for each group, containing arrays with the elements in the group.

syntax

      Object.groupBy(items, callbackFn)


      const inventory = [
         { name: "asparagus", type: "vegetables", quantity: 5 },
         { name: "bananas", type: "fruit", quantity: 0 },
         { name: "goat", type: "meat", quantity: 23 },
         { name: "cherries", type: "fruit", quantity: 5 },
         { name: "fish", type: "meat", quantity: 22 },
         ];

const result = Object.groupBy(inventory, ({ type }) => type);

      /* Result is:
      {
      vegetables: [
         { name: 'asparagus', type: 'vegetables', quantity: 5 },
      ],
      fruit: [
         { name: "bananas", type: "fruit", quantity: 0 },
         { name: "cherries", type: "fruit", quantity: 5 }
      ],
      meat: [
         { name: "goat", type: "meat", quantity: 23 },
         { name: "fish", type: "meat", quantity: 22 }
      ]
      }
      */


- Object.defineProperty
The Object.defineProperty() static method defines a new property directly on an object, or modifies an existing property on an object, and returns the object.

   ### syntax : 

         Object.defineProperty(obj, prop, descriptor)

####  what is a descriptor ??
      descriptor tells whether the property can be writable, configurable, editable,value.

      configurable : true/false - means object can be configured or deleted .

      writable : true if the value associated with the property may be changed with an assignment operator. Defaults to false.

      value
      The value associated with the property. Can be any valid JavaScript value (number, object, function, etc.). Defaults to undefined.


#### we know we can add property to already created object using :
      const obj ={a:1};
      obj.b = 2 -> it will add another property b to obj object.

      so how does defineProperty makes a difference is that :


- ## Object.is ()
The `Object.is()` method is a built-in JavaScript method that compares two values for strict equality, similar to the `===` equality operator. However, there are some differences in how `Object.is()` behaves compared to `===`.

Here's the key difference:

- `===` (strict equality operator): Compares values to check if they are equal. It returns `true` if the values are strictly equal, meaning they have the same type and the same value.

- `Object.is()`: Compares values to check if they are the same. It returns `true` if the values are considered the same, according to the SameValueZero algorithm. This algorithm is almost the same as strict equality (`===`), with a few exceptions:
  - `NaN` is considered equal to `NaN` (unlike `===`, where `NaN` is not equal to `NaN`).
  - `-0` (negative zero) is not considered equal to `+0` (positive zero).

Here's an example:

```javascript
console.log(Object.is(5, 5)); // true (same as ===)
console.log(Object.is(0, -0)); // false (different from ===)
console.log(Object.is(NaN, NaN)); // true (different from ===)
```

The primary use case for `Object.is()` is when you need to perform comparisons where the differences between `NaN` and `-0` matter, or when you need to ensure the most accurate equality check possible. In most cases, `===` is sufficient for comparing values in JavaScript.


- ## Object.freeze

The `Object.freeze()` method in JavaScript is used to freeze an object, making it immutable. When an object is frozen, you cannot add, modify, or delete its properties or change its prototype. It essentially locks the object down, making it read-only and preventing any further changes to its structure.

Here's how to use `Object.freeze()`:

```javascript
const obj = {
  prop1: 42,
  prop2: "Hello",
};

Object.freeze(obj);

// Attempting to modify the object will have no effect and will not throw an error, but it will silently fail.
obj.prop1 = 100; // No effect
obj.prop3 = "New Property"; // No effect

// You can still access the object's properties.
console.log(obj.prop1); // Outputs: 42

// You can check if an object is frozen using Object.isFrozen()
console.log(Object.isFrozen(obj)); // true
```

Keep in mind that freezing an object is shallow, meaning that the properties of the object are frozen, but if the object's properties are themselves objects, those nested objects are not automatically frozen. If you want to deep freeze an object, you would need to recursively apply `Object.freeze()` to all nested objects and their properties.

Freezing an object is a way to ensure that its structure remains consistent and that it won't be accidentally modified in your code. It's useful for creating immutable data structures, but it should be used with caution, as it makes the object unchangeable.


- ### Object.seal

The `Object.seal()` method in JavaScript is used to seal an object, making it non-extensible. When an object is sealed, you cannot add or delete properties from it, but you can still modify the values of its existing properties. It's a level of control between a completely open object and a frozen (immutable) object.

Here's how to use `Object.seal()`:

```javascript
const obj = {
  prop1: 42,
  prop2: "Hello",
};

Object.seal(obj);

// Attempting to add or delete properties will have no effect and will not throw an error.
obj.prop3 = "New Property"; // No effect
delete obj.prop1; // No effect

// You can still modify the values of existing properties.
obj.prop1 = 100; // Allowed
console.log(obj.prop1); // Outputs: 100

// You can check if an object is sealed using Object.isSealed()
console.log(Object.isSealed(obj)); // true
```

Sealing an object is a way to prevent further expansion or contraction of its properties while still allowing you to change the values of existing properties. It's useful when you want to maintain the object's structure but don't need it to be fully immutable.


## what are descriptors ?

In JavaScript, descriptors are objects that define the properties of an object when using the `Object.defineProperty()`, `Object.defineProperties()`, or `Object.create()` methods. Descriptors specify how a property behaves in terms of its configurability, writability, enumerability, and value. There are typically three types of descriptors:

1. **Data Descriptors:**
   - Data descriptors define properties with a value. They have the following attributes:
     - `value`: The value of the property.
     - `writable`: A boolean indicating if the property's value can be changed.
     - `enumerable`: A boolean indicating if the property appears in `for...in` loops and `Object.keys()`.
     - `configurable`: A boolean indicating if the property can be deleted or if its attributes can be changed.

2. **Accessor Descriptors:**
   - Accessor descriptors define properties that have getter and/or setter functions. They have the following attributes:
     - `get`: A function to retrieve the property's value.
     - `set`: A function to set the property's value.
     - `enumerable`: A boolean indicating if the property appears in `for...in` loops and `Object.keys()`.
     - `configurable`: A boolean indicating if the property can be deleted or if its attributes can be changed.

3. **Generic Descriptors:**
   - A generic descriptor can be used to define properties that have both value and getter/setter methods. You can include both `value` and `get`/`set` in a descriptor, but they cannot coexist.

Here's an example of using `Object.defineProperty()` with descriptors:

```javascript
const obj = {};

// Data descriptor
Object.defineProperty(obj, 'dataProperty', {
  value: 42,
  writable: true,
  enumerable: true,
  configurable: true,
});

// Accessor descriptor
Object.defineProperty(obj, 'accessorProperty', {
  get: function() {
    return 'Getter';
  },
  set: function(value) {
    console.log('Setter:', value);
  },
  enumerable: true,
  configurable: true,
});

console.log(obj.dataProperty); // Outputs: 42
obj.accessorProperty = 'New Value'; // Outputs: Setter: New Value
console.log(obj.accessorProperty); // Outputs: Getter
```

These descriptors are powerful tools for defining and controlling the behavior of object properties in JavaScript. They allow you to set fine-grained control over how properties can be accessed and modified.


### what is difference between Object.seal and Object.freeze ?
`Object.seal()` and `Object.freeze()` are both methods in JavaScript that are used to make objects non-extensible and prevent changes to their properties, but they differ in the level of immutability they provide:

1. **`Object.seal()`**:

   - Makes an object non-extensible, which means you cannot add or delete properties from the object.
   - Allows you to modify the values of existing properties.
   - The object's properties remain configurable, which means you can still change the attributes of the existing properties, such as their values or enumerability.
   - The properties of nested objects within the sealed object are not automatically sealed. You need to seal them explicitly if needed.

2. **`Object.freeze()`**:

   - Makes an object fully immutable, making it read-only and preventing any changes to its properties.
   - You cannot add, delete, or modify the values of its properties.
   - The properties of the frozen object become non-configurable and non-writable, which means they cannot be changed or deleted.
   - The properties of nested objects within the frozen object are not automatically frozen. You need to freeze them explicitly if needed.

In summary, the key difference is that `Object.seal()` allows modifications to the values of existing properties and doesn't make the properties non-configurable, while `Object.freeze()` makes the object and its properties fully immutable, preventing any changes. The choice between them depends on the level of immutability you need for your specific use case.


## what is Object destructuring ?
Object destructuring is a feature in JavaScript that allows you to extract values from objects and bind them to variables in a more concise and convenient way. It provides an elegant method for extracting properties from objects and using them in your code. Object destructuring is commonly used in a variety of JavaScript scenarios, such as when working with function parameters or extracting data from complex objects.

Here's the basic syntax of object destructuring:

```javascript
const { property1, property2, ... } = sourceObject;
```

- `property1`, `property2`, etc., are the names of the properties you want to extract from `sourceObject`.
- `sourceObject` is the object from which you are extracting the properties.

Here's an example:

```javascript
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
};

const { firstName, lastName } = person;

console.log(firstName); // "John"
console.log(lastName);  // "Doe"
```

In this example, object destructuring is used to extract the `firstName` and `lastName` properties from the `person` object and bind them to variables.

Object destructuring is not limited to extracting single properties; you can also destructure nested objects and provide default values for properties that may not exist. It makes your code more concise and easier to read, especially when working with complex data structures.

Here's an example of destructuring nested objects and providing default values:

```javascript
const user = {
  name: "Alice",
  address: {
    city: "New York",
    zipCode: "10001",
  },
};

const { name, address: { city, country = "USA" } } = user;

console.log(name);    // "Alice"
console.log(city);    // "New York"
console.log(country); // "USA"
```

Object destructuring is a powerful and widely used feature in modern JavaScript, and it simplifies working with objects and their properties.

### MORE Use cases

      const [a, b] = array;
      const [a, , b] = array;
      const [a = aDefault, b] = array;
      const [a, b, ...rest] = array;
      const [a, , b, ...rest] = array;
      const [a, b, ...{ pop, push }] = array;
      const [a, b, ...[c, d]] = array;

      const { a, b } = obj;
      const { a: a1, b: b1 } = obj;
      const { a: a1 = aDefault, b = bDefault } = obj;
      const { a, b, ...rest } = obj;
      const { a: a1, b: b1, ...rest } = obj;
      const { [key]: a } = obj;

      let a, b, a1, b1, c, d, rest, pop, push;
      [a, b] = array;
      [a, , b] = array;
      [a = aDefault, b] = array;
      [a, b, ...rest] = array;
      [a, , b, ...rest] = array;
      [a, b, ...{ pop, push }] = array;
      [a, b, ...[c, d]] = array;

      ({ a, b } = obj); // parentheses are required
      ({ a: a1, b: b1 } = obj);
      ({ a: a1 = aDefault, b = bDefault } = obj);
      ({ a, b, ...rest } = obj);
      ({ a: a1, b: b1, ...rest } = obj);



## how can we iterate the object ?

You can iterate over the properties of an object in JavaScript using various methods. Here are some common ways to iterate through the properties of an object:

1. **For...In Loop:**

   The `for...in` loop allows you to iterate over the enumerable properties of an object. Here's an example:

   ```javascript
   const person = {
     name: "John",
     age: 30,
   };

   for (const key in person) {
     if (person.hasOwnProperty(key)) {
       console.log(key + ": " + person[key]);
     }
   }
   ```

   Note the use of `hasOwnProperty()` to ensure that you are only iterating over the object's own properties and not properties from the object's prototype chain.

2. **Object.keys(), Object.values(), Object.entries():**

   JavaScript provides several built-in methods to work with object properties:

   - `Object.keys(object)` returns an array of property names.
   - `Object.values(object)` returns an array of property values.
   - `Object.entries(object)` returns an array of key-value pairs.

   Here's how you can use them:

   ```javascript
   const person = {
     name: "John",
     age: 30,
   };

   const keys = Object.keys(person);
   const values = Object.values(person);
   const entries = Object.entries(person);

   console.log(keys);    // Outputs: ["name", "age"]
   console.log(values);  // Outputs: ["John", 30]
   console.log(entries); // Outputs: [["name", "John"], ["age", 30]]
   ```

3. **Object.getOwnPropertyNames():**

   `Object.getOwnPropertyNames(object)` returns an array of all property names, including non-enumerable ones.

   ```javascript
   const person = {
     name: "John",
     age: 30,
   };

   const propertyNames = Object.getOwnPropertyNames(person);

   console.log(propertyNames); // Outputs: ["name", "age"]
   ```

Choose the method that best suits your needs based on whether you want to work with property names, values, or both, and whether you want to include non-enumerable properties or not.

## what are rest and spread parameters ?

Rest and spread are two features in JavaScript that are related to handling arrays and objects. They are denoted by the use of three dots (`...`). Let's discuss each of them:

### Spread Operator:

**Syntax:**
```javascript
const newArray = [...existingArray];
const newObj = {...existingObj};
```

- **Arrays:** The spread operator is used to make a shallow copy of an array. It allows you to expand an array or object into places where multiple elements or key-value pairs are expected.

  ```javascript
  const array1 = [1, 2, 3];
  const array2 = [...array1, 4, 5];
  console.log(array2); // Output: [1, 2, 3, 4, 5]
  ```

- **Objects:** Similarly, for objects, the spread operator creates a shallow copy.

  ```javascript
  const obj1 = { a: 1, b: 2 };
  const obj2 = { ...obj1, c: 3, d: 4 };
  console.log(obj2); // Output: { a: 1, b: 2, c: 3, d: 4 }
  ```

### Rest Parameter:

**Syntax:**
```javascript
function myFunction(...rest) {
  // rest is an array containing all the arguments passed to the function
}
```

- The rest parameter allows you to represent an indefinite number of arguments as an array.

  ```javascript
  function sum(...numbers) {
    return numbers.reduce((acc, num) => acc + num, 0);
  }

  console.log(sum(1, 2, 3, 4)); // Output: 10
  ```

- It is often used in function parameters to gather remaining arguments into an array.

  ```javascript
  function example(first, second, ...rest) {
    console.log(first); // Output: 1
    console.log(second); // Output: 2
    console.log(rest); // Output: [3, 4, 5]
  }

  example(1, 2, 3, 4, 5);
  ```

In summary, the spread operator is used to unpack elements from arrays or properties from objects, creating shallow copies. The rest parameter, on the other hand, is used in function parameters to gather up remaining arguments into an array.


## what is template literal string ?

Template literals, also known as template strings, are a way to work with strings in JavaScript that allows for embedding expressions within the string. They are denoted by backticks (`) and can contain placeholders `${expression}` that are replaced with the result of evaluating the expression.

Here's a simple example:

```javascript
const name = "John";
const greeting = `Hello, ${name}!`;
console.log(greeting);
// Output: Hello, John!
```

In this example, the template literal `${name}` is a placeholder that gets replaced with the value of the `name` variable.

### Features of Template Literals:

1. **Multiline Strings:**
   Template literals allow multiline strings without needing to concatenate or use escape characters:

   ```javascript
   const multiline = `
     This is a multiline
     string using template literals.
   `;
   ```

2. **Expression Interpolation:**
   You can embed expressions directly within the string:

   ```javascript
   const a = 10;
   const b = 20;
   const result = `The sum of ${a} and ${b} is ${a + b}.`;
   ```

3. **Tagged Templates:**
   Advanced usage involves using a function (a tag function) to process the template literal. This is known as tagged templates.

   ```javascript
   function customTag(strings, ...values) {
     // Process strings and values here
     return "Processed result";
   }

   const taggedResult = customTag`Value 1: ${x}, Value 2: ${y}`;
   ```

   The `strings` array contains the literal text parts, and `values` contain the evaluated expressions.

Template literals provide a more concise and readable way to work with strings, especially when you need to include variables or expressions within the string. They are widely used in modern JavaScript for constructing strings in a more flexible and clean manner.


## Nullish coalescing assignment (??=);

The nullish coalescing assignment (??=) operator, also known as the logical nullish assignment operator, only evaluates the right operand and assigns to the left if the left operand is nullish (null or undefined).


eg : 

      const a = { duration: 50 };

      a.duration ??= 10;
      console.log(a.duration);
      // Expected output: 50

      a.speed ??= 25;
      console.log(a.speed);
      // Expected output: 25

## what is DOM ?
The DOM, or Document Object Model, is a programming interface and representation of the structure and content of a web document. It provides a way for programs (typically JavaScript) to interact with and manipulate the structure, style, and content of HTML and XML documents.

Key points about the DOM:

1. **Document Structure:**
   - The DOM represents an HTML or XML document as a tree structure.
   - Each element, attribute, and piece of text in the document is a node in this tree.

2. **Programming Interface:**
   - The DOM provides a programming interface (API) for scripting languages like JavaScript to access and manipulate the content and structure of a document dynamically.

3. **Dynamic Interaction:**
   - With the DOM, you can dynamically modify the content, structure, and style of a document based on user actions, events, or other conditions.

4. **Platform and Language Agnostic:**
   - While JavaScript is the most commonly used language for DOM manipulation in web browsers, the DOM itself is language-agnostic. Other programming languages can also interact with the DOM using appropriate interfaces.

5. **Tree Hierarchy:**
   - The DOM represents the document as a hierarchical tree, with the root being the `document` node, followed by nodes representing HTML elements, attributes, and text.

   ```html
   <!-- Example HTML document structure -->
   <html>
     <head>
       <title>Document Title</title>
     </head>
     <body>
       <h1>Hello, World!</h1>
       <p>This is a paragraph.</p>
     </body>
   </html>
   ```

   The corresponding DOM tree structure:
   ```
   document
   ├── html
   │   ├── head
   │   │   └── title
   │   │       └── (text)
   │   └── body
   │       ├── h1
   │       │   └── (text)
   │       └── p
   │           └── (text)
   └── (other nodes)
   ```

6. **Manipulation and Events:**
   - You can use the DOM to create, modify, and delete elements, change their attributes, and respond to user events such as clicks and keyboard input.

The DOM is a crucial part of web development as it enables dynamic, interactive, and responsive web applications by allowing developers to manipulate the content and structure of web pages in real-time. It serves as a bridge between the static HTML content and the dynamic behavior controlled by scripts.


JS which is used for dynamically updating web pages or manipulating web pages uses this DOM.

#### The DOM (Document Object Model) is created by the browser when it parses an HTML or XML document. The process of creating the DOM is part of the initial rendering phase when a web page is loaded.

### The DOM represents a document with a logical tree. Each branch of the tree ends in a node, and each node contains objects. DOM methods allow programmatic access to the tree. With them, you can change the document's structure, style, or content.

### so objects of document and tree lioke structure of document object is DOM. The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on the web.

## note : A web page is a document that can be either displayed in the browser window or as the HTML source. In both cases, it is the same document but the Document Object Model (DOM) representation allows it to be manipulated. As an object-oriented representation of the web page, it can be modified with a scripting language such as JavaScript.

#### https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction

## what is document in DOM , is it part of dom or html ?

In the context of the DOM (Document Object Model), the term "document" refers to the top-level object that represents the entire HTML or XML document. The `document` object is a fundamental part of the DOM, and it provides an interface for interacting with the content and structure of the document.

Here are some key points about the `document` object:

1. **Top-Level Object:**
   - The `document` object is part of the DOM and is created automatically by the browser when it parses an HTML or XML document.

2. **Representation of the Document:**
   - The `document` object represents the entire document as a hierarchical tree structure, where each node in the tree corresponds to an element, attribute, or piece of text in the document.

3. **Root of the DOM Tree:**
   - The `document` object is the root of the DOM tree. All other elements and nodes are descendants of this root node.

4. **Access to Document Elements:**
   - Through the `document` object, developers can access and manipulate elements in the document, change styles, modify content, add or remove elements, and handle events.

   ```javascript
   // Example: Accessing an element by its ID
   const myElement = document.getElementById('myElement');
   ```

5. **Document-Level Properties and Methods:**
   - The `document` object provides various properties and methods that allow developers to interact with the document at a high level. For example, `document.title` accesses the title of the document, and `document.createElement()` creates a new HTML element.

   ```javascript
   // Example: Changing the title of the document
   document.title = 'New Document Title';
   ```

6. **Interface for Scripting Languages:**
   - The `document` object serves as an interface for scripting languages like JavaScript to dynamically manipulate the document. It enables developers to create interactive and dynamic web pages.

In summary, the `document` object is a central and crucial part of the DOM, providing a programming interface for interacting with the content and structure of a web document. While it's a key component of the DOM, it is distinct from the HTML document itself; it's a dynamic representation created by the browser for scripting languages to work with.

## what is a DOM tree ?

Using the Document Object Model
The Document Object Model (DOM) is an API for manipulating DOM trees of HTML and XML documents (among other tree-like documents). This API is at the root of the description of a page and serves as a base for scripting on the web.

What is a DOM tree?
A DOM tree is a tree structure whose nodes represent an HTML or XML document's contents. Each HTML or XML document has a DOM tree representation. For example, consider the following document:

HTML
Copy to Clipboard

      <html lang="en">
      <head>
         <title>My Document</title>
      </head>
      <body>
         <h1>Header</h1>
         <p>Paragraph</p>
      </body>
      </html>

The DOM as a tree-like representation of a document that has a root and node elements containing content
Although the above tree is similar to the above document's DOM tree, it's not identical, as the actual DOM tree preserves whitespace.

When a web browser parses an HTML document, it builds a DOM tree and then uses it to display the document.

## what does DOM api do ?

- The Document API, also sometimes called the DOM API, allows you to modify a DOM tree in any way you want. It enables you to create any HTML or XML document from scratch or to change any contents of a given HTML or XML document. Web page authors can edit the DOM of a document using JavaScript to access the document property of the global object. This document object implements the Document interface.

## what are the different different interface method provided by DOM ?

The `Document` interface in the DOM (Document Object Model) provides various methods for interacting with and manipulating the content, structure, and style of an HTML or XML document. Here are some of the commonly used methods:

### Document Retrieval Methods:

1. **`getElementById(id: string): Element | null`**
   - Returns the element with the specified ID or `null` if not found.

2. **`getElementsByClassName(className: string): HTMLCollectionOf<Element>`**
   - Returns a live `HTMLCollection` of elements with the specified class name.

3. **`getElementsByTagName(tagName: string): HTMLCollectionOf<Element>`**
   - Returns a live `HTMLCollection` of elements with the specified tag name.

4. **`getElementsByName(name: string): NodeListOf<HTMLElement>`**
   - Returns a non-live `NodeList` of elements with the specified name attribute.

5. **`querySelector(selectors: string): Element | null`**
   - Returns the first element that matches the specified CSS selectors or `null` if not found. It is generally used for querying the elements directly using tag, class,id.

6. **`querySelectorAll(selectors: string): NodeList`**
   - Returns a static `NodeList` of all elements that match the specified CSS selectors.

### Document Creation and Modification Methods:

7. **`createElement(tagName: string): Element`**
   - Creates a new HTML element with the specified tag name.

8. **`createTextNode(data: string): Text`**
   - Creates a new text node with the specified content.

9. **`appendChild(newChild: Node): Node`**
   - Adds a new child node to the end of the list of children of a specified parent node.

10. **`removeChild(oldChild: Node): Node`**
    - Removes a child node from the DOM.

11. **`replaceChild(newChild: Node, oldChild: Node): Node`**
    - Replaces one child node with another.

### Document Information and Navigation Methods:

12. **`getElementById(id: string): Element | null`**
    - Returns the element with the specified ID or `null` if not found.

13. **`getElementsByTagName(tagName: string): HTMLCollectionOf<Element>`**
    - Returns a live `HTMLCollection` of elements with the specified tag name.

14. **`createElement(tagName: string): Element`**
    - Creates a new HTML element with the specified tag name.

15. **`createDocumentFragment(): DocumentFragment`**
    - Creates an empty `DocumentFragment` node that can be used as a temporary container.

16. **`createEvent(eventInterface: string): Event`**
    - Creates a new event of the specified type.

### Document Loading and Scripting Methods:

17. **`open(): void`**
    - Opens a new document for writing.

18. **`close(): void`**
    - Closes the document for writing.

19. **`write(...text: string[]): void`**
    - Writes HTML expressions or JavaScript code to a document.

20. **`writeln(...text: string[]): void`**
    - Writes HTML expressions or JavaScript code to a document, followed by a newline character.

These are just a few examples of the methods provided by the `Document` interface. The actual set of methods can vary depending on the DOM specification and the version of the browser. It's recommended to refer to the official documentation or use browser developer tools for more comprehensive information and examples.

## what are the properties which can be updated using the element ref from document interface ?

consider an element 

      <h1 id="heading" class="h1">Welcome to the Js </h1>

1. **we can change the textContent**

- to change the text content of the h1 element we need the element reference , which we can get using **getElementById** or **querySelector** or **getElementsByClassName**.

      let element =  document.getElementsByClassName("heading");
      // to access or change the textcontent we have to get the textContent property of element 
      element.textContent = "Text Changed";

2. **innerHTML Property**

when we render content using textContent it is simple text format, but when we want the content to be changed and text contains html tags then we should use innerHTML.

      element.innerHTML = "<i>Welcome</i>"

now content will be welcome in italic.

3. **we can add or remove Styles**

         element.style.color = "red";

4. **we can add classes**

         element.classList.add('heading1')

5. **remove classes**

         element.classList.remove('heading1')

6. **lets say we have a anchor tag and we want to dynamically update its href**

- ### we can add attributes like src/href.
         
         <a href="" id="link">Click to Navigate</a>
         let anchortag = document.getElementById("link");
         anchorTag.href="https.google.com";


## what are different events in js ?

Events are things that happen in the system you are programming — the system produces (or "fires") a signal of some kind when an event occurs, and provides a mechanism by which an action can be automatically taken (that is, some code running) when the event occurs.

For example:

- The user selects, clicks, or hovers the cursor over a certain element.
- The user chooses a key on the keyboard.
- The user resizes or closes the browser window.
- A web page finishes loading.
- A form is submitted.
- A video is played, paused, or ends.
- An error occurs.

## what are different events ?

In JavaScript, events represent occurrences or interactions that happen in the browser. Here are some of the commonly used events:

1. **Mouse Events:**
   - `click`: Occurs when the user clicks an element.
   - `dblclick`: Occurs when the user double-clicks an element.
   - `mousedown`: Occurs when the mouse button is pressed over an element.
   - `mouseup`: Occurs when the mouse button is released over an element.
   - `mousemove`: Occurs when the mouse pointer is moving while over an element.
   - `mouseover`: Occurs when the mouse pointer enters an element.
   - `mouseout`: Occurs when the mouse pointer leaves an element.

2. **Keyboard Events:**
   - `keydown`: Occurs when a key is pressed down.
   - `keyup`: Occurs when a key is released.
   - `keypress`: Occurs when a key is pressed and released.

3. **Form Events:**
   - `submit`: Occurs when a form is submitted.
   - `reset`: Occurs when a form is reset.
   - `change`: Occurs when the value of an input element changes.
   - `input`: Similar to `change`, occurs when the value of an input element changes.

4. **Focus Events:**
   - `focus`: Occurs when an element gets focus.
   - `blur`: Occurs when an element loses focus.

5. **Window Events:**
   - `load`: Occurs when a page has finished loading.
   - `unload`: Occurs when a page is being unloaded (closed or navigated away).
   - `resize`: Occurs when the browser window is resized.
   - `scroll`: Occurs when the user scrolls in an element.

6. **Document Events:**
   - `DOMContentLoaded`: Occurs when the HTML document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.
   - `readystatechange`: Occurs when the readyState property of the document changes (used in older versions of Internet Explorer).

7. **Media Events:**
   - `play`: Occurs when media playback begins.
   - `pause`: Occurs when media playback is paused.
   - `ended`: Occurs when media playback completes.

8. **Drag and Drop Events:**
   - `dragstart`: Occurs when the user starts dragging an element.
   - `dragend`: Occurs when the user has finished dragging an element.
   - `dragover`: Occurs when a dragged element is being dragged over a valid drop target.
   - `drop`: Occurs when the dragged element is dropped on a valid drop target.

9. **Animation Events:**
   - `animationstart`: Occurs when a CSS animation starts.
   - `animationend`: Occurs when a CSS animation completes.
   - `animationiteration`: Occurs when a CSS animation completes one iteration.

These events are just a subset, and there are many more events available in the DOM. Additionally, custom events can be created using the `CustomEvent` constructor for more specialized use cases.

## what is event delegation and event capturing ?

Event capturing and event bubbling are two phases of the event propagation process in the DOM (Document Object Model). These phases describe the order in which events are handled when they occur on a nested structure of HTML elements.

### Event Capturing (Trickling Phase):

- **Order:** During the capturing phase, the event starts from the root of the DOM hierarchy and trickles down to the target element.
- **Useful for:** It can be useful for global operations or setups that need to be executed before the event reaches the target element.

```plaintext
| | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| root                                                                                                   |
|   |                                                                                                     |
|   |   |                                                                                                 |
|   |   |   |                                                                                             |
|   |   |   |   |                                                                                         |
|   |   |   |   |   |      capturing phase                                                                |
|   |   |   |   |   |-----------------------> target element                                             |
|   |   |   |   |   |                                                                                     |
|   |   |   |   |                                                                                         |
|   |   |   |                                                                                             |
|   |   |                                                                                                 |
|   |                                                                                                     |
|                                                                                                         |
```

### Event Bubbling (Bubbling Phase):

- **Order:** During the bubbling phase, the event starts from the target element and bubbles up to the root of the DOM hierarchy.
- **Useful for:** It is useful for handling events on specific elements and allows you to capture the event at various levels in the DOM hierarchy.

```plaintext
| | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | | |
| root                                                                                                   |
|   |                                                                                                     |
|   |   |                                                                                                 |
|   |   |   |                                                                                             |
|   |   |   |   |                                                                                         |
|   |   |   |   |   |      bubbling phase                                                                 |
|   |   |   |   |   |<----------------------- target element                                             |
|   |   |   |   |                                                                                         |
|   |   |   |                                                                                             |
|   |   |                                                                                                 |
|   |                                                                                                     |
|                                                                                                         |
```

### How to Use Event Capturing and Bubbling:

- **addEventListener:**
  - When you use `addEventListener`, the third parameter is a boolean that specifies the event phase: `true` for capturing and `false` (or omitted) for bubbling.
  
  ```javascript
  element.addEventListener('click', handler, true); // Capturing phase
  element.addEventListener('click', handler, false); // Bubbling phase (default)
  ```

- **Legacy Methods:**
  - The older methods like `attachEvent` (for Internet Explorer) do not support event capturing.

### Event.stopPropagation():

- To prevent an event from continuing through either the capturing or bubbling phase, you can use the `stopPropagation` method.
  
  ```javascript
  function handleClick(event) {
    // Handle the event
    event.stopPropagation(); // Stop the event from propagating further
  }

  element.addEventListener('click', handleClick, true); // Capturing phase
  ```

Understanding event capturing and bubbling is crucial for managing complex event handling scenarios, especially when dealing with nested HTML structures.

## how can we stop propagation of events?

To stop the propagation of an event in JavaScript, you can use the `stopPropagation()` method. This method is available on the event object that is passed to your event handler function.

Here's an example:

```html
<button id="parentButton">
  Click me
  <button id="childButton">Nested Button</button>
</button>

<script>
  document.getElementById('parentButton').addEventListener('click', function (event) {
    console.log('Parent button clicked');
    // Stop the event from propagating further
    event.stopPropagation();
  });

  document.getElementById('childButton').addEventListener('click', function (event) {
    console.log('Child button clicked');
    // The event will not reach the parent button due to stopPropagation
  });
</script>
```

In this example, when the nested button (`childButton`) is clicked, the event handler for the child button is triggered first. Inside that handler, `event.stopPropagation()` is called, preventing the event from reaching the parent button's event handler. As a result, the parent button's click event won't be triggered.

Here's a breakdown of the code:

- Clicking the child button triggers its event handler, logging "Child button clicked" to the console.
- The `event.stopPropagation()` method is called in the child button's event handler, preventing the event from reaching the parent button.
- As a result, the parent button's event handler is not executed.

Keep in mind that while `stopPropagation()` prevents the event from propagating to the parent and further up the DOM hierarchy, it doesn't prevent the default behavior associated with the event. If the event has a default action (e.g., following a link or submitting a form), you might also need to use `event.preventDefault()` to prevent that default action.

## What is prevent default behavior ?

In the context of web development and JavaScript, the term "preventDefault" refers to a method that can be called on an event object to stop the default behavior associated with that event.

When an event occurs in a web page, such as a click on a link or a form submission, the browser performs a default action associated with that event. The `preventDefault` method allows you to stop this default behavior.

Here's an example using JavaScript and the DOM (Document Object Model):

```javascript
document.getElementById('myLink').addEventListener('click', function(event) {
  // Prevent the default behavior of the link click
  event.preventDefault();

  // Your custom code goes here
  console.log('Link clicked, but default behavior prevented.');
});
```

In this example, when a user clicks on the HTML element with the ID "myLink," the associated event listener is triggered. Inside the event listener, `event.preventDefault()` is called, preventing the default behavior of the link click, which would typically navigate to the URL specified in the href attribute.

This technique is often used in scenarios where you want to handle an event in a custom way without allowing the browser to perform its default action. It's commonly used with form submissions, link clicks, and other user interactions in web development.
- ### Let's consider an example using an HTML form and JavaScript. Suppose you have a form with an input field and a submit button, and you want to prevent the form from being submitted when the user clicks the submit button. Instead, you want to perform some custom validation and handling. Here's how you can use preventDefault:

eg : 

      <!DOCTYPE html>
      <html lang="en">
      <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Prevent Default Example</title>
      </head>
      <body>

      <form id="myForm">
         <label for="username">Username:</label>
         <input type="text" id="username" name="username" required>
         <button type="submit" id="submitButton">Submit</button>
      </form>

      <script>
         document.getElementById('myForm').addEventListener('submit', function(event) {
            // Prevent the default form submission behavior
            event.preventDefault();

            // Perform custom validation or handling
            validateAndSubmit();
         });

         function validateAndSubmit() {
            // Custom validation logic goes here
            var usernameInput = document.getElementById('username');
            var username = usernameInput.value;

            if (username.length < 3) {
            alert('Username must be at least 3 characters long.');
            } else {
            // If validation passes, you can perform the form submission or other actions
            alert('Form submitted successfully!');
            }
         }
      </script>

      </body>
      </html>


## Different Node Methods ?

 ###   1. firstChild : 

         The read-only firstChild property of the Node interface returns the node's first child in the tree, or null if the node has no children.
   - ####   Note: This property returns any type of node that is the first child of this one. It may be a Text or a Comment node. If you want to get the first Element that is a child of another element, consider using Element.firstElementChild

   eg : 

            <p id="para">
            <span>hey</span>
            </p>

            Here first child is the text node.
   - so if we do document.getElementById("para").firstChild it will return #text

   ### In the above, the console will show '#text' because a text node is inserted to maintain the whitespace between the end of the opening <p> and <span> tags. Any whitespace will create a #text node, from a single space to multiple spaces, returns, tabs, and so on.

### 2. Element: firstElementChild and (lastElementChild) property

The Element.firstElementChild read-only property returns an element's first child Element, or null if there are no child elements.
Element.firstElementChild includes only element nodes. To get all child nodes, including non-element nodes like text and comment nodes, use Node.firstChild.

### 3. to get previous and nextSibling 

To specifically get the next and previous sibling elements (skipping text or comment nodes) in JavaScript, you can use the following methods:

1. **`nextElementSibling` Property:**
   - The `nextElementSibling` property returns the next sibling element of the specified element, excluding text nodes and comment nodes.

   Example:
   ```javascript
   var currentElement = document.getElementById('exampleElement');
   var nextElementSibling = currentElement.nextElementSibling;
   ```

2. **`previousElementSibling` Property:**
   - The `previousElementSibling` property returns the previous sibling element of the specified element, excluding text nodes and comment nodes.

   Example:
   ```javascript
   var currentElement = document.getElementById('exampleElement');
   var previousElementSibling = currentElement.previousElementSibling;
   ```

Here's a more complete example:

```javascript
var currentElement = document.getElementById('exampleElement');

// Get the next sibling element
var nextElementSibling = currentElement.nextElementSibling;
if (nextElementSibling) {
    console.log('Next Element Sibling:', nextElementSibling);
} else {
    console.log('No next element sibling.');
}

// Get the previous sibling element
var previousElementSibling = currentElement.previousElementSibling;
if (previousElementSibling) {
    console.log('Previous Element Sibling:', previousElementSibling);
} else {
    console.log('No previous element sibling.');
}
```

These properties directly provide the next and previous sibling elements of the specified element, making it convenient to work with element nodes specifically, excluding text nodes and comment nodes.

### 4. AppendChild

The appendChild() method of the Node interface adds a node to the end of the list of children of a specified parent node.

# Append a paragraph to the body
const p = document.createElement("p");

document.body.appendChild(p);


### 5. contains 

The `contains` method of a Node in JavaScript is used to check if a specific node is a descendant of the given node. It returns a boolean value: `true` if the node is a descendant, and `false` otherwise.

Here's an example to illustrate how the `contains` method works:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Node Contains Example</title>
</head>
<body>

  <div id="parentDiv">
    <p id="childParagraph">This is a paragraph inside a div.</p>
  </div>

  <script>
    var parentDiv = document.getElementById('parentDiv');
    var childParagraph = document.getElementById('childParagraph');

    // Check if parentDiv contains childParagraph
    var isChildInParent = parentDiv.contains(childParagraph);

    if (isChildInParent) {
      console.log('childParagraph is a descendant of parentDiv.');
    } else {
      console.log('childParagraph is not a descendant of parentDiv.');
    }
  </script>

</body>
</html>
```

In this example:

- We have an HTML structure with a `<div>` element (`parentDiv`) containing a `<p>` element (`childParagraph`).
- In the script, we use `document.getElementById` to get references to both the parent and child elements.
- We then use the `contains` method on the `parentDiv` to check if it contains the `childParagraph`.
- The result is stored in the variable `isChildInParent`, and we log a message based on the result.

When you run this script, it should log "childParagraph is a descendant of parentDiv" because the `childParagraph` is indeed contained within the `parentDiv`. If you were to change the parent-child relationship or check for containment in a different way, the result might be different. The `contains` method is useful for checking the hierarchy relationships between nodes in the DOM.


### 5. Element.insertBefore 

The insertBefore() method of the Node interface inserts a node before a reference node as a child of a specified parent node.

If the given node already exists in the document, insertBefore() moves it from its current position to the new position. (That is, it will automatically be removed from its existing parent before appending it to the specified new parent.)


### 6. Element.setAttribute
Sets the value of an attribute on the specified element. If the attribute already exists, the value is updated; otherwise a new attribute is added with the specified name and value.


            <button>Hello World</button>
            const button = document.querySelector("button");
            button.setAttribute("name", "helloButton");

- there are similar methods to setAttribute, like setAttribute sets or adds the new attribute same way, `removeAttribute` removes the attribute, `getAttribute` returns the value of attribute,if attribute not present it returns null. `getAttributeNames` which returns the array of attributes.

### 7. Element.Remove()
The Element.remove() method removes the element from the DOM

---
---
---
---
---
---
---
---
---
# Projects link  regarding DOM and js Events


### Project 1 - Drag and Drop Events
https://github.com/rohitsachdeva27/JS-Example-For-Drag-Drop

### Project 2 - Tic Tac Toe Game
https://github.com/rohitsachdeva27/TicTacToeGame

--- 
---
---
---
---
---
---
---

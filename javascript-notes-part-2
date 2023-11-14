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

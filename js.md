
# Javascript notes



## Authors

### Rohit Sachdeva
### for any suggestions or queries mail to email : codingtitans2@gmail.com


## FAQ

#### 1. what is javascript ?

javascript is a programming language, commonly known as language of web. it is used to make web pages interactive by manipulating dom(document object model). it is a client side programming language.

#### 2. what is client side programming ?

language which runs on clients side is known as clients side language. javascript runs on users browsers thats why it is client side language. 
like : html,css, js

#### 3. what is server side programming language ?

Server side programming language stands for language which runs at server side , server side refers to the server (web server)  other than user physical machine. 

like java is server side programming language because it is used to interact with database generate dynamic data at run time. it cannot execute at users machine.

like : java, dot net, ruby, node js

#### 4. is javascript single threaded or multiple threaded language ?

before jumping to conclusion lets understand what is single threaded and multi threaded.

eg. we have our computer system which comprises of cpu, which is central processing unit, and it is divided into cores.
if we examine we could see our processor is eg : intel core i5 7 generation it has 4 core means it has 4 different areas and at same time it can handle 4 different task.

in our mobile phones also we octa core processor means processor can handle 8 different task .

so in our system how a task is executed ?

a task is known as process, a octa core processor can handle 8 different process at a time. computer system dedicates each task to different thread , consider thread a person (octa core means 8 processor or 8 thread or 8 person).

when one thread completed execution it releases and gets freed and system gives another task to exxecute.

so now js is single threaded or multi threaded ?

it is single threaded --> javascript can perform single task at a time.

#### 8. how can i include javascript in my code ?

There are 2 ways
a. internal using script tag in head tag or body tag
    <script></script>

b. external js file. (linking external js file in the head tag)
    <script src="path to external js file">

#### 9. how to include javascript in our code ?

we can include javascript in our code in head or body section

we know browser reads the file from top to bottom

when we place our script tag in head section then browser reads the script and then reads the body section, means scripy is loaded first before html

when we place our script in body section at the last , it parses the html first then loads the script, wich is good practice, because loading script can cause time delay.

#### 10. what javascript can do or why do we need javascript ?

when we have developed the page structure using html and css, if we need to make the page dynamic like when user clicks then on some action the content should changed or page should behave like this,this can be controlled using javascript.

    a) js can change HTML content
    b) it can change html attribute values
    c) hide/show elements and much more

![image](data:image/png;base64,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)
    

#### 11. what are js variables ?

variables are the containers for storing data , we can declare js variables in 3 different ways.

    1. let ( introduced in es6)
    2. const ( introduced in es6 )
    3. var (since starting of js)


    eg : var a = 10;
    where var is a data type 
    a is variable name 
    10 is value

    lets understand what is declaration and definition.

    variable declaration : variable declaration refers to the specifiying data type and name of variable woitjout assigning a value.
    eg : var a;

    variable definition : Variable definition is the process of both declaring a variable and assigning it an initial value.
    var a = 10;

#### 11. what is identifier ?

    variable name is known as identifier. basically how can a variable can be identified.

    var age = 25; 
    here age is a variable name or identifer.

    Rule for identifers : 
    a) name should begin with letter
    b)reserved words should not be used for identifiers like let, break, for , while


#### 12. what are let and const ?

    variables declared using var can be re-declared means 
    var a = 10;
    var a= 20;

    here we first declared a =10 then re declare a =20;

    while let and const  does not allow re-declaration

    let a=10;
    let a=20;

    error : syntax error 

    const : const is for storuing constant values which do not change during run time.values declared in const cannot be re defined

    const a=10;

    a=20; // it will give error

    eg: const PI= 3.14
    we know value of pi will never change so we can use const variable for this.

    Always declare a variable with const when you know that the value should not be changed.

    Use const when you declare:

    A new Array
    A new Object
    A new Function
    A new RegExp

#### 13. what are different data types in javascript ?

    undefined -> variables which are not defined holds the value undefined
    null -> when user inteyonally adds value null , data type is object.
    number 
    boolean
    string 
    object 


####  what are operators ?

There are various types of operators in js such as.
    
    a)Arithmetic operator
    b) Assignment operator
    c) Comparision Operator
    d)logical Operator
    e)bitwise operator
    f)ternary operator


#### what are various Arithmetic operators ?

The various Arithmetic operator are.

    let a=5,b=10

    a) Addition (+)
        used for addition of 2 values 
            let result = a+b.
            result = 15

    b) Subtraction (-)
        let result = b-a;
            result = 5;

    c) Multiplication (*)
            let result = a*b;
                result = 150;

    d) division (/)
            let result = b/a;
            result = 2

    e) Modulo (%) -- it gives remainder
            let result = b%a;
            result =0;

    f) Exponetiation Operator(introduced in ecma 2016) (**)
        let a=5;
        exponentiation is similar to power 
        a**2 means 5^2 or 5 power 2 which is 25 
        a**2 gives = 25

    g) Increment operator (++)
        increment operator can be used as suffix and prefix 
            let a=10,b=20;
                ++a --> pre increment 
                a++ -> post increment

    Difference between the 2 is in pre increment number is incremented first and in post increment it is later.

    eg ++a + b. -> it will output 31
    because ++a will increment 10 to 11 then add 20         

    a++ + b--> will give 30 
    because it will first add numbers then increment value of a

    h) Decrement operator (--)
    same is for decrement operator. 
    --a , a-- 

#### what are Assignment operators ?
The various assignment operators are :

    a) = -> it is used to assign valye to variable.
    eg: let a= 10

    eg: let a=10;
    a = a+20;

    here a =30 because 10+20 will result into (30) the result will be assigned back to variable a using assignment operator.

    there is also shorthand to this which is 
    a+=20 which means a=a+20

    similary a=a*20 can be written as 
    a*=20



#### what are comparison operator ?

the comparison operators are :

    a) == --> it is used to compare 2 values, it return true or false based on comparison.

    b) === -> it is known as triple equal operator , the difference between == and === operator is that == operator looks to compare 2 values while === operator compares value and type.

    eg : let a= 5 , b=5 

    a==b -> returns true becayse a is 5 and b is also 5 

    a===b --> it return true because value matches both are 5 and type , type of a is number and type of b is also number

    eg :2 let a=5, b="5";
    a==b --> it return true because both are 5
    a===b --> false

    value comparison :  5 ==='5' --> true
    type comparison : number === 'syring' --> false

    c)!= and !==

    d) greater than(>) and less than (<)
        let a=5,b=10;
        a>b --> false;
        b>a --> true 

    e) greater than equal and less than equal (>= and <=)

#### what are logical operators ?

Logical operators in programming are used to perform logical operations on one or more boolean values or expressions. These operators allow you to combine, compare, and manipulate boolean values to make decisions and control the flow of your program. In most programming languages, logical operators include:

1. **AND Operator (`&&`):**
   - The AND operator returns `true` if both of its operands are `true`.
   - It returns `false` if at least one of its operands is `false`.
   - Example: `true && true` evaluates to `true`, while `true && false` evaluates to `false`.

2. **OR Operator (`||`):**
   - The OR operator returns `true` if at least one of its operands is `true`.
   - It returns `false` only if both of its operands are `false`.
   - Example: `true || false` evaluates to `true`, while `false || false` evaluates to `false`.

3. **NOT Operator (`!`):**
   - The NOT operator is a unary operator that negates (flips) the boolean value of its operand.
   - It returns `true` if its operand is `false`, and `false` if its operand is `true`.
   - Example: `!true` evaluates to `false`, and `!false` evaluates to `true`.

Logical operators are commonly used in conditional statements (such as `if`, `else if`, and `while`) to control program flow based on conditions. They are also used to combine multiple conditions to create more complex logic.

Additionally, logical operators follow short-circuiting behavior in many programming languages, which means they may not evaluate all of their operands. For example, in an `&&` expression, if the first operand is `false`, the second operand is not evaluated because the overall result will be `false` regardless of the second operand. This behavior can be leveraged for efficiency and to avoid potential errors in certain situations.

#### what are ternary operator ?

The ternary operator, often referred to as the conditional operator, is a concise way to write conditional statements in many programming languages, including JavaScript. It allows you to evaluate a condition and return one of two values based on whether the condition is true or false.

The syntax of the ternary operator is as follows:

```
condition ? expression_if_true : expression_if_false
```

Here's how it works:

- The `condition` is evaluated first. If it is `true`, the `expression_if_true` is executed, and its value becomes the result of the entire expression. If the `condition` is `false`, the `expression_if_false` is executed, and its value becomes the result.

Here's an example in JavaScript:

```javascript
let isRaining = true;
let weather = isRaining ? "Bring an umbrella" : "Leave your umbrella at home";

console.log(weather); // Outputs: "Bring an umbrella"
```

In this example:

- `isRaining` is the condition.
- `"Bring an umbrella"` is the value returned if the condition is true.
- `"Leave your umbrella at home"` is the value returned if the condition is false.

The ternary operator is often used for simple conditional assignments or to make code more concise when the condition and the two possible outcomes are short expressions. However, for complex conditions or when the expressions involve multiple statements, using a regular `if...else` statement is usually more readable.

#### what does + operator do ?

While the primary purpose of the unary plus (`+`) operator in JavaScript is to convert values to numbers (when possible), it can be used in a few other ways or in combination with other operations:

1. **Mathematical Operations:**
   You can use the unary plus operator to perform mathematical operations. For example:

   ```javascript
   let x = 5;
   let y = 10;
   let sum = +x + +y; // Equivalent to 5 + 10, results in 15
   ```

2. **Parsing Numbers from Strings:**
   It's commonly used to parse numeric values from user input, such as form fields or text boxes, where the input is received as a string. This is a common technique to ensure that user input is treated as a number.

   ```javascript
   let userInput = "42";
   let numberValue = +userInput; // Converts the string "42" to the number 42
   ```

3. **Converting Number-Like Values:**
   The unary plus operator can handle values that are "number-like" but not strictly numeric, such as numbers with trailing spaces.

   ```javascript
   let numberAsString = "42  ";
   let numberValue = +numberAsString; // Converts "42  " to 42
   ```

4. **Converting Dates to Timestamps:**
   You can use `+` to convert a `Date` object to a Unix timestamp (number of milliseconds since January 1, 1970).

   ```javascript
   let now = new Date();
   let timestamp = +now; // Converts the Date object to a timestamp
   ```

5. **Using in Comparison:**
   The unary plus operator can be used in comparisons to convert values to numbers before performing comparisons.

   ```javascript
   let str1 = "5";
   let str2 = "10";
   if (+str1 < +str2) {
     console.log("str1 is less than str2");
   }
   ```

In general, while the primary purpose of the unary plus operator is for type conversion to numbers, it can also be employed in various other contexts where type conversion or mathematical operations are needed. However, you should use it judiciously, as it may make the code less readable when used for purposes other than type conversion.

#### what is difference between ?? and || operator ?

The `??` operator and the `||` operator are both used in JavaScript for handling default values or providing fallback values, but they have some key differences:

1. **Nullish Coalescing Operator (`??`):**
   - The nullish coalescing operator, denoted as `??`, is used to provide a default value when a variable is `null` or `undefined`, but it does not provide a default value for other falsy values such as `0`, `""`, `false`, `NaN`, or empty objects.
   - It specifically checks for `null` or `undefined` and short-circuits (returns the right-hand operand) if the left-hand operand is one of these values.
   - It is designed to handle cases where you want to distinguish between null/undefined and other falsy values.

   Example:
   ```javascript
   let x = null;
   let y = x ?? "Default Value";
   console.log(y); // Outputs: "Default Value"
   ```

2. **Logical OR Operator (`||`):**
   - The logical OR operator, denoted as `||`, is used to provide a default value when a variable is falsy, which includes `null`, `undefined`, `0`, `""`, `false`, `NaN`, and empty objects.
   - It short-circuits (returns the right-hand operand) if the left-hand operand is falsy.

   Example:
   ```javascript
   let x = null;
   let y = x || "Default Value";
   console.log(y); // Outputs: "Default Value"
   ```

In summary, the key difference between `??` and `||` is their behavior when the left-hand operand is a falsy value other than `null` or `undefined`. The `??` operator only checks for `null` or `undefined`, whereas the `||` operator checks for any falsy value. Choose the operator that best fits your specific use case and the behavior you want for handling defaults.

#### what does !! operator do ?

    !! is the double NOT operator, which coerces the operand to a boolean value. It’ll convert truthy values to true and falsy values to false .

    console.log(!!0);  == false
    console.log(!!'');  == false
    console.log(!!false);  == false
    console.log(!!NaN); == false
    console.log(!!undefined);  == false
    console.log(!!null); == false

#### what are truthy and falsy values ?

    truthy values : truthy or true values (values which are not undefined or are not null)

    a) non zero number
    b) non empty strings
    c) arrays
    d) objects 
    e) functions
    f) NaN

    Falsy Values 

    a) 0 
    b) -0 
    c) false 
    d) null
    e) undefined
    f) empty string



#### what are functions in javascript and how can we create a function ?

A function is a block of code designed to perform particular task.

function needs to be invoked to perform a task.
 
 syntax

    function name(parameter1, parameter2, parameter3) {
     // code to be executed
    }   

parameter are basically the inputs to the functions. 

    eg . function add (a,b){
            console.log(a+b)
        }



### what is function invocation ?
    consider we created a function to add 2 numbers.

    function add (a,b){
        console.log(a+b)
    }

this above function will not be called or return us the sum of 2 numbers , we have to call the function.

clling function is known as function invocation.

syntax:

    function_name()


### why do we need function ?

    With functions you can reuse code

    You can write code that can be used many times.

    You can use the same code with different arguments, to produce different results.


#### what is block ?

    a block is denoted using curly braces {}.

    anything enclosed inside this will be called inside a block.

    eg . { // block starts
    let a=10;    // defining variable a inside a block

    } // block ends


    block start: when curly braces or scope of block starts
    block ends: when curly brarces or scope of block ends.

#### what is function declaration and function expression ?

function declaration and function expression are 2 ways to define functions in js.

function declaration : Function declaration defines a function using function keyword followed by function name.

    function add(a, b) {
        return a + b;
    }

function expression :  function expression defines a anonymous function, (a function without name is called anonymous function.) or a function assigned to a variable.

    eg: var add = function(a,b){

    }


#### what are defualt arguments or default parameter values ?

default parameter are a way to provide default values to function paramaters. 

    eg : function add(a,b){
        console.log(a+b)
    }

### add(5) 

    it can clearly seen the function requires 2 arguments but during function call we passed just 1 , it will result in NaN because 5+undefined will result in NaN.

    if we want,if user doesnot assign a value or pass a value to parameter then default value should be assigned to the variable, then we can use the default arguments.

    When a function is called and an argument for a parameter is not provided, the default value is used instead. Default arguments are a convenient way to make functions more flexible and handle cases where not all arguments are provided by the caller.


    function greet(name, greeting = 'Hello') {
    console.log(`${greeting}, ${name}!`);
    }

    greet('Alice'); // Output: "Hello, Alice!"
    greet('Bob', 'Hi'); // Output: "Hi, Bob!"


#### Conditional Statements in js ?

Conditional statements in JavaScript are used to make decisions in your code. They allow you to execute different blocks of code based on whether a specified condition evaluates to true or false. JavaScript provides several conditional statements, including:

## if Statement: 

    The if statement is the most basic conditional statement. It executes a block of code if a specified condition is true.

## if...else Statement:
    The if...else statement allows you to execute one block of code if a condition is true and another block if the condition is false.

## Switch Statement:
    The switch statement is used to test a variable against multiple values and execute different code blocks for each value.


### what is If statement and how to use ?

The if statement in JavaScript is a statement that allows you to execute a block of code if a specified condition evaluates to true.

    if (condition) {
    // Code to execute if the condition is true
    }

### condition: This is a boolean expression or any expression that can be evaluated to true or false. If the condition is true, the code block enclosed within the curly braces {} is executed. If the condition is false, the code block is skipped.

    const age = 25;

    if (age >= 18) {
    console.log("You are an adult.");
    }


#### what is if..else statement ?

in if statement we can execute block of code if condition execute to be true , but what if the condition is false.  
In this case we can use if...else statement 

### syntax:

    if(condition){
        // code to be executed if condition is true
    }else{
        // code to be executed if condition is false.
    }

#### what is if...else...else if statements ?

The `if...else if...else` statement in JavaScript is an extension of the `if...else` statement that allows you to handle multiple conditions in a sequence. It provides a way to test a series of conditions, executing different blocks of code based on the first condition that evaluates to `true`. Here's the syntax:

```javascript
if (condition1) {
  // Code to execute if condition1 is true
} else if (condition2) {
  // Code to execute if condition2 is true
} else {
  // Code to execute if none of the conditions are true
}
```

- `condition1`, `condition2`, etc.: These are boolean expressions or expressions that can be evaluated to `true` or `false`. The conditions are evaluated in the order in which they are written. If `condition1` is `true`, it executes the code block associated with it. If `condition1` is `false`, it moves on to `condition2`, and so on.

Here's an example of how the `if...else if...else` statement works:

```javascript
const temperature = 25;

if (temperature > 30) {
  console.log("It's hot outside.");
} else if (temperature >= 20) {
  console.log("The weather is pleasant.");
} else {
  console.log("It's cold outside.");
}
```

In this example, it first checks if `temperature` is greater than 30. If that condition is `true`, it logs "It's hot outside." If the temperature is not greater than 30, it moves on to the next condition, which checks if the temperature is greater than or equal to 20. If that condition is `true`, it logs "The weather is pleasant." If neither condition is `true`, it executes the code in the `else` block, which logs "It's cold outside."

The `if...else if...else` construct is useful when you have multiple conditions to check in a specific order and want to handle different scenarios based on the first condition that is satisfied.


#### what is switch statement ?

The `switch` statement in JavaScript is a conditional statement that is used to test a variable against multiple values or expressions and execute different code blocks based on the value that matches. It provides an alternative way to handle multiple conditions compared to a series of `if...else if...else` statements.

The basic syntax of the `switch` statement looks like this:

```javascript
switch (expression) {
  case value1:
    // Code to execute if expression === value1
    break;
  case value2:
    // Code to execute if expression === value2
    break;
  // more cases can follow
  default:
    // Code to execute if expression doesn't match any case
}
```

Here's how the `switch` statement works:

- The `switch` statement is provided with an `expression`, which is typically a variable or an expression that you want to compare against the `case` values.

- Inside the `switch` statement, there are multiple `case` labels that represent different values or expressions to be compared to the `expression`.

- If the `expression` matches one of the `case` values, the corresponding block of code associated with that `case` label is executed.

- The `break` statement is used to exit the `switch` statement once a match is found. Without `break`, the code execution would continue into the next `case` block even if a match has already been found.

- If none of the `case` values match the `expression`, the `default` block is executed.

Here's an example of a `switch` statement:

```javascript
const day = "Monday";

switch (day) {
  case "Monday":
    console.log("It's the start of the workweek.");
    break;
  case "Friday":
    console.log("It's almost the weekend!");
    break;
  default:
    console.log("It's a regular day.");
}
```

In this example, the `switch` statement compares the `day` variable to different values and executes the corresponding code block based on the value that matches. In this case, it will execute the code in the "Monday" case because `day` is set to "Monday."

The `switch` statement is particularly useful when you have a variable with multiple possible values and you want to simplify the handling of each value with different code blocks.

#### why do we need loop ?

    loops are used to iterate the statements number of times. loops help us to reduce redundancy.

    without loop : 
    eg. if we want to print number from 1 to 5 without loops , we do like 

    console.log(1)
    console.log(2)
    console.log(3)
    console.log(4)
    console.log(5)

    with loops we can reduce the following line of the code significantly.

#### Different Kinds of Loops ?

    for - loops through a block of code a number of times
    for/in - loops through the properties of an object
    for/of - loops through the values of an iterable object
    while - loops through a block of code while a specified condition is true
    do/while - also loops through a block of code while a specified condition is true


#### what is for-loop ?

syntax:

    for (initialization; condition; update) {
    // Code to be executed in each iteration
    }


    The "initialization" part is executed only once, at the beginning of the loop, to set up the initial conditions.

    The "condition" is checked before each iteration. If it's true, the loop executes the code block inside the loop. If it's false, the loop terminates.

    After each iteration of the loop, the "update" statement is executed, which typically increments or decrements the control variable.

    eg :
        for (let i = 1; i <= 5; i++) {
        console.log(i);
        }

#### While loop ?
    A `while` loop in JavaScript is a control flow structure that repeatedly executes a block of code as long as a specified condition is true. It is often used when you don't know in advance how many iterations are needed and want to continue looping as long as the condition remains true.

The basic syntax of a `while` loop in JavaScript is as follows:

```javascript
while (condition) {
    // Code to be executed as long as the condition is true
}
```

Here's how a `while` loop works:

1. The `condition` is evaluated before each iteration. If the condition is true, the code inside the loop is executed.

2. After executing the code block, the program returns to the `condition`, and if it is still true, the loop continues to the next iteration. This process repeats until the condition becomes false.

3. When the condition becomes false, the loop terminates, and the program continues with the code after the loop.

Here's an example of a `while` loop that prints numbers from 1 to 5:

```javascript
let i = 1;
while (i <= 5) {
    console.log(i);
    i++;
}
```

In this example, `i` is initially set to 1. The `while` loop checks if `i` is less than or equal to 5. If this condition is true, it prints the value of `i`, increments `i` by 1, and then checks the condition again. This process repeats until `i` is no longer less than or equal to 5.

The loop will produce the following output:

```
1
2
3
4
5
```

While `for` loops are typically used when you know the number of iterations in advance, `while` loops are more suitable when the number of iterations depends on a dynamic condition or when you need to create a loop with more complex exit conditions. Be careful when using `while` loops to avoid infinite loops by ensuring that the condition will eventually become false.

#### do-while loop ?

A "do-while" loop in programming is a control flow structure that is similar to a "while" loop, but with a crucial difference: it guarantees that the code block within the loop will be executed at least once, even if the loop's condition is initially false. 

The basic syntax of a do-while loop in most programming languages, including JavaScript, is as follows:

```javascript
do {
    // Code to be executed
} while (condition);
```

Here's how a do-while loop works:

1. The code block inside the `do` is executed first, regardless of whether the condition is true or false.

2. After the code block executes, the program checks the `condition` specified in the `while` statement.

3. If the `condition` is true, the loop will continue to execute the code block and then reevaluate the condition. This process repeats until the `condition` becomes false.

4. If the `condition` is initially false, the code block still executes once before checking the condition. If the condition remains false, the loop terminates after the first iteration.

Here's an example of a do-while loop in JavaScript that prompts the user for a number and continues to prompt until the user enters a positive number:

```javascript
let number;
do {
    number = parseFloat(prompt("Enter a positive number:"));
} while (isNaN(number) || number <= 0);
console.log("You entered a valid positive number: " + number);
```

In this example, the code inside the `do` block prompts the user for a number, and the loop will keep executing as long as the user's input is not a positive number. The loop ensures that the user is prompted at least once, even if they enter an invalid value.

The do-while loop is useful in situations where you want to perform a task that must be done at least once, and then continue repeating the task based on a condition. It's less common than the standard `for` or `while` loops but can be valuable in specific scenarios where you need to guarantee an initial execution.

#### what is parseInt and parseFloat ?
`parseInt` and `parseFloat` are JavaScript functions used for converting strings into numbers. However, they have different use cases and behavior:

1. `parseInt`:
   - `parseInt` is used to parse a string and convert it into an integer (whole number).
   - It starts parsing from the beginning of the string and stops when it encounters a non-numeric character or a decimal point.
   - It also accepts an optional second parameter, the radix, which specifies the base of the number system (e.g., 10 for decimal, 16 for hexadecimal).
   - It discards any decimal portion of the number.
   - Example:
     ```javascript
     const parsedInt = parseInt("123.45"); // Returns 123
     ```

2. `parseFloat`:
   - `parseFloat` is used to parse a string and convert it into a floating-point number (a number that can have a decimal point).
   - It parses the entire string until it encounters an invalid character or the end of the string.
   - It retains the decimal portion of the number, allowing for floating-point values.
   - Example:
     ```javascript
     const parsedFloat = parseFloat("123.45"); // Returns 123.45
     ```

Use Cases:
- Use `parseInt` when you want to convert a string to an integer, discarding any decimal places.
- Use `parseFloat` when you want to convert a string to a floating-point number, retaining decimal places if present in the string.

Here's an example demonstrating the difference:

```javascript
const intResult = parseInt("42.67"); // Result is 42 (decimal portion is truncated)
const floatResult = parseFloat("42.67"); // Result is 42.67 (decimal portion is retained)

console.log(intResult); // Outputs 42
console.log(floatResult); // Outputs 42.67
```

In summary, `parseInt` is for converting strings to integers, and it truncates any decimal portion. `parseFloat` is for converting strings to floating-point numbers, and it retains decimal places if they exist in the string. The choice between them depends on your specific use case and the desired type of conversion.

####  what is break and continue statements ?

In JavaScript, "break" and "continue" are control flow statements used within loops to modify the flow of the program's execution:

1. **break**:

   - The "break" statement is used to exit a loop prematurely. When a "break" statement is encountered inside a loop, it terminates the loop, and program control continues with the next statement after the loop.
   - It is commonly used when you want to exit a loop based on a certain condition being met.

   Example in a "for" loop:
   ```javascript
   for (let i = 1; i <= 5; i++) {
       if (i === 3) {
           break;  // Exit the loop when i is 3
       }
       console.log(i);
   }
   ```

2. **continue**:

   - The "continue" statement is used to skip the current iteration of a loop and move to the next iteration. When a "continue" statement is encountered, the rest of the code inside the current iteration is skipped, and the loop continues with the next iteration.
   - It is often used when you want to skip specific iterations based on a condition without terminating the entire loop.

   Example in a "for" loop:
   ```javascript
   for (let i = 1; i <= 5; i++) {
       if (i % 2 === 0) {
           continue;  // Skip even numbers
       }
       console.log(i);
   }
   ```

Both "break" and "continue" are valuable tools for controlling the flow of loops in JavaScript, allowing you to handle specific conditions or requirements within the loop's execution.

#### what will happen if i have outer and inner loop and i use break statement inside the inner loop ?

**Answer:** The "break" statement inside the inner loop will exit only the inner loop. It does not directly affect the outer loop. The outer loop will continue its execution unless a "break" statement is explicitly used within the outer loop as well. If you want to exit both the inner and outer loops when a condition is met, you would need to use a labeled "break" statement, which specifies the loop to break out of. Here's an example:

```javascript
outerloop:
for (let i = 1; i <= 3; i++) {
    for (let j = 1; j <= 3; j++) {
        if (i === 2 && j === 2) {
            break outerloop;  // This breaks out of both loops
        }
        console.log(`i=${i}, j=${j}`);
    }
}
```

In this example, the labeled "break" statement "break outerloop;" will exit both the outer and inner loops when `i` is 2 and `j` is 2.
 ### try this on console.

####  what are arrays ?

Array is a data structure which can store multiple element in index manner and sequential.

we can declare array like :

    eg : let arr = [];

charactersticks of array

    1. Arrays maintain the order of elements, and each element in the array has a unique position or index
    2. In Other languages , arrays are homogeous which means they only contain same type of data, while in js which is dynamic typed language, it can store the heterogenous data.

    let arr=[1,"a",true];
        here array contains number, string and boolean value.
    3. Arrays provide fast and direct access to elements based on their index.

#### How to access elements of an array ?

Array are type of Object. 
    let arr = [1,2,3,4]

    typeof arr => 'object'

Array declaration => let arr = []

    here variable arr in type of array , which does not have any value.

    lets declare an array with elements 

    let arr =[10,20,30,40,50,60,70,80]
    
    as we know arrays are index based which means elements are stored at index starting from zero 

    at index 0 => 10 
    at index 1 => 20
    at index 2 => 30
    at index 3 => 40
    at index 4 => 50
    at index 5 => 60
    at index 6 => 70
    at index 7 => 80
    at index 8 => 90

### if we want to access first element which means which have to get the zero index element.

    to get the zero index element we have to do :

        arr[0] => 10
        arr[1] => 20
        arr[5] => 60
    


#### how to check length of an array ?  

    we can check length of an array using length property.

    let arr=[1,2,3,4,5,6,7,8,9]
     arr.length => 9 

#### what is Array constructor ?

    In JavaScript, the `Array` constructor is a built-in constructor function that is used to create and initialize arrays. You can use it to create new arrays, either empty or with initial values. The `Array` constructor can be called in two ways:

1. **Using `new` keyword**:

   You can create an empty array by invoking the `Array` constructor with the `new` keyword. You can also pass a single argument, which specifies the initial length of the array.

   ```javascript
   const emptyArray = new Array();
   const arrayWithLength = new Array(3); // Creates an array with a length of 3
   ```

   Note that when you provide a single numeric argument, it sets the length of the array, but the actual elements are `undefined`.

2. **Using array elements**:

   You can create an array by passing individual values as arguments to the `Array` constructor. These values become the elements of the array.

   ```javascript
   const fruits = new Array('apple', 'banana', 'cherry');
   ```

   This is equivalent to creating an array using array literal notation:

   ```javascript
   const fruits = ['apple', 'banana', 'cherry'];
   ```

Using array literals is the more common and preferred way to create arrays in JavaScript because it's more concise and readable. The `Array` constructor is rarely used in practice, except for some specific scenarios where you need to create an array with a specified length.

It's important to be aware of potential issues with using the `Array` constructor to create arrays, particularly when dealing with a single numeric argument. In some cases, it might be more intuitive and safer to create arrays using array literals or other array creation methods provided by JavaScript.

#### how to add and remove elements from array ?

    There are 4 different methods to add or delete elements in array .

    1. Push => Adds one or more elements to the end of an array.

    let fruits = ['apple', 'banana'];
    fruits.push('cherry');
    // fruits is now ['apple', 'banana', 'cherry']

    we can push more than 1 element 

    fruits?.push('orange','mango')
    // ['apple','banana','cherry','orange','mango'];

  2. Pop :  Removes the last element from an array.

    let arr= [1,2,3,4]
    arr.pop() -> returns 4

  3. Unshift: Adds one or more elements to the beginning of an array.

    let fruits = ['banana', 'cherry'];
    fruits.unshift('apple');
    // fruits is now ['apple', 'banana', 'cherry']

  4. Shift : Removes the first element from an array.

    let fruits = ['apple', 'banana', 'cherry'];
    fruits.shift();
    // fruits is now ['banana', 'cherry']







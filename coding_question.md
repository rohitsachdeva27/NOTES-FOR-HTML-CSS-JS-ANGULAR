## Beginner 




## 1   WAP to print hello world in js ?

    function helloWorld(){
        console.log("Hello World!")
    }

    helloWorld();

    output => Hello World!

## 2. WAP to print your name ?

    function printName(name){
        console.log("My Name is "+name);
    }

    printName("Alex");

    output => My Name is Alex

## 3. Get Input from user and print it ?

    In JavaScript, `prompt` is a built-in function that displays a dialog box with a message and an input field for the user to enter data. It's a way to interact with users and collect information from them in a simple text-based form. The `prompt` function takes two arguments:

1. **Message (optional)**: A string that serves as the message or prompt displayed to the user. This message typically instructs the user on what kind of input is expected.

2. **Default Value (optional)**: A string that is pre-filled in the input field as the default value. The user can either accept this value or provide a different one.

Here's the basic syntax for using the `prompt` function:

```javascript
let userInput = prompt(message, defaultValue);
```

The user's input, once entered, is returned as a string, or `null` if the user cancels the prompt. It's important to note that the `prompt` function can only capture simple text input and returns the result as a string, regardless of the actual data type of the input.

Example:

```javascript
let no = prompt("Enter Number");
if (no !== null) {
  alert("The number is , " + no + "!");
} else {
  alert("You canceled the prompt.");
}
```

In this example, the user is prompted to enter their name. If they enter a name and click "OK," their no is stored in the `no` variable, and an alert displays a greeting. If they click "Cancel," `no` will be `null`, and an alert indicates that the prompt was canceled.

It's important to handle the case where the user clicks "Cancel" to prevent unexpected behavior in your JavaScript code, as `null` is returned when the prompt is canceled.

## 4. Swap 2 numbers ?

    function swapNumbers(a,b){

        let temp = a;
        a = b;
        b = temp;

        console.log(a,b);
    }


## 5. Calculate Farhenhit to calcius ?

- the formula for converting the temp from faherehnhit to celcius is 

- temp in c = (F-32)*5/9
- temp in f = (c * 9/5) + 32

        function convertTempToCelcius(temp){
        let result;
        result = ((temp - 32) * 5)/9;
        console.log(result);

    }


## 6. print Prime numbers from 1 to n ?

Answer

## 7. Wap to check whether number is positive, negative or zero ?

    function checkNumberEvenOrOdd(no){

        if(no < 0)
        console.log("Number is negative")
        else if(no > 0)
        console.log("number is positive")        
        else 
        console.log("number is zero");
    }

## 8. WAP to check Whether Number is Even or Odd?

    function checkNumberEvenOrOdd(num){
        if(isNaN(num) || num == 0)
        console.log("Not a valid number")
        else if(num %2 === 0)
        console.log("number is even");
        else if (num %2 !==0 )
        console.log("number is odd");
        
    }


## 9. Check Whether a Character is Vowel or Consonant ?

-  the function will check whether user inputs correct character from a-z or A-Z .
- after checking check whether the input character is either 
    `a,e,i,o,u` so it will vowel else constant.
- we can ignore case like if user enters a or A it should be converted to lowerCase first and then check.

####  to check whether input character is character we can check the ascii code or unicode code (<stringInput>.charCodeAt())

        
         function checkVowelOrConstant(char){

             let charCode = char.toLowerCase().charCodeAt();
             let vowels = ['a','e','i','o','u'];

             if(charCode >=97 && charCode <=122){
                 if(vowels.includes(char.toLowerCase()))            
                 console.log("vowel")
                 else 
                 console.log("constant")
             }else{
                 console.log("not a character");
             }
         }


## 10. WAP to Find Largest Number Among Three Numbers ?
    
- to find largest among 3 numbers we have to compare 3 numbers with each other 
- consider 3 numbers to be 10,20,5
-  first 10 will be compared with 20 and 10 will be compared with 5, if is false we will move to second number comparison.
- if not we will check for 20 with other 2 numbers, (20 > 10 && 20> 5) it is  true means 20 is largest.

        function LargestNumber(a,b,c){

            if(a > b && a> c{
                console.log("a is largest")
            }
            else if(b > a && b>c){
                console.log("b is largest");                
            }
            else if(c > a && c > b){
                console.log("c is largest");
            }
        }

## 11. WAP to Calculate Sum of Natural Numbers  ?

    way : 1

        function sumOfNaturalNumbers(n) {

            let sum = 0;
            for(let i=1;i<n;i++){
                sum+=i;
            }
            console.log(sum);
        }
----
    way : 2
- sum of n natural numbers can be calculated using n*(n+1)/2

        function sumOfNaturalNumbers(n){
            let result = (n*(n+1))/2;
            console.log(result);
}


## 12. Wap to print Alphabets From A to Z  ?

- String.fromCharCode(charCode). - returns the character at the paryicular code.

- unicode charCode of A is 65 and a is 97

        function printAlphabets(){

            for(let i = 'A'.charCodeAt();i<='Z'.charCodeAt();i++){
                console.log(String.fromCharCode(i))
            }
        }

## 13. Check Leap Year?

    To check if a year is a leap year in JavaScript, you can use the following criteria: A leap year is either:

    1. Divisible by 4, but not divisible by 100, or
    2. Divisible by 400.

Here's a JavaScript function to check if a year is a leap year based on these criteria:

```javascript
function isLeapYear(year) {
  // Check if the year is divisible by 4 and not divisible by 100, or divisible by 400
  return (year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0);
}

// Example usage:
const yearToCheck = 2024;
if (isLeapYear(yearToCheck)) {
  console.log(`${yearToCheck} is a leap year.`);
} else {
  console.log(`${yearToCheck} is not a leap year.`);
}
```

In this code:

- The `isLeapYear` function takes a `year` as input.
- It checks two conditions:
  - The year should be divisible by 4 and not divisible by 100 (`year % 4 === 0 && year % 100 !== 0`).
  - Alternatively, the year can be divisible by 400 (`year % 400 === 0`).
- If either of these conditions is met, the function returns `true`, indicating that the year is a leap year. Otherwise, it returns `false`.

You can replace the `yearToCheck` variable with any year you want to check, and the function will determine if it's a leap year.


## 14. Find Factorial of a Number?
- factorial of a number can be calculated by multiplying that number with the subequent descending number like 

    factorial of 5 can be calculated as 
        5 * 4 * 3 * 2 *1 = 120 
    
how can we do this using code ?

- we can subsequent multiply the number with its decrement value like.

        function factorial(num){
            let fact=1;      // step 1
            for(let i=num;i>0 ;i--){                
                fact*=i;
            }
            console.log("factorial of number is = ",fact)
        }

### explanation
- step 1 :  we took a variable fact and initailize it with default value 1.
- we iterate the number , but now we did the initialization with the num because we wanted the loop to start from number and should go till 1.
- fact = fact * i and after each statement i will be decrement by 1.


## 15. Make a Simple Calculator 

Answer

## 16. Print Fibonacci Series ?

Answer

## 17. Check Armstrong Number ?

Answer

## 18. Reverse a Number ?

Answer

## 19. Check Whether a Number is a Palindrome or Not ?

Answer

## 20. Find All Factors of a Natural Number ?

Answer


## Intermediate 

### 1. Display Armstrong Numbers Between 1 to 1000 ?

Answer


### 2. 

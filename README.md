# lection1
## What Is JavaScript?
JavaScript (JS) is a computer programming language used to make websites and applications dynamic and interactive.
It’s unique because it can run directly in your browser, not just on a server.
Along with hypertext markup language (HTML) and cascading style sheets (CSS), JavaScript is one of the most commonly used programming languages of the internet.
 
 In fact, 98.4% of all websites use JavaScript as of March 2023.

JavaScript, CSS, and HTML work together to make up the user-facing elements of most websites and online applications.

Think of these coding languages as the components of a house:

HTML is the foundation of the house. It provides the basic layout, structure, and content of a website.
CSS is the interior design. It provides design, fonts, colors, effects, and other visual elements. 
JavaScript is the electrical and plumbing systems. JS brings dynamism and interactivity to the website. For example, pop-ups, animations, video and social media embeds, drop-down menus, and many other website components are created using JavaScript.
______

 ## History of JavaScript.
  Brendan Eich developed JavaScript in 1995 while working for Netscape.

Netscape sought to develop a scripting language that could help make early versions of the World Wide Web more dynamic.

JavaScript quickly gained popularity as developers realized its ability to add dynamism and interactivity to webpages. 

In 1996, Netscape submitted JavaScript to the European Computer Manufacturers Association (ECMA International), an organization that aims to standardize the use of information technology systems.

This led to the creation of the ECMAScript standard, the formal specifications for JavaScript. 

Its growing popularity has facilitated the development of libraries and frameworks, dedicated JS engines such as V8 (which powers Chrome), and server-side environments.

Despite similarities in name, JavaScript is entirely different from Java.
_____
## Functions
Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.
  ## Defining functions
  ### Function declarations
A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:
 
+ The name of the function.
+ A list of parameters to the function, enclosed in parentheses and separated by commas.
+ The JavaScript statements that define the function, enclosed in curly braces, { /* … */ }.

For example, the following code defines a simple function named square:

JS
Copy to Clipboard
function square(number) {
  return number * number;
}
The function square takes one parameter, called number. The function consists of one statement that says to return the parameter of the function (that is, number) multiplied by itself. The return statement specifies the value returned by the function, which is number * number.
____
### Function expressions
While the function declaration above is syntactically a statement, functions can also be created by a function expression.

Such a function can be anonymous; it does not have to have a name. For example, the function square could have been defined as:

JS
Copy to Clipboard
+ const square = function (number) {
  return number * number;
};

console.log(square(4)); // 16
However, a name can be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces:
  + const factorial = function fac(n) {
  return n < 2 ? 1 : n * fac(n - 1);
};

console.log(factorial(3)); // 

 Function expressions are convenient when passing a function as an argument to another function. The following example shows a map function that should receive a function as first argument and an array as second argument:
____

 ### Calling functions
 Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters. For example, if you define the function square, you could call it as follows:
+ square(5);
he preceding statement calls the function with an argument of 5. The function executes its statements and returns the value 25.

Functions must be in scope when they are called, but the function declaration can be hoisted (appear below the call in the code). The scope of a function declaration is the function in which it is declared (or the entire program, if it is declared at the top level).

A function can call itself. For example, here is a function that computes factorials recursively:

JS
Copy to Clipboard
 + function factorial(n) {
  if (n === 0 || n === 1) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}
You could then compute the factorials of 1 through 5 as follows:

JS
Copy to Clipboard
+ console.log(factorial(1)); // 1
 + console.log(factorial(2)); // 2
 + console.log(factorial(3)); // 6
 + console.log(factorial(4)); // 24
 + console.log(factorial(5)); // 120

 ____

 # JavaScript Variables and Constants
 ## JavaScript Variables
In programming, a variable is a container (storage area) to hold data. For example,
+ let num = 5;
Here, num is a variable. It's storing 5.
## JavaScript Declare Variables
In JavaScript, we use either var or let keyword to declare variables. For example,
+ var x;
 + let y;
 Here, x and y are variables.
 ## JavaScript var Vs let.
 Both var and let are used to declare variables. However, there are some differences between them.
 ### Var
 + var is used in the older versions of JavaScript.
 + var is function scoped (will be discussed in later tutorials).
 + For example, var x;
 ### Let
 + let is the new way of declaring variables starting ES6 (ES2015).
 + let is block scoped (will be discussed in later tutorials).
 + For example, let y;
 Note: It is recommended we use let instead of var. However, there are a few browsers that do not support let. Visit JavaScript let browser support to learn more

 # Primitive types vs objects in JavaScript
hat is the main difference between primitive types and objects in JavaScript?

First, let’s define what are primitive types.

Primitive types in JavaScript are
+ strings
+ numbers (Number and BigInt)
+ booleans (true or false)
+ undefined
+ Symbol values
null is a special primitive type. If you run typeof null you’ll get 'object' back, but it’s actually a primitive type.

Everything that is not a primitive type is an object.

Functions are objects, too. We can set properties and method on functions. typeof will return 'function' but the Function constructor derives from the Object constructor.

The big differences between primitive types and objects are

+ primitive types are immutable, objects only have an immutable reference, but their value can change over time
+ primitive types are passed by value. Objects are passed by reference
+ primitive types are copied by value. Objects are copied by reference
+ primitive types are compared by value. Objects are compared by reference

# Operators IN JavaScript
+ Arithmetic - +,-,*,/
+ Comprasion ==, ===, >=, <=, !=, !==
+ Logical    ||, &&, !
+ Type Conversions    Number("3.14")
+ Assignment    =, +=, -=, *=, /=, %=
___
## CONDITION If/else statement
+ bignumber(n1,n2){
     if(n1>n2){
      return n1;
     }
     return n2;
}
   console.log(bignumber(12,8))
 ## CONDITION Ternary operator
 The conditional (ternary) operator is the only JavaScript operator that takes three operands: a condition followed by a question mark (?), then an expression to execute if the condition is truthy followed by a colon (:), and finally the expression to execute if the condition is falsy. This operator is frequently used as an alternative to an if...else statement.
 + bignumber(n1,n2){
    n1>n2? n1:n2;
 }

 ## CONDITION Switch statment.
 Use the switch statement to select one of many code blocks to be executed.
 + switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}

## LOOP for.
Loops are handy, if you want to run the same code over and over again, each time with a different value.
 + for(let i=0; i<=a; i++){
      console.log(i)
 }
 ## The While Loop.
 The while loop loops through a block of code as long as a specified condition is true.
 + while (i < 10) {
  text += "The number is " + i;
  i++;
}
## LOOP Do/while.
The do...while statements combo defines a code block to be executed once, and repeated as long as a condition is true.

The do...while is used when you want to run a code block at least one time.

##

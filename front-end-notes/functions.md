# Functions

A function is an arbitrary amount of code that can be _called_ by other code internal or external to the function.  The code statements inside of the function are called the _body_.  Functions can be passed in data as _arguments_ when called, and will always _return_ a value.

In JavaScript, functions are declared with the keyword _function_ followed by parentheses which can contain argument names, followed by the function body contained within curly braces.  When declared in this manner, without a name, it is known as an _anonymous function_.  Anonymous functions run immediately upon program execution reaching them and cannot be called otherwise.

An anonymous function with no arguments that opens an alert:
```
function() {
  alert("Hi!");
}
```

When declared with a name, the name follows the _function_ keyword and precedes the parentheses.  Function naming follows the same rules as JavaScript variable naming.  Named functions can be called by name from elsewhere in the program by using their name followed by parentheses & a semicolon, and will not run otherwise.

A function named _foo_ that opens an alert:
```
function foo() {
  alert("Hi again!");
}
```
Calling _foo_ elsewhere:
```
foo();
```

The parentheses of a function can contain arguments that are then available within the function body.  These arguments can be passed in when calling the function by including data within the parentheses of the function call.  Functions can take up to 255 arguments.  Not all arguments are required to call a function, and any arguments passed on call will populate the argument list from left to right in order.

A function _bar_ that takes one argument:
```
function bar(arg) {
  alert(arg);
}
```
Calling _bar_ with an argument of "Hello", which will result in an alert that says _Hello_:
```
bar("Hello");
```
A function _fizz_ that takes 5 arguments:
```
function fizz(firstArg, secondArg, thirdArg, fourthArg, fifthArg) {
  alert(thirdArg);
}
```
Two calls of _fizz_, the first resulting in an alert saying _Hello_ the second resulting in an alert saying _undefined_:
```
fizz("buzz", "fish", "Hello");

fizz("buzz", "fish");
```

All functions return a value.  If not explicitly defined with a _return_ statement, a function will return _undefined_.  Return values can be any legitimate data type (string, boolean, integer, float, function, object, etc.).

Example of a function that when called will always return the value _3_:
```
function threeGiver() {
  return 3;
}
```
Example of a function that does work on arguments passed in and then returns the result:
```
function adder(arg1, arg2) {
  return arg1 + arg2;
}

adder(3, 2); // return value of 5
```

These return values can be used/captured by setting a variable equal to the function call.

Example of using _threeGiver_ to set a variable _numberHolder_ to _3_:
```
var numberHolder = threeGiver();
```

Function declarations are _hoisted_, and as such the function is brought into memory at program execution and is available for calling even before the function declaration block in the code.  For example, this will run even though the function call appears before the function declaration:
```
theFunction();

function theFunction() {
  alert("I work");
}
```
For further information, see [hoisting](https://github.com/elizabrock/software-development-curriculum/blob/master/front-end-notes/hoisting.md)

Functions can also be invoked as a _function expression_ instead of a _function declaration_.  The format for that is setting a variable equal to the declaration of either a named or unnamed function.  Both of these are examples of a function expression:
```
var firstFunc = function() {
  alert("I'm a function expression");
}

var secondFunc = function namedFunc() {
  alert("I am also a function expression!");
}
```

Functions are useful for code that needs to be excuted more than once in a program.  Instead of duplicating code, the code can be placed in a function that can then be called as needed.

For further information on functions, check the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions" target="_blank">Mozilla Development Network documentation on functions</a>.
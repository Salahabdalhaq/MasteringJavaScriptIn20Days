
**Scope:**

Scope in programming refers to the context in which variables are defined and accessed. It determines where a variable can be accessed and where it cannot. Understanding scope helps in managing variable access and preventing unintended conflicts.

```javascript
var teacher = "salah";

function otherClass() {
  teacher = "ahmad";
  topic = "math";
  console.log("FFF");
}

teacher; // "salah"

otherClass(); // Logs "FFF"

teacher; // "ahmad"
topic; // "math"
```

The variable `teacher` is initially set to "salah". The function `otherClass` updates the `teacher` variable to "ahmad" and creates a global variable `topic` with the value "math". When the function is invoked, "FFF" is logged to the console. After the function call, `teacher` is "ahmad", and `topic` is "math".

Adding `"use strict"` enforces strict mode, catching common coding mistakes:

```javascript
"use strict"
var teacher = "salah";

function otherClass() {
  teacher = "ahmad"; // ReferenceError: assignment to undeclared variable "teacher"
  topic = "math"; // ReferenceError: assignment to undeclared variable "topic"
  console.log("FFF");
}

otherClass();
```

**Scope & Function Expressions:**

Function expressions are named or anonymous functions defined within expressions. Naming functions provides benefits such as reliable self-reference, better debuggable stack traces, and more self-documenting code.

Naming benefits:
1. Reliable function self-reference.
2. Improved debuggable stack traces.
3. Enhanced self-documenting code.

Understanding scope and using meaningful function names contribute to writing clearer and more maintainable code.

**QUESTION #1**
Create a function called arrowHOF that takes an arrow function as input and returns a new arrow function that enhances the behavior of the input function.

The enhanced function should accept additional arguments and execute the input function multiple times based on these arguments.
```javascript
const exampleNormalFunc1 = (a, b, c) => {
  return a * (b + c);
}

const exampleNormalFunc2 = (x, y) => {
  return x * y;
}

const exampleNormalFunc3 = (string) => {
  return string + " " + string + " " + string + "!";
}


const arrowHOF = (normalFunc) => {
  return (...argsOuter) => {
    return (...argsInner) => {
      const resultOuter = normalFunc(...argsOuter);
      const resultInner = normalFunc(...argsInner);
      return () => {
        for (let i = 0; i < resultInner; i++) {
          console.log(resultOuter);
        }
    };};};};

const hofNormalFunc1 = arrowHOF(exampleNormalFunc1);
const hofNormalFunc2 = arrowHOF(exampleNormalFunc2);
const hofNormalFunc3 = arrowHOF(exampleNormalFunc3);

console.log(hofNormalFunc1(3, 4, 5)(2)); // logs 60 twice
console.log(hofNormalFunc2(20, 35))(4); // logs 700 four times
console.log(hofNormalFunc3("Meow")()); // logs "Meow Meow Meow!" once
```


**QUESTION #2**
Build a function called preserveThis that takes a function as input and returns a new arrow function that behaves the same way as the input function but preserves the original this context when used as a method of an object.

// Example object
const obj = {
  name: 'John',
  greet: function (greeting) {
    console.log(`${greeting}, ${this.name}!`);
  }
};

const preserveThis = (func) => {
  return function (...args) {
    return func(...args);
  };
};

// Wrap the greet function using preserveThis
const preservedGreet = preserveThis(obj.greet);

// Call the wrapped function as a method of the object
preservedGreet('Hello'); // Output: "Hello, John!"

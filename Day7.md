**JavaScript Principles:**

- When running JavaScript code, it goes through line by line, executing each line. This process is known as the "thread of execution."

- Data is stored in memory while the code is running.

- JavaScript executes one thread at a time.

**Call Stack:**

- When a function is called, it's added to the call stack.

- When a function finishes executing, it's removed from the call stack.

- The function at the top of the stack is the one currently running.

**Functions & Callbacks:**

- Functions can be made more general to avoid repeating the same code multiple times.

- In JavaScript, functions are first-class objects, which means they can be treated like any other JavaScript object.

- Functions can be:
  1. Assigned to variables.
  2. Passed as arguments to other functions.
  3. Returned as values from other functions.

**Pair Programming:**

Pair programming is a development technique where two programmers work together at one computer. They switch between the "driver," who writes code, and the "navigator," who reviews and guides the process.

**1.Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem:**
Challenge Link: [Use Higher-Order Functions map, filter, or reduce to Solve a Complex Problem](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-higher-order-functions-map-filter-or-reduce-to-solve-a-complex-problem)

```javascript
const squareList = arr => {
  // Only change code below this line
  return arr.filter(num => Number.isInteger(num) && num > 0).map(num => num * num);

  // Only change code above this line
};

const squaredIntegers = squareList([-3, 4.8, 5, 3, -3.2]);
console.log(squaredIntegers);

```

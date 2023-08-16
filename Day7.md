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

**2.Apply Functional Programming to Convert Strings to URL Slugs:**
Challenge Link: [Apply Functional Programming to Convert Strings to URL Slugs](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/apply-functional-programming-to-convert-strings-to-url-slugs)

```javascript
// Only change code below this line
function urlSlug(title) {
   return title 
    .split(' ') 
    .filter(word => word !== '') 
    .map(word => word.toLowerCase()) 
    .join('-');
}
// Only change code above this line
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");
```

Sure, here are the questions as you provided them:

**Question 3: Functions and Callbacks**
Implement a JavaScript function called `mapAsync` that takes an array and a callback function. The function should map each element of the array to a new value using the callback function asynchronously.

The final result should be returned as a Promise.


###############################################

**Question 4: Call Stack and Recursion**
Write a JavaScript function called `sumRange` that calculates the sum of all integers in a given range. The function should use recursion to handle the calculation and demonstrate understanding of the call stack.
```javascript
function sumRange(from, to) {
  if (start > end) {
    return 0;
  }
  return from + sumRange(from + 1, to;
}

```




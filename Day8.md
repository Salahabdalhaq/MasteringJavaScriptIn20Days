
**Closure:**

- Functions can be returned from other functions in JavaScript.

```javascript
function createFunction() {
  function multiplyBy2(num) {
    return num * 2;
  }
  return multiplyBy2;
}

const generateFunc = createFunction();
const result = generateFunc(3); // Output: 6
```

- Calling a function within the same function call as it was defined:

```javascript
function outer() {
  let counter = 0;
  function incrementCounter() {
    counter++;
  }
  incrementCounter();
}
outer();
```

- Calling a function outside of the function call in which it was defined:

```javascript
function outer() {
  let counter = 0;
  function incrementCounter() {
    counter++;
  }
  return incrementCounter;
}
const myNewFunction = outer();
myNewFunction(); // Output: 1
```

- Closures create a "backpack" of live data attached to the function.

- Closure gives our function persistent memory.

**Asynchronous JavaScript:**

- Promises are a significant ES6 feature.

- Asynchronous behavior is a crucial feature that enables dynamic web applications.

- In JavaScript, tasks must be completed before moving on.

- JavaScript alone is not sufficient; we use JavaScript in conjunction with web features like `setTimeout` or DOM manipulation.

- Closure allows functions to remember the variables of their parent scope even after the parent function has finished executing.

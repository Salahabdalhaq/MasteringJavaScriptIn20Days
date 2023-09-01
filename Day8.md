
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


**Question 1:**
Write a closure named `createCounter` that takes an initial value `start` and returns a function. The returned function, when invoked, should increment the counter by 1 and return the updated value.

```javascript
function createCounter(start) {
  let counter = start;
  
  function incrementCounter() {
    counter++;
  }
  
  return incrementCounter();
}

const myNewFunction = createCounter();
myNewFunction(1); //2

```


**Question 2:**
Write a closure named `calculateAverage` that takes an array of numbers, `nums`, and returns a function. The returned function, when invoked, should calculate and return the average of the numbers in the array.
```javascript
function calculateAverage(nums) {
  let sum = 0;

  function avegSum() {
    for (let i = 0; i < nums.length; i++) {
      sum += nums[i];
    }
    return sum / nums.length; 
  }

  return avegSum; 
}
const averageCalculator = calculateAverage([2,5, 4, 6, 8, 10]);

averageCalculator(); 
```
**Question 3:**
Write a closure named `powerOf` that takes a base number `base` and returns a function. The returned function, when invoked with an exponent `exp`, should calculate and return the result of `base` raised to the power of `exp`.

```javascript
function powerOf(base) {
  return function(exp) {
    return Math.pow(base, exp);
  };
}
const newPowerOf = powerOf(3);
newPowerOf() ; // 8
```





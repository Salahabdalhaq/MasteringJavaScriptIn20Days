
**Lexical Scope:**

- Lexical scope refers to the scope determined by the location of code in the source code.

```javascript
var teacher = "salah";

function otherClass() {
  var teacher = "ahmad";

  function ask(question) {
    console.log(teacher, question);
  }
  ask("way?");
}
```

**Dynamic Scope:**

- Dynamic scope refers to scope determined by the location of the calling code, not the location of the code in the source code.

```javascript
var teacher = "salah";

function ask(question) {
  console.log(teacher, question);
}

function otherClass() {
  var teacher = "ahmad";
  ask("way?");
}

otherClass();
```

**Function Scoping:**

- Variables defined within a function are not accessible outside the function's scope.

**IIFE (Immediately Invoked Function Expression) Pattern:**

- IIFE is used to create a new scope to prevent variable name clashes.

```javascript
var teacher = "salah";

(function anotherTeacher() {
  var teacher = "suzy";
  console.log(teacher); // Output: suzy
})();
```

**Block Scoping:**

- Variables declared using `let` and `const` are block-scoped.

```javascript
var teacher = "salah";

{
  let teacher = "ahmad";
  console.log(teacher); // Output: ahmad
}

console.log(teacher); // Output: salah
```

**Hoisting:**

- Variables declared using `var` are hoisted to the top of their scope.

```javascript
student; // undefined
teacher; // undefined
var student = "salah";
var teacher = "ahmad";
```


**Question #1:**

Given the following code snippet and explain what's happening.

```javascript
for (var i = 0; i < 5; i++) {
    setTimeout(function() {
      console.log("value of [i] is: ", i);
    }, 100);
}
```


**Solution:**
The issue is that using 'var' in the loop makes the variable shared

```javascript
for (let i = 0; i < 5; i++) {
    setTimeout(function() {
      console.log("value of [i] is: ", i);
    }, 100);
}
```


**Question #2:**

Given the following code snippet and explain what's happening.

```javascript
for (let i = 0; i < 5; i++) {
   let array = [];
   array.push(i);
   console.log("Current array is: ", array);
}
```

**Solution:**
The code uses a loop to iterate from 0 to 4. In each iteration, a new array is created, and the current value of 'i' is added to it. The array is then printed to the console.
```javascript
 let array = [];
for (let i = 0; i < 5; i++) {
   array.push(i);
}
  console.log("Current array is: ", array);
```


**Question #3:**

Given the following code snippet and explain what's happening.

```javascript

let functions = [];

for (var i = 0; i < 5; i++) {
  functions.push(() => {
    console.log("Current value of i is:", i);
  });
}

functions.forEach((func) => func());

```
The current output is:

"Current value of i is: 5" "Current value of i is: 5" "Current value of i is: 5" "Current value of i is: 5" "Current value of i is: 5"

The output should be:

"Current value of i is: 0" "Current value of i is: 1" "Current value of i is: 2" "Current value of i is: 3" "Current value of i is: 4"


**Solution:**
The issue is that using 'var' in the loop makes the variable shared

```javascript

let functions = [];

for (let i = 0; i < 5; i++) {
  functions.push(() => {
    console.log("Current value of i is:", i);
  });
}

functions.forEach((func) => func());

```

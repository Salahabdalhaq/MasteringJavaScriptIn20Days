
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


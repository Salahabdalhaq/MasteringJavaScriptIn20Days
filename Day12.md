
**Philosophy of Coercion:**

Coercion in programming refers to the automatic conversion of one data type into another. It often occurs when operations are performed on variables of different data types. Understanding coercion helps us write code that behaves predictably and avoids unexpected errors.

**Coercion Exercise:**

**Function `isValidName`**

```javascript
function isValidName(name) {
  if (typeof name === "string" && name.trim().length >= 3) {
    return true;
  }
  return false;
}
```

**Function `hoursAttended`**

```javascript
function hoursAttended(attended, length) {
  if (typeof attended === "string" && attended.trim() !== "") {
    attended = Number(attended);
  }

  if (typeof length === "string" && length.trim() !== "") {
    length = Number(length);
  }

  if (
    typeof attended === "number" &&
    typeof length === "number" &&
    attended >= 0 &&
    length >= 0 &&
    Number.isInteger(attended) &&
    Number.isInteger(length) &&
    attended <= length
  ) {
    return true;
  }
  return false;
}
```

In the `isValidName` function, the code checks if the input name is a non-empty string with a length of at least 3 characters. If so, it returns `true`.

In the `hoursAttended` function, the code handles potential coercion scenarios. It first checks if the input `attended` and `length` are non-empty strings. If so, it coerces them into numbers. Then it checks if both inputs are valid numbers, integers, and satisfy the conditions specified. If all conditions are met, it returns `true`.

**Equality:**

The `==` operator allows coercion for different types, while the `===` operator disallows coercion and requires both types to be the same.

**Algorithm == Summary:**
- If the types are the same: use `===`.
- If `null` or `undefined`: consider them equal.
- If dealing with non-primitives: coerce to primitive.
- Prefer: use `ToNumber`.

`[] == ![]` // true (Yes, that's correct!)

However, it's recommended to use `==` carefully and avoid:
1. Comparing with 0, "", or " ".
2. Comparing with non-primitives.
3. Using `==` with `true` or `false`; use `toBoolean` or `===` instead.

**Static Typing:**

Languages like TypeScript and Flow offer static typing.
Benefits:
1. Detect type errors.
2. Communicate type intent.
3. Provide feedback in IDEs.

Example:
```typescript
type Student = { name: string };
function getName(studentRec: Student): string {
  return studentRec.name;
}
```

Using static typing enhances code quality and helps prevent type-related bugs.

**QUESTION #1:**


**QUESTION #2:**
What will be the output of the following code snippet? Pick the right choice then justify your answer with an explanation.

```javascript
function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();
```

**Choices:**

A) undefined, undefined, undefined

B) 1, undefined, ReferenceError

C) 1, ReferenceError, ReferenceError

D) 1, ReferenceError

**Explanation:**

The correct choice is D) 1, ReferenceError

a is declared using var making it accessible within the whole testScope1 function
b is declared using let making it accessible only within the if block.   result ReferenceError because b is not defined in that scope.
 


**QUESTION #3:**
What will be the output of the following code snippet? Pick the right choice then justify your answer with an explanation.
```javascript
function testScope2() {
  console.log(a);
  console.log(b);
  console.log(c);
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
}

testScope2();
```
Choices:

A) undefined, ReferenceError
B) 1, undefined, ReferenceError
C)undefined, undefined, ReferenceError
D) 1, ReferenceError

**Explanation:**
The correct choice is A) undefined, ReferenceError

var declarations are hoisted to the top with an initial value of undefined.
let and const declarations are not hoisted, and they are not accessible before the point they are declared.

**QUESTION #4:**
What will be the output of the following code snippet? Pick the right choice then justify your answer with an explanation.

```javascript
function testScope3() {
  var a = 36;
  let b = 100;
  const c = 45;

  console.log([a, b, c]);

  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log([a, b, c]);
  }

  console.log([a, b, c]);
}

testScope3();
```

**Choices:**

A) [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 36, 2, 3 ]

B) [ 36, 100, 45 ] | [1, 2, 3 ] | [ 36, 100, 45 ]

C) [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 1,100, 45 ]

D) [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 1, 2, 3 ]

**Explanation:**

The correct choice isC) [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 1, 100, 45 ]

First, the code run the initial values of a, b, and c: [36, 100, 45].
Inside the if block, new values for a, b, and c are assigned: [1, 2, 3].
Outside the if block, the value of a changes to 1, but b and c retain their outer values.
The code logs the values of a, b, and c again: [1, 100, 45].


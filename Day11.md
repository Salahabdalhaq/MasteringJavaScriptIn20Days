**Primitive Data Types:**

- Primitive data types include: `undefined`, `string`, `number`, `boolean`, `object`, and `symbol`.

**Undefined vs. Undeclared:**

- Undeclared variables are those that have not been created in any accessible scope.
- Undefined variables exist but have no value assigned at the moment.

```javascript
var v;
typeof v; // Output: "undefined"

v = {};
typeof v; // Output: "object"
```

**NaN and isNaN:**

- `NaN` stands for "not a number" and represents an invalid number.
- `isNaN(value)` returns `true` if the value is `NaN`.

```javascript
var myCatsAge = Number("n/a"); // NaN
myCatsAge - "hiiiii"; // NaN
isNaN("hiiii"); // Output: true
```

**Negative Zero:**

- JavaScript supports a negative zero value.
- Negative zero is equal to regular zero but behaves differently in some cases.

```javascript
var trendRate = -0;
trendRate === -0; // Output: true
trendRate.toString(); // Output: "0"
Object.is(trendRate, -0); // Output: true
Object.is(trendRate, 0); // Output: false
```

**Object.is Exercise:**

```javascript
if (!Object.is || true) {
  Object.is = function objectIS(x, y) {
    var xNegZero = isItNegZero(x);
    var yNegZero = isItNegZero(y);

    if (xNegZero || yNegZero) {
      return xNegZero && yNegZero;
    } else if (isItNaN(x) && isItNaN(y)) {
      return true;
    }

    function isItNegZero(v) {
      return v === 0 && 1 / v === -Infinity;
    }

    function isItNaN(v) {
      return v !== v;
    }
  };
}
```

**Coercion:**

`ToPrimitive(hint)`

- `toString(null)` // "null"
- `toString(undefined)` // "undefined"
- `toString(-0)` // "0"

`toNumber("")` // 0
`toNumber(-0)` // -0
`toNumber(".")` // NaN

`toBoolean()`

**Falsy:** [0, -0, null, NaN, false, undefined]

**Truthy:** Other values are truthy.

**How to access the `.length` of a string value?**

**Boxing:**

```javascript
if (studentNameElem.value.length > 50) {
  console.log("dfds");
}
```

**Question 1:**

Write a function called `convertStringToNumber` that converts a string to a number using the unary plus operator.

If the input is not a string, return an object of the input's value and type.

```javascript
function convertStringToNumber(input) {
   if (typeof input === 'string') {
    return +input;
  }
 else{
    return {
      value: input,
      type: typeof input
    };
  }
}
```

**Question 2:**

Write a function called `checkNaN` that takes a single argument and returns `true` if the argument is `NaN`, and `false` otherwise.

```javascript
const checkNaN = (value) => {
  return Number.isNaN(value);
};

```


**Question 3:**

Write a function called `isEmptyValue` that checks if a given input is an empty value (undefined, null, or empty string).

```javascript
function isEmptyValue(value) { return value === null|| value === undefined || value === '';  }

```

**Question 4:**

Write a function called `compareObjects` that takes 2 arguments of type "object" and compares them. If both arguments are equal, return `true`. If not, return `false`.

If either argument is not of type "object", the function should return an array of the arguments.

```javascript
function compareObjects(input1, input2) {
  if (typeof input1 !== 'object' || typeof input2 !== 'object') {
    return [input1, input2];
  } else {
    return String(input1) === String(input2);
  }
}

```
**Question 5:**

Write a function called `complexCoercion` that takes a single argument and checks if its type is primitive. If the input is primitive, the function returns a coerced value according to the following rules:

**Coercion Rules:**

- If the input is a number, convert it to a string and then return a boolean.
- If the input is a string, return a boolean.
- If the input is `null` or `undefined`, return `false`.
- If the input is not a primitive type, return the argument itself.

```javascript

const complexCoercion = (input) => {
  if (typeof input !== 'object') {
    if (typeof input === 'number') {
      return Boolean(String(input));
    } else if (typeof input === 'string') {
      return Boolean(input);
    } else if (input === null || input === undefined) {
      return false;
    }
 } return input;
};

```


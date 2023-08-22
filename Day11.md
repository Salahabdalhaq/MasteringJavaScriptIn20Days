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


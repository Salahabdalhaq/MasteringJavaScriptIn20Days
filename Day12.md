
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

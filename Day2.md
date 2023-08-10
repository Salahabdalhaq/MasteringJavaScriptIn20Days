# Values & Data Types
**Primitive Data Types:**
1. String
2. Number
3. Boolean
4. Null
5. Undefined

**Object:**
- Document

To define a string in JavaScript, you can use:
- Double quotes: "salah"
- Single quotes: 'salah'
- Backticks: `salah`

For example, "100" is a string.

You can use the `typeof` JavaScript code to determine the type:
- `typeof "100"` returns "string"
- `typeof 100` returns "number"
- `typeof null` returns "object" (Note: This is a historical quirk. Null is a primitive!)

To access characters in a string, you can use indexing. For example, `Salah[0]` returns "S", the first character in "Salah". In JavaScript, string indices start from 0.

To find the index of a character, you can use `"Salah".indexOf("S")`, which returns 0.

You can check if a string contains another string using the `.includes("")` method. To check if a string starts with another string, you can use `.startsWith("")`.

To concatenate strings, you can use the `+` operator, like `"salah " + "abdalahq"`, which results in "Salah Abdalahq".

To convert a string to lowercase, use `.toLowerCase()`. To convert to uppercase, use `.toUpperCase()` for uppercase conversion.

Remember, in JavaScript:
- String indices start at 0.
- `typeof null` returns "object," but null is a primitive.


# Operators 
Certainly, here's the information organized and presented more clearly:

**Operators:**

**Typeof Operator:**
- `typeof` is an operator used to determine the data type of a value.

**Arithmetic Operators:**
- Addition: `+`
- Subtraction: `-`
- Multiplication: `*`
- Division: `/`

**Comparison Operators:**
- Greater than: `>`
- Less than: `<`
- Greater than or equal to: `>=`
- Less than or equal to: `<=`

**Equality Operators:**
- Strict equality: `===`
- Loose equality: `==`
- Strict inequality: `!==`
- Loose inequality: `!=`

**Examples:**
- `1 === 1` is true.
- `1 == 1` is true.
- `"1" === "1"` is true.
- `"1" == "1"` is true.
- `1 === "1"` is false.
- `1 == "1"` is true.

It's recommended to use `===` in most cases because it considers both value and type during comparison.


# Expressions

**Expressions and Variable Declaration/Assignment:**

**Declaring and Assigning Variables:**
- To declare and assign a variable, you can use `let` followed by the variable name.
  - Example: `let remember = "22/3";` assigns the value "22/3" to the variable `remember`.

**Declaring Variables:**
- To declare a variable without assigning a value, you can use `let` followed by the variable name.
  - Example: `let myVariable;` declares a variable named `myVariable` with an initial value of `undefined`.

**Assigning Values to Variables:**
- Assign a value to a variable using the variable name followed by the assignment operator (`=`).
  - Example: `myVariable = "my name is salah";`

**Using `const` for Constants:**
- You can use `const` to declare a variable that cannot be reassigned.
  - Example: `const x = 10;`

**Performing Arithmetic with Variables:**
- Variables can be used in arithmetic expressions.
  - Example: If `x` is 10, then `x - 4` will result in 6.

**Variable Naming Rules:**
- Variable names cannot start with a number.
- Variable names should follow the camelCase naming convention.
  - Example: `myVariableName`

**Variables and Values:**
- Variables do not contain values directly; they point to values in memory.

**Copying Values Between Variables:**
- When you assign one variable's value to another variable, they both refer to the same value in memory.
  - Example: `let y = x;` makes `y` refer to the same value as `x` ("hi ").

**Reassigning Variables:**
- Changing the value of one variable does not affect the value of another variable.
  - Example: `x = "salah";` changes the value of `x` to "salah".

**Expressions and Statements:**

**Expressions:**
- Expressions are code snippets that return a value.
- Example: `3 + 5` is an expression that evaluates to `8`.

**Statements:**
- Statements perform actions and do not return a value directly.
- Example: `if` statements, `for` loops, variable assignments are statements.


### QUESTION #1

Consider the following JavaScript code:

```javascript
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b);
console.log(b === c);
console.log(!!d);
```

What will be the output of each console.log statement? **_You MUST explain WHY_**.
# solv:
- console.log(a == b); // the output  is True because (==) its comparing by value not type 
- console.log(b === c); // the output is False because (===) its comparing by data type  string and  boolean
- console.log(!!d);     // the output is True because (!!) its converte d  to true 


### QUESTION #2:


Consider the following JavaScript expression:

```javascript
console.log(4 + 5 * "7");
```

What will be the output of this expression? **_You MUST explain the steps of evaluation taken by JS_**.
# solv:

- 1- The js do (5 * "7") by converte the string to number type it will be 35 
- 2- the js do (4+ 35) it will be 39 

### QUESTION #3:

Evaluate the following expression:

```javascript
let result = 5 + 2 * 3 - 1;
```

What will be the output of this expression? **_You MUST explain the steps of evaluation taken by JS_**.
# solv:

- 1- the js do  (2 * 3) it will be  6
- 2- the js do  (5 + 6)it will be  11
- 3- the js do  (11 - 1) it will be  10
- So, the final value of the expression 5 + 2 * 3 - 1 is 10



### QUESTION #4:

Consider the following code:

```javascript
let x = 10;
let y = '10';
console.log(x == y);
console.log(x === y);
```
What will be the output of each `console.log` statement? **_You MUST explain WHY_**.
# solv:
- console.log(x == y); // the output is true because (==) compare  value 
- console.log(x === y); // the output  is falus because they have different types


### QUESTION #5:

Given the code below:

```javascript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result);
```

What is the value of result? **_You MUST explain the steps of evaluation taken by JS_**
# solv:


- 1- num > 10 its  true because js convert the string to a number 
- 2- isPositive is already true
- 3- (num > 10 && isPositive) its true
- 4- num < 0 its false
- 5- (num > 10 && isPositive) || num < 0 its  true
- 6- value of result will be true 

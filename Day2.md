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

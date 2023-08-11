
**Conditionals:**

- Code in an `if` block runs only if the condition is true.

```javascript
if (you.reallyBug(me)) {
  me.say("goodbye");
} else {
  me.say("hi");
}
```

- In JavaScript, `0` is considered false, while non-empty strings are considered true.

- To create a function `isEmpty(array)`:

```javascript
function isEmpty(array) {
  if (array.length === 0) {
    console.log("Empty");
  } else {
    console.log("Not Empty");
  }
}
```

**Ternary Operator:**

You can use the ternary operator to create a shorter version of an `if...else` statement.

```javascript
let mood = forecast === "sunny" ? "happy" : "sad";
```

**Loops:**

- `for` loop example:

```javascript
for (let count = 0; count <= 100; count += 10) {
  console.log(count);
}
```

- Iterating through an array using a `for` loop:

```javascript
const numbers = [1, 2, 3];
for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}
```

- Using `for...of` to iterate over characters in a string:

```javascript
for (let char of "salah") {
  console.log(char);
}
```

**Map and Filter:**

- The `map` method calls a function on each item in an array to create a new array.

```javascript
const nicknames = NameOfMainArray.map(variable => variable.elementNeed + "anything");
```

- The `filter` method creates a new array with items that satisfy a true/false function.

```javascript
const mels = NameOfMainArray.filter(variable => variable.elementNeed.includes("mel"));
```

**String Interpolation:**

You can use `${}` inside a string to include JavaScript expressions:

```javascript
`the sum of 1 and 2 is ${1 + 2}`
```

**Spread Operator:**

The spread operator `...` can be used to concatenate arrays into a new array:

```javascript
const cArray = [...aArray, ...bArray];
```

**While Loops:**

- A `while` loop repeatedly executes a block of code as long as the specified condition is true.

```javascript
let fiveRandomNumbers = [];
while (fiveRandomNumbers.length < 5) {
  fiveRandomNumbers.push(Math.random());
}
```

- In this example, the loop will generate and add random numbers to the array until it contains 5 numbers.

**Asynchronous Behavior and `setTimeout`:**

- JavaScript executes code in a single thread, so it can only do one thing at a time.

- The `setTimeout` function allows you to delay the execution of a function.

```javascript
setTimeout(() => console.log("text"), 1000);
```

- In this example, the message "text" will be logged after a delay of 1000 milliseconds (1 second).

- This demonstrates the asynchronous behavior of JavaScript. The code doesn't wait for `setTimeout` to finish; it continues executing other tasks and then executes the callback when the time is up.

**1. Use Multiple Conditional (Ternary) Operators:**
Challenge Link: [Use Multiple Conditional (Ternary) Operators](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators)
```javascript
function checkSign(num) {
return(num>0) ? "positive"
: (num<0) ? "negative"
:"zero"
}

checkSign(10);
```

**2.Use the map Method to Extract Data from an Array:**
Challenge Link: [Use the map Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array)

```javascript

// Only change code below this line
const ratings = watchList.map(movie => {
  return { title: movie["Title"], rating: movie["imdbRating"] };
});
// Only change code above this line

console.log(JSON.stringify(ratings));
```

**3.Use the filter Method to Extract Data from an Array:**
Challenge Link: [Use the filter Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-filter-method-to-extract-data-from-an-array)

```javascript
// Only change code below this line

const filteredList = watchList
  .filter(movie => +(movie.imdbRating) >= 8.0)
  .map(movie => ({ title: movie.Title, rating: (movie.imdbRating) }));

// Only change code above this line

// note : we can use "+" or "parseFloat" to convert string into numbers :DD
```

**4.Golf Code:**
Challenge Link: [Golf Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code)

```javascript
const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

function golfScore(par, strokes) {
 if (strokes === 1) {
    return names[0]; 
  } else if (strokes <= par - 2) {
    return names[1]; 
  } else if (strokes === par - 1) {
    return names[2]; 
  } else if (strokes === par) {
    return names[3]; 
  } else if (strokes === par + 1) {
    return names[4]; 
  } else if (strokes === par + 2) {
    return names[5]; 
  } else {
    return names[6];
  }
}


golfScore(5, 4);
```

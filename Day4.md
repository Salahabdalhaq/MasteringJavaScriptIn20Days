
**Function Basics:**

```javascript
function add(x, y) {  
  return x + y;
}

add(2, 3); 
```

- Parameters should be named like variables and behave like variables within the function body.

- Function names should not start with numbers or contain special characters.

- If a function is called with fewer arguments than it expects, the missing arguments are treated as `undefined`.

- `typeof NaN` returns `"number"`.

- If a function doesn't have a `return` statement, it implicitly returns `undefined`.

- The `=>` (fat arrow) syntax can be used to create unnamed functions.

**Arrow Function Exercises:**

1. Given two numbers, return the result of the first number divided by the second:

```javascript
const divide = (x, y) => x / y;
divide(9, 3);
```

2. Given an uppercase string, log its lowercase version to the console:

```javascript
const test = (a) => console.log(a.toLowerCase());
test("ABC");
```

3. Given two arrays, return whether the first array is shorter than the second:

```javascript
const arr = (a1, a2) => a1.length < a2.length;
```

**setAttribute and Scope:**

- `.setAttribute(name, value)` sets the value of an attribute on a specific element.

- Example:
```javascript
const disable = (button) => {
  button.setAttribute("disabled", "");
};

const enable = (button) => {
  button.removeAttribute("disabled");
};
```

- **Scope**: Determines where variables are accessible.

- Variables declared with `let` are block-scoped and can't be accessed outside the block `{}` they are defined in.

- Variables declared with `var` can be accessed outside the block they are defined in, which can lead to unexpected behavior.

```javascript
let name = "salah";
function fun() {
  let name = "ahmad";
  console.log("insideFun", name);
}
fun(); // Output: "insideFun ahmad"
console.log("outFun", name); // Output: "outFun salah"
```

**Event Listeners:**

You can use event listeners in JavaScript to "listen" for events that occur on the DOM (Document Object Model). When the specified event occurs.

```javascript
document.addEventListener("click", () => {
  console.log("clicked");
});
```

- `document.addEventListener()` attaches an event listener to the document.
- `"click"` is the event type, and the provided function is the event handler.

**Event Object:**

When an event occurs, JavaScript automatically passes an event object to the event handler function. This object contains information about the event and allows you to access details such as the event type, target element, and more.

**Types of Events:**

JavaScript supports various types of events. Some common event types include:
- `"click"`: Fired when an element is clicked.
- `"dblclick"`: Fired when an element is double-clicked.
- `"mouseover"`: Fired when the cursor enters an element.
- `"mouseout"`: Fired when the cursor exits an element.



**1. Global Scope and Functions:**
Challenge Link: [Global Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions)
```javascript
// Declare the myGlobal variable below this line

const myGlobal =10;

function fun1() {
  oopsGlobal=5;
  // Assign 5 to oopsGlobal here

}

// Only change code above this line

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```

**2.Local Scope and Functionsy:**
Challenge Link: [Local Scope and Functions(https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions)

```javascript
function myLocalScope() {
  // Only change code below this line
let myVar;
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);

```

**3.Global vs. Local Scope in Functions:**
Challenge Link: [Global vs. Local Scope in Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions)

```javascript
// Setup
const outerWear = "T-Shirt";

function myOutfit() {
  // Only change code below this line
  const myOutfit="sweater";
  return myOutfit;
  // Only change code above this line
  return outerWear;
}

myOutfit();
```

**4.Stand in Line:**
Challenge Link: [Stand in Line](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/stand-in-line )

```javascript
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item);
  item=arr.shift();
  return item;
  // Only change code above this line
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```



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


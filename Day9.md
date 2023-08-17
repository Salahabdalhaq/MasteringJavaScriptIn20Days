**ES5 Web Browser APIs with Callback Functions:**

- A common problem with callback functions is that response data is only available within the callback, leading to a situation called "callback hell."

- Callback functions have the benefit of being explicit, making it clear how they work under the hood.

**Promises (ES6 Solution):**

- Promises are a solution introduced in ES6 to deal with the issues of callback hell.

- Promises use a two-pronged "facade" approach:
  1. Initiating background web browser work.
  2. Returning a placeholder object (promise) immediately in JavaScript.

**Using Promises:**

```javascript
function display(data) {
  console.log(data);
}

const futureData = fetch('http://...');
futureData.then(display);
console.log("me first");
```

- In this example, `fetch` creates a promise object with a `fulfilled[]` array.

- The promise is stored in `futureData`, and the network request is sent to the web browser.

- The `.then` method is used to join the hidden `fulfilled[]` array.

- When the promise is fulfilled, the `display` function is put in the `fulfilled[]` array.
  

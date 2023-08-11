**Data Fetching and Promises:**

- APIs provide URLs to access data.
- JSON is a common data format used for APIs.
- You can use `fetch()` to load data from APIs:
```javascript
fetch("https://dog.co/api/breed/hound/list");
```

- The `fetch` function returns a promise with three states: pending, fulfilled (got the value), and rejected.
- Promises are asynchronous, meaning they take time to fetch data from the network.

**Using `await` with Promises:**

- `await` is used to tell JavaScript to stop and wait for an asynchronous operation to finish.
- Example:
```javascript
let response = await fetch("https://dog.co/api/breed/hound/list");
let responseBody = await response.json();
```

**Destructuring Data:**

- Destructuring allows you to declare multiple variables at once from objects or arrays.

**Destructuring Objects:**

```javascript
const spices = [
  { name: "salah", nickname: "sa" },
];
let { name, nickname } = spices[0];
// name will be "salah" and nickname will be "sa"
```

**Destructuring Arrays:**

```javascript
let [one, two, three] = [1, 2, 3];
```

**Using the Rest Operator:**

```javascript
let [one, ...other] = [1, 2, 3];
// one will be 1, and other will be [2, 3]
```

**Using `split()` with Destructuring:**

```javascript
let [one, two, three] = "hi salah abdalhaq".split(" ");
// one will be "hi", two will be "salah", and three will be "abdalhaq"
```

**Async Functions:**

- You can't use `await` in regular functions; it's allowed only in `async` functions.

- `async` functions are special functions that allow the use of `await`.

```javascript
async function fetchData() {
  let response = await fetch("https://api.example.com/data");
  let data = await response.json();
  return data;
}
```

**Modules:**

- Modules help split large codebases across multiple files.

- To import and export functions or variables between modules:

Module: `model.js`
```javascript
export function fun() {
  // function code
}
```

Module: `main.js`
```javascript
import { fun } from './model.js';
```

**Debugging:**

- Use `console.log()`, `.warn()`, and `.error()` to understand what's happening when your program runs.

- Browser debuggers provide tools to inspect and debug your code, set breakpoints, and step through execution.

- Use the `debugger;` statement to create a breakpoint in your code, which pauses execution for debugging.

**Error Handling:**

- Use `try {} catch (error) {}` to manage errors when they occur.

```javascript
try {
  // Code that may throw an error
} catch (error) {
  // Code to handle the error
}
```

- Error handling helps prevent unexpected crashes and provides better user experience.
![oic](https://github.com/Salahabdalhaq/MasteringJavaScriptIn20Days/assets/120148077/b341163d-1a19-49b0-a4a3-d05a07a759bc)

![css](https://github.com/Salahabdalhaq/MasteringJavaScriptIn20Days/assets/120148077/db98cf70-7958-4fc5-89a0-ae3107fd820c)

![html](https://github.com/Salahabdalhaq/MasteringJavaScriptIn20Days/assets/120148077/ecc987ed-798b-40bf-b642-0391c87bf7aa)

![js](https://github.com/Salahabdalhaq/MasteringJavaScriptIn20Days/assets/120148077/d447fdff-911e-4e12-906b-019f2e057d39)



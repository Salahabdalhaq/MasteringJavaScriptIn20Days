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


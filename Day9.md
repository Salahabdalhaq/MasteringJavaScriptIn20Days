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

- Many developers have a limited understanding of how promises work under the hood, which can make debugging challenging and lead to difficulties in technical interviews.

- Promises offer benefits such as a cleaner and more readable code style resembling pseudo-synchronous code and improved error handling.

**Execution Rules for Asynchronous Code:**

1. Promises and deferred functions are held in a microtask queue, while callback functions are in a task queue.
2. When a web browser feature (API) finishes, the function from the microtask queue is added to the call stack if it's empty and all global code has run.
3. Functions in the microtask queue are prioritized over those in the callback queue.

**Non-Blocking Application:**

- Promises enable non-blocking applications, allowing code to continue executing regardless of how long a task takes.
- Promises provide an abstraction for handling asynchronous operations.
- Understanding promise execution rules can help manage asynchronous code more effectively.
- The non-blocking nature of promises ensures smoother application behavior, even with long-running tasks.
## Question 1:
'
You are given a function executeInSequenceWithCBs and some code. The task is to modify the executeInSequenceWithCBs function so that it runs and executes all the tasks inside the asyncTasks array.
The function should return an array of messages obtained from each task's execution.
You are only allowed to change the executeInSequenceWithCBs function or add new functions/code. You cannot modify the tasks' functions.
# solve

```javascript
const task1 = (cb) => setTimeout(() => {
  const message = "Task 1 has executed successfully!";
  cb(message);
}, 3000);

const task2 = (cb) => setTimeout(() => {
  const message = "Task 2 has executed successfully!";
  cb(message);
}, 0);

const task3 = (cb) => setTimeout(() => {
  const message = "Task 3 has executed successfully!";
  cb(message);
}, 1000);

const task4 = (cb) => setTimeout(() => {
  const message = "Task 4 has executed successfully!";
  cb(message);
}, 2000);

const task5 = (cb) => setTimeout(() => {
  const message = "Task 5 has executed successfully!";
  cb(message);
}, 4000);

const asyncTasks = [task1, task2, task3, task4, task5];

const executeInSequenceWithCBs = (tasks, callback) => {
  const results = [];
  let currentIndex = 0;

  const executeNextTask = () => {
    if (currentIndex < tasks.length) {
      tasks[currentIndex]((message) => {
        results.push(message);
        currentIndex++;
        executeNextTask();
      });
    } else {
      callback(results);
    }
  };

  executeNextTask();
};

executeInSequenceWithCBs(asyncTasks, (messages) => {
  console.log(messages);
});

```


  

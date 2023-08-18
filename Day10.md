**Using Objects:**

- Objects can be created using literal notation, but this can lead to code repetition.

```javascript
const user1 = {
  name: "will",
  score: 3,
  increment: function() {
    user1.score++;
  }
};
user1.increment(); // Output: user1.score -> 4
```

**Object Creation Patterns:**

- We can create objects using dot notation for each property, but this can be tedious for multiple objects.

```javascript
const user2 = {};
user2.name = "salah";
user2.score = 6;
user2.increment = function() {
  user2.score++;
};
```

- `Object.create(null)` creates an object without any properties.

**Using Functions to Generate Objects:**

- Functions can be used to generate objects and avoid code repetition.

```javascript
function userCreator(name, score) {
  const newUser = {};
  newUser.name = name;
  newUser.score = score;
  newUser.increment = function() {
    newUser.score++;
  };
  return newUser;
}

const user1 = userCreator("salah", 4);
user1.increment(); // Output: 5
```

**Prototype Chain:**

- The prototype chain allows storing shared functions in one object, and the interpreter checks the chain for properties and methods.

**Using `Object.create()`:**

- `Object.create()` links objects together using the prototype chain.

```javascript
const userFunctionStore = {
  increment: function() {
    this.score++;
  },
  login: function() {
    console.log("logged in");
  }
};

function userCreator(name, score) {
  const newUser = Object.create(userFunctionStore);
  newUser.name = name;
  newUser.score = score;
  return newUser;
}

const user1 = userCreator("salah", 4);
user1.increment(); // Output: 5
```

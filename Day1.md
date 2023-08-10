


# Day 1: JavaScript Introduction and DOM 

# JavaScript is a language used to modify websites and make them interactive.
# We write JavaScript in the console of Browser.

```js
 An example of how to print something using the console is by writing the JavaScript code: console.log("we write here")```

  document.body.children;  // Returns an HTML collection (all elements in the body)

// If we need to find an element by ID, we use:
document.getElementById("id");

// Or using document.querySelector():
document.querySelector("#id");

// To get an HTMLCollection of elements with a specific tagName:
document.getElementsByTagName("h1"); 

// Or using document.querySelectorAll():
document.querySelectorAll("h1");

// To get elements with a specific className:
document.getElementsByClassName("className"); // or (" .className")
// This returns all elements with that class name.

// If we need to get the number of elements with a specific class "className":
document.getElementsByClassName("className").length;

// To retrieve the text content of an element with a specific ID:
document.getElementById("id").textContent;
// This will print the content of that element.
// To edit or change the page title, you can use:
document.title = "the title I want";

// To change the text content using an element's ID, you should correct the function name:
document.getElementById("id").textContent = "the new content

// To append new text to the end of the old text, you can use:
document.getElementById("id").append("new text");


```

**1. Compound Assignment With Augmented Multiplication:**
Challenge Link: [Compound Assignment With Augmented Multiplication](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)

```javascript
let a = 5;
let b = 12;
let c = 4.6;

a *= 5;
b *= 3;
c *= 10;
```

**2. Concatenating Strings with the Plus Equals Operator:**
Challenge Link: [Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)

```javascript
let myStr = "This is the first sentence. ";
myStr += "This is the second sentence.";
```

**3. Use Bracket Notation to Find the Nth-to-Last Character in a String:**
Challenge Link: [Use Bracket Notation to Find the Nth-to-Last Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string)

```javascript
const lastName = "Lovelace";
const secondToLastLetterOfLastName = lastName[lastName.length - 2];
```







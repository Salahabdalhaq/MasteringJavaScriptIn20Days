JavaScript is a language used to modify websites and make them interactive.
We write JavaScript in the console.
An example of how to print something using the console is by writing the JavaScript code: console.log("we write here")
_________

document.body.children; // Returns an HTML collection (all elements in the body)

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


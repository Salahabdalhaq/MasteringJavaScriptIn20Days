
1. **Arrays in JavaScript**:
   An array is a data structure that holds an ordered collection of values. Each value is associated with an index, starting from `0`.

   Example:
   ```javascript
   let myFirstArr = ["salah", "abdalhaq"];
   ```

2. **Array Methods**:
   - `.pop()`: Removes and returns the last element of an array.
   - `.push()`: Adds elements to the end of an array.
   - `.sort()`: Sorts the elements of an array. It may not work as expected with numbers due to how sorting works for strings.
   - `.join()`: Joins the elements of an array into a single string using a specified separator.
   - `.concat()`: Combines two or more arrays.

   Example:
   ```javascript
   let myFirstArray = ["salah", "abdalhaq"];
   let last = myFirstArray.pop(); // last contains "abdalhaq"
   myFirstArray.push("abdalhaq"); // myFirstArray becomes ["salah", "abdalhaq"]
   let sortedArray = ["a", "v", "b"].sort(); // sortedArray becomes ["a", "b", "v"]
   let joinedString = ["salah", "ahmad"].join("&"); // joinedString becomes "salah&ahmad"
   let concatenatedArray = [1, 2, 3].concat([4, 5, 6]); // concatenatedArray becomes [1, 2, 3, 4, 5, 6]
   ```

3. **Mutable and Immutable Data**:
   - **Mutable Data**: Arrays are mutable, which means their elements can be modified after creation.
   - **Immutable Data**: Strings are immutable, meaning they cannot be changed after creation.

   Example:
   ```javascript
   let array1 = [1, 2, 3];
   let array2 = array1;
   array1[1] = 4;
   // Now array1 is [1, 4, 3]
   // array2 is also [1, 4, 3] because they reference the same array in memory.


41. **Objects in JavaScript**:

   Example:
   ```javascript
   const js = {
     name: "salah",
     isAvailable: true,
     birthYear: 1998
   };
   ```

5. **Accessing Object Properties**:
   You can access object properties using dot notation or square brackets.

   Example:
   ```javascript
   js.name; // "salah"
   js["isAvailable"]; // true
   ```

6. **Calculations and Modifications**:
   You can perform calculations using object properties,
   Example:
   ```javascript
   let age = 2023 - js.birthYear;
   js.name = "salahAbdalhaq";
   js.salary = "1000$"; // Adding a new property
   ```

7. **Functions in Objects**:
   You can define functions as properties within objects. These are often referred to as methods.

   Example:
   ```javascript
   const dog = {
     name: "doo",
     speak: function() {
       console.log("woof woof", this.name);
     }
   };

   dog.speak(); // Output: "woof woof doo"
   ```

8. **Using `this` Keyword**:
   The `this` keyword refers to the current object and allows you to access its properties from within methods.

9. **Nested Objects**:
   Objects can contain other objects as their properties, creating a hierarchical structure.

   Example:
   ```javascript
   const person = {
     name: "John",
     address: {
       street: "123 Main St",
       city: "Some City"
     }
   };
   ```

# 1 :
# Copy Array Items Using Slice
link :https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice


   function forecast(arr) {
  // Only change code below this line
  return arr.slice(2,4);
}
// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));



# 2 :
# Combine Arrays with the Spread Operator
link :https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator

function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = [ 'learning',...fragment , 'is','fun']; // Change this line
  return sentence;
}

console.log(spreadOut());


# 3 :
# Profile Lookup
link :https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup


function lookUpProfile(name, prop) {
  // Only change code below this line

  for (let i = 0; i < contacts.length; i++) {
    if (name === contacts[i].firstName ) {
      if (contacts[i][prop]) {
        return contacts[i][prop];
      } else {
        return "No such property";
      }
    }
  }
  return "No such contact";

  // Only change code above this line
}

lookUpProfile("Akira", "likes");

# 4 :
# Write Reusable JavaScript with Functions
link :https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/write-reusable-javascript-with-functions

function reusableFunction(){
 console.log("Hi World");
}

reusableFunction();


# 5 :
# Understanding Undefined Value returned from a Function
link :https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understanding-undefined-value-returned-from-a-function

// Setup
let sum = 0;

function addThree() {
  sum = sum + 3;
}

// Only change code below this line
function addFive(){
  sum +=5 ;
}
// Only change code above this line

addThree();
addFive();



# 6 :
# Return a Value from a Function with Return
link :https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return

function timesFive(arg){

arg*=5 ;

return arg;

}








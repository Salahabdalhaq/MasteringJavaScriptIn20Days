
**1. Use Multiple Conditional (Ternary) Operators:**
Challenge Link: [Use Multiple Conditional (Ternary) Operators](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators)
```javascript
function checkSign(num) {
return(num>0) ? "positive"
: (num<0) ? "negative"
:"zero"
}

checkSign(10);
```

**2.Use the map Method to Extract Data from an Array:**
Challenge Link: [Use the map Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array)

```javascript

// Only change code below this line
const ratings = watchList.map(movie => {
  return { title: movie["Title"], rating: movie["imdbRating"] };
});
// Only change code above this line

console.log(JSON.stringify(ratings));
```

**3.Use the filter Method to Extract Data from an Array:**
Challenge Link: [Use the filter Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-filter-method-to-extract-data-from-an-array)

```javascript
// Only change code below this line

const filteredList = watchList
  .filter(movie => +(movie.imdbRating) >= 8.0)
  .map(movie => ({ title: movie.Title, rating: (movie.imdbRating) }));

// Only change code above this line

// note : we can use "+" or "parseFloat" to convert string into numbers :DD
```

**4.Golf Code:**
Challenge Link: [Golf Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code)

```javascript

```

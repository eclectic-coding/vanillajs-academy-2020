# Converting a string into an array

The `split()` method converts a string to an array. It accepts a `delimiter` as a first argument. It also accepts as a second argument, and optional number limit of the array.

```javascript
var petList = 'cat, dog, rat, snake, flea';

var animals = petList.split(', ');
var favoritePets = petList.split(', ', 2);

// logs ["cat", "dog", "rat", "snake", "flea"]
console.log(animals)

// logs ["cat", "dog"] - because the rest are weird
console.log(favoritePets)
```

**Browser Compatibility**

Supported in all modern browsers, and at least back to IE6.

## Filter an array

The `Array.filter()` method creates a new array based on a test condition.

```javascript
// Create a new array with only numbers greater than 10
var newArray = [1, 2, 7, 42, 99, 101].filter(function (item) {
	return item > 10;
});

// logs [42, 99, 101]
console.log(newArray);

```

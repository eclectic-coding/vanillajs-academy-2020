# Getting multiple elements in the DOM

Selecting multiple matching elements on a page cane be accomplished with `document.querySelectorAll()` and will return a Nodelist:

```javascript
// Get all elements with the class .btn-primary
var elemsBtn = document.querySelectorAll('.btn-primary')

````

**Browser Compatibility**

This works in all modern browsers, and IE9 and above. It can also be used in IE8 with CSS2.1 selectors (no CSS3 support).

## Looping over elements

With ES5, a new array feature was added to loop over elements: `Array.forEach()`.
Using this you pass a callback function where the first argument is the current item in the loop and the second is the index:

```javascript
var animals = ['cat', 'dog', 'rat', 'alligator']

// logs 0, cat, 1, dog, 2, rat, 3, alligator
animals.forEach(function (animal, index) {
    console.log(index)
    console.log(animal)
}
)
```

The `Array.forEach()` method only works with arrays, but will not work with NodeLists. There is a `NodeList.forEach()` method, but currently has poor browser support at this time.

To convert NodeLists into Arrays, you can pass them into `Array.prototype.slice.call()`, which will apply the `Array.slice()` method to other array-like objects.

```javascript
var animals = Array.prototype.slice.call(document.querySelectorAll('.animals'));
animals.forEach(function (animal, index) {
	console.log(animal.textContent);
});
````

**Browser Compatibility**

Both the Array.forEach() method and the Array.prototype.slice.call() trick are supported in all modern browsers, and IE9 and above.

##  Project: Toggling multiple password fields
In today’s project, we’re going to take our toggle password script and add the ability to toggle the visibility of multiple fields.

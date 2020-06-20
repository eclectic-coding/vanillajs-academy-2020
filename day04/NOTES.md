# Checking if an element matches a selector

The `matches()` method checks if an element would be selected by a particular selector or set of selectors. It will return a boolean value - `true` or `false`.

```javascript
var elem = document.querySelector('#animals');
if (elem.matches('.cat')) {
	console.log('The element has the .cat class!');
} else {
	console.log('Not a match... =(');
}

```

**Browser Compatibility**
Works in all modern browsers, and IE9 and above.

*However**, as Paul Harvey was famous for saying ...*page 2**.
Several browser have implemented a nonstandard, prefixing, so if `matches()` is used you should use a polyfill for consistent behavior.

## Events on multiple elements

The Vanilla JS `eventListener()` is designed to work with a single specific individual element to listen to.
```javascript
/**
 * This won't work!
 */
var btns = document.querySelectorAll('.click-me');

btns.addEventListener('click', function (event) {
	console.log(event); // The event details
	console.log(event.target); // The clicked element
}, false);
```
The option is to listen to the `window`or `document`:
```javascript
// Listen for clicks on the entire window
window.addEventListener('click', function (event) {

	// If the clicked element has the `.click-me` class, it's a match!
	if (event.target.matches('.click-me')) {
		// Do something...
	}

}, false);
```

## Working with custom attributes
It is possible to get, set, remove, and check for attributes with `getAttributes()`, `setAttributes()`, `removeAttributes()`, and `hasAttributes()`.

```javascript
var elem = document.querySelector('#animals');

// Get the value of an attribute
var sandwich = elem.getAttribute('data-cat');

// Set an attribute value
elem.setAttribute('data-cat', 'alley');

// Remove an attribute
elem.removeAttribute('data-dogs');

// Check if an element has an attribute
if (elem.hasAttribute('data-alligator')) {
	console.log('Add a alligator!');
}

```

**Browser Compatibility**
Supported by all modern browsers, and back to IE6.

## Project: Toggling passwords in multiple forms
Work with the Password toggle script, we have two separate forms that show up on the same page—one to change your username, and another to change your password. Both have password fields in them, and for each form, we again want to include a checkbox that let’s the user toggle password visibility on or off. But, each checkbox should only toggle the fields in its own form.

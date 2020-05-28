# Getting an Element in the DOM

Use `document.querySelector()` to get the first matching element in the DOM:

First div: `var elem = document.querySelector('div')`

First div with class `cat`: `var elem = document.querySelector('.cat')`

You can also target `data-attributes`:
`var elem = document.querySelector('[data-food="meat"]')`


**Browser Compatibility**

IE9 and above.
IE8 if you use CSS2.1 selectors.

# Listening for Events

Use `addEventListener` to listen for interaction events with an element. A complete list of events are found at [MDN](https://developer.mozilla.org/en-US/docs/Web/Events).

```javascript
// Target an element
var btn = document.querySelector('#nav-toggle');

// Set eventListener
btn.addEventListener('click', function (event) {
	console.log(event); // The event details
	console.log(event.target); // The clicked element
}, false);

```

**Browser Compatibility**

IE9 and above.

# Toggle Password Visibility

For your first project, you’re going to write a script that let’s users toggle the visibility of a password field.




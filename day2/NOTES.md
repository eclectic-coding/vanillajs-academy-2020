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

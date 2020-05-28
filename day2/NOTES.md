# Common Issue Variable Location

It is possible to position variables inside the eventLister:

```javascript
// Check the toggle checkbox
var toggle = document.querySelector('#show-password');

// Listen for click events on the toggle
toggle.addEventListener('click', function (event) {

	// Get the password field
	var password = document.querySelector('#password');
	
	// Do stuff code

}, false);

````

However, it is more performant to define variables outside the eventListener.

```javascript
// Check the toggle checkbox
var toggle = document.querySelector('#show-password');
var password = document.querySelector('#password');

// Listen for click events on the toggle
toggle.addEventListener('click', function (event) {
	// Do stuff code

}, false);

````

# Common Issue: Using the field to determine visibilty

It is possible to check the status of the checkbox. However, it is possible for the checkbox and password field to get out of sync.

# Common Issue: Ready Event

If this problem is approach from JQuery experience, you can use `load` to load the script before needing the code.

```javascript
document.addEventListener('load', function () {

	// Get the password field and toggle checkbox
	var password = document.querySelector('#password');
	var toggle = document.querySelector('#show-password');

	// Listen for click events on the toggle
	toggle.addEventListener('click', function (event) {

	  
	//	...do stuff

	}, false);

}, false);

```
However, it is more performant to use a `click` event in the script section of the document.

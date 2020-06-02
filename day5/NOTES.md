# Common Issue: NodeLists and forEach()

Newer versions of modern browsers provide a NodeList.forEach() method.

```javascript
// Get the password field and toggle checkbox
var passwords = document.querySelectorAll('[type="password"]');
var toggle = document.querySelector('#show-passwords');

// Listen for click events on the toggle
toggle.addEventListener('click', function (event) {

	// Loop through each password field
	passwords.forEach(function (password) {

		// do stuff
		
	});

}, false);
```
This feature is inconsistent. A better approach is to either convert the NodeList returned by `querySelectorAll()` into an array, or [adding a polyfill](https://vanillajstoolkit.com/polyfills/nodelistforeach) for it.

## Common Issue: Targeting Individual Fields

It is possible to target each field separately, but this approach is not very DRY

```javascript
// Get the password field and toggle checkbox
var toggle = document.querySelector('#show-passwords');
var currentPW = document.querySelector('#current-password');
var newPW = document.querySelector('#new-password');

// Listen for click events on the toggle
toggle.addEventListener('click', function (event) {

	// If the toggle is checked, change the type to "text"
	// Otherwise, change it back to "password"
	if (toggle.checked) {
		currentPW.type = 'text';
		newPW.type = 'text';
	} else {
		currentPW.type = 'password';
		newPW.type = 'password';
	}

}, false);

```

# Adding text to an element

The `textContent` property can be used to get and set text content for an element. It ignores any markup inside the element.

```javascript
var elem = document.querySelector('#some-elem');

// Get text content
var text = elem.textContent;

// Set text content
elem.textContent = 'We can dynamically change the content.';

// Add text to the end of an element's existing content
elem.textContent += ' Add this after what is already there.';

// Add text to the beginning of an element's existing content
elem.textContent = 'We can add this to the beginning. ' + elem.textContent;
```

**Browser Compatibility**

Works in all modern browsers, and IE9 and above.

## Project: Character Count
This project, we’re going to update the UI to display a live character count as a user types in a textarea field.



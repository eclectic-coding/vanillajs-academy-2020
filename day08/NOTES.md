# Common Issue: Picking the right event

The struggle of some approaches to the Project is picking the right event. For instance, other events work, like `keydown`, but it does not take into account copy and pasting content. To use `keydown` additional event `paste` will have to be used to do the same as `input`.

## Common Issue:

Be careful not to set redundant variables. For instance it might be tempting to create a `length` variable in the callback function:

```javascript
// Get the number of characters in the text area
var length = text.value.length;

// Display the characters count
charCount.textContent = length;
```

In this case, it works, but the original solution does not use extra variables and is cleaner.

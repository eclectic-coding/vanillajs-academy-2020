# Common Issue: Keeping Code DRY

The struggle of some approaches to the Project to toggle multiple password fields, is to keep the code DRY (*Don't Repeat Yourself*).

For instance, one approach would be:
```javascript
// Get checkboxes
var showPW = document.querySelector('#show-password');
var showPWs = document.querySelector('#show-passwords');
```

Then loop through all the fields with `querySelectorAll()`. Tis will lead to a lot of code duplication, and code that is hard to maintain.

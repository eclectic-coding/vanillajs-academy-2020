# Getting an Element in the DOM

Use `document.querySelector()` to get the first matching element in the DOM:

First div: `var elem = document.querySelector('div')`

First div with class `cat`: `var elem = document.querySelector('.cat')`

You can also target `data-attributes`:
`var elem = document.querySelector('[data-food="meat"]')`


**Browser Compatibility**

IE9 and above.
IE8 if you use CSS2.1 selectors.

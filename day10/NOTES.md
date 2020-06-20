# Common Issue: Catching Line Breaks

The original code does not take into consideration a line break:
```javascript
const words = text.value.split(' ')
```

The solution us to use regex:
```javascript
const words = text.value.split(/[\n\r\s]+/g);
```

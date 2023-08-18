# Day4 Summary

## How to Write functions in JS
-  A Function as a Statement
- A function as an expression
- A function as an arrow function


## Scopes 
- Global Scope: In the global scope, the variable can be accessed from any part of the JavaScript code.

- Local Scope: In the local scope, the variable can be accessed within a function where it is declared.

## var VS let 
- Variables declared by **let** are only available inside the block where they’re defined.

- Variables declared by **var** are available throughout the function in which they’re declared.

## Event Listner 
We use **addEventListener()** method  to add event listeners on any HTML object, it takes two parameters, the first is the event object and the seconed is the fnction we want it to happen.

## Event Object
there are many events in Js, Examples:
-  select
- click
- change
- open
 these objects are used inside the eventListner method.



## Day4 Challenges 
#### QUESTION #1:
```javascript

let myGlopal = 10;
function fun1() {
  // Assign 5 to oopsGlobal here
  oopsGlobal = 5;
}

```
#### 	QUESTION #2:
```javascript
function myLocalScope() {
  // Only change code below this line
  let myVar
  console.log('inside myLocalScope', myVar);
}
myLocalScope();
```
#### 	QUESTION #3:
```javascript
function myOutfit() {
  // Only change code below this line
  let outerWear = "sweater"
  // Only change code above this line
  return outerWear;
}

```

#### 	QUESTION #4:
```javascript
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item)
  item = arr.shift()
  return item;
  // Only change code above this line
}
```


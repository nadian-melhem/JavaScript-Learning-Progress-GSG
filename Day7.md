# Day7 Summary

## JavaScript principles
- Functions: Code we save (‘define’) functions & can use (call/invoke/execute/run) later with the function's name & ( )

- Execution context: Created to run the code of a function - has 2 parts
   - Thread of execution
   - Memory

- Call stack:  JavaScript keeps track of what function is currently running 

## Generalizing functions
functions use Parameters’ (placeholders)  which means we don't need to decide what data to run our functionality on until we run the function. Then provide an actual value (‘argument’) when we run the function

## Pair Programming
Pair programming is a software development technique in which two programmers work together at one workstation. One, writes code while the other reviews each line of code as it is typed in

## Higher-order functions
Takes in a function or passes out a function Just a term to describe these functions - any function that does it we call that - but there's nothing different about them inherently


# Day7 Summary

## JavaScript principles
- Functions: Code we save (‘define’) functions & can use (call/invoke/execute/run) later with the function's name & ( )

- Execution context: Created to run the code of a function - has 2 parts
   - Thread of execution
   - Memory

- Call stack:  JavaScript keeps track of what function is currently running 

## Generalizing functions
functions use Parameters’ (placeholders)  which means we don't need to decide what data to run our functionality on until we run the function. Then provide an actual value (‘argument’) when we run the function

## Pair Programming
Pair programming is a software development technique in which two programmers work together at one workstation. One, writes code while the other reviews each line of code as it is typed in

## Higher-order functions
Takes in a function or passes out a function Just a term to describe these functions - any function that does it we call that - but there's nothing different about them inherently


# Day7 Summary

## JavaScript principles
- Functions: Code we save (‘define’) functions & can use (call/invoke/execute/run) later with the function's name & ( )

- Execution context: Created to run the code of a function - has 2 parts
   - Thread of execution
   - Memory

- Call stack:  JavaScript keeps track of what function is currently running 

## Generalizing functions
functions use Parameters’ (placeholders)  which means we don't need to decide what data to run our functionality on until we run the function. Then provide an actual value (‘argument’) when we run the function

## Pair Programming
Pair programming is a software development technique in which two programmers work together at one workstation. One, writes code while the other reviews each line of code as it is typed in

## Higher-order functions
Takes in a function or passes out a function Just a term to describe these functions - any function that does it we call that - but there's nothing different about them inherently


## Day7 Challenge
#### QUESTION #1:
```javascript
const squareList = arr => {
 return arr
 .filter(num => num>0 && num % parseInt(num) === 0)
 .map(num => num * num)
};

```
#### QUESTION #2:
```javascript
function urlSlug(title) {
return title
.toLowerCase()
.trim()
.split(/\s+/)
.join("-");
}
```
#### Question #3:
```javascript
async function convertToPromise(value){
  return new Promise((resolve) => {
    return resolve(callback(value));
  })
}

function mapAsync (arr, callback){
  return arr.map((value) => {
    return convertToPromise(value);
  })
}
```

#### Question #4:
```javascript
function sumRange(start, end) {
  let sum = start;
    if (start === end)
      return sum;
    return calculate(++start,end) + sum;
}
```

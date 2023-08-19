# Day8 Summary

## Clousre
A closure is a feature of JavaScript that allows inner functions to access the outer scope of a function. Closure helps in binding a function to its outer boundary and is created automatically whenever a function is created.

## Bond
When a function is defined, it gets a bond to the surrounding Local Memory ("Variable Environment") in which it has been defined

## BackPack
Backpack is the global namespace everything gets attached too, so you have a global dispatcher/observer.

## Higher-order functions
Takes in a function or passes out a function Just a term to describe these functions - any function that does it we call that - but there's nothing different about them inherently

## Asynchronicity in JS 
Asynchronicity means that if JavaScript has to wait for an operation to complete, it will execute the rest of the code while waiting.

## Asynchronous Operations and Web APIs
The Web APIs are a set of functions provided by the browser that the JavaScript engine can utilize. which are:
- fetch
- setInterval
- setTimeout
- promises

## Day8 Challenge
#### QUESTION #1:
```javascript
function createCounter (start){
    const counter = start;
    function increment() {
        counter++;
        return counter;
    }
    return increment;
}
```
#### QUESTION #2:
```javascript
function calculateAverage(nums) {
    function calculateAvg() {
        const sum = nums.reduce(
            (sum, num) => {
                return sum + num;
            }, 0)
        avg = sum / nums.length;
        return avg;
    }
    return calculateAvg
}
```
#### QUESTION #3:
```javascript
function powerOf(base) {
    function calculate(exp) {
        return Math.pow(base, exp);
    }
    return calculate;
}


```

#### QUESTION #4:
```javascript
function compose(functions) {

    function reverse(firstFunc) {
        return functions.reduceRight((parameter, func) =>{ 
            const newParameter = func(parameter);
            return newParameter

        }, firstFunc)

    }
    return reverse;

}
```

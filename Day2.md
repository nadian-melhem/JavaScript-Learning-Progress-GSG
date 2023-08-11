# Day2 Summary

## Data Types :smile:
- Strings
- Numbers
- Objects

## String Methods
-  indexOf()
- toLowerCase()
- toUpperCase()
- includes()


## Operators
there are different operators in JavaScript here are some of them:
-  ==
- ===
- != 
- !== 
- mathmatic operations

## Constant and Variables
we use **let** to define a variable in JS and **const** to define a constant value that can't be changed. 


## Day2 Challenges 
#### QUESTION #1
Consider the following JavaScript code:
```javascript
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b);
console.log(b === c);
console.log(!!d);
```
What will be the output of each console.log statement? You MUST explain WHY.

####Answer
    console.log(a == b);     true, == compares valuse without types
    console.log(b === c);   false, === compares valuse and types
    console.log(!!d);   true, d is a string not boolean
	
#### 	QUESTION #2:
   Consider the following JavaScript expression:
   ```javascript
console.log(4 + 5 * "7");
```
What will be the output of this expression? You MUST explain the steps of evaluation taken by JS.

#### Answer
    5*7 = 35 
    4+5 = 39 
	
#### 	QUESTION #3
Evaluate the following expression:
```javascript
let result = 5 + 2 * 3 - 1;
```
What will be the output of this expression? You MUST explain the steps of evaluation taken by JS.

#### Answer
    2*3 = 6
    5+6-1 = 10
	
#### QUESTION #4:
Consider the following code:
```javascript
let x = 10;
let y = '10';
console.log(x == y);
console.log(x === y);
```
What will be the output of each console.log statement? You MUST explain WHY.


#### Answer
    true, because == compares values
    false, because === compares valuse and types
	
#### 	QUESTION #5:
Given the code below:
```javascript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result);
```
What is the value of result? You MUST explain the steps of evaluation taken by JS.

#### Answer
```javascript
15>10 ? true
true && true ? true
num < 0 ? false
true || false ? true
```






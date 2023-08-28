# Day12 Summary

## Equality:
- loosly eqaulity: perform a type conversion when comparing two things.
- strict equality: do the same comparison as double equals (including the special handling for NaN, -0, and +0) but without type conversion.

## Static Typing:



## Day12 Challenge
#### QUESTION #1:

#### QUESTION #2:
```javascript
function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();

```
    var can be seen at the whole scope of the function, but let and const can't be.
    so the compiler will read the value of , but can't see b&c
    so will return 1, and refrenceerror when reach to b.

#### QUESTION #3:
```javascript
function testScope2() {
  console.log(a);
  console.log(b);
  console.log(c);
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
}

testScope2();

```
        var a can be seen at the whole scope of the function, but let and const can't be.
        so the compiler will see that we have a declared witout having a value yet , but can't see b&c
        so will return undefined, and refrenceerror when reach to b..
     

#### QUSTION #4:

```javascript
function testScope3() {
  var a = 36;
  let b = 100;
  const c = 45;

  console.log([a, b, c]);

  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;

    console.log([a, b, c]);
  }

  console.log([a, b, c]);
}

testScope3();

```
    The answer is 
    C) [ 36, 100, 45 ] | [ 1, 2, 3 ] | [ 1,100, 45 ]
    for the first part it will take the first values ut see 
    for the seconedpart it will take the values from the scope we are in 
    for the third part it will take the values from the scope that the values can seen from, but for var ibecause it is functionally scoped will take the updated value.


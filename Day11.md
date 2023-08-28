# Day11 Summary

## Types in JS
1. String
2. Number
3. Bigint
4. Boolean
5. Undefined
6. Null
7. Symbol
8. Object

## NaN & isNaN
- Nan: Not a Number.
- isNaN():  method returns true if a value is Not-a-Number.

## Coercion
The process of automatic or implicit conversion of values from one data type to another.In case the behavior of the implicit conversion is not sure, the constructors of a data type can be used to convert any value to that datatype, like the Number(), String() or Boolean() constructor.

## Boxing
Boxing is the process in which a primitive value is wrapped in an Object.

## Day11 Challenge
#### QUESTION #1:
```javascript
function convertStringToNumber(input) {
  if(typeof input === 'string')
      return (+input);
    return {value: input, type: typeof input};
}
```
#### QUESTION #2:
```javascript
const checkNaN = (value) => {
return isNaN(value);
}
```
#### QUESTION #3:
```javascript
function isEmptyValue(value) {
    if(value === 0) return false;
 return !value;
}
```
#### QUSTION #4:
```javascript
function compareObjects(input1, input2) {
  if (typeof input1 == 'object' && typeof input2 == 'object')
      return JSON.stringify(input1) === JSON.stringify(input2);
  return[input1,input2];
}
```
#### QUESTION #5:
```javascript
const complexCoercion = (input) => {
  if( typeof input !='function' && typeof input != 'object'){
      if( typeof input == 'number')
          return ( !! input.toString());
      if(typeof input =='string')
          return(!!input);
      if( input != 0 && !input)
          return false;
  }
 return input;
}
```

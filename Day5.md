# Day5 Summary

## if statement
conditional statements like in any other programming language.

## Conditional ternary operator
it is a "shortcut" operator for writing quick conditionals
it needs 3 values to work:
```javascript
condition ? valueIfTrue : valueIfFalse;
```

## Loops in J
to loop through number of iterations, it's implimented like any other programming language.


## Map 
map calls a function on each item in an array to create a new array.
example: 
```javascript
const nicknames = spices.map(s => s.nickname + " Spice");
```

## Filter 
filter calls a true/false function on each item and creates a new array with only the items where the function returns true.
example:
```javascript
const mels = spices.filter(s => s.name.includes("Mel"));
```
## Spread 
It lets us take all the items in an array and spread them around.
example:
```javascript
const oldBurns = ["square", "wack"];
const newBurns = ["basic", "dusty", "sus"];
const burnBook = [...oldBurns, ...newBurns];
```

## Day5 Challenges 
#### QUESTION #1:
```javascript
function checkSign(num) {
  return (num === 0) ? "zero"
  : (num > 0) ? "positive"
  : "negative";
}

checkSign(10);
```
#### 	QUESTION #2:
```javascript
const ratings = watchList.map(object => ({
  title: object["Title"],
  rating: object["imdbRating"]
}));
```
#### 	QUESTION #3:
```javascript
const filteredList = watchList
.filter(item => item.imdbRating  >= 8.0)
.map(item => ({
  title: item["Title"],
  rating: item["imdbRating"]
}));
```

#### 	QUESTION #4:
```javascript
function golfScore(par, strokes) {
  // Only change code below this line
return strokes === 1
    ? names[0]
    : strokes <= par - 2
    ? names[1]
    : strokes === par - 1
    ? names[2]
    : strokes === par
    ? names[3]
    : strokes === par + 1
    ? names[4]
    : strokes === par + 2
    ? names[5]
    : names[6];
  // Only change code above this line
}

```



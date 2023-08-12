# Day3 Summary

## Usefull Array Methods
- push()
- pop()
- concat() 
- indexOf()


## Difference between Mutable and Immutable Data
Mutability refers to data types that can be accessed and changed after they've been created and stored in memory. Immutability, on the other hand, refers to data types that you can't change after creating them – but that you can still access in the memory.


## Objects
A JavaScript object is a collection of named values.
Object values are written as name : value pairs


## Built-in Objects
there are built-in objects in JS, here are examples on it:
- undefined
- infinity

## Day3 Challenges 
#### QUESTION #1
```javascript
function forecast(arr) {
  // Only change code below this line
  let index = arr.indexOf('warm') 
  return arr.slice(index,index+2);
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

#### 	QUESTION #2:
```javascript
function spreadOut() {
  let fragment = ['to', 'code'];
  let start = ['learning'];
  fragment = start.concat(fragment);
  let sentence = fragment.concat(['is', 'fun']); // Change this line
  return sentence;
}

console.log(spreadOut());
```
#### 	QUESTION #3
```javascript
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];


function lookUpProfile(name, prop) {
  let output;
  for (let a = 0; a < contacts.length; a++) {
    if (contacts[a].firstName === name) {
      if (contacts[a].hasOwnProperty(prop))
        return contacts[a][prop]
      else
        return "No such property";
    }
  }
  return "No such contact";
}

lookUpProfile("Akira", "likes");
```





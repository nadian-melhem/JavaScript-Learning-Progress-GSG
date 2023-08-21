# Day9 Summary

## Web API Rules
- Hold promise-deferred functions in a microtask queue
- Hold callback function in a task queue when the Web Browser Feature (API) finishes
- Add the function to the Call stack when Call stack is empty & all global code run
- Prioritize functions in the microtask queue over the Callback queue

## Callback Queue
A software mechanism that stores callback functions to be run after the Web APIs have processed asynchronous functions.

## Microtask Queue
It is like the Callback Queue, but Microtask Queue has higher priority. All the callback functions coming through Promises will go inside the Microtask Queue.

## Event Loops
A loop that continuously checks if the call stack is empty. When the call stack is not empty, it allows the ongoing process to continue. But when the call stack becomes empty, the event loop fetches the task at the top of the callback queue and adds it to the call stack.

## Promises
A Promise is a proxy for a value not necessarily known when the promise is created

## Then Method
The then() method schedules callback functions for the eventual completion of a Promise — either fulfillment or rejection. It is the primitive method of promises



## Day9 Challenges

### QUESTION #1:
```javascript
function convertToPromise(callback) {
    return new Promise(resolve => callback(resolve));

}

const executeInSequenceWithCBs = (tasks, callback) => {
    let promises = [];
    for (let i = 0; i < tasks.length; i++) {
        promises.push(convertToPromise(tasks[i]));
    }
   return Promise.all(promises).then((values) => {
        values.map(task => callback(task))
    })
}

```
### QUESTION #2:
```javascript
async function fetchApi(api) {
  const response = await fetch(api.apiUrl);
  return response.json();
}

const executeInParallelWithPromises = (apis) => {
  const promises = apis.map(fetchApi);
  return Promise.all(promises).then((responses) => {
    return responses.map((response, index) => {
      return {
        ...apis[index],
        apiData: response,
      };
    });
  });
};
```
### QUESTION #3:
```javascript
const apis = [
  {
    apiName: "products", 
    apiUrl: "https://dummyjson.com/products",
  }, 
  {
    apiName: "users", 
    apiUrl: "https://dummyjson.com/users",
  }, 
  {
    apiName: "posts", 
    apiUrl: "https://dummyjson.com/posts",
  }, 
  {
    apiName: "comments", 
    apiUrl: "https://dummyjson.com/comments",
  }
]
async function fetchApi(api) {
  const response = await fetch(api.apiUrl);
  return response.json();
}
const executeInSequenceWithPromises = (apis) => {
  const promises = apis.map(api => fetchApi(api));
  let responses = [];
  for (let i = 0; i < promises.length; i++) {
    Promise.resolve(promises[i]).then((response) => {
      return responses.push({...apis[i], apiData : response});
    })
  }
  return responses;

}

```



## 💾 Requirements

* `Web Browser` - Can be used as an emulator to build applications. Example [Chrome, Firefox, Safari & Opera].
* `Internet` - Because many use CDN and to make it easier to find solutions to all problems.

## 🎯 How To Use

#### Example Syntax

```javascript
const { promiseAll, promiseRace, promiseTimeout } = require('promise-utilities');

const promises = [Promise.resolve(1), Promise.resolve(2), Promise.resolve(3)];

// Example of using promiseAll
promiseAll(promises).then(result => {
    console.log('All promises resolved:', result);
});

// Example of using promiseRace
promiseRace(promises).then(result => {
    console.log('First resolved promise:', result);
});

// Example of using promiseTimeout
const timeout = 1000;
promiseTimeout(timeout).then(() => {
    console.log('Timeout reached after', timeout, 'milliseconds');
});
```

#### Explanation

* `promiseAll(promises)`: Resolves all promises in the given array and returns a new promise that resolves with an array of results.
* `promiseRace(promises)`: Resolves the promise that resolves first in the given array and returns a new promise.
* `promiseTimeout(ms)`: Creates a promise that resolves after the specified time (in milliseconds).

#### Return Value

* `promiseAll`: Returns a promise that resolves with an array containing the results of all input promises.
* `promiseRace`: Returns a promise that resolves with the value of the first input promise to resolve.
* `promiseTimeout`: Returns a promise that resolves after the specified timeout.

# Promises
- Promises are ES6 new way of handling asynchronous work (that take time)
- In old days we used to do it with callbacks
- You can either `make` a promise or `consume` a promise (most probably you will be consuming promises)
- In a promise there are 3 states
  – Pending
  - Resolved (Fulfilled)
  - Rejected
- Making a Promise
  ```js
    const myPromise = new Promise (
        function (resolve, reject) {
            if (something) {
                resolve(resolveParams)
            } else {
                reject(rejectParams)
            }
        }
    )
  ```
- Consuming a Promise
  ```js
    myPromise.then( function (success) {
        console.log(success) // success Param
    }).catch(function (failure) {
        console.log(failure) // failure Parma
    })
  ```
  - Check the following example [here](https://www.digitalocean.com/community/tutorials/javascript-promises-for-dummies)
 
- `Promise.all()` resolves after all the promises are resolved. if one is failed the result is a failed promise
 ```js
 const p1 = new Promise (resolve => resolve(1))
 const p2 = new Promise (resolve => resolve(2))
 const p3 = new Promise (resolve => resolve(3))

 Promise.all([p1,p2,p3]).then((success) => {
     console.log(success) // [1,2,3]
 })
 
 ```
- `Promise.race()` takes an array of promises and return the first promise that brings a result whether it's successful or not 
    ```js
    const p1 = new Promise((resolve) => {
      setTimeout(() => {
        resolve("p1");
      }, 1000);
    });
    const p2 = new Promise((resolve, reject) => {
      setTimeout(() => {
        reject("p2");
      }, 2000);
    });
    Promise.race([p1, p2])
      .then((res) => {
        console.log(res, "suc");
      })
      .catch((err) => {
        console.log(err, "failed");
    });
    ```
- You can chain promises as long as a `promise` is returned
  ```js
    const p = new Promise((resolve) => {
      setTimeout(() => {
        resolve("Parent");
      }, 1000);
    });

    p.then((resp) => {
      const test = resp;
      return new Promise(function (resolve) {
        resolve(test + " form other promise");
      });
    }).then((resp) => {
      console.log(resp + "chaining is 🔥");
    });
  ```
- if the promise failed in anytime, the error will appear in the first catch statment
- Example of using promises is when handling Ajax requests;
  ```js
    fetch("https://randomuser.me/api")
    .then((res) => res.json())
    .then(({ results, info }) => {
      console.log(results);
    });
  ```
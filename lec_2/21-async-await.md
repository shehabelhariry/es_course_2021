# Async - Await

- New keywords proposed by ES8 to do some asynchronous work 
- The word `async` before a function means one simple thing: a function always returns a promise. Even If a function actually returns a non-promise value

```js
 async function f () {
     return 1
 }

 f().then( i => console.log(i)) // 1
```
- The keyword `await` makes JavaScript wait until that promise settles and returns its result.
- It can only be used inside an async function.
  ```js
    async function func () {
      let promise = new Promise ((resolve) => {
          setTimeout(() => resolve('done!'), 1000)
      })
      let result = await promise;
      alert(result)
    }

    func()
    

  ```
- You can combine it with the arrow notation to implement really neat logic.
 
```js
const getUsers = async () => {
    const response = await fetch('https://randomuser.me/api')
    const users = response.json();
    console.log(users)
}

getUsers()
```
- Bonus:  Error handling in promises and async await.

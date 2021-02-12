## Default Params

- ES6 make it possible to assign default params to functions to get  a value instead of undefined

```js
 function greet (greeting = 'hello') {
     return greeting
 }
 greet() // hello
```
- Default params must come at the end of the param list
  ```js
  function multiply(a,b,c = 3) {
      return a * b * c
  }
  multiply(1,2) // 6

  function multiply2(x = 2 ,y ,z) {
      return x * y * z
  }
  multiply2(5, 4) // 5 * 6 * undefined = NaN
  ```
- Default pramas are availbl for later default params
  ```js
  function complain (name = 'ahmed', complain_body = `I hate ${name}`){
      console.log(complain_body)
  }
  complain('Ramy')
  ```
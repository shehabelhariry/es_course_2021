## Arrow Functions

- ES6 Introduced a new kind of function called the arrow function
- It can replace other ES5 functions by doing some steps and changing the syntax a bit
  ```js
    const getName = () => 'name'
  ```
- There are 2 types of functions in JavaScript
  - Declaration functions
  ```js
    function sayHello () {
        console.log('hello')
    }
  ```
  - Expression  function
  ```js
    const sayHello = function () {
        console.log('hello')
    }
  ```
- Arrow functions can only be used as an expression and cannot be used as a declaration
- Arrow functions can be stored in variables 
- Arrow functions can be used as callback functions
- The steps you need to convert a function to an arrow function
  - remove the function  keyword
  - remove the return keyword
  - remove the semicolon
  - add and arrow => between the parameter list and the function body
- if a function takes one parameter we can remove the brackets
  ```js

    const myFunc = name => {
        return name
    }

  ```
- If the body of the function is only `one` statement, we can remove the curly braces {} and in that case we don't need the `return` keyword
  ```js
  const myFunc = () => 'my name is Shehab'
  const es5Square = function (num) {
      return num * num
  }

  //Tada🎉🎉
  const es6Square = num => num * num
  
  ```
  
- the main difference between arrow functions and old es5 functions  is how it deals with the `this` keyword
  ```js
      const obj = {
        param1: 'ali',
        displayName: function () {
          setTimeout(  () => {
            console.log(this.param1, 'from inside the timeout')
          }, 1000)
          console.log(this)
        }
      }
  ```
- How does `this` behave in JS? 
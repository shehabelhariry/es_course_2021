## Spread Operator

- The spread operator written with three consecutive dots (...)
- It gives you the ability to expand, or spread `iterables` into multiple elements
  ```js
    const arr = [1,2,3,4];
    console.log(...arr) // 1,3,4,5
  ```
- It can be used for merging 2 arrays into one
  ```js
    const arr1 = [1,2,3]
    const arr2 = [4,5,6]
    const newArr = [...arr1, ...arr2] 
  ```
- it can be used in function params
  ```js
    const arr = [1,2,3]
    function sum (a,b,c) {
        return a + b + c
    }

    sum(...arr) // 6
  ```
- I can do the same operation for objects
    ```js

    const obj1 = {
        name: 'Shehab',
        age: 29
    }

    const obj2 = {
        hobbies: ['reading', 'wrting']
    }

    const person = {...obj1, ...obj2}
    ```

- One thing to note that the properties are overwritten
  ```js
      const obj1 = {
          param1: 'param1 obj 1'
      }
      const obj2 = {
          param1: 'param1 obj 2'
      }

      const result = {...obj1, ...obj2} // param 1 from obj ?
  ```
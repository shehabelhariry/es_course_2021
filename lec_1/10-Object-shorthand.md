## Object Shorthand Creation
- this works if the name of the param and the name of the new variable are the same
  ```js
  function getPersonalInfo (fname, lname) {
      const fullname = `Mr. ${fname} ${lname}`
      return {fname, lname, fullname}
  }
  ```

## New method short hand
- This obj:
  ```js
   const myObj = {
       param: 10,
       getParam: function () {
           return this.param
       }
   }  
  ```
- is the same as this
  ```js
  const myObj = {
      param: 10,
      getParam () {
         return this.param
      }   
  }
  ```
## Trailing Comma

- We have also added the ability to add a trailing comma without errors
  ```js
   // this is valid
   const validObj = {
       param1: 1,
       param2: 2, // ⬅️ There is an extra comma here
   }
  ``` 

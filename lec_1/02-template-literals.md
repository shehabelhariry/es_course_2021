# Template Literals

- If we had an array of names: 
  ```js
    const names = ['Ahmed', 'Shehab', 'Ramy']
  ```
  and we wanted the output to be like this:

  `Ahmed said: "I want to go on a trip with 'Shehab' and 'Ramy'"`

- In ES5 you would have to write something like this: 

   ```js
   const names = ['Ahmed', 'Shehab', 'Ramy']
   
   const phrase = names[0] + ' said: "' + "I want to go on a trip with '"+ names[1] + "' and '" + names[2] + "'\""   
   ```
- They are strings that include in them some variables you want to embed
- They are written between backquotes `` and not '' or ""
- The expression you want to write will be written inside `${someVariable}`
- This is an awesome alternative to extensive concatenation with a lot of single and double quotes

  ## Example 1

    ```js
      const names = ['Ahmed', 'Shehab', 'Ramy']

      const phrase = `${names[0]} said: "I want to go on a trip with '${names[1]}' and '${names[2]}'"`
    ```
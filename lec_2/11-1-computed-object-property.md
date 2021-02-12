## Computed Properties
- If we want to use variables as key names in an object, ES6 has provided us with a new notation to help us to do that.
  ```js
    const keyname = 'apple'

    const fruit = {
        [keyname] : {
            color: 'green',
            taste: 'delicious 🍏'
        }
    }
  ```
- It can be a more complex expression and not a simple variable call.
  ```js
      const param = 'size';
      const config = {
          [param]: 12,
          // mobileSize
          [`mobile${param[0].toUpperCase()}${param.slice(1)}`] : 'large'
      }
  ```
 
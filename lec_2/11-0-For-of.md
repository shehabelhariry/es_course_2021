# For...of

- A new looping expression that can be used with `iterable` objects
- It simplifies the looping by dropping the index and counter and just work with the value
  ```js
  const array = [1,2,3,4,5];

  //using for in
  for (let i in array) {
      console.log(array[i])
  }

  // using for of
  for (let item of array) {
      console.log(item)
  }
  ```
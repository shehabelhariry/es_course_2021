## Symbols

- Symbols is a new primitive data type which has a unique value
- It's used to create a unique object key
- You can add a `description` for the symbol but it really wouldn't have an effect on the value of that symbol
- Meaning that 2 symbols with the same description are not equal
  ```js
    const mySym1 = Symbol('abc');
    typeof mySym1 //symbol 

    const mySym2 = Symbol('abc');

    mySym1 === mySym2 // false
  ```
- The main use case:
  ```js
    const user = {...} // this is coming from a source

    // You need to add another propety to the user which does not override the user properties

    const id = Symbol('id')

    user[id] = 12
  ```
- To be noted that you must save a reference for the symbol so that you can retrieve the value

- Symbols are not enumerable meaning that you won't be able to check the symbol values when iterating over an object conatining a Symbol property
  ```js
  const symbolId = Symbol(10);
  const myObj = {
      param1: 'hello',
      [symbolId]: 'Symbol are odd 🌚'
  }

  for (let i in myObj) {
      console.log(i) //  param1 only
  }
  ```
- To get the Symbol items you should use `Object.getOwnPropertySymbols`
  ```js
  const symbolId = Symbol(10);
  const myObj = {
      param1: 'hello',
      [symbolId]: 'Symbols are odd 🌚'
  }
  let test = Object.getOwnPropertySymbols(myObj)[0]

  myObj[test] // 'Symbols are odd 🌚'
  ```
- To know more about symbols: [here](https://www.youtube.com/watch?v=4J5hnOCj69w)
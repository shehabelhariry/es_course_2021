# Maps
- Maps are a new data structure in ES6
  ```js
    const myMap = new Map();
  ```
- to set Map items, you should define the key value pairs and insert them using the constructor
  ```js
    const myMap = new Map([["one", 1], ["two", 2]]);
    console.log(myMap) // Map (2) { one => 1, two => 2}
  ```
- To add items or change the values of items you can use the `set` method
  ```js
    const myMap = new Map([
      ["x", 2],
      ["y", 10],
    ]);
    myMap.set("z", 40);
    console.log(myMap) // {x => 2, y => 10, z => 40}
    myMap.set('y', 30) // {x => 2, y => 30, z => 40}
  ```
- Map keys can be any js data type. but it's recommended to either be a string or a `symbol`
- Keys in map cannot be repeated
- You can use `Map.entries` and `Map.keys` and `Map.values`
- To get the size of the Map use `size` property
  ```js
   const myMap = new Map([["one", 1], ["two", 2]]);
   myMap.size // 2
  ```
- Delete an item from the Map using delete function and clear using clear function
  ```js
    const myMap = new Map([["one", 1], ["two", 2]]);
    myMap.delete("one") // true
    myMap.delete("oppa") // false
    myMap.clear() // remove all items
  ```
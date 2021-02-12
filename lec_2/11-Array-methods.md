## map
- map is a method used to loop through an array in a functional style while modifying the array items.
- It takes one parameter: a callback function
- That callback takes one parameter: the current item.
- It returns a new array with the applied modifications.

```js
const newArray = array.map(function (item) {
    return item
})
```
- The logic you might apply to modify the item goes before the return keyword
 
 ```js
 const array = [1,2,3]
 const newArray = array.map(function (item) {
     let newItem = item * 2
     return newItem;
 })
 console.log(newArray)
 ```
- Because of the new arrow notation, map functions allow us to neatly write code in one line
 ```js
 const array = [1,2,3]
 const newArray = array.map(item => item * 2)
 console.log(newArray)
 ```
- We also get in the arguments of the callback, the index for each loop and the original array.
```js
 const array = [1,2,3,4]
 const newArray = array.map((item, index, array) => ({item, index, array}))
```

## Filter
- Filter loops through each item of an array and return a new array that fulfills a certain condition.
```js
const numbers = [0,1,2,3,4,5]
const evenNumbers = numbers.filter(function (item) {
    return item % 2 === 0 // condition that should be fulfiled
})
console.log(evenNumbers) //[0,2,4]
```
- like map it can be written with an arrow function notation.
 
## Find
- Find works the same way as filter except that it returns the first item that matches the condition.
- It’s used to look for a specific item.

```js
  const employees = [
    {id: 0, name: 'Shehab'},
    {id: 1, name: 'Ali'},
    {id: 2, name: 'Essam'},
  ]

  const emp = employees.find(employee => employee.id === 2)
```
## Reduce
- Reduce is a function used to get one output from a series of inputs (array)

```js
 const people = [
     {name: 'shehab', age: 29},
     {name: 'ahmed', age: 20},
     {name: 'magdy', age: 30}
 ]

 const sumOfAges = people.reduce(function (acc, item, index) {
     acc = acc + item.age
     return acc
 }, 0)
```

- It takes a call back function with 2 main params: 
  - The accumulator
  - The current item
- It takes a second param the initial accumulator value
- the function loops through the array and each time, it returns a value, it saves it into the accumulator.
- The value that is returned in the end is the last value saved in the accumulator.

- Example for Reduce
  - Array Flatten
  - Counting names

 
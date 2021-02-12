## Sets
- In a mathematical sense a Set is a group of numbers that are unique
- ES6 has introduced a new object that can only contain unique values called a Set It is an`iterable` object
- We create a Set by creating a new instance of the object `Set()`
```js
    let set = new Set();
    console.log(set)
```
- We can pass an array when I am creating a set and this will remove the duplicate items (used a lot)
 ```js
 const names = ['Ali', 'Mohamed', 'Ibrahim', 'Ali']
 let newSet = new Set(names);
 console.log(newSet) // Set(3) {'Ali', 'Mohamed', 'Ibrahim'}
 ```
- We can add items to a set using the function `add` 
- If you attempt to .add() a duplicate item to a Set, you won’t receive an error, but the item will not be added to the Set
  ```js
   const names = ['Ali', 'Mohamed', 'Ibrahim']
   let newSet = new Set(names);
   newSet.add('Shehab')
   console.log(newSet) // {'Ali', 'Mohamed', 'Ibrahim', 'Shehab'} 
   newSet.add('Ali') // {'Ali', 'Mohamed', 'Ibrahim', 'Shehab'} 
  ```
- We can delete items to a set using the function delete, if you try to .delete() an item that is not in the Set, you won’t receive an error, and the Set will remain unchanged.
 ```js
 const names = ['Ali', 'Mohamed', 'Ibrahim']
 let newSet = new Set(names);
 newSet.delete('Ali') //{'Mohamed', 'Ibrahim'}
 ```
- You can also clear the items in the set using the .clear() function
 ```js
  const names = ['Ali', 'Mohamed', 'Ibrahim']
  let newSet = new Set(names);
  newSet.clear()
 ```
- .size property gets us the number of items in a set
- .has() check if a value exist or not in the set and returns a boolean
 ```js
  const names = ['Ali', 'Mohamed', 'Ibrahim']
  let newSet = new Set(names);
  newSet.size // 3
  newSet.has('Ali') // true
  newSet.has('ibra') // false
 ```
- We can use for...of loop to go through the items of a set (we can also use forEach)
```js
  const names = ['Ali', 'Mohamed', 'Ibrahim']
  let newSet = new Set(names);
  for (name of newSet) {
      console.log(name)
  }
```
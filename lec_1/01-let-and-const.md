# let vs const

- Declaring variables in ES5 was done using the `var` keyword
- To create a constant in ES5, there was no easy way to do it instead there was a convention
- The old convention was to name the constant values in all caps

```js
var PI = 3.14
```

## const
- `const` is used for variables that you don't intend to change in the future
- if you try to change it, you get an error in the browser console.
- You should always give an initial value to a `const` variable

## let
- `let` is used for values that you intend to change (in loops and reasigns)

## var vs let
- The main difference betweeen var and let is that let is scoped to the `block` while var is scoped to the function 
- The other difference is that let (and const) are not hoisted

### Example 1
```js
    let x = 4;

    if (x === 4) {    
      let x = 3
      console.log(x) // what is the value of x?
    }
    
    console.log(x) // what is the value of x?
```

### Example 2
```js
    const array = [1,2,3,4];

    function getSumWithVar (array) {
        var sum = 0;
        console.log(i) // what is the value?
        for (var i = 0; i <= array.length; i++) {
            sum = sum + array[i]
        }
        console.log(i) // what is the value?
    }

    function getSumWithLet (array) {
        let sum = 0;
        console.log(i) // what will happen?

        for (let i = 0; i <= array.length; i++) {
            sum = sum + array[i]
        }

        console.log(i) // what is the value?
    }

    getSumWithVar(array)
    getSumWithLet(array)
```

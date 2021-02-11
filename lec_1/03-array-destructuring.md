## Array Destructuring

- Destructuring is the act of extracting values from arrays and objects in just a single step
(Very commonly used)

  ```js
  const names = ['ahmed', 'shehab', 'ali'];

  let name1 = names[0];
  let name2 = names[1];
  let name3 = names [2]

  ```

- To do the same thing we did in the previous example:

  ```js
  const [name1, name2, name3] = names;
  console.log(name1, name2, name3)
  ```
- I can skip an index in case I didn't want to destructure all the array
  
  ```js
  const [name1, , name3] = names;
  ```
- In case I have an array that contains empty or undefined values. I can use destructuring and give the empty array item a default value

  ```js
  const names = ['ahmed', 'osama', 'ali', , 'ibrahim'];

  let [name1, name2 = 'Unnamed', name3, name4 = 'Unnamed' ,name5] = names;

  ```

## Object Destructuring

- Destructuring can also be done to objects but with a small twist
    ```js
     const person = {
         name: 'Shehab',
         age: 29
     }
     const {name, age} = person
    ```
- The variables name you choose must be the same as the name of the properties inside the object you are destructuring

- The following code
  ```js
  const car = {
      fast: true,
      color: 'red',
      wheels: 4
  }

  const fast = car.fast;
  const color = car.color;
  const wheels = car.wheels
  ```
  is converted to:

  ```js
  const car = {
      fast: true,
      color: 'red',
      wheels: 4
  }

  const {fast, color, wheels} = car;

  ```
- You can rename the variable name to another using the following syntax:

  ```js
  const car = {
      fast: true,
      color: 'red',
      wheels: 4
  }

  const {fast, color, wheels: carWheels} = car;
  ```
- As with arrays we can give the properties we are destructuring an default value
  
  ```js
   const school = {
       seats: 100,
       classes: 10,
       principle: 'Ahmed',
   }

   const {seats, classes, principle, grade = "A"} = school;
  ```
- We can also destruct nested Objects
  
  ```js
    const person = {
        name: 'Ahmed',
        birthInfo: {
            birthMonth: 12,
            birthDay: 1,
            birthYear: 1992
        }
    }

    const {name, dateOfBirth: {birthMonth: month, birthDay: day, birthYear: year}} = person;
  ```
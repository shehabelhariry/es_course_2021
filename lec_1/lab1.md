## Lab 1

- Using the following object
    ```js
    let developer = {
      name: "Ahmed",
      birthYear: 1992,
      skills: ["PhotoShop", "HTML", "CSS", "JS"],
    };
    ```
  - Create a method `getAge` on the object, that uses the birthYear to get the age of the developer
  - Divide the `skills` array into 2 different arrays on the object:  `designSkills` (Containing Photoshop) and `devSkills` containing the rest
  -  using the following array `newSkills` merge the its values to the object property `devSkills`
  ```js
     const newSkills = ["ES6", "ES7", "ES😎"];
  ```
- Welcome to `ES Snacks` a restaurant that contains the best nerdy food aroud. 
    ```js
    const restaurant = {
      name: "ES-Snacks",
      drinks: {
        hot: ["coffee", "tea"],
        cold: ["pepsi", "7up", "fanta", "juice"],
      },
      meals: ["burger", "pizza"],
    };
    ```
  - Destructure the cold drinks array to a variable with the name `coldDrinks`
  - Write a function that return all the `coldDrinks` that have the letter `u`
  - Create a method `addOrder` on the `restaurant` object
  - It should take an object as a param which should look something like this:
    ```js
      {name: 'Shehab', order: {meal: 1, drink: {c: 1}}}
    ```
  - It should return a confirmation string after 2 seconds that should look something like this:
    ```js
    /*
    Thank you for ordering from ES-Snacks 
    
    Order Summary
    =============
    Mr/Ms: "Shehab"
    Order: "coffee", "pizza"

    have a great day!
    */
    ```
  - People were creating the order wrong a lot of the times. The manager of the restaurant decided to add some validation on the order.
  - Using the proxy API starting wih an `empty` object. The user should be able to create his order step by step with the following restrictions
    ```js
        order.meal = "Pizza" // error: meal should be a number
        order.meal = 10 // error: meal should be less than 2
        order.oppa = 'ay 7aga' // You cannot add a property oppa
        order.meal = 1// Done
        order.drink = 1 // This should be an object
        order.drink = {h:1} // Done
    ```
- Create a function `styled` using `tagged templates` that generate CSS strings using an internal `theme`
  - the `theme` object is as follows:
    ```js
      const theme = {
        color: {
          primary: "red",
          secondary: "blue",
        },
        fontSize: {
          small: "10px",
          large: "20px",
        },
      };
    ``` 
  - the theme object should be `inside` the method.
  - the method should be used as follows
    ```js
    styled`
      .h1 {
          color: ${ theme => theme.color.primary},
          font-size: ${ theme => theme.fontSize.large}
      }
    `
    ```
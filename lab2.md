## Lab2
1
    - Using the following array
    ```js
    const arrayOfFood = ["burger", "pizza", "donuts", "pizza", "koshary", "donuts", "seafood", "burger"]
    ```
    - Create a Set with the values of this array
    - Add `pasta` to the set and log the set to the console.
    - Remove `burger` from the set and log the set to the console.
    - Write a function that takes the set as a paramter and clear the set if it has more than 2 items
2
    - Create a `Vehicle` class that has a constructor function that takes 2 params: `wheels` and `speed`
    - wheels has a default value of 4 and speed has a default value of 100  
    - Create a subclass `Bike` that inherits from Vehicle and has different
    default values wheels = 2, speed = 10, basket = boolean
    - Add a static method to the Vehicle class to compare
    speeds of vehiles
    - find out how many times an object was created from the `Vehicle` class 
3
    - Using the fetch api and async await, get the data from that (../user.json)
    - format the array of users by adding an extra full_name attribute to each item 
    - only get the male users who are older than 50
    -  group the filtered users by nationality
        { EG: [{...}] , ... }  
    - Get the oldest person with a nationality of ‘FR’
 
- Create a `range` iterable object. When we loop on it with for...of and consoling log each item, I should get the numbers form 1 to 10
  ```js
    const range = {
        from: 1,
        to: 10,
    }

    for (let item of range) {
        console.log(item) 
    }
  ```
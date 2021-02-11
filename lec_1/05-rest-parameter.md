## Rest Parameter

- The rest parameter, also  written with three consecutive dots (...) allows you to represent an indefinite number of elements as an array
  
  ```js
    const order = [92, 15, 'Big Tasty', 'Large Fries', 'Diet Pepsi 🤣']	
    const [total, taxes, ...mealItems] = order;
  ```
- We can use the rest parameter as a function parameter to group the rest of the arguments
  ```js
    function sumFirstNum (num1, ...nums) {
        let newArr = [];
        nums.forEach(num => {
            newArr.push(num + num1)
        })
        return newArr;
    }

    sumFirstNum(4, 10,20,30);
  ```
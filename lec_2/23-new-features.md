# New Features

- `Array.includes`
  ```js
    const arr = [1,2,3]
    arr.includes(1) // true
    arr.includes('sss') // false
  ```
- `Exponential operator **`
  ```js
    const res =  Math.pow(5,10);
    const res2 = 5**10 
  ```
- `Object.vaules`, `Object.entries` and `Object.fromEntries`
- `Nullish operator`
  - When we used to do `||` the result would be the left if the value of `param1` is a falsy value (undefined, null, false, 0)
    ```js
    const x = null;
    const y = undefined;
    const z = 0;
    const val = 'value'

     const var1 = x || 5 // 5
     const var2 = z || 5 // 5
     const var3 = z ?? 5 // 0
    ```
- Optional Chaining
  - This operator came to solve the problem `cannot find something of undefined`


  ```js
  const obj = {
    name: "Shehab",
    contacts: [
      { name: "ahmed", phone: "01000200" },
      { name: "ahmed", phone: "01000200", pets: ["cat", "dog"] },
    ],
  };

  const { contacts } = obj;

  contacts.forEach((contact) => {
    // Preview the first pet
    console.log(contact?.pets?.[0]);
  });
  ```

  ```js
  let customer = {
    name: "Carl",
    details: {
      age: 82,
      location: "Paradise Falls" // detailed address is unknown
    }
  };
  let customerCity = customer.details?.address?.city;

  ```
## Classes 

- ES6 added a syntactic sugar over prototypes to simplify the development for programmers coming from other languages.
- The `class` construct allows one to define prototype-based classes with a clean, nice-looking syntax.
  ```js
    class User {
        constructor(name) {
            this.name = name
        }
        sayHi() {
            alert(this.name)
        }
    }

    const user1 = new User('Ahmed')
    user1.sayHi()
  ```
- Each class should have a `constructor` to give it an initial value
  ```js
    class Food {
        constructor(name){
            this.name = name;
        }
    }

    const myFood = new Food('Pizza🍕')
    console.log(myFood) // { name: 'Pizza🍕'}
  ```
- We can use default parameters in constructor functions in case a value is not passed
 ```js
    class Person {
        constructor (name = 'Unnamed Person') {
            this.name = name;
        }
    }

    const person1 = new Person('Ahmed') // {name: 'Ahmed'}
    const person2 = new Person() // {name: 'Unnamed Person'}
 ```
- We could have methods inside a class that can be called afterwards
 
 ```js
    class Person {
        constructor (name = 'Unnamed Person') {
            this.name = name;
        }

        says(statement) {
            return `${this.name} says: ${statement}`
        }
    }

    const person1 = new Person('Shehab');
    person1.says('Hi') // Shehab says: Hi
 ```
- You can use `setters` and `getters` to interact with the class members and enforce some validations
  ```js
    class Person {
        constructor(name) {
            this.name = name
            this._age = null
        }

        set age (age) {
            if (typeof age !== 'number') {
                throw 'Age should be a number'
            }
            this._age = age 
        }

        get age () {
            return this._age;
        }
    }

    const p = new Person('Shehab')
    p.age = '12' // Age should be a number
    p.age = 12 // OK
    p.age // 12
    p._age // 12
  ```
- You can also add `static methods` which are utility functions embedded inside a class
- It’s attached to the class and not the resulting object
    ```js
        class Square {
            constructor (height = 12) {
                this.height = height
            }

            calculateArea() {
                return this.height * this.height
            }

            static isEqual(sq1, sq2) {
                return sq1.height = sq2.height 
            }
        }
        const sq1 = new Square()
        const sq2 = new Square(10)

        Square.isEqual(sq1, sq2) // false
    ```
- We could have `subclasses` that extends parent classes
- We use the keyword `super` to call the parent constructor.
  ```js
      class Animal {
          constructor (legs = 2, color = 'brown') {
              this.legs = legs
              this.color = color
          }
      }

      class Cat extends Animal {
          constructor (legs, color, sound = 'Meow') {
              super(legs, color)
              this.sound = sound
          }
      }

      const kitty = new Cat(4, 'red', 'Meowwwwww 🐈')
  ```
- You can get very close to creating private members by creating members that have `symbols` as a key
    ```js
    class Person {
      constructor(name, phone) {
        this.name = name;
        this[Symbol("phone")] = phone;
      }
    }

    const p = new Person("shehab", 010002030);
    ```
- You can now create private members using names that are preceded by `#`
  ```js
  class Person {
    #name;
    constructor(name, phone) {
      this.#name = name;
    }
  }

  const p = new Person("shehab", 010002030); 
  p.#name // Error this member is private
  ```
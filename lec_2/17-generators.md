## Generators

- Generators are iterable objects.
- They look like a function declaration except there is an `*` between the function keyword and the function name
- The generator contains one or more yield statement
  ```js
    function* gen () {
        yield 10
        yield 20
    }

    const myGen = gen();
    myGen.next() // {value: 10, done: false};
    myGen.next() // {value: 20, done: false};
    myGen.next() // {value: undefined, done: true};

  ```
- You can also use everything that uses iterators on generators
  ```js
    function* gen () {
        yield 10
        yield 20
    }

    const myGen = gen();
    for (let item of myGen) {
        console.log(item)
    }
  ```  
- You can add any code you want and have it excuted in a certain step
  ```js
    function * gen () {
        console.log('this is my first step');
        const a = 12;
        yield a
        const b = 22
        const result = a + b;
        yield result;
    }

    const myGen = gen();
  ```
- if you are yielding an iterable object and you want to pause on each item you can precede it by an `*`
  ```js
    function* gen () {
        yield *[1,2]
        yield 20
    }

    const myGen = gen();
    myGen.next() //{value: 1, done: false}
    myGen.next() //{value: 2, done: false}
    myGen.next() //{value: 20, done: false}
    myGen.next() //{value: undefined, done: true}
  ```
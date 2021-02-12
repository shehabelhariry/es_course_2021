## Iterable Object

- An object is considered iterable if it has `Symbol.iterator` property in its prototype
- We can use with iterables:
  - `for...of`
  - `destructuring`
  - `spread operator`

```js
    const array = ['a', 'b', 'c']
    const iterator = array[Symbol.iterator]()
    iterator.next() // {value: 'a', done: false}
    iterator.next() // {value: 'b', done: false}
    iterator.next() // {value: 'c', done: false}
    iterator.next() // {value: undefined, done: true}
```
- iterators are very useful when used with `generators`
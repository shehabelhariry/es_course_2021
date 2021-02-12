## Tagged Template

- tagged templates are another way to write functions. it looks like this
  ```js
    const fuc = (strings, ...values) => strings.map((str, index) => values[index]? str + values[index] : str ).join('')
    const emoji = '🎇'
    fuc`ES6+ is ${emoji}!!!`
  ```
- The first param contains an array of all the strings we have in the template provided (الفواصل )
- The second param is all the values (variables) used in the string provided
  ```js
  const name = "Shehab";

  function fun(strings, ...variables) {
    console.log(strings, variables);
    let res = "";
    for (let i = 0; i < strings.length; i++) {
      res = variables[i] ? res + strings[i] + variables[i] : res + strings[i];
    }
    console.log(res);
  }

  fun`${name}  hello there`;
  ```
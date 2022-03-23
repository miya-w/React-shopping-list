# React-shopping-list
![shopping-list](https://github.com/miya-w/React-shopping-list/blob/main/imgs/shoppinglist00.png)

**What will you learn in this React project?**
CRUD -> Create, Read, Update, Delete
### 1.Create & Read (Add function)
- complex state & Javascript ES6 Spread Operator

  ` function addItems(){
    setItems(prevItems => {
      // Javascript ES6 Spread Operator
      return [...prevItems, inputText];
    })
    // set the input text to an empty
    setInputText(" ")
  }`

---
### 2.map() method & arrow function
`{items.map(todoItem =>{return<li>{todoItem}</li>})}`
map() method
arrow function
[Arrow function expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

---
### 3. 
# React-shopping-list
![shopping-list](https://github.com/miya-w/React-shopping-list/blob/01-create-add-function/imgs/shoppinglist-add.png)

**What will you learn in this React project?**

### 1.Create & Read ( Add function )
1.  set initial state

```
const [inputText, setInputText] = useState("");
<input onChange={handleChange} type="text" value={inputText} />
``` 
So the first thing we're going to tackle is when new text is written into the input, it's state should be saved.
we should do  is to add a value property to our inputs and to tie it to this inputText state. So this way we are controlling the inputs and keeping the input value inline with the input text.

2. Add an onChange to this input and get it to call a function

create a new constant which is going to keep hold of the new value of the input. So we'll just call it newValue and I'm going to set it to *** event.target.value. ***  Now notice how in this case we've only got one input. And once we've gotten that, then we can call setInputText and inside this function, we're going to pass it this new value. And because in this case I'm not actually changing the inputText, I don't actually need the previous value. I've got this whole new value that I want to give it which is going to correspond to whatever the users typing inside this input.

3. Now the initial value for items is just going to be an empty array.
```
const [items, setItems] = useState([]);
```


4. complex state & Javascript ES6 Spread Operator

  ```
   function addItems(){
    setItems(prevItems => {
      // Javascript ES6 Spread Operator
      return [...prevItems, inputText];
    })
    // set the input text to an empty
    setInputText(" ")
  }
  ```
and inside here we want to get hold of the previous items so that we can simply add the new input at the end of the array as a new item. and inside here we want to get hold of the previous items so that we can simply add the new input at the end of the array as a new item.
So to do that, we're going to have to create a new arrow function. Inside the input of this arrow function is going to be the previous items
Then what we're going to return is going to be a new array using the spread operator
So let's add our spread operator, add in all of the items from our previous items and then we're going to add the new item which is going to be what's currently inside are inputText.
5. map() method & arrow function
```
 {items.map(todoItem => {return <li>{todoItem}</li>})}
 ```
So if we want to use this array of items to render all of the s to contain the text inside each item, we need map function. So we can tap into our items, call the map function and then inside the map function we can pass it an arrow function and inside this arrow function we'll get access to each item.
map through all of the items for each to-do item, create array put the to-do item in that 


---


arrow function
[Arrow function expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
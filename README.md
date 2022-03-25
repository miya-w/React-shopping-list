# React-shopping-list
![shopping-list]( https://github.com/miya-w/React-shopping-list/blob/02-update-line-through/imgs/shoppinglist03.png)
---
### What will you learn in this React project?
- Get item line-through
---
## 3. props
```
// App.jsx
{items.map(todoItem => (<ToDoItem text = {todoItem}/>))}
```
in order to display a different ToDoItem each time we map through our items array, we're going to pass this ToDoItem which is the text,this should display as a property. So we'll call it text maybe and set it equal ToDoItem. So now we can receive this text inside our ToDoItem as one of the props and instead of having this text.
```
// ToDoItem.jsx
 <li>{props.text}</li>
```
## 4. React Conditional Rendering with the Ternary Operator 
```

function ToDoItem(props){
    const [isDone, setIsDone] = useState(false);
    function handleClick(){
   setIsDone( prevValue => {
     <!-- if eles -->
       return !prevValue
   });
}
    return(
    <div onClick={ handleClick }>
       <li style = {{ textDecoration: isDone ? "line-through": "none" }}>{props.text}</li>
    </div>
    )
```
Ｓet a boolean maybe to true or to false depending on whether if this text decoration should be applied. Let's say that I had a constant called isDone and this isDone property is either true or false depending on whether if the user clicked on this div. And to set this isDone property, I'm going to have a function called setIsDone.
Use state to achieve this. Now the initial value of isDone is going to be false because all items should start out being not done with no line through.
**Ternary Operator** 
use this isDone to conditionally render this textDecoration. When this isDone is true, we're going to apply line-through text decoration, when this is false we're going to change the textDecoration back to none even if this was already applied.
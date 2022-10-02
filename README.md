**1. Explain what the simple List component does?**

```
Simple list component accepts various props and renders a list item on the page and background color of list item 
is determined by is Selected prop. If item is selected  then background color of item is green else background color
is red by default.
```
**2. What problems / warnings are there with code?**

- Defining a default prop as null is not recommended. Either use Undefined or an array of values.

```
WrappedListComponent.defaultProps = {
  items: null,
};

```

- Unique key prop is missing for List items.

```
<ul style={{ textAlign: 'left' }}>
      {items.map((item, index) => (
        <SingleListItem
          onClickHandler={() => handleClick(index)}
          text={item.text}
          index={index}
          isSelected={selectedIndex}
        />
      ))}
</ul>

```

- Syntax errors in the following code. ShapeOf should be shape and array should be arrayOf.

```
 WrappedListComponent.propTypes = {
   items: PropTypes.array(
     PropTypes.shapeOf({
       text: PropTypes.string.isRequired,
     })
   ),
 };
 
```

- Syntax error in useState() hook.

```
 const [setSelectedIndex, selectedIndex] = useState(); 
 
```

- In list item's onClick method there is a function call but onClick accepts function's reference.

```
 <li style={{ backgroundColor: isSelected ? "green" : "red" }}
      onClick={onClickHandler(index)}>
       {text}
 </li>
 
```




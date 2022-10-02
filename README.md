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




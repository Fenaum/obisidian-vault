### Tags: [[language-basics]], [[datatypes]]
### References:  [[Variables and Data Types]]

## Notes:


### Lists (Arrays)

Lists in Python are dynamic, mutable, and equivalent to JavaScripts arrays

Examples:

```Python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
```

```JavaScript
let fruits = ["apple", "banana", "cherry"];
fruits.push("orange");
```

Use [[Slicing]] for easy subsetting:

```python
first_two = fruits[:2] # ['apple', 'banana']
```

Lists can also hold mixed type: [1, "apple", True]
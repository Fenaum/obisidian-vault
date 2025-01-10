### Tags: [[datatypes]], [[language-basics]]
### References: [[Variables and Data Types]]

## Notes:

A **tuple** in Python is an **ordered, immutable** collection of items. Tuples are similar to lists, but once a tuple is created, it cannot be modified (no adding, removing, or changing items).

1. Using Parentheses:
```python
my_tuple = (1, 2, 3)
print(my_tuple)  # (1, 2, 3)
```

1. Without Parentheses (Comma-Separated)
```python
my_tuple = 1, 2, 3
print(my_tuple)  # (1, 2, 3)
```

1. Single Element Tuple (add a trailing coma)
```python
single_element = (42,)
print(single_element)  # (42,)
```

1. Empty Tuple
```python
empty_tuple = ()
print(empty_tuple)  # ()
```


---

**Key Characteristics of Tuples**

1. **Ordered**:
• Items in a tuple retain their order.
• You can access items using an index.

```python
my_tuple = (10, 20, 30)
print(my_tuple[0])  # 10
```

2. **Immutable**:
```python
my_tuple = (1, 2, 3)
# my_tuple[1] = 99  # This will raise a TypeError
```

3. **Can Hold Mixed Data Types**:
```python
mixed_tuple = (1, "hello", [3, 4, 5])
print(mixed_tuple)  # (1, 'hello', [3, 4, 5])
```

4. **Hashable**:
```python
my_dict = {(1, 2): "point"}
print(my_dict[(1, 2)])  # point
```

**When to Use Tuples?**

1. **Immutability Needed**:
• Use tuples when the data shouldn’t change. For example:
• Storing coordinates: (x, y, z)
• Days of the week: ("Monday", "Tuesday", ...)

2. **Performance**:
• Tuples are faster than lists for read-only operations because they are immutable.

3. **Dictionary Keys**:
• Tuples can be used as keys in dictionaries, unlike lists.
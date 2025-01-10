### Tags: 
### References: [[Loops]]

## Notes:

Python's for loop iterates over a squence (like a list, tuple, dictionary, or string) rather using indices

Syntax:

Iterating over a list
```python
for variable in sequence:
# Code block

fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

Iterating with range()
```python
for i in range(5):  # Generates numbers 0 to 4
    print(i)
```

Key Features of range():
• **Basic usage**: range(n) generates numbers from 0 to n-1.
• **Custom start/step**: range(start, stop, step):

```python
for i in range(1, 10, 2):  # 1, 3, 5, 7, 9
    print(i)
```

Iterating over Dictionaries

Python allows you to directly iterate over dictionary keys, values, or both
```python
person = {"name": "Alice", "age": 25}
for key, value in person.items():  # key-value pairs
    print(key, value)
```
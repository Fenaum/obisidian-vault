### Tags: [[language-basics]]
### References: [[Method]], [[Async Function]], [[Functional Programming Constructs]]

## Notes:

Reusable block of code designed to perform a specific task.

# Defining a Function

Use the def keyword:
```python
def greet(name):
	return f"hello, {name}!"
```

Calling a Function
```python
print(greet('Alice')) # Hello, Alice!
```

Function Anatomy
```python
def function_name(parameters):
    """Docstring: describes what the function does."""
    # Code block
    return result  # Optional
```

---

# Types of Functions

**Built-in Functions**

Python comes with many built-in functions, such as:
* len(): Returns the length of an object
* type(): Returns the type of the object
* print(): Prints to the console
```python
nums = [1, 2, 3]
print(len(nums))  # 3
print(type(nums))  # <class 'list'>
```

**User-Define Functions**

Functions you define to perform custom operations

**Lambda (Anonymous) Functions**

A one-line function using lambda keyword.
```python
lambda arguments: expression

square = lambda x: x**2
print(square(4))  # 16
```
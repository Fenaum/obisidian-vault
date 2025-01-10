### Tags: [[language-basics]], [[datatypes]]
### References: [[Variables and Data Types]]

## Notes:

A **set** in Python is an **unordered collection of unique items**. Sets are mutable, meaning you can add or remove elements, but the elements themselves must be immutable.

**Key Characteristics of a Set**

1. **Unordered**:
• Elements in a set do not have a defined order.
• You cannot access set elements by index or slicing.

2. **Unique Elements**:
• A set automatically removes duplicates.

3. **Mutable**:
• You can add or remove elements from a set.

4. **Immutable Elements**:
• Elements in a set must be hashable and immutable (e.g., numbers, strings, tuples).

---

## How to Create a Set

1. Using Curly Braces {}:
```python
my_set = {1, 2, 3}
print(my_set)  # {1, 2, 3}
```
2. Using the Set() Constructor:
```python
my_set = set([1, 2, 3, 3, 4])
print(my_set)  # {1, 2, 3, 4}
```
3. Empty Set
```python
empty_set = set()
print(empty_set)  # set()
```

---

## Basic Set Operations

1. Adding Elements
```python
my_set = {1, 2}
my_set.add(3)
print(my_set)  # {1, 2, 3}
```
2. Removing Elements
```python
my_set = {1, 2, 3}
my_set.remove(2)
print(my_set)  # {1, 3}
#remove(): raises an error if the element doesn't exist

my_set.discard(4)  # No error
# doesn't raise an error if the element doesn't exist

my_set = {1, 2, 3}
print(my_set.pop())  # 1 (or another element)
#pop(): Removes and returns any arbitrary element

```
3. Clearing a Set
```python
my_set = {1, 2, 3}
my_set.clear()
print(my_set)  # set()
```

Sets are powerful tools in Python for tasks that involve unique elements, fast membership testing, and mathematical operations. Here’s a detailed breakdown of what sets can accomplish:

## Mathematical Set Operations

**Union**:

Combine elements from two sets.
```python
a = {1, 2, 3}
b = {3, 4, 5}
print(a | b)  # {1, 2, 3, 4, 5}
```

**Intersection**:

Find common elements between sets
```python
print(a & b)  # {3}
```

**Difference**:

Find elements in one set but not for the other
```python
print(a - b)  # {1, 2}
```

**Symmetric** **Difference**

Find elements in either set, but not in both
```python
print(a ^ b)  # {1, 2, 4, 5}
```

### Tags: 
### References: [[Data Transformation & Manipulation]], [[Function]]

## Notes:

Functional programming (FP) is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state or mutable data. Python supports functional programming constructs, and in this context, it provides several important functions that allow you to work with data in a functional style. Below are the **core and common functional programming constructs** in Python, including map(), filter(), reduce(), lambda, and others.

# [[map()]]
• **Purpose:** Transforms each element of an iterable (e.g., list, tuple) by applying a given function.
• **How it works:** It takes a function and an iterable as arguments and applies the function to each item in the iterable, returning a map object (which is an iterator).

```python
numbers = [1, 2, 3, 4]
squared = map(lambda x: x ** 2, numbers)
print(list(squared))  # [1, 4, 9, 16]
```

# [[filter()]]
• **Purpose:** Filters elements from an iterable based on a given condition (function).
• **How it works:** It takes a function and an iterable, applies the function (which should return True or False) to each element, and returns an iterator that includes only those elements for which the function returned True.

```python
numbers = [1, 2, 3, 4, 5]
evens = filter(lambda x: x % 2 == 0, numbers)
print(list(evens))  # [2, 4]
```

# [[reduce() (from frunctools module)]]
• **Purpose:** Reduces an iterable to a single cumulative result by applying a function that takes two arguments.
• **How it works:** The function is applied cumulatively to the elements of the iterable, from left to right, so as to reduce the iterable to a single value. It requires an initial accumulator value.

```python
from functools import reduce

numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print(product)  # 24 (1*2*3*4)
```

# [[any() and all()]]
• **Purpose:** Check if any or all elements in an iterable satisfy a given condition.
• **How it works:**
	• any() returns True if at least one element is True.
	• all() returns True if all elements are True.

```python
numbers = [1, 2, 3, 4]
print(any(x > 3 for x in numbers))  # True (since 4 > 3)
print(all(x > 0 for x in numbers))  # True (all numbers are positive)
```

# [[zip()]]
• **Purpose:** Combines multiple iterables into one by pairing elements from each iterable.
• **How it works:** It returns an iterator of tuples where each tuple contains elements from the iterables at the same index.

```python
names = ["Alice", "Bob", "Charlie"]
scores = [85, 92, 78]
zipped = zip(names, scores)
print(list(zipped))  # [('Alice', 85), ('Bob', 92), ('Charlie', 78)]
```

# [[sorted()]]
• **Purpose:** Returns a new sorted list from the elements of any iterable.
• **How it works:** It sorts the iterable by default, but you can provide a custom sorting function with the key argument.

```python
numbers = [4, 1, 3, 2]
sorted_numbers = sorted(numbers)
print(sorted_numbers)  # [1, 2, 3, 4]

# Custom sorting by length of strings
words = ["apple", "banana", "kiwi"]
sorted_words = sorted(words, key=lambda x: len(x))
print(sorted_words)  # ['kiwi', 'apple', 'banana']
```

# [[enumerate()]]
• **Purpose:** Adds a counter to an iterable and returns an iterator of tuples (index, value).
• **How it works:** This is useful when you need both the index and the value of the items in an iterable.

```python
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
```

```output
0: apple
1: banana
2: cherry
```

# [[list() and set() (conversions)]]
• **Purpose:** These functions convert other iterables (e.g., tuples, dictionaries) into lists or sets.
• **How it works:** Useful for ensuring that the type you’re working with has the desired properties (e.g., uniqueness for set()).

```python
# Convert a string to a list of characters
word = "hello"
word_list = list(word)
print(word_list)  # ['h', 'e', 'l', 'l', 'o']

# Convert a list to a set (removes duplicates)
numbers = [1, 2, 2, 3, 4, 4]
unique_numbers = set(numbers)
print(unique_numbers)  # {1, 2, 3, 4}
```

---

The functional programming constructs in Python are powerful tools for working with data in a more concise, modular, and functional style. They allow you to transform, filter, reduce, and manipulate data without resorting to traditional looping and state changes. These methods are integral to **data transformation** in Python and are widely used in many applications.
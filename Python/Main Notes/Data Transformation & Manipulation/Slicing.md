### References: [[List]], [[Data Transformation & Manipulation]]

## Notes:


Slicing is used for **Subsetting** which refers to the process of selecting specific portions (subsets) of data from a larger dataset or collection.

Slicing can be used to extract parts of sequences such as lists, strings, or tuples

----

**Slicing is a concise way to extract a portion of sequence using the syntax.**

```python
sequence[start:stop:step]
```

**Parameters:**
1. start: The index where the slice begins (inclusive).
2. stop: The index where the slice ends (exclusive).
3. step _(optional)_: The stride or interval between elements in the slice.

Basic Slicing Examples

```python
fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry']

first_two = fruits[:2] # ['apple', 'banana']
# start is omitted, so it defaults to 0
# stop is 2, so it includes indices 0 and 1 but excludes 2.

from_third = fruits[2:] # ['cherry', 'date', 'elderberry']
# start is 2 (begin at 'cherry').
# stop is omitted, so it goes to the end of the list

middle = fruits[1:4] # ['banana', 'cherry', 'date']
# start is 1 ('banana')
# stop is 4, so it exludesa 'elderberry'

every_second = fruits[::2] # ['apple', 'cherry', 'edlerberry']
# start and stop are omitted (defaults to the entire list)
# step is 2, so it tgake every second element.

reversed_fruits = fruis[::-1] # ['elderberry', 'date', 'cherry', 'banana', 'apple']
``` 

## Subsetting with Strings

Slicing works with strings because they are also sequence.

Examples

```python
word = "pineapple"

# First three characters
print(word[:3])  # 'pin'

# Last three characters
print(word[-3:])  # 'ple'

# Every second character
print(word[::2])  # 'pnapl'

# Reverse the string
print(word[::-1])  # 'elppaenip'
```


**Why Use Subsetting?**
  
Subsetting allows you to:
1. Extract relevant parts of data for analysis.
2. Simplify operations by isolating the required subset.
3. Manipulate sequences without modifying the original data.

Slicing can also be applied to nested lists:

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Extract the first two rows
subset_rows = matrix[:2]
print(subset_rows)
# Output: [[1, 2, 3], [4, 5, 6]]

# Extract first two elements of each row
subset_elements = [row[:2] for row in matrix]
print(subset_elements)
# Output: [[1, 2], [4, 5], [7, 8]]
```

----

Subsetting in Javascript using Slice Method():

```javascript
array.slice(start, end)
```
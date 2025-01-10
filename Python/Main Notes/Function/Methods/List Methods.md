### Tags: 
### References: [[Method]]

## Notes:

Lists are mutable, and these methods allow modification and manipulation.

a. Common List Methods
```python
# Example list
fruits = ["apple", "banana", "cherry"]

# 1. Adding Elements
fruits.append("date")  # ["apple", "banana", "cherry", "date"]
fruits.insert(1, "blueberry")  # ["apple", "blueberry", "banana", "cherry", "date"]

# 2. Removing Elements
fruits.remove("banana")  # ["apple", "blueberry", "cherry", "date"]
last_fruit = fruits.pop()  # Removes and returns "date"
fruits.clear()  # []

# 3. Finding and Sorting
nums = [3, 1, 4, 2]
nums.sort()  # [1, 2, 3, 4]
nums.reverse()  # [4, 3, 2, 1]

# 4. Counting and Indexing
nums = [1, 2, 3, 1, 2, 1]
print(nums.count(1))  # 3 (number of times 1 appears)
print(nums.index(3))  # 2 (index of first occurrence of 3)
```

### List (Array) Methods:

- `.append(item)`: Adds an item to the end of the list.
- `.extend(iterable)`: Extends the list by appending elements from an iterable.
- `.insert(index, item)`: Inserts an item at a specified position.
- `.remove(item)`: Removes the first occurrence of an item.
- `.pop([index])`: Removes and returns the item at the given index (default is the last item).
- `.clear()`: Removes all items from the list.
- `.index(item, [start, [end]])`: Returns the index of the first occurrence of an item.
- `.count(item)`: Returns the number of occurrences of an item.
- `.sort(key=None, reverse=False)`: Sorts the list in place.
- `.reverse()`: Reverses the elements of the list in place.
- `.copy()`: Returns a shallow copy of the list.
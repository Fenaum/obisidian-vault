### Tags: 
### References: [[Method]]

## Notes:

Sets are unordered collections of unique items.
```python
# Example sets
a = {1, 2, 3}
b = {3, 4, 5}

# 1. Adding and Removing
a.add(4)  # {1, 2, 3, 4}
a.discard(2)  # {1, 3, 4}

# 2. Set Operations
print(a.union(b))  # {1, 2, 3, 4, 5}
print(a.intersection(b))  # {3}
print(a.difference(b))  # {1, 4}

# 3. Checking Membership
print(3 in a)  # True
print(6 not in a)  # True
```

### Tags: 
### References: [[Method]]

## Notes:

Dictionaries store key-value pairs. These methods help in accessing and modifying them.

a. Common Dictionary Methods
```python
# Example dictionary
person = {"name": "Alice", "age": 25, "city": "New York"}

# 1. Accessing Keys, Values, and Items
print(person.keys())  # dict_keys(['name', 'age', 'city'])
print(person.values())  # dict_values(['Alice', 25, 'New York'])
print(person.items())  # dict_items([('name', 'Alice'), ('age', 25), ('city', 'New York')])

# 2. Adding and Updating
person["job"] = "Developer"  # Adds a new key-value pair
person.update({"age": 26})  # Updates existing key-value pair

# 3. Removing
person.pop("city")  # Removes "city" key
person.clear()  # Clears the dictionary
```

### Dictionary (Object) Methods:

- `.keys()`: Returns a view object that displays a list of all the keys.
- `.values()`: Returns a view object that displays a list of all the values.
- `.items()`: Returns a view object that displays a list of dictionary's key-value tuple pairs.
- `.get(key, default=None)`: Returns the value for the specified key if the key is in the dictionary.
- `.update([other])`: Updates the dictionary with the key-value pairs from another dictionary or an iterable of key-value pairs.
- `.pop(key, [default])`: Removes the specified key and returns the corresponding value.
- `.popitem()`: Removes and returns a key-value pair from the dictionary.
- `.clear()`: Removes all items from the dictionary.
- `.copy()`: Returns a shallow copy of the dictionary.
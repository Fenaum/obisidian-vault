### Tags: [[language-basics]], [[datatypes]]
### References: [[Variables and Data Types]]

## Notes:

Dictionaries are key-value pairs like JavaScript objects.

```python
user = {"name": "Alice", "age": 30}

print(user["name"])  # Alice
```

Python keys can be of **any immutable type**, such as:
• Strings
• Numbers
• Tuples (containing only immutable elements)
• Other immutable types (e.g., frozenset).

```python
data = {
    "name": "Alice",  # String key
    42: "The Answer",  # Integer key
    (1, 2): "Tuple Key"  # Tuple key
}

print(data["name"])  # Alice
print(data[42])      # The Answer
print(data[(1, 2)])  # Tuple Key
```

Python’s dict.get(key, default) method is used for **safe key access**:

• If the key exists, it returns the value.
• If the key doesn’t exist, it returns the specified default (or None if omitted).

```python
data = {"name": "Alice", "age": 25}

print(data.get("name"))        # Alice
print(data.get("nonexistent")) # None
print(data.get("nonexistent", "Default Value"))  # Default Value
```

**On the contrary:**
JavaScript doesn’t have a built-in equivalent to Python’s .get() for objects, but you can achieve similar behavior:

```javascript
let obj = { name: "Alice", age: 25 };
console.log(obj?.name);        // Alice
console.log(obj?.nonexistent); // undefined
```
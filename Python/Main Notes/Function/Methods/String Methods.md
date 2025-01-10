### References: [[Method]]

## Notes:

These methods help manipulate and process strings.

a. Common String Methods
```python
# Example string
text = "Hello, Python!"

# 1. Case Conversion
print(text.lower())  # "hello, python!"
print(text.upper())  # "HELLO, PYTHON!"
print(text.capitalize())  # "Hello, python!"
print(text.title())  # "Hello, Python!"

# 2. Searching and Finding
print(text.find("Python"))  # 7 (index of "Python")
print(text.index("Python"))  # 7 (throws error if not found)
print(text.count("o"))  # 2 (number of 'o' characters)

# 3. Replacing and Stripping
print(text.replace("Python", "World"))  # "Hello, World!"
print(text.strip("!"))  # "Hello, Python" (removes '!' from both ends)

# 4. Splitting and Joining
words = text.split()  # ['Hello,', 'Python!']
print(" ".join(words))  # "Hello, Python!"

# 5. Checking String Properties
print(text.startswith("Hello"))  # True
print(text.endswith("!"))  # True
print(text.isalpha())  # False (contains spaces and punctuation)
```


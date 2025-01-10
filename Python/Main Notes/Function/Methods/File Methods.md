### Tags: 
### References: [[Method]]

## Notes:

File methods allow interaction with files.
```python
# Example: Reading and Writing to Files
with open("example.txt", "w") as file:
    file.write("Hello, world!")

with open("example.txt", "r") as file:
    content = file.read()
    print(content)  # "Hello, world!"
```


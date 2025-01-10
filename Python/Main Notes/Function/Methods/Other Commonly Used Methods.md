### Tags: 
### References: [[Method]]

## Notes:

a. **Enumerate**

Adds an index to iterate items during iteration
```Python
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(index, fruit)
# 0 apple
# 1 banana
# 2 cherry
```

b. **Zip**

Combines two or more iterable into tuples
```Python
names = ["Alice", "Bob", "Charlie"]
ages = [25, 30, 35]
print(list(zip(names, ages)))
# [('Alice', 25), ('Bob', 30), ('Charlie', 35)]
```

c. **Map**

Applies a function to each element in an iterable
```Python
nums = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, nums))
print(squared)  # [1, 4, 9, 16]
```

d. **Filter**

Filter elements based on a condition
```Python
nums = [1, 2, 3, 4]
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)  # [2, 4]
```
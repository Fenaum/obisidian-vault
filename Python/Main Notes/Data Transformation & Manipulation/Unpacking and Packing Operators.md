### Tags: 
### References: [[Syntax]], [[Data Transformation & Manipulation]]


## Notes:

Python does not have explicit **spread** (...) or **rest** (...) operators like JavaScript, but it provides equivalent functionality through the **unpacking operators** (* and **) for lists/tuples and dictionaries, respectively. 

---

**Spread Operator Equivalent in Python (* and **)**

## For Lists/Tuples (*)

Python uses the * operator to unpack elements of a list or tuple into another list, function call, or any other context where individual elements are needed.

```python
# Combine lists (like spreading in JavaScript)
list1 = [1, 2, 3]
list2 = [4, 5, 6]
combined = [*list1, *list2]
print(combined)  # [1, 2, 3, 4, 5, 6]

# Pass arguments to a function
def add(a, b, c):
    return a + b + c

nums = [1, 2, 3]
print(add(*nums))  # 6
```

## For Dictionaries (**)

The ** operator is used to unpack key-value pairs from a dictionary.

```python
# Merge dictionaries (like spreading in JavaScript)
dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}
merged = {**dict1, **dict2}
print(merged)  # {'a': 1, 'b': 2, 'c': 3, 'd': 4}
```

---

**Rest Operator Equivalent in Python (* and ** in Function Parameters)**

## For Positional Arguments `*args`:

The * operator collects multiple positional arguments into a single tuple. This is equivalent to JavaScript’s rest operator for arguments.

```python
def sum_all(*args):
    return sum(args)

print(sum_all(1, 2, 3, 4))  # 10
```
### Tags: [[language-basics]]
### References: [[Data Transformation & Manipulation]], [[For Loop]], [[While Loop]], [[Control Statement]], [[Pythonic Iteration]], [[List Comprehensions]], [[Dictionary Comprehension]]

## Notes:

Loops in Python are used to iterate over sequences like lists, tuples, strings, dictionaries, or ranges, much like in TypeScript. While the concept of looping is universal, Python’s syntax and features differ in significant ways.

---
# **Types of Loops in Python**

Python has two main types of loops:

• [[For Loop]]: Iterate over a sequence (similar to for...of or for...in in JavaScript/TypeScript).
```python
for variable in sequence:
    # Code block
```

• [[While Loop]]: Continue as long as a condition is True.
```python
while condition:
    # Code block
```

---
# [[Control Statement]]

## break: 
* Exits the loop entirely.
```python
for i in range(10):
    if i == 5:
        break
    print(i)
```
## continue:
* Skips the rest of the current iteration and moves to the next one.
```python
for i in range(5):
    if i % 2 == 0:
        continue
    print(i)
```
## else Clause in Loops:
* Python allows an else clause with loops, which executes if the loop completes normally (without a break).
```python
for i in range(5):
    print(i)
else:
    print("Loop completed without break.")
```

---
# **Nested Loops**

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i} * {j} = {i * j}")
```

---
# **[[Pythonic Iteration]]**

Python’s for-loops are designed to be more intuitive and less verbose than TypeScript loops. Instead of managing indices explicitly, you work directly with the elements of a sequence.

**In Python, enumerate() provides indices and values:**
```python
fruits = ["apple", "banana", "cherry"]
for i, fruit in enumerate(fruits):
    print(i, fruit)
```

---

1. **Python is sequence-focused**:
• Instead of managing indices explicitly, Python lets you iterate directly over items.
• Use range() for numeric iterations.
• Use enumerate() for indices and items.

2. **Fewer curly braces**:
• Python uses indentation instead of braces for defining blocks, which requires careful attention to spacing.

3. **List/Dictionary comprehensions**:
• These offer a succinct way to filter and transform sequences.

4. **Loop** else **clause**:
• Python’s unique else clause runs when the loop exits naturally.

5. **Flexible sequence iteration**:
• Python loops work naturally with lists, tuples, strings, dictionaries, sets, and more.
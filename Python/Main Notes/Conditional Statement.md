### Tags: [[language-basics]]
### References: 

## Notes:

Conditional statements in Python allow your program to make decisions based on certain conditions. If the condition is True, a specific block of code will execute; otherwise, another block of code may execute. This is analogous to if, else if, and else in JavaScript/TypeScript.

## Syntax of Conditional Statements

## Basic Syntax
```python
if condition:
    # Code to execute if the condition is True
elif another_condition:
    # Code to execute if the previous condition is False but this one is True
else:
    # Code to execute if none of the above conditions are True
```

---
## No switch Statement in Python

Python doesn’t have a built-in switch statement like TypeScript. Instead, you use if-elif-else or, for more complex cases, a dictionary mapping or the match statement (introduced in Python 3.10).

TypeScript:
```TypeScript
const fruit = "apple";

switch (fruit) {
    case "apple":
        console.log("Apple is red.");
        break;
    case "banana":
        console.log("Banana is yellow.");
        break;
    default:
        console.log("Unknown fruit.");
}
```

Python (using if-elif-else):
```Python
fruit = "apple"

if fruit == "apple":
    print("Apple is red.")
elif fruit == "banana":
    print("Banana is yellow.")
else:
    print("Unknown fruit.")
```

Python (using match)
```python
fruit = "apple"

match fruit:
    case "apple":
        print("Apple is red.")
    case "banana":
        print("Banana is yellow.")
    case _:
        print("Unknown fruit.")
```

---
## Nested Conditionals

Python
```python
age = 20
is_student = True

if age < 18:
    if is_student:
        print("You are a minor and a student.")
    else:
        print("You are a minor.")
else:
    print("You are an adult.")
```

Typescript
```typescript
const age = 20;
const isStudent = true;

if (age < 18) {
    if (isStudent) {
        console.log("You are a minor and a student.");
    } else {
        console.log("You are a minor.");
    }
} else {
    console.log("You are an adult.");
}
```

---
## Python supports a more readable version of ternary operator compared to TypeScript

TypeScript
```typescript
const age = 20;
const status = age < 18 ? "minor" : "adult";
console.log(`You are a ${status}.`);
```

Python
```python
age = 20
status = "minor" if age < 18 else "adult"
print(f"You are a {status}.")
```

---
## Short-Circuiting

Python’s and and or operators short-circuit, just like && and || in TypeScript.

Typescript
```typescript
const x = 0;
console.log(x && "Hello");  // 0
console.log(x || "Hello");  // "Hello"
```

Python
```python
x = 0
print(x and "Hello")  # 0
print(x or "Hello")   # "Hello"
```

---
## Common Comparison Operators

| **Operator** | **Python Example** | **TypeScript Example** | **Description**          |
| ------------ | ------------------ | ---------------------- | ------------------------ |
| ==           | x == 10            | x === 10               | Equal to                 |
| != x         | x != 10            | x !== 10               | Not equal to             |
| <            | x < 10             | x < 10                 | Less than                |
| <=           | x <= 10            | x <= 10                | Less than or equal to    |
| >            | x > 10             | x > 10                 | Greater than             |
| >=           | x >= 10            | x >= 10                | Greater than or equal to |
| and          | x > 5 and x > 15   | x < 5 && x > 5         | Logical AND              |
| or           | x < 5 or x > 15    | x < 5 \|\| x > 5       | Logical OR               |
| not          | not x > 10         | !(x > 10)              | Logical NOT              |
|              |                    |                        |                          |

---
## Best Practices for Conditional Statements in Python.

1. Keep Conditions Readable:
* Use parentheses if conditions are complex
```python
if (x > 10 and y < 20) or z == 0:
    print("Condition met")
```

2. Avoid Deep Nesting
* Refactor nested Conditionals using return or break

3. Use Python-Specific Features
* Use in membership checks
* use any() and all() for complex logical conditions
```python
if any([x > 10, y < 20, z == 0]):
    print("At least one condition is True")
```
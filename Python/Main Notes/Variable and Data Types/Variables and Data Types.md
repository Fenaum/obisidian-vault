### Tags: [[datatypes]],  [[language-basics]]
### References: [[List]], [[Dictionary]], [[Tuple]]

## Notes:


# Summary

Python uses dynamic typing by default. You can optionally annotates types

## Variable Declaration

``` Python
x = 5              # No need to declare a type
name: str = "Alice"  # Optional type annotation
is_active = True   # Boolean`
```

## Reassigning Variables

Python variables use mutable by default (unless declared inmutable like tuple)

Example:

```Python
x = 42        # Integer
x = "Hello"   # String
x = [1, 2, 3] # List
```


| Type                 | Python                                                       | JavaScript                                |
| -------------------- | ------------------------------------------------------------ | ----------------------------------------- |
| String               | str                                                          | string                                    |
| Integer              | int                                                          | number (no distinction between int/float) |
| Float                | float                                                        | number                                    |
| Boolean              | bool                                                         | boolean                                   |
| None (Null)          | NoneType                                                     | (None),null/undefined                     |
| [[List]] (Array)     | list                                                         | array                                     |
| [[Dictionary]] (Map) | dict                                                         | object                                    |
| [[Tuple]]            | tuple (immutable),No direct equivalent (use array or object) |                                           |
| [[Set]]              | set                                                          | Set                                       |
|                      |                                                              |                                           |

* **Strings**
	strings are enclosed in single (') or double (") quotes.

* String Operations:
	* Concatenation: name + greeting
	* String interpolation: use f-strings for (more powerful than JS template literals):

``` Python
# Python
message = f"Hello, {name}!"
```

``` Javascript
// JavaScript
let message = `Hello, ${name}!`;
```

* Numbers
	Python distinguishes between integers (int) and floating-point-numbers(float).

```Python
x = 10       # int
y = 3.14     # float
```

* Arithmetic operations behave similarly to Javascript:
* + , - , * , / (Division always returns a float in Python).
* / / (floor division), # (modulo), and ** (exponentiation) are Python-specific.

```Python
result = 5 // 2  # 2 (floor division)
power = 2 ** 3   # 8 (exponentiation)
```

* Booleans
	Booleans in Python use True or False (uppercase) instead of true/false like in Javascript

	Also support logical operations
	and, or, not (instead of &&, ||, ! in JS)

Example:

```Python
if is_active and not is_done:
    print("Still working!")
```

```Javascript
if (isActive && !isDone) {
    console.log("Still working!");
}
```


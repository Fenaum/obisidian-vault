### Tags: [[language-basics]]
### References: [[PEP 8]]

## Notes:


# Summary

Python is **indentation-sensitive** and avoids braces ({}) and semicolons (;);

Example:

`print("Hello, World!")`

* No need for semicolons in Python
* Indentation replaces braces for defining code blocks

### Using Underscores

using underscores _ in variable names (e.g. is_active) is very common in Python and aligns with its [[PEP 8]] style guide, which is the standard coding convention for python. This convention is known as **snake_case .

``` Python
# Python (snake_case)
is_active = True
user_name = "Alice"
total_count = 42
```

## PEP 8 Recommendations

* Variable Names: Use snake_case for variable and function names
``` Python
def calculate_total():
    total_amount = 0
    return total_amount
```
* Constants: Use ALL-CAPS
``` Python
MAX_RETRIES = 5
```

## Should You Always Use  Snake Case in Python?

It's best to stick to snake_case for consistency with the exceptions of:

* For class names, use PascalCase (e.g., MyClass)

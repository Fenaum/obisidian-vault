### References: [[Syntax]]

## Notes:

### Python supports a more readable version of ternary operator compared to TypeScript

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
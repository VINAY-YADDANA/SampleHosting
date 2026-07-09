# Add Two Numbers

This branch implements a simple function that adds two numbers together.

## Purpose
The goal is to provide a clear, minimal example of a utility function that takes two numeric arguments and returns their sum. This can serve as a reference implementation for basic arithmetic operations in the project.

## Usage Example
```python
def add_two_numbers(a, b):
    return a + b

# Example usage
result = add_two_numbers(3, 5)
print(result)  # Output: 8
```

You can import the function from its module (e.g., `utils.py`) and call it wherever needed.

## Notes
- The function works with any types that support the `+` operator (e.g., integers, floats, and custom numeric types).
- No error handling is included; callers should ensure that both arguments are appropriate numeric values.
- This implementation is intentionally straightforward to demonstrate basic function definition and documentation practices.
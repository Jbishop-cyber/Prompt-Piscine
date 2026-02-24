# Objective

## Use role-based prompts for personalized feedback.

### Step 1: Write a python function with a bug

```py
Code:

def divide_numbers(a, b):
    result = a / b
    return result

print(divide_numbers(10, 0))

Output:

ZeroDivisionError: division by zero
```

### Step 2: Act as a coding mentor

```
Prompt:

Act as a mentor reviewing this code. Provide corrections and explain improvements.
```

- **Feedback:**

The function works correctly for normal inputs, but it does not handle division by zero.

**When you call:**

print(divide_numbers(10, 0))

Python will raise a ZeroDivisionError, and the program will crash.

- So the correct code would be

```py
Code:
def divide_numbers(a, b):
    if b == 0:
        return "Error: Division by zero is not allowed."
    return a / b

print(divide_numbers(10, 0))

Output:
Error: Division by zero is not allowed.
```

This code is better because it prevents the program from crashing, it handles an important edge case and it makes the function safer and more predictable.

- **Mentorship advice:**
    
When writing functions:
```
Always think about edge cases (zero, negative numbers, wrong data types).

Ask yourself: “What inputs could break this?”

Defensive programming makes your code more reliable.
```

### Step 4: Review the response

The tone is more educational, it explained what was wrong, the consequences and suggested improvements rather than just fixing the code. It also introduce me to a new principle, that is handling edge cases.

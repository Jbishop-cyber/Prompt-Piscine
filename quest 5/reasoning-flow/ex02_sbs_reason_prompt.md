# Objective

## Use structured prompting to encourage reasoning.

### Step 1: Choose a math problem

```
Problem:

Calculate the factorial of 7
```

### Step 2: Prompting the model

- Prompt 1 (without reasoning):
```
What is 7 factorial?

Output:

The value of 7 factorial (written as 7!) is 5,040.
```

- Prompt 2 (with reasoning):
```
Let’s think step by step before answering. What is 7 factorial?

Output:

Factorial means multiplying a number by all positive integers below it.

To find 7 factorial (written as 7!), we multiply all positive integers from 7 down to 1.

Start with 7 times 6: 7 × 6 = 42

Multiply the result by 5: 42 × 5   = 210

Multiply the result by 4: 210 × 4 = 840

Multiply the result by 3: 840 × 3 = 2,520

Multiply the result by 2: 2,520 × 2 = 5,040

Multiply the result by 1: 5,040 × 1 = 5,040

So, 7! = 5,040.
```

### Step 3: Comparing results (With and without reasoning)

Without reasoning instruction, the model provided only the final answer, it is faster but doesn't show workings. But with reasoning instruction, the model first defined what a factorial is, showed each multiplication step by step, thereby making it easier to understand. 

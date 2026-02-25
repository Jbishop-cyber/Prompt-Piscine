# Objective

## Guide the model to solve a problem with explicit reasoning.

### Step 1: Write a logic puzzle
```
Rita is 7 years old.
Five years ago, Johnathan was twice Rita’s age at that time.
How old is Johnathan now?
```

### Step 2: Prompting the model

```
Step 1: Rita’s Current Age

Rita is 7 years old.

Step 2: Rita’s Age Five Years Ago

7 − 5 = 2 years old.

So five years ago, Rita was 2.

Step 3: Johnathan’s Age Five Years Ago

We are told:

Johnathan was twice Rita’s age at that time.

Twice 2 = 4.

So five years ago, Johnathan was 4 years old.

Step 4: Johnathan’s Current Age

If five years ago he was 4:

4 + 5 = 9.

Final Answer:

Johnathan is 9 years old.
```

### Step 3: Verification
The model did provide a very clear step-by-step explanation before presenting the final answer.  It started by stating rita's current age, then proceed to calculate Rita's age five years ago, then determined Johnathan's age at that time. After that, it proceeded to add five five years to find Johnathan's current age. The reasoning was explicit and it forces algebraic reasoning, so the final answer 9 is correct. 

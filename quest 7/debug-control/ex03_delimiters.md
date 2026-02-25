# Objective

## Restrict responses to a specific block of text.

### Step 1: Write a prompt without using delimiters

```py
Prompt:

Python, C++ and java, the sun is hot, Kelvin is a boy
```
```py
Output:

Looks like you’re tossing out a mix of programming languages, facts, and a name!
```

### Step 2: Write a prompt with delimiters

```py
Prompt:

Answer using only the text

###
Python, C++ and java, the sun is hot, Kelvin is a boy
###

Question: List the programming language
```
```py
Output:

Python, C++, java
```

### Step 3: Comparing the output

The difference is clear, without delimiters, the model treated the entire input as a whole sentence that mixed unrelated statements together and as a result it responded with a vague answer, whereas with the delimiters the model followed the instruction and extract out only the programming languages. This shows that delimiters helps to focus the model's attention on the most important text, thereby improving accuracy and reducing irrelevant responses.

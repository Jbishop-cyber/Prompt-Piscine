# Overview

This quest focuses solely on using language model with external tools such as calculator, search system and APIs. It also introduces the basics of function calling for structured responses in a way that is machine readable.

# Learning Objectives

By completing this quest, I should be able to:

**Understand prompt chaining and tool use:**

To break down a user's query into different steps, to ensure that the model understands the intent first, before stimulating a calling tool (like a weather API), then formatting the response to language that the use understands.

**Design prompts that request structured JSON output:**

To enforce a consistent, machine-readable response by properly defining a clear JSON schema and the type of data it needs in the prompts. 

**Simulate API calls with controlled prompts:**

To write prompts that can mimic how a real API should respond, to ensure a desired structure and thereby preventing unnecessary explanations.

**Combine multiple prompts to mimic simple agent flows:**

To link prompts together, so that the model can behave like an agent that is capable of receiving an input, call a tool (in this case the weather API) and can as well return a properly formatted output.

```
Note:

A clear structure and a well defined JSON schema can help to transform a very simple text to a controlled system.

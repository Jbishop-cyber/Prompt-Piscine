# Objective

## Understand how parameters affect output diversity.

- Use the same prompt with temperature = 0.2 and then with temperature = 0.9.

- Repeat with different top-p values (e.g., 0.5 vs 1).

- Prompt:
```
Talk to me about inflation
```
### Test 1: Temperature = 0.2, Top-p = 1

- Response:

Inflation is the sustained rise in the general price level of goods and services over time. It reduces purchasing power, meaning each unit of currency buys fewer goods and services. Inflation can result from increased demand, higher production costs, or expansionary monetary policy. Central banks monitor inflation to maintain economic stability.

### Test 2: Temperature = 0.9, Top-p = 1

- Response:

Inflation is like watching your money slowly fade in strength. One year your paycheck feels solid; the next, it stretches thinner across rent, groceries, and fuel. It’s not just one price jumping. It’s the quiet, steady climb of many prices at once, reshaping how people budget, save, and even dream about the future.

### Test 3: Temperature = 0.2, Top-p = 0.5

- Response:

Inflation is a sustained increase in the general price level of goods and services. As inflation rises, purchasing power declines, meaning money buys fewer goods over time. It affects everyday expenses such as food, housing, and transportation. Governments use monetary policy to manage inflation and maintain economic stability.

### Test 4: Temperature = 0.9, Top-p = 0.5

- Response:

Inflation is the steady rise in prices that slowly reduces the value of money. Over time, the same income covers fewer goods and services. It influences daily costs and changes how households plan spending and saving. While it is a normal part of economic cycles, excessive inflation can create instability.

## Record how the style, randomness, and focus of responses change.

### Style change:

- Low temperature (0.2) produce a formal, textbook style and more academic definition.

- High temperature (0.9) produce a more expressive, imaginative and metaphoric narrative, it becomes less academic compared to low temperature.

- When both temperature was paired with top-p 0.5, even high temperatures definition became less expressive.

### Randomness changes:
- Low temperature (0.2) resulted in a structured sentence patterns.

- High temperature (0.9) increased the range in the words and sentence rhythm.

- Lowering top-p reduced the overall randomness overall by reducing the range of vocabulary choices.

### Focus of response:
-  All low temperature (0.2) response remained formal, structured and focused on textbook like definitions.

- High temperature (0.9) with top-p = 1 is more expressive and less academic, it even expanded into a more broader narrative by talking about the effect on budgeting, savings and dreams about the future.

- High temperature (0.9) with top-p = 0.5 response is a bit more fluid but still controlled, due to the restriction the top-p provides.

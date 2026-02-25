## Step 1: Ask for a user query

```
Prompt:

What is the temperature in Tokyo today?
```
```
Output:

The temperature in Tokyo today, February 23, 2026, is approximately 20°C (68°F)
```

## Step 2: Simulate a call to the weather API

```
Prompt:

Simulate a weather API response for Tokyo today.

Return only valid JSON:

{
  "location": string,
  "temperature_celsius": number,
  "condition": string
}
```

```json
Output:

{
  "location": "Tokyo, Japan",
  "temperature_celsius": 20,
  "condition": "Clear/Mostly Sunny"
}
```

## Step 3: Format the final answer back to the user

```
Prompt

Reformat the JSON into a readable answer
```

```
Output:

In Tokyo, Japan, it is currently an unseasonably warm 20°C with clear skies today.
```

### Step 4: Document the chained process and outputs

In step one, the model receives a user query in a normal language, the model's focus is to identify what the user wants and get the accurate information.

In step two, the agent then converts this regular language into a structured machine readable language, by stimulating the weather API through an enforced JSON schema.

In step three, the structured JSON response is then reformatted back into a user readable answer. 

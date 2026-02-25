# Objective

## Extract structured data from unstructured input.

### Step 1: Choose an unstructured text:
```
Text:

John Doe, age 29, lives in Paris with his wife Jane Doe, age 27. Both of them work as software engineers.
```

### Step 2: Create a template prompt

- Prompt 1 (weak prompt):

What information can you extract from this text:
```
Text:

John Doe, age 29, lives in Paris with his wife Jane Doe, age 27. Both of them work as software engineers.
```
```
Output:

The text mentions John Doe, who is 29 years old and lives in Paris with his wife Jane Doe, who is 27 years old. Both of them work as software engineers.
```

- Prompt 2 (Strong Prompt):

Extract the following fields from the text: Name, Age, Relationship, Location, Occupation. Return the output in JSON format.
```
Text:

John Doe, age 29, lives in Paris with his wife Jane Doe, age 27. Both of them work as software engineers.
```
```json
Output:

[
  {
    "Name": "John Doe",
    "Age": 29,
    "Relationship": "Husband",
    "Location": "Paris",
    "Occupation": "Software engineer"
  },
  {
    "Name": "Jane Doe",
    "Age": 27,
    "Relationship": "Wife",
    "Location": "Paris",
    "Occupation": "Software engineer"
  }
]
```

### Step 3: Testing with multiple inputs

#### Input 1:

- Weak prompt:

What information can you extract from this text?
```
Text

Maria Lopez, 41, lives in Madrid with her partner Carlos Lopez, 45. Maria is a financial analyst and Carlos is an architect
```
```
Output:

The text mentions Maria Lopez, who is 41 years old and lives in Paris with her husband Carloz Lopez, who is 45 years old. Maria works as a financial analyst, while Carlos works as an architect.
```

- Strong prompt:

Extract the following fields from the text: Name, Age, Relationship, Location, Occupation. Return the output in JSON format.
```
Text:

Maria Lopez, 41, lives in Madrid with her partner Carlos Lopez, 45. Maria is a financial analyst and Carlos is an architect
```
```json
Output:

[
  {
    "Name": "Maria Lopez",
    "Age": 41,
    "Relationship": "Partner",
    "Location": "Madrid",
    "Occupation": "Financial analyst"
  },
  {
    "Name": "Carlos Lopez",
    "Age": 45,
    "Relationship": "Partner",
    "Location": "Madrid",
    "Occupation": "Architect"
  }
]
```

#### Input 2:

- Weak prompt:

What information can you extract from this text?
```
Text:

Alice Smith, 35, lives in New York with her husband Bob Smith, 37. Alice is a project manager, and Bob is a data scientist.
```
```
Output:

The text mentions Alice Smith, who is 35 years old and lives in New York with her husband Bob Smith, who is 37 years old. Maria works as a project manager, while Carlos works as an data scientist.
```

- Strong prompt:

Extract the following fields from the text: Name, Age, Relationship, Location, Occupation. Return the output in JSON format.
```
Text:

Alice Smith, 35, lives in New York with her husband Bob Smith, 37. Alice is a project manager, and Bob is a data scientist.
```
```json
Output:

[
  {
    "Name": "Alice Smith",
    "Age": 35,
    "Relationship": "Husband",
    "Location": "New York",
    "Occupation": "Project manager"
  },
  {
    "Name": "Bob Smith",
    "Age": 37,
    "Relationship": "Wife",
    "Location": "New York",
    "Occupation": "Data scientist"
  }
]
```

### Validation Check:

The output clearly separates each individual into the right field, the relationship field clearly shows the connection between the two people, the JSON output format makes the file ready for automation. This same prompts can also work for multiple inputs and still maintain the same output format. 

# Objective

## Create prompts that produce structured machine-readable output

### Step 1: Unstructured prompt:

```
Prompt:

List four footballers, their clubs and age
```
```
Output:

Lionel Messi: 38 years old (born June 24, 1987), playing for Inter Miami CF.

Cristiano Ronaldo: 41 years old (born February 5, 1985), playing for Al-Nassr FC.

Kylian Mbappé: 27 years old (born December 20, 1998), playing for Real Madrid CF.

Erling Haaland: 25 years old (born July 21, 2000), playing for Manchester City F.C. 
```

### Step 2: Structured prompt (only JSON):

```
Prompt:

List four footballers and their clubs. Return only valid JSON in this format:[{name:string,club:string,age:number}]
```
```json
Output:

[
  {
    "name": "Lionel Messi",
    "club": "Inter Miami CF",
    "age": 38
  },
  {
    "name": "Cristiano Ronaldo",
    "club": "Al Nassr",
    "age": 41
  },
  {
    "name": "Kylian Mbappé",
    "club": "Real Madrid",
    "age": 27
  },
  {
    "name": "Erling Haaland",
    "club": "Manchester City",
    "age": 25
  }
]
```

### Step 3: Test with multiple inputs:

- Input 1:

```
Prompt:

List five states in Nigeria, Governors name and age along with their population
```
```
Output:
- Lagos State
Governor: Babajide Sanwo-Olu
Governor's Age: 60 years old (Born June 25, 1965)
Population: Estimated at 22 million to 24 million. Lagos remains the most populous state, driven by intense urbanisation and migration.

- Kano State
Governor: Abba Kabir Yusuf
Governor's Age: 63 years old (Born January 5, 1963)
Population: Estimated at 16.2 million to 18 million. It is the most populous state in Northern Nigeria.

- Rivers State
Governor: Siminalayi Fubara
Governor's Age: 51 years old (Born January 28, 1975)
Population: Estimated at 9.8 million to 10.5 million. Rivers is a major economic hub and the 4th most populous state in Nigeria.

- Kaduna State
Governor: Uba Sani
Governor's Age: 54 years old (Born December 31, 1970)
Population: Estimated at 8.3 million to 10.2 million. Kaduna serves as the central administrative hub for the Northwest region.

- Oyo State
Governor: Seyi Makinde
Governor's Age: 58 years old (Born December 25, 1967)
Population: Estimated at 7.5 million to 9.2 million. Its capital, Ibadan, is one of the largest cities in Africa by land area.
```
```
Prompt:

List five states in Nigeria, Governors name and age along with their population. Return only valid JSON in this format:[{name:string,age:number,state:string,population:number}]
```

```json
Output:

[
  {
    "name": "Babajide Sanwo-Olu",
    "age": 60,
    "state": "Lagos",
    "population": 22000000
  },
  {
    "name": "Abba Kabir Yusuf",
    "age": 63,
    "state": "Kano",
    "population": 16200000
  },
  {
    "name": "Siminalayi Fubara",
    "age": 51,
    "state": "Rivers",
    "population": 9800000
  },
  {
    "name": "Uba Sani",
    "age": 55,
    "state": "Kaduna",
    "population": 8300000
  },
  {
    "name": "Seyi Makinde",
    "age": 58,
    "state": "Oyo",
    "population": 7500000
  }
]
```

- Input 2:

```
Prompt:

List three countries, their tourist spots and the number of tourist visit they get
```
```
Output:

- France
2025 Visitors: 102 million (a record high).
Tourist Spots: The Eiffel Tower, the Louvre Museum, Notre-Dame de Paris (which recently reopened), the French Riviera, and the Alps.

- Spain
2025 Visitors: 97 million (a new all-time record).
Tourist Spots: Barcelona (Sagrada Família), the Balearic Islands (Ibiza and Mallorca), the Canary Islands, and historic cities like Seville and Madrid.

- United States
2025 Visitors: Estimated between 67.9 million and 77.1 million (reports indicate a slight decline in 2025 arrivals compared to previous years).
Tourist Spots: New York City (Times Square, Statue of Liberty), Grand Canyon National Park, Walt Disney World in Orlando, and California (Los Angeles and San Francisco).
```
```

Prompt:

List three countries, their tourist spots and the number of tourist visit they get. Return only valid JSON in this format:[{country:string,visitors:number,tourist_spot:string}]
```

```json
Output:

[
  {
    "country": "France",
    "visitors": 102000000,
    "tourist_spot": "Eiffel Tower"
  },
  {
    "country": "Spain",
    "visitors": 97000000,
    "tourist_spot": "Sagrada Família"
  },
  {
    "country": "United States",
    "visitors": 77100000,
    "tourist_spot": "Grand Canyon"
  }
]
```

### Step 4: Verifying the output:

The output in the JSON format did not change but rather, it remained consistent across multiple inputs, although I did notice during the JSON output for the footballers, when I changed [{club:string}] to [{club:number}], it returned their Jersey number instead of the club they play for. This shows that a model can adjust it's response to match a new data type, therefore how you structure the data type in the prompt can directly influence the output.

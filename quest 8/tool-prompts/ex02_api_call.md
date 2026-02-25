# Objective

## Practice designing prompts that mimic function calls.

### Step 1: Basic prompt:

```
Prompt:

Simulate a weather response for Lagos today
```
```
Output:
For Friday, February 20, 2026, the weather in Lagos
is expected to be partly cloudy and hot, with a slight chance of morning showers and afternoon thundery outbreaks.
```

### Step 2: Basic API prompt:

```
Prompt:

Simulate a weather API response for Lagos today.
```

```json
Output:

{
  "location": {
    "name": "Lagos",
    "region": "Lagos State",
    "country": "Nigeria",
    "lat": 6.4541,
    "lon": 3.3947,
    "timezone_id": "Africa/Lagos",
    "localtime_epoch": 1771597800,
    "localtime": "2026-02-20 14:30"
  },
  "current": {
    "last_updated_epoch": 1771597200,
    "last_updated": "2026-02-20 14:20",
    "temp_c": 32.0,
    "feelslike_c": 37.5,
    "condition": {
      "text": "Partly cloudy",
      "icon": "//://cdn.weatherapi.com",
      "code": 1003
    },
    "wind_mph": 6.7,
    "wind_kph": 10.8,
    "wind_degree": 210,
    "wind_dir": "SSW",
    "pressure_mb": 1011.0,
    "precip_mm": 0.0,
    "humidity": 65,
    "cloud": 40,
    "uv": 9.0,
    "visibility_km": 10.0
  }
}
```

### Step 3: Define an expected JSON schema

```
Prompt:

Simulate a weather API response for Lagos today.Return only valid JSON in the following format:{ "location": string, "temperature_celsius": number, "condition": string}
```

```json
Output:
{

"location": "Lagos, Nigeria",
"temperature_celsius": 33,
"condition": "partly sunny"
} 
```

### Step 4: Test the model with different cities

- Input 1:

```
Prompt:

Simulate a weather API response for Ottawa today. Return the same JSON schema
```

```json
Output:
{

"location": "Ottawa, Canada",
"temperature_celsius": -4,
"condition": "Light Snow"
}
```

- Input 2

```
Prompt:

Simulate a weather API response for Tokyo today. Return the same JSON schema
```

```json
Output:
{

"location": "Tokyo, Japan",
"temperature_celsius": 12,
"condition": "Clear Sky"
}
```

- Input 3
```
Prompt:

Simulate a weather API response for Barcelona today. Return the same JSON schema
```

```json
Output:
{

"location": "Barcelona, Spain",
"temperature_celsius": 16,
"condition": "Cloudy"
} 
```

### Step 5: Comparing outputs

When I asked it to stimulate the weather report using API, it automatically responded with a JSON input. This is because of the phrase "a weather API response" which implied that I wanted it in a format that is machine readable, and most models usually associate API's with a well structured data (typically JSON). So I had to define the JSON schema (which acts like a gatekeeper to ensure that the incoming and outgoing data follows a specific rule) to get the kind of output I want. Despite all these, after testing for various cities, the structure remained the same and only the values (i.e the location, temperature_Celsius and condition) changed.

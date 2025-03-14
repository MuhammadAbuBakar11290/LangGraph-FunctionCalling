# Day 3 - Function Calling with the Gemini API

This notebook is part of the Kaggle 5-day Generative AI course, focusing on using the Gemini API for function calling. It demonstrates how to interact with the Gemini model to extract structured information and invoke functions dynamically.

## Table of Contents
1. [Introduction](#introduction)
2. [Setting Up the Gemini API](#setting-up-the-gemini-api)
3. [Defining Function Calls](#defining-function-calls)
4. [Executing Function Calls](#executing-function-calls)
5. [Handling Multiple Functions](#handling-multiple-functions)
6. [Conclusion](#conclusion)

## Introduction
This notebook explores function calling capabilities within the Gemini API, allowing the model to execute structured tasks dynamically. By defining and invoking functions, the model can integrate with external services and automate complex workflows.

## Setting Up the Gemini API
The notebook initializes the Gemini API and sets up the required environment. Authentication and API key configurations are handled to ensure smooth interaction with the model.

## Defining Function Calls
A structured function definition is created, specifying the function name, input parameters, and expected outputs. This allows the Gemini model to understand and execute tasks accurately.

```python
function_schema = {
    "name": "get_weather",
    "parameters": {
        "location": "string",
        "unit": "string"
    },
    "description": "Fetches weather information for a given location."
}
```

## Executing Function Calls
The Gemini model is prompted to recognize when a function call is needed. Upon detection, it extracts relevant information and invokes the corresponding function.

```python
def get_weather(location, unit):
    # Simulated weather data retrieval
    return {"temperature": "25C", "condition": "Sunny"}
```

## Handling Multiple Functions
The notebook extends the concept by managing multiple function calls within a single interaction. This enables the model to execute diverse operations based on user queries.

```python
functions = [get_weather, another_function]
response = model.call_function(user_input, functions)
```

## Conclusion
This notebook provides a hands-on guide to leveraging function calling within the Gemini API. By integrating function execution into AI workflows, developers can build more interactive and automated systems.


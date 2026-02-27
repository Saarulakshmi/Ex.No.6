# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date: 27/02/2026
# Register no: 212223050040
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

# AI Tools Required:
- ChatGPT  
- Google Gemini  
- Claude (Anthropic)  

# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 

## Selected Application Domain:

Smart Manufacturing – Predictive Maintenance Data Analysis  

The system collects machinery performance data from two monitoring APIs and compares results to generate maintenance recommendations.

# PROMPT DESIGN AND EXECUTION

## Stage 1: Prompt for Generating Python Code to Interact with Multiple APIs

### Designed Prompt:

Act as a professional Python developer.  
Write Python code that fetches data from two REST APIs (API 1 and API 2), parses JSON responses, and stores key metrics such as temperature, vibration, and machine status. Include proper error handling and comments.

### AI-Generated Response (Sample Code)

```python
import requests

def fetch_api_data(url):
    try:
        response = requests.get(url)
        response.raise_for_status()
        return response.json()
    except requests.exceptions.RequestException as e:
        print("Error fetching data:", e)
        return None

api1_url = "https://api1.example.com/machine"
api2_url = "https://api2.example.com/machine"

data1 = fetch_api_data(api1_url)
data2 = fetch_api_data(api2_url)

if data1:
    print("API 1 Data:", data1)

if data2:
    print("API 2 Data:", data2)
```

## Stage 2: Prompt for Comparing Outputs

### Designed Prompt:

Compare the outputs received from API 1 and API 2. Highlight differences in temperature, vibration levels, and machine status clearly.

### AI-Generated Response (Comparison Code)

```python
def compare_data(d1, d2):
    comparison = {
        "temperature_difference": d1["temperature"] - d2["temperature"],
        "vibration_difference": d1["vibration"] - d2["vibration"],
        "status_match": d1["status"] == d2["status"]
    }
    return comparison

if data1 and data2:
    result = compare_data(data1, data2)
    print("Comparison Result:", result)
```

## Stage 3: Prompt for Generating Actionable Insights

### Designed Prompt:

Based on the comparison results, suggest actionable maintenance recommendations if temperature or vibration exceeds safe thresholds.

### AI-Generated Response (Insight Code)

```python
def generate_insights(comparison):
    if abs(comparison["temperature_difference"]) > 10:
        print("Warning: Significant temperature variation detected.")
    if abs(comparison["vibration_difference"]) > 5:
        print("Alert: Vibration levels require inspection.")
    if not comparison["status_match"]:
        print("Machine status mismatch detected. Immediate review required.")

if data1 and data2:
    insights = compare_data(data1, data2)
    generate_insights(insights)
```

# ANALYSIS OF MULTIPLE AI TOOLS

| Criteria | ChatGPT | Gemini | Claude |
|----------|----------|----------|----------|
| Code Structure | Well structured | Moderate | Detailed |
| Error Handling | Included | Basic | Included |
| Code Comments | Clear | Limited | Detailed |
| Practical Relevance | High | Moderate | High |

### Observations:

- Structured prompts resulted in better organized and modular code.
- ChatGPT provided balanced structure and clarity.
- Gemini produced simpler but functional code.
- Claude gave detailed explanations but slightly longer outputs.
- Prompt refinement improved overall output quality across all tools.

# REFLECTION NOTE

The experiment demonstrates that prompt clarity directly influences AI-generated code quality. When prompts included:

- Role specification (Professional Python Developer)
- Clear task breakdown
- Output expectations
- Error handling requirements

The generated responses were significantly more structured and practical.

Future improvements may include:
- Adding API authentication (API keys or tokens)
- Defining threshold values explicitly
- Requesting unit test cases
- Specifying logging instead of print statements

# Conclusion:

Structured and role-based prompts significantly enhance AI-assisted coding performance. Comparing outputs across multiple AI tools shows that prompt clarity improves accuracy, modularity, and actionable insights.

# Result: 
The corresponding Prompt is executed successfully.

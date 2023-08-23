# API for Creating CSV and JSON Files

This is a documentation for an API that allows you to create CSV and JSON files. The API provides endpoints to generate both CSV and JSON files containing data that you can specify. It's a simple way to export data in these popular formats for further analysis, sharing, or integration with other systems.

## Base URL
The base URL for accessing the API is: `https://example.com/api`

## Endpoints

### 1. Create CSV File

#### Endpoint
```
POST /create-csv
```

#### Request Parameters
- `data`: JSON object containing the data you want to include in the CSV file.

#### Response
- Status: 200 OK
- Content: The generated CSV file.

#### Example
```shell
curl -X POST -H "Content-Type: application/json" -d '{"data": [{"name": "Alice", "age": 25}, {"name": "Bob", "age": 30}]}' https://example.com/api/create-csv > data.csv
```

### 2. Create JSON File

#### Endpoint
```
POST /create-json
```

#### Request Parameters
- `data`: JSON object containing the data you want to include in the JSON file.

#### Response
- Status: 200 OK
- Content: The generated JSON file.

#### Example
```shell
curl -X POST -H "Content-Type: application/json" -d '{"data": [{"name": "Alice", "age": 25}, {"name": "Bob", "age": 30}]}' https://example.com/api/create-json > data.json
```

## Usage Notes
- The API expects a POST request for both endpoints.
- Provide the data you want to include in the file in the `data` parameter as a JSON object.
- The generated file will be returned as the response content.
- You can then save the response to a file on your local system using standard command-line tools like `curl` or programming libraries.

## Example Use Case
Let's say you have a list of user information, and you want to export it in both CSV and JSON formats. You can use this API to create both files programmatically, which is particularly useful for automation.

### CSV Creation
```python
import requests

data = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30}
]

response = requests.post("https://example.com/api/create-csv", json={"data": data})
with open("data.csv", "wb") as file:
    file.write(response.content)
```

### JSON Creation
```python
import requests

data = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30}
]

response = requests.post("https://example.com/api/create-json", json={"data": data})
with open("data.json", "wb") as file:
    file.write(response.content)
```

This API simplifies the process of generating CSV and JSON files, making it easy to export and manage your data in these common formats.


### **Authors**
--- 

![GitHub Contributors Image](https://contrib.rocks/image?repo=RM92023/holbertonschool-low_level_programming)
Robinson Muñetón Jaramillo - <a href="https://github.com/RM92023" target="_blank"> @RM92023</a> ![Your Repository's Stats](https://github-readme-stats.vercel.app/api?username=RM92023&show_icons=true)
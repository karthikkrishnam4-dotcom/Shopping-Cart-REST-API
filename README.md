# Shopping Cart REST API

A simple Shopping Cart application built using Python Flask and HTML. This project demonstrates how to create API routes, add products to a cart, and delete products using HTTP methods.

## Features

- Add products to the shopping cart
- Delete products from the cart
- Display cart items on an HTML page
- Create REST API endpoints using Flask
- Handle HTTP requests and JSON responses
- Use HTML forms without JavaScript

## Technologies Used

- Python
- Flask
- REST API
- HTML
- Git and GitHub

## Project Structure

```text
API_Practice/
│
├── templates/
│   └── index.html
│
├── apicall.py
├── requirements.txt
└── README.md
```

## Installation

**1. Clone the repository**

```bash
git clone https://github.com/karthikkrishnam4-dotcom/Shopping-Cart-REST-API.git
```

**2. Navigate to the project folder**

```bash
cd Shopping-Cart-REST-API
```

**3. Install dependencies**

```bash
pip install flask requests
```

## Run the Application

Start the Flask application:

```bash
python apicall.py
```

Open your browser and visit:

http://127.0.0.1:5000/

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Display the shopping cart page |
| POST | `/api/add` | Add a product to the cart |
| DELETE | `/api/delete/<product_name>` | Delete a product by name |

## Example API Request

Add a product using Python:

```python
import requests

url = "http://127.0.0.1:5000/api/add"

response = requests.post(
    url,
    json={"name": "Laptop"}
)

print(response.status_code)
print(response.json())
```

Delete a product using Python:

```python
import requests

url = "http://127.0.0.1:5000/api/delete/Laptop"

response = requests.delete(url)

print(response.status_code)
print(response.json())
```

**Note:** The API routes must support the request formats shown above. The cart is currently stored in memory, so products are cleared when the Flask server restarts.

## Learning Objectives

- Understand Flask routing
- Learn REST API fundamentals
- Practise GET, POST, and DELETE requests
- Connect HTML forms with a Python backend
- Learn how to test API endpoints

## Author

Karthik Krishna

GitHub: https://github.com/karthikkrishnam4-dotcom

---

This project was created for learning and practising Python Flask and REST API development.
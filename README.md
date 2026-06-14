# 🚀 100 Days of Python API Challenge

Build one API every day and gradually move from beginner to advanced topics.

This challenge covers:
- REST APIs
- Databases
- Authentication
- Caching
- External APIs
- AI APIs
- Real-time systems
- Microservices

---

# 🚀  Temperature Converter API 

A simple REST API built with **FastAPI** that converts temperatures between **Celsius**, **Fahrenheit**, and **Kelvin**.

---

## 📚 What I Learned

* ✅ Query parameters
* ✅ Mathematical calculations
* ✅ Returning JSON responses
* ✅ Input validation
* ✅ API documentation with Swagger UI
* ✅ Working with multiple temperature units

---

## 📁 Project Structure

```
temperature_converter_api/
│
├── app.py
├── requirements.txt
```

---

## ⚙️ Installation

### 1. Create Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### 2. Install Dependencies

```bash
pip install fastapi uvicorn
```

---

## ▶️ Run the API

```bash
uvicorn app:app --reload
```

Server runs at:

```
http://127.0.0.1:8000
```

---

## 🏠 Home Endpoint

### Request

```
GET /
```

### Response

```json
{
  "message": "Welcome to Temperature Converter API"
}
```

---

## 🌡️ Temperature Conversion Endpoint

### Request

```
GET /convert
```

### Query Parameters

| Parameter   | Type   | Description                               |
| ----------- | ------ | ----------------------------------------- |
| temperature | float  | Temperature value                         |
| from_unit   | string | Source unit (celsius, fahrenheit, kelvin) |
| to_unit     | string | Target unit (celsius, fahrenheit, kelvin) |

---

## Example Requests

### Celsius → Fahrenheit

```
GET /convert?temperature=100&from_unit=celsius&to_unit=fahrenheit
```

Response:

```json
{
  "input_temperature": 100,
  "from_unit": "celsius",
  "to_unit": "fahrenheit",
  "converted_temperature": 212
}
```

---

### Fahrenheit → Celsius

```
GET /convert?temperature=98.6&from_unit=fahrenheit&to_unit=celsius
```

Response:

```json
{
  "input_temperature": 98.6,
  "from_unit": "fahrenheit",
  "to_unit": "celsius",
  "converted_temperature": 37
}
```

---

### Kelvin → Celsius

```
GET /convert?temperature=300&from_unit=kelvin&to_unit=celsius
```

Response:

```json
{
  "input_temperature": 300,
  "from_unit": "kelvin",
  "to_unit": "celsius",
  "converted_temperature": 26.85
}
```

---

## 📖 Interactive API Documentation

FastAPI automatically generates Swagger UI.

Open:

```
http://127.0.0.1:8000/docs
```

You can test all endpoints directly from your browser.

---

## 🛠 Built With

* Python
* FastAPI
* Uvicorn



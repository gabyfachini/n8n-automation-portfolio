# Fake Data Generator API (n8n)

Simple API for generating **random fake data** using **n8n**.

The workflow receives an HTTP request and returns a user with **random name, city, and age**.

---

# Features

* Random fake data generation
* JSON response format
* Simple endpoint using Webhooks

---

# Technologies Used

* n8n
* Webhooks
* JavaScript

---

# Endpoint

### Generate Fake Data

```http
GET /webhook/fake-user
```

---

# Example Response

```json
{
  "name": "Marina",
  "city": "Curitiba",
  "age": 29
}
```

Each request generates **a different set of data**.

---

# Workflow Structure

The workflow has three main nodes:

```text
Webhook
   ↓
Code (JavaScript)
   ↓
Respond to Webhook
```

### Webhook

Receives the HTTP request.

### Code Node

Generates random data using JavaScript.

### Respond to Webhook

Returns the generated JSON to whoever called the API.

---

# Testing the API

You can test the API using **Postman**, **curl**, or a browser.

---

# Importing into n8n

1. Download the `workflow.json` file
2. Open **n8n**
3. Click **Import Workflow**
4. Select the workflow file

---

# Possible Improvements

* Add last name
* Add fake email
* Generate multiple users
* Generate company data

---

# Project Purpose

This project was created to study **automation and API development using n8n**.

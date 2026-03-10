# Visit Counter API (n8n)

Simple API that counts how many times an endpoint has been accessed, built using **n8n** and **Webhooks**.

Each request increments a counter stored in the **workflow Static Data**, allowing you to track the total number of visits.

---

# Features

* Count accesses to an endpoint
* Store data using **Workflow Static Data**
* Return the total number of visits
* Create a simple API endpoint

---

# Technologies Used

* n8n
* Webhooks
* JavaScript
* REST API

---

# Endpoint

### Count Visit

```http
GET /webhook/visit
```

Each call to this endpoint **increments the visit counter**.

---

# Example Response

First request:

```json
{
  "visits": 1
}
```

Second request:

```json
{
  "visits": 2
}
```

Fifteenth request:

```json
{
  "visits": 15
}
```

---

# Workflow Structure

The workflow contains three main nodes:

```
Webhook
   ↓
Code (JavaScript)
   ↓
Respond to Webhook
```

### Webhook

Receives the HTTP request.

### Code Node

Updates the counter stored in the workflow **Static Data**.

### Respond to Webhook

Returns the total number of visits.

---

# Testing the API

You can test it using **Postman**, **curl**, or a browser.

### URL (test mode)

```
GET http://localhost:5678/webhook-test/visit
```

### URL (active workflow)

```
GET http://localhost:5678/webhook/visit
```

### Example using curl

```bash
curl http://localhost:5678/webhook-test/visit
```

---

# Import into n8n

1. Download the `workflow.json` file
2. Open **n8n**
3. Click **Import Workflow**
4. Select the file

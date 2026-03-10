# Password Generator API

Simple API built with **n8n** that generates a **secure random password** using a webhook and JavaScript logic.

---

# Endpoint

```
POST /webhook/password
```

---

# Example Response

```json
{
  "password": "A8d!K2p9@Lm3"
}
```

Each request generates a **new random password**.

---

# How It Works

The workflow performs the following steps:

1. **Webhook Node**
   Receives the HTTP request.

2. **Function Node**
   Runs JavaScript logic to generate a random password.

3. **Respond to Webhook Node**
   Returns the generated password as the API response.

Workflow structure:

```
Webhook
   ↓
Function
   ↓
Respond to Webhook
```

---

# Nodes Used

* Webhook
* Function
* Respond to Webhook

---

# How to Use

1. Install **n8n**
2. Import the workflow JSON file
3. Activate the workflow
4. Call the endpoint to generate passwords

---

# Purpose

This project was created to demonstrate:

* Creating API endpoints using **n8n**
* Executing custom JavaScript logic in workflows
* Returning responses through webhooks

---

# License

This project is open for educational and portfolio purposes.

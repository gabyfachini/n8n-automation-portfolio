# n8n Automation Portfolio

Collection of automation workflows built with **n8n**.

All workflows are built **without external APIs**, using only native n8n nodes.

## Workflows included

### 🔐 Password Generator

Webhook API that generates secure random passwords.

Endpoint:

```
GET /webhook/password
```

---

### ✅ ToDo API

Simple task management API built with n8n.

Endpoints:

```
POST /task
GET /tasks
POST /task/done
```

---

### 💬 Motivational Quotes Generator

Cron workflow that generates a random motivational quote daily.

---

### 📊 Visit Counter

Webhook that counts visits using n8n static data.

---

### 🧾 CPF Validator

Simple API to validate CPF format.

---

### 🎲 Fake Data Generator

Generates random fake data for testing APIs.

---

## How to use

1. Install n8n
2. Import the workflow JSON
3. Activate the workflow

## Tech

* n8n
* Webhooks
* Function Nodes
* Cron Nodes

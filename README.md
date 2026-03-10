# n8n Automation Portfolio

Collection of **automation workflows built with n8n** to demonstrate the creation of simple APIs and automations, using only native nodes from the platform.

All workflows were built **without external APIs**, using only native features of n8n.

---

# Included Workflows

## Password Generator

Simple API that generates **secure random passwords**.

Endpoint:

```
GET /webhook/password
```

Example response:

```json
{
  "senha": "A8d!K2p9@Lm3"
}
```

---

## ToDo API

Simple **task management API** built with n8n.

Endpoints:

```
POST /task
GET /tasks
POST /task/done
```

Example task:

```json
{
  "id": 1,
  "task": "Study n8n",
  "done": false
}
```

---

## Motivational Quotes Generator

Workflow using a **Cron Node** that generates a random motivational quote daily.

Example quote:

```
"Consistency beats talent."
```

---

## Visit Counter

Webhook that counts how many times the API has been accessed using **Workflow Static Data**.

Endpoint:

```
GET /visit
```

Response:

```json
{
  "visits": 15
}
```

---

## CPF Validator

Simple API that validates the **format of a Brazilian CPF number**.

Endpoint:

```
POST /validar-cpf
```

Input body:

```json
{
  "cpf": "12345678901"
}
```

Response:

```json
{
  "cpf": "12345678901",
  "valid": false
}
```

---

## Fake Data Generator

Generates random fake data for **API and application testing**.

Example response:

```json
{
  "name": "Marina",
  "city": "Curitiba",
  "age": 29
}
```

---

# How to Use

1. Install **n8n**
2. Import the workflow JSON file
3. Activate the workflow
4. Test the endpoints using tools such as Postman or curl

---

# Technologies Used

* n8n
* Webhooks
* Function Nodes
* Cron Nodes
* JavaScript

---

# Project Purpose

This repository aims to demonstrate:

* Building simple APIs with n8n
* Task automation
* Data manipulation using JavaScript
* Use of Webhooks and Cron workflows
* Creating mini backends using automation

---

# License

Open project for study and demonstration purposes of automation with n8n.

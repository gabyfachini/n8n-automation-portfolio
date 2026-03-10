# CPF Validator API (n8n)

Simple API for basic CPF validation built using **n8n** and **Webhooks**.

---

# Features

* Receives a CPF through an HTTP request
* Removes non-numeric characters
* Checks if the CPF has **11 digits**
* Returns whether the CPF is valid or not

⚠️ This validation is **basic**, verifying only the CPF format.

---

# Technologies

* n8n
* Webhooks
* JavaScript

---

# Endpoint

### Validate CPF

```
POST /webhook/cpf-validator
```

---

# Request

### Body

```json
{
  "cpf": "12345678901"
}
```

---

# Response

```json
{
  "cpf": "12345678901",
  "valid": false
}
```

---

# Workflow Structure

The workflow consists of three main nodes:

```
Webhook
   ↓
Code (JavaScript)
   ↓
Respond to Webhook
```

### Webhook

Receives the HTTP request containing the CPF.

### Code Node

Runs the CPF validation using JavaScript.

### Respond to Webhook

Returns the validation result.

---

# Import into n8n

1. Download the `workflow.json` file
2. Open **n8n**
3. Click **Import Workflow**
4. Select the JSON file

---

# Future Improvements

* Full CPF validation (verification digits)
* API for CNPJ validation
* API for CEP validation
* Combine into a **Brazilian Validation API**

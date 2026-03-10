# CPF Validator API (n8n)

API simples para validação básica de CPF criada utilizando **n8n** e **Webhooks**.

---

# Funcionalidades

* Recebe um CPF via requisição HTTP
* Remove caracteres não numéricos
* Verifica se o CPF possui **11 dígitos**
* Retorna se o CPF é válido ou não

⚠️ Esta validação é **básica**, verificando apenas o formato do CPF.

---

# Tecnologias

* n8n
* Webhooks
* JavaScript

---

# Endpoint

### Validar CPF

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
  "valido": false
}
```

---

# Estrutura do Workflow

O workflow é composto por três nodes principais:

```
Webhook
   ↓
Code (JavaScript)
   ↓
Respond to Webhook
```

### Webhook

Recebe a requisição HTTP contendo o CPF.

### Code Node

Executa a validação do CPF utilizando JavaScript.

### Respond to Webhook

Retorna o resultado da validação.

---

# Importar no n8n

1. Baixe o arquivo `workflow.json`
2. Abra o n8n
3. Clique em **Import Workflow**
4. Selecione o arquivo JSON

---

# Melhorias futuras

* Validação completa de CPF (dígitos verificadores)
* API para validação de CNPJ
* API para validação de CEP
* Agrupar em uma **Brazilian Validation API**

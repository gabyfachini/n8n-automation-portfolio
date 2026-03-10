# CPF Validator API (n8n)

API simples para validação básica de CPF criada utilizando **n8n** e **Webhooks**.

Este projeto demonstra como criar um **mini endpoint de API** dentro do n8n usando JavaScript para validar entradas recebidas via HTTP.

---

# 📌 Funcionalidades

* Recebe um CPF via requisição HTTP
* Remove caracteres não numéricos
* Verifica se o CPF possui **11 dígitos**
* Retorna se o CPF é válido ou não

⚠️ Esta validação é **básica**, verificando apenas o formato do CPF.

---

# 🧠 Tecnologias

* n8n
* Webhooks
* JavaScript
* API REST

---

# 🚀 Endpoint

### Validar CPF

```
POST /webhook/validar-cpf
```

---

# 📥 Request

### Headers

```
Content-Type: application/json
```

### Body

```json
{
  "cpf": "12345678901"
}
```

---

# 📤 Response

```json
{
  "cpf": "12345678901",
  "valido": false
}
```

---

# ⚙️ Estrutura do Workflow

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

# 🧩 Código de validação

```javascript
function validarCPF(cpf) {

  if (!cpf) return false;

  cpf = cpf.replace(/[^\d]+/g,'');

  if (cpf.length !== 11) return false;

  return true;
}

const cpf = $json.body.cpf;

return [
  {
    json: {
      cpf: cpf,
      valido: validarCPF(cpf)
    }
  }
];
```

---

# 🧪 Testando com Postman

### URL

```
POST http://localhost:5678/webhook-test/validar-cpf
```

### Body

```json
{
  "cpf": "12345678901"
}
```

---

# 📦 Importar no n8n

1. Baixe o arquivo `workflow.json`
2. Abra o n8n
3. Clique em **Import Workflow**
4. Selecione o arquivo JSON

---

# 📁 Estrutura do Projeto

```
cpf-validator-n8n
│
├── workflow.json
├── workflow.png
└── README.md
```

---

# 💡 Melhorias futuras

* Validação completa de CPF (dígitos verificadores)
* API para validação de CNPJ
* API para validação de CEP
* Agrupar em uma **Brazilian Validation API**

---

# 👨‍💻 Autor

Projeto criado para estudo de **automação e criação de APIs utilizando n8n**.

# Fake Data Generator API (n8n)

API simples para geração de **dados fictícios aleatórios** usando **n8n**.

O workflow recebe uma requisição HTTP e retorna um usuário com **nome, cidade e idade aleatórios**.

---

# Funcionalidades

* Geração de dados fake aleatórios
* Retorno em formato JSON
* Endpoint simples via Webhook

---

# Tecnologias utilizadas

* n8n
* Webhooks
* JavaScript

---

# Endpoint

### Gerar dados fake

```http id="fake02"
GET /webhook/fake-user
```

---

# Exemplo de resposta

```json id="fake03"
{
  "nome": "Marina",
  "cidade": "Curitiba",
  "idade": 29
}
```

Cada requisição gera **um conjunto diferente de dados**.

---

# Estrutura do Workflow

O workflow possui três nodes principais:

```text id="fake04"
Webhook
   ↓
Code (JavaScript)
   ↓
Respond to Webhook
```

### Webhook

Recebe a requisição HTTP.

### Code Node

Gera dados aleatórios usando JavaScript.

### Respond to Webhook

Retorna o JSON gerado para quem chamou a API.

---

# Testando a API

Você pode testar usando **Postman**, **curl** ou navegador.

---

# Importar no n8n

1. Baixe o arquivo `workflow.json`
2. Abra o n8n
3. Clique em **Import Workflow**
4. Selecione o arquivo do workflow

---

# Possíveis melhorias

* Adicionar sobrenome
* Adicionar email fake
* Gerar múltiplos usuários
* Gerar dados de empresa

---

# Objetivo do projeto

Este projeto foi criado para estudo de **automação e criação de APIs utilizando n8n**.

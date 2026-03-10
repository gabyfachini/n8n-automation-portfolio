# Fake Data Generator API (n8n)

API simples para geração de **dados fictícios aleatórios** usando **n8n**.
Ideal para **testes de APIs, mocks de frontend e desenvolvimento de aplicações**.

O workflow recebe uma requisição HTTP e retorna um usuário com **nome, cidade e idade aleatórios**.

---

# 📌 Funcionalidades

* Geração de dados fake aleatórios
* Ideal para testes de APIs
* Retorno em formato JSON
* Endpoint simples via Webhook

---

# 🧠 Tecnologias utilizadas

* n8n
* Webhooks
* JavaScript
* API REST

---

# 🚀 Endpoint

### Gerar dados fake

```http id="fake02"
GET /webhook/fake-user
```

---

# 📤 Exemplo de resposta

```json id="fake03"
{
  "nome": "Marina",
  "cidade": "Curitiba",
  "idade": 29
}
```

Cada requisição gera **um conjunto diferente de dados**.

---

# ⚙️ Estrutura do Workflow

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

# 🧩 Código utilizado

```javascript id="fake05"
const nomes = ["Ana","Carlos","Marina","Pedro"];
const cidades = ["São Paulo","Rio","Curitiba","Recife"];

return [
  {
    json: {
      nome: nomes[Math.floor(Math.random()*nomes.length)],
      cidade: cidades[Math.floor(Math.random()*cidades.length)],
      idade: Math.floor(Math.random()*60) + 18
    }
  }
];
```

---

# 🧪 Testando a API

Você pode testar usando **Postman**, **curl** ou navegador.

### URL

```http id="fake06"
GET http://localhost:5678/webhook-test/fake-user
```

### Exemplo com curl

```bash id="fake07"
curl http://localhost:5678/webhook-test/fake-user
```

---

# 📦 Importar no n8n

1. Baixe o arquivo `workflow.json`
2. Abra o n8n
3. Clique em **Import Workflow**
4. Selecione o arquivo do workflow

---

# 📁 Estrutura do projeto

```text id="fake08"
fake-data-generator-n8n
│
├── workflow.json
├── workflow.png
└── README.md
```

---

# 💡 Possíveis melhorias

* Adicionar sobrenome
* Adicionar email fake
* Gerar múltiplos usuários
* Gerar dados de empresa
* Criar parâmetros de quantidade (`/fake-user?count=10`)

---

# 👨‍💻 Objetivo do projeto

Este projeto foi criado para estudo de **automação e criação de APIs utilizando n8n**, demonstrando como criar **micro serviços simples sem backend tradicional**.

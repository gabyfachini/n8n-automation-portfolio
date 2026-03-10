# Visit Counter API (n8n)

API simples que conta quantas vezes um endpoint foi acessado, criada utilizando **n8n** e **Webhooks**.

Cada requisição incrementa um contador armazenado no **Static Data do workflow**, permitindo acompanhar o número total de acessos.

Este projeto demonstra como criar **um micro serviço simples usando n8n como backend**.

---

# 📌 Funcionalidades

* Contar acessos em um endpoint
* Armazenar dados usando **Workflow Static Data**
* Retornar número total de visitas
* Criar um endpoint simples de API

---

# 🧠 Tecnologias utilizadas

* n8n
* Webhooks
* JavaScript
* API REST

---

# 🚀 Endpoint

### Contar visita

```http
GET /webhook/visit
```

Cada chamada ao endpoint **incrementa o contador de visitas**.

---

# 📤 Exemplo de resposta

Primeira chamada:

```json
{
  "visitas": 1
}
```

Segunda chamada:

```json
{
  "visitas": 2
}
```

Décima quinta chamada:

```json
{
  "visitas": 15
}
```

---

# ⚙️ Estrutura do Workflow

O workflow possui três nodes principais:

```
Webhook
   ↓
Code (JavaScript)
   ↓
Respond to Webhook
```

### Webhook

Recebe a requisição HTTP.

### Code Node

Atualiza o contador armazenado no **Static Data** do workflow.

### Respond to Webhook

Retorna o número total de visitas.

---

# 🧩 Código utilizado

```javascript
const staticData = $getWorkflowStaticData('global');

if (!staticData.visitas) {
  staticData.visitas = 0;
}

staticData.visitas += 1;

return [
  {
    json: {
      visitas: staticData.visitas
    }
  }
];
```

---

# 🧪 Testando a API

Você pode testar usando **Postman**, **curl** ou navegador.

### URL (modo teste)

```
GET http://localhost:5678/webhook-test/visit
```

### URL (workflow ativo)

```
GET http://localhost:5678/webhook/visit
```

### Exemplo com curl

```bash
curl http://localhost:5678/webhook-test/visit
```

---

# 📦 Importar no n8n

1. Baixe o arquivo `workflow.json`
2. Abra o n8n
3. Clique em **Import Workflow**
4. Selecione o arquivo

---

# 📁 Estrutura do projeto

```
visit-counter-n8n
│
├── workflow.json
├── workflow.png
└── README.md
```

---

# 💡 Possíveis melhorias

* Registrar endereço IP da visita
* Armazenar histórico de acessos
* Contar visitas por endpoint
* Criar painel de estatísticas

---

# 👨‍💻 Objetivo do projeto

Este projeto foi criado para estudo

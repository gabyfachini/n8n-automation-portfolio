# Visit Counter API (n8n)

API simples que conta quantas vezes um endpoint foi acessado, criada utilizando **n8n** e **Webhooks**.

Cada requisição incrementa um contador armazenado no **Static Data do workflow**, permitindo acompanhar o número total de acessos.

---

# Funcionalidades

* Contar acessos em um endpoint
* Armazenar dados usando **Workflow Static Data**
* Retornar número total de visitas
* Criar um endpoint simples de API

---

# Tecnologias utilizadas

* n8n
* Webhooks
* JavaScript
* API REST

---

# Endpoint

### Contar visita

```http
GET /webhook/visit
```

Cada chamada ao endpoint **incrementa o contador de visitas**.

---

# Exemplo de resposta

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

# Estrutura do Workflow

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

# Testando a API

Pode testar usando **Postman**, **curl** ou navegador.

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

# Importar no n8n

1. Baixe o arquivo `workflow.json`
2. Abra o n8n
3. Clique em **Import Workflow**
4. Selecione o arquivo

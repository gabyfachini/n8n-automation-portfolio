# API Geradora de Senhas

API simples construída com **n8n** que gera uma **senha aleatória segura** utilizando um webhook e lógica em JavaScript.

---

# Endpoint

```
POST /webhook/password-generator
```

---

# Exemplo de Resposta

```json
{
  "password": "A8d!K2p9@Lm3"
}
```

Cada requisição gera **uma nova senha aleatória**.

---

# Como Funciona

O workflow executa os seguintes passos:

1. **Node Webhook**
   Recebe a requisição HTTP.

2. **Node Function**
   Executa a lógica em JavaScript para gerar uma senha aleatória.

3. **Node Respond to Webhook**
   Retorna a senha gerada como resposta da API.

Estrutura do workflow:

```
Webhook
   ↓
Function
   ↓
Respond to Webhook
```

---

# Nodes Utilizados

* Webhook
* Function
* Respond to Webhook

---

# Como Utilizar

1. Instale o **n8n**
2. Importe o arquivo JSON do workflow
3. Ative o workflow
4. Faça uma requisição para o endpoint para gerar uma senha

---

# Objetivo do Projeto

Este projeto foi criado para demonstrar:

* Criação de endpoints de API com **n8n**
* Execução de lógica personalizada em **JavaScript**
* Uso de **Webhooks para responder requisições HTTP**

---

# Licença

Projeto aberto para fins de **estudo e portfólio**.

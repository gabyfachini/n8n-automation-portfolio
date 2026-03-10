# Portfólio de Automações com n8n

Coleção de **workflows de automação criados com n8n** para demonstrar a criação de APIs simples e automações, utilizando apenas nodes nativos da plataforma.

Todos os workflows foram construídos **sem APIs externas**, utilizando somente recursos nativos do n8n.

---

# Workflows incluídos

## Gerador de Senha

API simples que gera **senhas aleatórias seguras**.

Endpoint:

```
GET /webhook/password-generator
```

Exemplo de resposta:

```json
{
  "senha": "A8d!K2p9@Lm3"
}
```

---

## ToDo API

API simples para **gerenciamento de tarefas** construída no n8n.

Endpoints:

```
POST /task
GET /tasks
POST /task-done
```

Exemplo de tarefa:

```json
{
  "id": 1,
  "task": "Estudar n8n",
  "done": false
}
```

---

## Gerador de Frases Motivacionais

Workflow com **Cron Node** que gera automaticamente uma frase motivacional aleatória todos os dias.

Exemplo de frase:

```
"A consistência vence o talento."
```

---

## Contador de Visitas

Webhook que conta quantas vezes a API foi acessada utilizando **Workflow Static Data**.

Endpoint:

```
GET /visit-counter
```

Resposta:

```json
{
  "visitas": 15
}
```

---

## Validador de CPF

API simples que valida **o formato de um CPF**.

Endpoint:

```
POST /cpf-validator
```

Body de entrada:

```json
{
  "cpf": "12345678901"
}
```

Resposta:

```json
{
  "cpf": "12345678901",
  "valido": false
}
```

---

## Gerador de Dados Fake

Gera dados fictícios para **testes de APIs e aplicações**.

Resposta exemplo:

```json
{
  "nome": "Marina",
  "cidade": "Curitiba",
  "idade": 29
}
```

---

# Como utilizar

1. Instale o **n8n**
2. Importe o arquivo JSON do workflow
3. Ative o workflow
4. Teste os endpoints usando ferramentas como Postman ou curl

---

# Tecnologias utilizadas

* n8n
* Webhooks
* Function Nodes
* Cron Nodes
* JavaScript

---

# Objetivo do projeto

Este repositório tem como objetivo demonstrar:

* Criação de APIs simples com n8n
* Automação de tarefas
* Manipulação de dados com JavaScript
* Uso de Webhooks e Cron workflows
* Construção de mini backends utilizando automação

---

# Licença

Projeto aberto para fins de estudo e demonstração de automação com n8n.

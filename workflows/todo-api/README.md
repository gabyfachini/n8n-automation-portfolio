# ToDo API (n8n)

API simples de lista de tarefas criada utilizando **n8n**.

Este projeto demonstra como criar um **mini backend utilizando Webhooks e Workflow Static Data**.

---

# Funcionalidades

* Criar tarefas
* Listar tarefas
* Marcar tarefas como concluídas

---

# Tecnologias

* n8n
* Webhooks
* JavaScript
* Static Data

---

# Estrutura da tarefa

```json
{
"id":1,
"task":"Estudar n8n",
"done":false
}
```

---

# Endpoints

## Criar tarefa

POST /webhook/task

Body:

```json
{
"task":"Estudar n8n"
}
```

Resposta:

```json
{
"id":1,
"task":"Estudar n8n",
"done":false
}
```

---

## Listar tarefas

GET /webhook/tasks

Resposta:

```json
[
{
"id":1,
"task":"Estudar n8n",
"done":false
}
]
```

---

## Marcar tarefa como concluída

POST /webhook/task/done

Body:

```json
{
"id":1
}
```

Resposta:

```json
{
"id":1,
"task":"Estudar n8n",
"done":true
}
```

---

# Estrutura do workflow

```
Webhook
 ↓
Code
 ↓
Respond to Webhook
```

---

# Como testar

Exemplo usando curl:

```
curl -X POST http://localhost:5678/webhook-test/task \
-H "Content-Type: application/json" \
-d '{"task":"Estudar n8n"}'
```

---

# Estrutura do projeto

```
todo-api-n8n
│
├── create-task.json
├── list-tasks.json
├── complete-task.json
└── README.md
```

---

# Melhorias futuras

* Deletar tarefas
* Atualizar tarefa
* Buscar tarefa por ID
* Persistir dados em banco de dados

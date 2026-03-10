# ToDo API (n8n)

Simple **task management API** built using **n8n**.

This project demonstrates how to create a **mini backend using Webhooks and Workflow Static Data**.

---

# Features

* Create tasks
* List tasks
* Mark tasks as completed

---

# Technologies

* n8n
* Webhooks
* JavaScript
* Static Data

---

# Task Structure

```json
{
  "id": 1,
  "task": "Study n8n",
  "done": false
}
```

---

# Endpoints

## Create Task

```
POST /webhook/task
```

Body:

```json
{
  "task": "Study n8n"
}
```

Response:

```json
{
  "id": 1,
  "task": "Study n8n",
  "done": false
}
```

---

## List Tasks

```
GET /webhook/tasks
```

Response:

```json
[
  {
    "id": 1,
    "task": "Study n8n",
    "done": false
  }
]
```

---

## Mark Task as Completed

```
POST /webhook/task/done
```

Body:

```json
{
  "id": 1
}
```

Response:

```json
{
  "id": 1,
  "task": "Study n8n",
  "done": true
}
```

---

# Workflow Structure

```
Webhook
 ↓
Code
 ↓
Respond to Webhook
```

---

# Future Improvements

* Delete tasks
* Update tasks
* Search tasks by ID
* Persist data in a database

# Motivational Quotes (n8n)

Workflow simples no **n8n** que gera uma **frase motivacional aleatória todos os dias** e cria um **HTML simples com a frase e a data atual**.

---

## Como funciona

### 1. Schedule Trigger
Executa automaticamente **todos os dias às 09:00**.

### 2. Code (JavaScript)
Seleciona uma frase motivacional aleatória de uma lista.

### 3. Edit Fields
Organiza os dados no formato:

- `frase`
- `Day of week`
- `Month`
- `Year`

### 4. HTML
Gera uma página HTML simples com:

- frase centralizada
- data abaixo da frase

---

## Exemplo de saída

```json
[
  {
    "frase": "Consistência vence motivação.",
    "Day of week": "Monday",
    "Month": "March",
    "Year": "2026"
  }
]
# Motivational Quotes (n8n)

Simple **n8n workflow** that generates a **random motivational quote every day** and creates a **simple HTML page with the quote and the current date**.

---

## How It Works

### 1. Schedule Trigger

Runs automatically **every day at 09:00 AM**.

### 2. Code (JavaScript)

Selects a random motivational quote from a predefined list.

### 3. Edit Fields

Organizes the data in the following format:

* `quote`
* `Day of week`
* `Month`
* `Year`

### 4. HTML

Generates a simple HTML page containing:

* a centered quote
* the date displayed below the quote

---

## Example Output

```json
[
  {
    "quote": "Consistency beats motivation.",
    "Day of week": "Monday",
    "Month": "March",
    "Year": "2026"
  }
]
```

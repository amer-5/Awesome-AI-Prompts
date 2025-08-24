# 🗂️ JSON Prompting

Prompts designed to make AI tools return structured **JSON outputs** that are easy to parse and integrate into applications.  
Useful for developers, automation, chatbots, and any workflow that requires reliable machine-readable responses.

---

## 📋 Basic JSON Response

**Prompt:**
```
Return your answer in valid JSON format with the following keys:
{
  "summary": "...",
  "key_points": ["...", "...", "..."]
}
Question: Explain how photosynthesis works.
```

---

## 🛠️ API-like Response

**Prompt:**
```
You are an API. Always respond in JSON with these fields:
{
  "status": "success/error",
  "data": { ... },
  "timestamp": "ISO-8601"
}

Task: Generate a motivational quote with author.
```

---

## ✅ Boolean / Status Outputs

**Prompt:**
```
Analyze this statement and respond in JSON:
{
  "is_factually_correct": true/false,
  "explanation": "..."
}
Statement: The capital of Australia is Sydney.
```

---

## 📊 Structured Data Extraction

**Prompt:**
```
Extract all tasks from this text and return in JSON format:
{
  "tasks": [
    {"task": "...", "deadline": "...", "priority": "..."}
  ]
}
Text: Finish the report by Friday, email John tomorrow, and review code on Wednesday.
```

---

## 🧩 Custom Schema Example

**Prompt:**
```
Use this JSON schema for your answer:
{
  "title": "string",
  "difficulty": "easy/medium/hard",
  "steps": ["step1", "step2", "step3"]
}

Question: How to change a flat tire?
```

---

## 🚨 Tips

- Always say **"Return your answer in valid JSON"** to reduce parsing errors.  
- Avoid extra text outside JSON (use *"Respond only in JSON"* if needed).  
- Use **schemas** or **examples** to guide the structure.  
- Validate AI output with a JSON parser before using it in production.  

---
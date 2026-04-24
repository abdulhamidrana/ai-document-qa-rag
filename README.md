# 📄 AI Document Q&A System (RAG - Basic)

A simple **Retrieval-Augmented Generation (RAG)** based Web API built with ASP.NET Core that allows users to ask questions from a predefined set of documents.

---

## 🚀 Features

* Ask questions in natural language
* Retrieves relevant content from stored documents
* Generates contextual answers using LLM API
* Basic implementation of RAG (no vector DB)
* Clean architecture (API → Service → Infrastructure)

---

## 🧠 What is RAG?

Retrieval-Augmented Generation (RAG) is a technique where:

1. Relevant data is retrieved from a data source
2. That data is passed to an LLM
3. The LLM generates a more accurate and context-aware answer

---

## 🛠️ Tech Stack

* ASP.NET Core Web API (.NET 8)
* OpenAI API (Chat Completion)
* C#
* Simple in-memory data store (for documents)

---

## 📂 Project Structure

```
AiDocumentQA/
│
├── Controllers/
│     └── QAController.cs
│
├── Services/
│     ├── AIService.cs
│     └── DocumentService.cs
│
├── Models/
│     ├── QuestionRequest.cs
│     └── AnswerResponse.cs
│
├── Data/
│     └── Documents.cs
│
└── Infrastructure/
      └── OpenAIClient.cs
```

---

## ⚙️ How It Works

1. User sends a question
2. System searches for relevant document (keyword-based)
3. Retrieved text is combined with the question
4. LLM generates the final answer

---

## 📥 Sample Request

POST `/api/qa`

```json
{
  "question": "What is fabric booking?"
}
```

---

## 📤 Sample Response

```json
{
  "answer": "Fabric booking is the process of reserving fabric quantities for production..."
}
```

---

## 🧪 Running the Project

1. Clone the repository
2. Add your OpenAI API Key in `appsettings.json`

```json
"OpenAI": {
  "ApiKey": "YOUR_API_KEY",
  "Model": "gpt-4o-mini"
}
```

3. Run the project

```bash
dotnet run
```

---

## 🔍 Future Improvements

* Add vector database (for real semantic search)
* Use embeddings instead of keyword matching
* Add file upload (PDF, DOCX)
* Improve ranking algorithm

---

## 💡 Use Case

* ERP system document query
* Internal knowledge base
* FAQ automation

---

## 👨‍💻 Author

**Md. Rana Miah**
Software Engineer (.NET)

---

## ⭐ Note

This is a **basic RAG implementation** created for learning and demonstration purposes.
Focus is on understanding how LLM + retrieval works together in real applications.

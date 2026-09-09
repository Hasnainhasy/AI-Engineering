# 🤖 JAVED - AI Customer Support Agent

An AI-powered customer support agent built using the OpenAI API, Tool Calling, SQLite, and Gradio.

JAVED is designed as a customer support assistant for a fictional retail store. Unlike a basic chatbot that only generates text responses, this assistant can interact with backend functions and a SQLite database to verify customers, check orders, process returns, search inventory, and handle customer requests.

The application also supports image uploads, allowing the AI to process both text and images.

---

## 🚀 Features

- 🤖 AI-powered customer support agent
- 🔐 Customer identity verification
- 📦 Order status checking
- 🔄 Product return requests
- 🛒 Inventory search based on customer budget
- 🗄️ SQLite database integration
- 🔧 OpenAI Tool / Function Calling
- ⚠️ Handles invalid credentials and incorrect information
- 🖼️ Image input and analysis
- 💬 Multimodal chat interface using Gradio

---

## 🛠️ Technologies Used

- Python
- OpenAI API
- OpenAI Python Client Library
- GPT Models
- SQLite
- Gradio
- JSON
- Base64

---

## 🧠 How It Works

The AI assistant is connected to several backend functions using OpenAI Tool Calling.

When a customer makes a request, the LLM decides whether it needs to call a tool.

For example:

> "Where is my order?"

Before checking the order, the AI follows a verification process and asks the customer for their User ID and PIN.

After successful verification, the AI can call the appropriate backend function to retrieve information from the SQLite database.

The general workflow looks like this:

```text
User Request
     ↓
LLM
     ↓
Does the request require a tool?
     ↓
Tool Call
     ↓
Python Backend Function
     ↓
SQLite Database
     ↓
Tool Result
     ↓
LLM
     ↓
Final Response

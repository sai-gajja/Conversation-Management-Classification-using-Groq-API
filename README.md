# Conversation Management & Classification using Groq API

This repository contains a Jupyter Notebook that demonstrates conversation history management with summarization and JSON schema–based information extraction using the Groq API. The implementation is lightweight (no LangChain, LangGraph, or LlamaIndex) and built entirely with Python, Groq SDK, and helper libraries.

## 📌 Features

### Task 1: Conversation Management
- Add and store messages with role tracking (user, assistant)
- Truncate history by:
  - Turn count (last k turns)
  - Token count (last n tokens using tiktoken)
- Summarization of long conversations using Groq models
- Automatic periodic summarization every k turns
- Reset/clear conversation history

### Task 2: JSON Schema Classification & Information Extraction
- Define a JSON schema for user details:
  - name, email, phone, location, age
- Extract information using Groq function calling
- Validate extractions:
  - Email format
  - Age conversion & range check
  - Phone number length (10-digit Indian format)
- Works with multilingual/Indian-context examples

## 🛠️ Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/sai-gajja/Conversation-Management-Classification-using-Groq-API.git
cd Conversation-Management-Classification-using-Groq-API
pip install groq openai python-dotenv tiktoken
```

Or directly in Google Colab:

```python
!pip install groq openai python-dotenv tiktoken
```

## 🔑 Setup

1. Get your Groq API key from [Groq Console](https://console.groq.com/)
2. Store it in a `.env` file:

```
GROQ_API_KEY=your_api_key_here
```

The notebook loads it automatically:

```python
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv("GROQ_API_KEY")
```

## 🚀 Usage

Run the notebook:

1. Open `Conversation Management & Classification using Groq API.ipynb` in Jupyter or Colab
2. Execute all cells to see:
   - Conversation history management
   - Summarization examples
   - Information extraction and validation

## 📂 Repository Structure

```
.
├── Conversation Management & Classification using Groq API.ipynb
└── README.md
```

## ✅ Notes

- Uses Groq LLaMA-3.1 models (not deprecated versions)
- No external frameworks like LangChain, LangGraph, or LlamaIndex
- Safe for academic/assignment submission
- Features Indian context examples for realistic use cases

## 🔧 Technical Implementation

The implementation consists of two main components:

1. **ConversationManager Class**: Handles conversation history, truncation, and summarization
2. **Information Extraction Functions**: Uses Groq's function calling to extract structured data from conversations

The code demonstrates practical NLP techniques while maintaining simplicity and educational value.

## 📝 License

This project is intended for educational purposes. Please ensure you comply with Groq's terms of service when using their API.

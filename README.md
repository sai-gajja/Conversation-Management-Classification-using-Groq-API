# Conversation-Management-Classification-using-Groq-API

This repository contains a Jupyter Notebook that demonstrates conversation history management with summarization and JSON schema–based information extraction using the Groq API.
The implementation is lightweight (no LangChain, LangGraph, or LlamaIndex) and built entirely with Python, Groq SDK, and helper libraries.

📌 Features
Task 1: Conversation Management

Add and store messages with role tracking (user, assistant).

Truncate history by:

Turn count (last k turns).

Token count (last n tokens using tiktoken).

Summarization of long conversations using Groq models.

Automatic periodic summarization every k turns.

Reset/clear conversation history.

Task 2: JSON Schema Classification & Information Extraction

Define a JSON schema for user details:

name, email, phone, location, age.

Extract information using Groq function calling.

Validate extractions:

Email format.

Age conversion & range check.

Phone number length (10-digit Indian format).

Works with multilingual/Indian-context examples.

🛠️ Installation

Clone the repo and install dependencies:

git clone https://github.com/your-username/your-repo.git
cd your-repo
pip install -r requirements.txt


Or directly in Google Colab:

!pip install groq openai python-dotenv tiktoken

🔑 Setup

Get your Groq API key from Groq Console
.

Store it in a .env file:

GROQ_API_KEY=your_api_key_here


The notebook loads it automatically:

from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv("GROQ_API_KEY")

🚀 Usage
Run the notebook:

Open Conversation Management & Classification using Groq API.ipynb in Jupyter or Colab.

Execute all cells to see:

Conversation history management

Summarization examples

Information extraction and validation

📂 Repository Structure
.
├── Conversation Management & Classification using Groq API.ipynb
├── requirements.txt
└── README.md

✅ Notes

Uses Groq LLaMA-3.1 models (not deprecated versions).

No external frameworks like LangChain, LangGraph, or LlamaIndex.

Safe for academic/assignment submission.

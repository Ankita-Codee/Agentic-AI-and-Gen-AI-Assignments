
## 🎯 What is KidSciBot?

**KidSciBot** is an AI science tutor for kids that answers curious questions about space, animals, and experiments — all in simple, age-appropriate language.

It uses **LangGraph**, **Google Gemini**, **RAG**, and **web search** to find accurate, friendly answers from documents or live sources.

## 🧠 Tech Behind the Bot

- **LangGraph**: Smart decision-making graph (like a mini brain)
- **Gemini LLM**: Understands and generates natural language
- **RAG + Chroma + HuggingFace**: Pulls info from scientific PDFs
- **Tavily Web Search**: Gets current info from the internet

## 🤖 Agent vs LLM (Quickly)

- LLM = Writes answers  
- Agent = Chooses tools, routes queries, checks results  
- Think: LLM writes email → Agent sends it too!

## ⚙️ Flow Summary

1. Classifies the question  
2. Chooses between: PDF, LLM, or Web  
3. Validates + simplifies answer for kids

![Flow Diagram](path-to-diagram.png)

## 🛠️ Setup

```bash
pip install langchain langgraph langchain-google-genai \
langchain-huggingface chromadb pydantic tavily-python python-dotenv


# KidSciBot

**KidSciBot** is an intelligent science chatbot designed to provide kid-friendly answers to science questions. It uses a combination of Large Language Models (LLMs), Retriever-Augmented Generation (RAG) from science PDFs, and web search integration to deliver accurate and up-to-date responses.

---

## Features

- Classifies questions to determine if they are science-related.
- Retrieves answers from embedded science PDF documents using RAG.
- Fetches current event science news using web search.
- Generates general answers with an LLM when needed.
- Provides simple and easy-to-understand explanations suitable for children.

---

## Workflow Visualization

![KidSciBot Workflow]('Flowchart_KidSciBot.png')

*A flowchart showing KidSciBot’s smart decision-making pipeline.*

---

## Medium Blog

For a detailed explanation and step-by-step tutorial, check out the Medium blog post:

[🚀 KidSciBot — An Intelligent Science Tutor for Kids 📚🧒🔬](https://medium.com/@admane.ankita/kidscibot-an-intelligent-science-tutor-for-kids-327a73a81159)

---

## Technologies I Used 🔧

* LangGraph — For designing a smart agent workflow with nodes & edges
* Groq + DeepSeek LLM — Ultra-fast, open-weight LLM (deepseek-r1-distill-llama-70b) accessed via Groq for natural language understanding
* Retriever-Augmented Generation (RAG) — For science answers using PDF documents stored in a vector database
* Web Search Integration (Tavily)— To fetch fresh, current event info
* Chroma Vector Store and HuggingFace Embeddings — To organize and retrieve scientific documents

---

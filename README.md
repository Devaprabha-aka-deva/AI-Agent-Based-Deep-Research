# Dual-Agent AI System for Deep Research using LangGraph, LangChain & Tavily

This project implements a basic dual-agent AI system capable of performing deep web research and generating draft answers using LangGraph, LangChain, and the Tavily API.

---

## Overview

The system is divided into two key agents:

### 1. Research Agent  
- Handles online information gathering using the **Tavily API**.  
- Fetches top 5 relevant results for a given query, including title, URL, and content snippet.  
- Prepares the research content for use in the next stage.

### 2. Answer Drafting Agent  
- Takes the research output and generates a simple draft answer.  
- In this version, the answer is simulated to avoid LLM API charges, but it can be replaced with a real OpenAI call.  

---

## Flow of Execution

1. User enters a research query.
2. The **Research Agent** performs an advanced Tavily search.
3. The **Answer Drafter** processes the search results to create a structured response.
4. Final answer is returned to the user.

The entire system is built using **LangGraph** to manage the agent flow and **LangChain** for integrating external tools.

---

## Example

**Input Query:**  
`What are the latest advancements in quantum computing as of 2024?`

**Output:**  
`Based on the documents, here is a draft answer for: What are the latest advancements in quantum computing as of 2024?`

---

## Tech Stack

- Python  
- LangGraph  
- LangChain  
- Tavily API  
- OpenAI (LLM logic currently simulated)

---

## Installation & Setup

Install the required packages:

```bash
pip install langchain langgraph tavily-python openai langchain-community langchain-openai

Set API keys in the environment:

python
Copy
Edit
os.environ["OPENAI_API_KEY"] = "your_openai_key"
os.environ["TAVILY_API_KEY"] = "your_tavily_key"
Then run the script in a Python IDE or Google Colab.

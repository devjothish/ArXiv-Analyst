
# ArXiv Analyst – A Modular AI Research Assistant using MCP & LangChain

Welcome to **ArXiv Analyst**, a modular research assistant built using [Model Context Protocol (MCP)](https://mcp.so/), LangChain, FastAPI, and Streamlit. This tool can:

- 🔍 Search for relevant research papers from **ArXiv**
- 📝 Run linguistic analysis on documents
- 📊 Summarize and extract insights
- 🖥️ Display results through a simple web interface

---

## 🚀 Why MCP?

**Model Context Protocol (MCP)** is like a communication bridge that connects different AI models or tools, allowing them to collaborate without custom wiring.

In this project, MCP makes it easy to combine:
- A paper search tool (ArXiv)
- A document analysis tool (DocLing)

Instead of gluing everything together manually, MCP lets them work seamlessly.

---

## DEMO SCREENSHOTS

<img width="1371" alt="interface-1" src="https://github.com/user-attachments/assets/d6ff4c50-93b2-4c9b-aa09-3cdd9e2e4410" />

<img width="1376" alt="ss-search" src="https://github.com/user-attachments/assets/578d7e97-dbdf-416b-86a9-30509db28abd" />

<img width="1380" alt="ss-docling" src="https://github.com/user-attachments/assets/f3f1c95e-d075-495d-b2f6-2ac180d12e51" />

## 🏗 Project Overview

This system is made of 3 main parts:

### 1. MCP Servers

- **ArXiv Server** – Retrieves papers based on search queries
- **DocLing Server** – Analyzes text and extracts linguistic insights

### 2. FastAPI Client Server

- Uses `MultiServerMCPClient` to connect to the MCP servers
- Implements the logic for deciding which tool to use
- Provides an API layer for the UI to talk to

### 3. Streamlit UI

- Clean frontend interface
- Lets users submit queries and view search results, summaries, and analysis interactively

---

## ⚙️ How It Works (Step by Step)

1. User submits a query via Streamlit (e.g., “Find recent papers on GPT models”)
2. FastAPI Client routes the query to the correct MCP server
3. The agent invokes the right tools (search, analyze, etc.)
4. Results are returned to the UI
5. Streamlit displays everything neatly

---

## 🐳 Dockerized Setup

MCP services are fully containerized. No messy environments—just run with Docker.

### Included Dockerfiles:

- `arxiv-server`
- `docling-server`

```bash
# Build the ArXiv server
docker build -t arxiv-server ./arxiv_server

# Run it
docker run -p 8080:8080 arxiv-server
```
Do the same for the `docling-server`. Once both are running, they're accessible by the FastAPI client.

<img width="816" alt="ss1" src="https://github.com/user-attachments/assets/f41112e2-ed4f-48da-bd18-5bbc137eeab1" />

<img width="987" alt="docker-ss" src="https://github.com/user-attachments/assets/01f9fcc2-fd0b-4ba9-9957-ed3855dbb289" />

---

## 👨‍🔬 Why ArXiv Analyst is Useful for Researchers

If you're a PhD student or researcher, ArXiv Analyst helps by:

- Automating paper search and analysis
- Reducing the time spent scanning through full papers
- Giving fast, digestible insights for literature reviews or research planning

---

## 📂 Repo Links

- 🧠 GitHub: [github.com/devjothish/ArXiv-Analyst](https://github.com/devjothish/ArXiv-Analyst)
- 🛠 MCP Tools: [mcp.so](https://mcp.so/)

---

## 🙌 Questions or Feedback?

If you try the project or want to chat about modular AI systems, feel free to reach out!

**– Jothiswaran Arumugam**  
*Jo Cloud AI Hub*

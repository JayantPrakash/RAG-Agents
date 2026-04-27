# RAG Agents

A hands-on notebook repository for learning and building **Retrieval-Augmented Generation (RAG)**, **Agentic RAG**, and **AI Agent architectures** using LangChain, LangGraph, vector databases, document loaders, tool-calling agents, and self-reflective retrieval workflows.

This repository is designed as a practical learning path: start with document ingestion and parsing, move into traditional RAG, then progress into ReAct agents, LangGraph-based agent workflows, Chain-of-Thought RAG, and autonomous/self-reflective RAG systems.

---

## 🚀 What This Repo Covers

- Document ingestion and parsing
- PDF and DOC/DOCX processing
- Semantic chunking
- Traditional RAG pipelines
- Vector search with FAISS and ChromaDB
- LangChain-based retrieval chains
- ReAct-style agent reasoning
- LangGraph agent workflows
- Tool-augmented agents
- Chain-of-Thought RAG
- Self-reflection in RAG pipelines
- Autonomous RAG patterns

---

## 🧠 Project Structure

```text
RAG-Agents/
│
├── 0-DataIngestParsing/
│   ├── data/
│   ├── 1-dataingestion.ipynb
│   ├── 2-dataparsingpdf.ipynb
│   └── 3-dataparsingdoc.ipynb
│
├── AgenticRAG/
│   ├── 1-TraditionalRAG.ipynb
│   ├── 2-ReAct.ipynb
│   ├── AgenticRAG.ipynb
│   ├── research_notes.txt
│   └── sample_docs.txt
│
├── AgentsArchitecture/
│   ├── Debugging/
│   ├── ReActAgents.ipynb
│   ├── langgraph.json
│   └── reAct.py
│
├── AutonomousRAG/
│   ├── 3-COTRag.ipynb
│   ├── 4-Selfreflection.ipynb
│   └── research_notes.txt
│
├── 1-semantichunking.ipynb
├── requirements.txt
├── .python-version
└── README.md
```

---

## 📁 Folder Overview

### `0-DataIngestParsing`

Foundational notebooks for loading and parsing documents.

Topics covered:

- Loading raw documents
- Parsing PDFs
- Parsing Word documents
- Preparing documents for downstream RAG pipelines

Useful notebooks:

- `1-dataingestion.ipynb`
- `2-dataparsingpdf.ipynb`
- `3-dataparsingdoc.ipynb`

---

### `1-semantichunking.ipynb`

Notebook focused on semantic chunking strategies.

Semantic chunking helps split documents based on meaning instead of only fixed token or character length. This can improve retrieval quality by keeping related ideas together.

---

### `AgenticRAG`

Core RAG and agentic RAG experiments.

Topics covered:

- Traditional RAG
- ReAct-style reasoning
- Agentic retrieval workflows
- Using sample documents and research notes for retrieval experiments

Useful files:

- `1-TraditionalRAG.ipynb`
- `2-ReAct.ipynb`
- `AgenticRAG.ipynb`
- `sample_docs.txt`
- `research_notes.txt`

---

### `AgentsArchitecture`

Agent architecture experiments using LangGraph and ReAct-style agent design.

Topics covered:

- ReAct agent patterns
- LangGraph workflow configuration
- Python-based agent implementation
- Debugging agent behavior

Useful files:

- `ReActAgents.ipynb`
- `reAct.py`
- `langgraph.json`
- `Debugging/`

---

### `AutonomousRAG`

Advanced RAG workflows focused on autonomous and self-improving retrieval.

Topics covered:

- Chain-of-Thought RAG
- Self-reflective RAG
- Retrieval quality evaluation
- Agent reasoning over retrieved context

Useful notebooks:

- `3-COTRag.ipynb`
- `4-Selfreflection.ipynb`

---

## 🛠️ Tech Stack

This repository uses the following major tools and libraries:

- **Python**
- **Jupyter Notebook**
- **LangChain**
- **LangGraph**
- **LangChain Groq**
- **LangChain OpenAI**
- **FAISS**
- **ChromaDB**
- **Sentence Transformers**
- **Hugging Face embeddings**
- **PyPDF**
- **PyMuPDF**
- **Unstructured**
- **pdfminer**
- **python-docx**
- **docx2txt**
- **Pandas**
- **OpenPyXL**
- **Matplotlib**
- **rank-bm25**
- **Wikipedia**
- **Arxiv**

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/JayantPrakash/RAG-Agents.git
cd RAG-Agents
```

### 2. Create a virtual environment

Using `venv`:

```bash
python -m venv .venv
```

Activate it:

For macOS/Linux:

```bash
source .venv/bin/activate
```

For Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Some notebooks may require API keys for LLM providers such as OpenAI or Groq.

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
```

Load environment variables inside notebooks using:

```python
from dotenv import load_dotenv

load_dotenv()
```

---

## ▶️ How to Use This Repo

Recommended learning order:

1. Start with document ingestion:
   ```text
   0-DataIngestParsing/
   ```

2. Learn semantic chunking:
   ```text
   1-semantichunking.ipynb
   ```

3. Build a traditional RAG pipeline:
   ```text
   AgenticRAG/1-TraditionalRAG.ipynb
   ```

4. Explore ReAct agents:
   ```text
   AgenticRAG/2-ReAct.ipynb
   AgentsArchitecture/ReActAgents.ipynb
   ```

5. Build LangGraph-based agent workflows:
   ```text
   AgentsArchitecture/
   ```

6. Move into autonomous and self-reflective RAG:
   ```text
   AutonomousRAG/
   ```

---

## 🧪 Example RAG Flow

A typical RAG pipeline in this repo follows this pattern:

```text
Documents
   ↓
Load and parse files
   ↓
Split or semantically chunk text
   ↓
Generate embeddings
   ↓
Store embeddings in a vector database
   ↓
Retrieve relevant chunks for a query
   ↓
Send retrieved context to an LLM
   ↓
Generate grounded response
```

---

## 🤖 Example Agentic RAG Flow

An agentic RAG workflow adds reasoning and decision-making:

```text
User Query
   ↓
Agent analyzes the task
   ↓
Agent decides whether retrieval is needed
   ↓
Retriever fetches relevant context
   ↓
Agent evaluates retrieved context
   ↓
Agent may call tools or retry retrieval
   ↓
LLM generates final answer
```

---

## 📌 Key Concepts

### Retrieval-Augmented Generation

RAG combines information retrieval with text generation. Instead of relying only on the LLM's internal knowledge, the system retrieves relevant external documents and passes them into the model as context.

### Agentic RAG

Agentic RAG gives the model more control over the retrieval process. The agent can decide when to retrieve, what tools to use, whether retrieved context is useful, and whether another retrieval step is needed.

### ReAct Agents

ReAct stands for **Reasoning + Acting**. A ReAct agent alternates between reasoning steps and actions such as tool calls, retrieval, or API calls.

### Self-Reflective RAG

Self-reflective RAG adds an evaluation loop where the system checks whether retrieved context is relevant and whether the generated answer is grounded enough.

---

## ✅ Prerequisites

Before using this repo, it helps to understand:

- Python basics
- Jupyter Notebook
- LLM prompting
- Embeddings
- Vector databases
- LangChain basics
- Basic RAG architecture

---

## 📦 Requirements

Dependencies are listed in:

```text
requirements.txt
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```


# AI Engineer 90 Days — showcase draft

Use this as a public-facing summary, GitHub profile input, LinkedIn post scaffold, or interview prep note.
Replace placeholders later with your real shipped projects.

## One-liner
In 90 days I built a practical AI engineering portfolio focused on local inference, RAG, agent workflows, evaluations, and production-minded project packaging.

## What I built

### Project 1 — Local LLM API
- **Problem:** I wanted a clean local-first way to interact with an open-weight model through a small API instead of ad-hoc scripts.
- **Stack:** Python, FastAPI, Ollama, Docker, pytest
- **What it does:** wraps a local model behind a lightweight API with request/response structure and reproducible local setup
- **Hard part:** keeping the project simple instead of turning it into framework soup
- **GitHub:** `[add repo link]`

### Project 2 — Document RAG Assistant
- **Problem:** I wanted a document assistant that could answer questions with source grounding instead of just sounding confident.
- **Stack:** Python, LlamaIndex, Qdrant, FastAPI, Ragas
- **What it does:** ingests documents, indexes them, retrieves relevant chunks, answers with citations, and supports evaluation
- **Hard part:** chunking/retrieval quality and avoiding fake confidence from weak retrieval
- **GitHub:** `[add repo link]`

### Project 3 — Agentic Workflow Demo
- **Problem:** I wanted to move beyond single-turn prompts and show a stateful workflow with tools, branching, and failure handling.
- **Stack:** Python, LangChain/LangGraph, Ollama or API model, logging/eval layer
- **What it does:** accepts a task, decides what to retrieve or call, logs intermediate steps, and returns structured output
- **Hard part:** keeping the workflow inspectable instead of turning it into opaque agent magic
- **GitHub:** `[add repo link]`

## What I can do now
- build an LLM app behind an API
- design a retrieval pipeline over documents
- work with a vector database
- evaluate answer quality instead of relying on gut feel
- build a stateful agent workflow with tool usage
- package a project with README, architecture notes, and runnable setup

## What I did not pretend
- I am not claiming to be a research scientist
- I am not pretending a demo is the same thing as an enterprise platform
- I know the limits: hallucinations, retrieval failure modes, latency, cost, and operational friction

## Tech stack
- Python
- FastAPI
- Ollama
- LangChain / LangGraph
- LlamaIndex
- Qdrant
- Ragas
- Docker
- GitHub

## Best project to show first
- **Name:** `[choose strongest project]`
- **Why this one:** it best shows practical engineering instead of toy prompting
- **Link:** `[add link]`
- **30s pitch:** I built a practical AI application that combines model runtime, retrieval/workflow logic, and evaluation with enough documentation that another person can actually run and review it.

## Short flex without cringe
I did not go through the usual course-and-certificate route.
I used a build-first approach: open-source repos, broken prototypes, finished projects, and documentation solid enough to survive contact with another human.

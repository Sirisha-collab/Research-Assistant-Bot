# Research-Assistant-Bot
A system designed to help users explore, understand, and retrieve information from research papers and document collections using modern AI workflows.

**Overview**

The AI Research Assistant streamlines research by combining large language models with document retrieval systems. It enables users to efficiently query academic papers or custom document sets and receive concise, context-aware answers.

flowchart LR
    U[User Interface\n(Streamlit / React)] --> API[FastAPI Backend]

    API --> LG[LangGraph Workflow Engine]

    LG --> ING[Document Ingestion Pipeline]
    LG --> RET[Retrieval System]
    LG --> LLM[LLM Response Generator]

    ING --> EMB[Embedding Model]
    EMB --> VDB[FAISS Vector Store]

    RET --> VDB
    RET --> EMB

    LLM --> API --> U


**Tech Stack**

# Backend
Python
FastAPI
LangGraph (workflow orchestration)
FAISS (vector similarity search)
Embedding models + LLM APIs

# Frontend
Gradio

**Future Improvements**

1. Citation extraction and source tracing
2. Multi-document reasoning improvements
3. Streaming responses for better UX

# RAG API Project

This project demonstrates building a **Retrieval-Augmented Generation (RAG) API**, containerizing it, deploying it on **Kubernetes**, and setting up **CI/CD pipelines**.

---

## 1. Build RAG API

We first developed a Python-based RAG API using **FastAPI**, **ChromaDB** for document embeddings, and **Ollama** as the LLM.  
The API retrieves relevant context and generates answers for user queries.

**Diagram:**  
AI-RAG-API/API.png

---

## 2. Containerization

The API was containerized using **Docker**, ensuring it runs consistently across environments.  
- Docker image contains the API, dependencies, and database setup.  

**Diagram:**  
*(Insert Docker container structure diagram here)*

---

## 3. Kubernetes Deployment

The containerized API was deployed on **Kubernetes**, enabling scalable, self-healing services.  
- Pods run the API, Services route external traffic, and ConfigMaps manage configuration.

**Diagram:**  
*(Insert Kubernetes deployment diagram here)*

---

## 4. CI/CD Pipeline

Automated testing and deployment were implemented with **GitHub Actions**.  
- Semantic tests verify API responses.  
- Mock LLM mode ensures deterministic CI.  
- Pipeline triggers on code push to validate and deploy changes automatically.

**Diagram:**  
*(Insert CI/CD workflow diagram here)*

---

## 5. Key Technologies

- **FastAPI** – API development  
- **ChromaDB** – Document embeddings and retrieval  
- **Ollama** – LLM for answer generation  
- **Docker** – Containerization  
- **Kubernetes** – Deployment and orchestration  
- **GitHub Actions** – CI/CD automation  

---

## 6. Project Highlights

- Deterministic semantic tests for reliable CI/CD  
- Mock LLM for testing without dependency on external services  
- Modular project structure for scalability  

---

## 7. How to Run Locally

```bash
# Activate virtual environment
.\venv\Scripts\Activate.ps1

# Install dependencies
pip install -r requirements.txt

# Start RAG API
python -m uvicorn app:app --reload

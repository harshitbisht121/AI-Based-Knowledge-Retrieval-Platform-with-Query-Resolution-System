# AI-Based Knowledge Retrieval Platform with Query Resolution System

An AI-powered Retrieval-Augmented Generation (RAG) platform that enables users to upload knowledge-base documents and query them using natural language. The system processes documents, generates semantic embeddings, stores them in ChromaDB, and retrieves the most relevant content through a React-based conversational interface.

> **Detailed Documentation:** See **`PROJECT_GUIDE.md`** for the complete architecture, workflow diagrams, backend/frontend design, API documentation, and implementation details.

---

# Features

* 📄 Upload PDF, DOCX, TXT, and CSV documents
* 🔍 Semantic document search using Retrieval-Augmented Generation (RAG)
* 🧠 Sentence Transformer embeddings for semantic similarity
* 🗂️ Persistent vector storage using ChromaDB
* ⚡ Hybrid retrieval (semantic + exact identifier matching)
* 💬 React-based chat interface
* 📊 Document management (view and delete indexed documents)
* 📈 Background document processing with upload status tracking

---

# Technology Stack

### Frontend

* React 19
* Vite
* JavaScript
* Vanilla CSS

### Backend

* Python 3
* FastAPI
* Uvicorn
* Pydantic

### AI & Retrieval

* Sentence Transformers (`all-MiniLM-L6-v2`)
* LangChain Text Splitters
* ChromaDB (Vector Database)
* Retrieval-Augmented Generation (RAG)

### Document Processing

* pypdf
* python-docx
* pandas

### API & File Handling

* python-multipart

---

# Project Structure

```text
AI-Based Knowledge Retrieval Platform with Query Resolution System/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── core/
│   │   ├── models/
│   │   ├── rag/
│   │   ├── services/
│   │   ├── utils/
│   │   └── main.py
│   ├── chroma_db/
│   ├── metadata/
│   ├── uploads/
│   └── requirements.txt
│
├── Frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
│
├── PROJECT_GUIDE.md
└── README.md
```

---

# Installation & Setup

## Backend

```bash
# Create virtual environment
python -m venv .venv

# Activate virtual environment

# Windows
.venv\Scripts\activate

# macOS/Linux
source .venv/bin/activate

# Install dependencies
pip install -r backend/requirements.txt

# Start backend
cd backend
uvicorn app.main:app --reload
```

Backend runs at:

```
http://localhost:8000
```

Swagger API:

```
http://localhost:8000/docs
```

---

## Frontend

```bash
cd Frontend

npm install

npm run dev
```

Frontend runs at:

```
http://localhost:5173
```

---

# Usage

1. Start the FastAPI backend.
2. Start the React frontend.
3. Upload one or more supported documents.
4. Wait for document processing to complete.
5. Ask questions through the chat interface.
6. View retrieved document chunks and their source information.

---

# API Endpoints

| Method | Endpoint                   | Description              |
| ------ | -------------------------- | ------------------------ |
| GET    | `/`                        | Health check             |
| GET    | `/documents`               | List indexed documents   |
| POST   | `/upload`                  | Upload a document        |
| GET    | `/upload/status/{job_id}`  | Check upload status      |
| POST   | `/query`                   | Query the knowledge base |
| DELETE | `/documents/{document_id}` | Delete a document        |

---

# Supported File Types

* PDF
* DOCX
* TXT
* CSV

---

# Screenshots

Add screenshots or GIFs of:

* Upload page
* Chat interface
* Document list
* Query results

---

# License

Add your preferred license (e.g., MIT License) or your institution's licensing requirements.

---

# Documentation

For complete technical documentation, architecture diagrams, implementation details, API flow, RAG pipeline, project workflow, and development guidelines, refer to:

* **PROJECT_GUIDE.md**

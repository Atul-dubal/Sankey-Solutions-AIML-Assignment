# 📘 AI/ML Assignment: Academic RAG Study Assistant

## 🎯 Objective
This project implements a **Retrieval Augmented Generation (RAG)** based study assistant that answers questions using academic course materials (PDF notes).

---

## 🧠 Approach

The system follows this pipeline:

PDF Documents → Text Chunking → Embeddings → Vector Database → Retrieval → LLM (Ollama) → Answer

---

## 📂 Dataset

- Multiple Software Engineering PDFs used:
  - BSCIT_SE.pdf
  - SE_Book.pdf
  - SE_NOTES.pdf
  - SE_NOTES_2.pdf
- Total content: 200+ pages
- Covers topics like:
  - SDLC
  - Agile Model
  - Waterfall Model
  - Testing
  - Design & Maintenance

---

## ⚙️ Technologies Used

- Python (Jupyter Notebook)
- LangChain
- ChromaDB (Vector Database)
- HuggingFace Embeddings
- Ollama (Mistral Model - Local LLM)

---

## 🚀 Implementation

### 1. Data Processing
- Loaded multiple PDF files using PyPDFLoader
- Extracted text from documents

### 2. Chunking
Two chunking strategies were implemented:
- Fixed Chunking (CharacterTextSplitter)
- Sentence-based Chunking (RecursiveCharacterTextSplitter)

### 3. Embeddings
- Used HuggingFace model:
  - `sentence-transformers/all-mpnet-base-v2`

### 4. Vector Storage
- Stored embeddings using ChromaDB

### 5. LLM
- Used **Ollama (Mistral)** as local LLM
- Avoids API cost and rate limits

---

## 🧪 Experiments

### 🔬 Experiment 1: Chunking Strategies

| Method | Description |
|--------|------------|
| Fixed Chunking | Splits text into fixed size chunks |
| Sentence Chunking | Preserves sentence structure |

#### Result:
- Sentence chunking produced more complete and structured answers
- Fixed chunking sometimes broke context

#### Conclusion:
Sentence-based chunking is better for academic content.

---

### 🔬 Experiment 2: Prompting Techniques

| Method | Description |
|--------|------------|
| Basic Prompt | Simple instruction |
| Improved Prompt | Structured + explanatory |

#### Result:
- Improved prompt generated more detailed and readable answers
- Basic prompt produced shorter responses

#### Conclusion:
Improved prompting is more effective for academic Q&A.

---

## 📊 Sample Questions

- What is Software Engineering?
- What is SDLC?
- Explain Agile model
- Difference between Agile and Waterfall
- What is software testing?

---

## ⚠️ Challenges Faced

- PDF formatting issues (missing structure)
- Long text affecting chunk quality
- Some answers truncated in fixed chunking

---

## 💡 Solution

- Used sentence-based chunking
- Improved prompts for better clarity
- Used local LLM (Ollama) to avoid API limits

---

## 📈 Final Conclusion

- RAG system successfully answers academic questions
- Sentence chunking + improved prompts gave best results
- Local LLM (Ollama) is cost-effective and efficient

---

## 🔧 Setup Instructions

### 1. Install Dependencies
```bash
pip install langchain langchain-community chromadb sentence-transformers langchain-huggingface
```
### 2. Install Ollama
Download from: https://ollama.com

Run:
```ollama run mistral```

### 3. Run Notebook
- Open Jupyter Notebook
- Run all cells in order

---

## 📌 Note

This project focuses on **AI/ML concepts (RAG)** and not on UI or deployment.

---

## 🏁 Status

✅ Completed  
✅ Ready for Evaluation  

---

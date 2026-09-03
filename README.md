# 📚 Adaptive AI Tutor using RAG, LangGraph & QLoRA

> **An End-to-End Retrieval-Augmented Generation (RAG) based AI Tutor for Document Question Answering, Adaptive Quiz Generation, Automated Answer Evaluation, and Personalized Learning Feedback using Fine-tuned Large Language Models.**

---

## 🚀 Project Overview

Adaptive AI Tutor is an intelligent educational assistant that combines **Retrieval-Augmented Generation (RAG)**, **LangGraph**, and **QLoRA fine-tuned Large Language Models** to create a personalized learning experience.

The system allows users to upload learning materials and then:

- 📖 Ask document-based questions
- 📝 Generate adaptive subjective & MCQ quizzes
- ✅ Evaluate student answers automatically
- 🎯 Provide personalized feedback
- 📊 Track learning progress
- 🔄 Recommend practice questions based on weak concepts

The project employs a **Hybrid Retrieval Pipeline (Dense + Sparse + Re-ranking)** to improve retrieval quality and minimize hallucinations.

---

# ✨ Features

- 📖 Document-based Question Answering
- 🧠 Retrieval-Augmented Generation (RAG)
- 📝 Adaptive Quiz Generation
- ☑️ MCQ Generation
- 🤖 Automated Answer Evaluation
- 🎯 Personalized Feedback
- 📊 Session Performance Tracking
- 🔍 Hybrid Retrieval (FAISS + BM25)
- ⚡ Cross-Encoder Re-ranking
- 🔄 Stateful Workflow using LangGraph
- 🚀 Fine-tuned LLM using QLoRA

---

# 🏗️ System Architecture

```text
                     Learning Documents
                             │
                             ▼
                Document Preprocessing
                             │
                             ▼
                  Text Chunking
                             │
                             ▼
                     BGE-M3 Embeddings
                             │
                             ▼
                    FAISS Vector Store
                             │
                     BM25 Keyword Search
                             │
                             ▼
                  Hybrid Retrieval Pipeline
                             │
                   Cross-Encoder Re-Ranker
                             │
                             ▼
                  Context Construction
                             │
                             ▼
               Fine-tuned Qwen2.5-3B LLM
                             │
        ┌────────────────────┼────────────────────┐
        ▼                    ▼                    ▼
 Question Answering     Quiz Generation     Answer Evaluation
```

---

# ⚙️ Technology Stack

| Category | Technologies |
|-----------|--------------|
| Programming | Python |
| Framework | LangChain |
| Workflow Orchestration | LangGraph |
| RAG Framework | Retrieval-Augmented Generation |
| Vector Database | FAISS |
| Embedding Model | BAAI BGE-M3 |
| Base LLM | Qwen2.5-3B-Instruct |
| Question Generation | Google FLAN-T5-Large |
| Fine-tuning | LoRA, QLoRA |
| Re-ranking | Cross-Encoder (MS MARCO MiniLM) |
| Dense Retrieval | FAISS |
| Sparse Retrieval | BM25 |
| Datasets | SQuAD, CoQA, MS MARCO, RACE |
| LLM Framework | Hugging Face Transformers |
| Training | PEFT, BitsAndBytes |
| UI | Streamlit |
| Development | Google Colab, VS Code |
| Version Control | Git & GitHub |

---

# 🤖 Models Used

| Model | Purpose |
|--------|---------|
| **Qwen2.5-3B-Instruct** | Question Answering, MCQ Generation, Answer Evaluation |
| **Google FLAN-T5-Large** | Subjective Question Generation |
| **BAAI BGE-M3** | Dense Embeddings |
| **Cross Encoder (MS MARCO MiniLM)** | Re-ranking Retrieved Documents |

---

# 📚 Datasets

The project is trained and evaluated using multiple benchmark datasets.

| Dataset | Purpose |
|----------|----------|
| SQuAD | Question Answering |
| CoQA | Conversational QA |
| MS MARCO | Passage Retrieval |
| RACE | Multiple Choice Question Generation |

---

# 🔍 Hybrid Retrieval Pipeline

The retrieval system combines semantic and keyword search.

```text
User Query
     │
     ▼
Dense Retrieval (FAISS + BGE-M3)
     │
     ▼
Sparse Retrieval (BM25)
     │
     ▼
Merge Results
     │
     ▼
Cross Encoder Re-ranking
     │
     ▼
Top Relevant Context
     │
     ▼
Fine-tuned Qwen2.5-3B
```

---

# 🔄 LangGraph Workflow

```text
                 User Query
                      │
                      ▼
                Router Node
          ┌───────────┴───────────┐
          │                       │
          ▼                       ▼
   RAG Question Answering    Quiz Generator
          │                       │
          ▼                       ▼
     Generated Answer      Adaptive Questions
          │                       │
          └───────────┬───────────┘
                      ▼
              Answer Evaluation
                      │
                      ▼
              Session Analytics
                      │
                      ▼
             Personalized Feedback
```

---

# 📊 Evaluation Metrics

### 📖 Retrieval Evaluation

- Recall@K
- Precision@K
- Mean Reciprocal Rank (MRR)
- nDCG

### 🤖 Question Answering

- Exact Match (EM)
- F1 Score
- Semantic Similarity
- BERTScore

### 📝 Question Generation

- BLEU
- ROUGE
- METEOR

### ✅ Answer Evaluation

- Accuracy
- Precision
- Recall
- F1 Score
- Semantic Similarity

---

# 📂 Project Structure

```text
Adaptive-AI-Tutor/
│
├── app.py
├── requirements.txt
├── README.md
├── modules/
│   ├── config.py
│   ├── model_hub.py
│   ├── rag_engine.py
│   ├── vector_store.py
│   ├── langgraph.py
│   ├── q_gen.py
│   ├── eval.py
│   ├── quiz.py
│   └── utils.py
│
├── notebooks/
├── images/
├── data/
└── adapters/
```

---

# 🚀 Future Work

- 🌐 Multi-document reasoning
- 🎙️ Voice-based tutoring
- 🖼️ Image & Diagram understanding using Vision-Language Models
- 🧠 Long-term learner memory
- 🔗 Knowledge Graph integration
- 🌍 Real-time Web Search
- 📈 Personalized learning analytics dashboard
- 🌐 Multilingual tutoring support

---

# 👨‍💻 Author

**Kaushik Bhattacharyya**

M.Sc. Data Science

**Skills:** Python • Machine Learning • NLP • LLMs • RAG • LangChain • LangGraph • QLoRA • FAISS • Hugging Face

---

## ⭐ If you found this project useful, consider giving it a Star!

# **Resume JD Matcher**

An **AI-powered multi-agent recruitment platform** that intelligently matches resumes to job descriptions (JDs) using **LangGraph**, **vector embeddings**, and **LLM-driven contextual ranking**.

---

## **Table of Contents**
1. [Introduction](#introduction)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [Setup Instructions](#setup-instructions)
5. [Usage](#usage)
6. [Phase 1 Deliverables](#phase-1-deliverables)
7. [Phase 2 Roadmap](#phase-2-roadmap)
8. [Requirements](#requirements)
9. [Contributing](#contributing)
10. [License](#license)

---

## **Introduction**

The recruitment process often requires comparing job descriptions (JDs) with hundreds of resumes to find the right candidates. **Resume JD Matcher** automates this process by combining semantic search, LLM reasoning, and a multi-agent workflow to **rank resumes by contextual fit**.  
Our goal is to streamline resume screening, improve recruiter productivity, and deliver explainable candidate rankings.

---

## **Features**

- **Multi-Agent Architecture**:
  - **Comparison Agent** – Compares resumes with JDs using vector embeddings + contextual overlap.
  - **Ranking Agent** – Ranks candidates with LLM reasoning, highlighting skills and gaps.
  - **Communication Agent** – Prepares notifications/emails for recruiters and AR requestors.

- **Resume Parsing**: Automatically extracts skills, experience, and summary using **LlamaCloud** and **LangChain**.

- **Semantic Vector Matching**: Employs **ChromaDB with Google Embeddings** for context-aware similarity scoring.

- **Explainable Matching**: Provides detailed match reasons (e.g., “Skill overlap: Python, AI/ML; Missing: Kubernetes”).

- **Phase 1 UI**: Streamlit-based dashboard for:
  - Uploading JDs & resumes.
  - Viewing ranked candidates.
  - Tracking the pipeline (comparison → ranking → notification).

- **Persistent Storage**: **MongoDB** is integrated to store metadata and processed data.

---

## **Tech Stack**

**Backend:**
- Python 3.8+
- FastAPI, LangGraph, LangChain
- LlamaCloud (resume parsing)
- ChromaDB (vector storage)

**Frontend (Phase 1):**
- Streamlit (prototype UI)

**Database:**
- MongoDB (candidate metadata)

**LLMs & APIs:**
- OpenAI, Google Generative AI
- Groq API
- LlamaCloud API

---

## **Setup Instructions**

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/ResumeJDMatcher.git
cd ResumeJDMatcher
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables
Create a .env file in the project root:
```bash
GROQ_API_KEY=your_groq_key
OPENAI_API_KEY=your_openai_key
GOOGLE_API_KEY=your_google_key
LLAMA_CLOUD_API_KEY=your_llama_cloud_key
MONGODB_URI=your_mongodb_connection
```

### 4. Launch Streamlit (Phase 1 UI)
```bash
streamlit run app.py
```

## **Usage**
1. Upload **Job Description (JD)** PDFs via the Streamlit dashboard.  
2. Upload one or more **resume PDFs**.  
3. The **Comparison Agent** computes semantic similarity between JD & resumes.  
4. The **Ranking Agent** provides **top 3 candidates** with relevance scores and reasoning.  
5. The **Communication Agent** prepares notifications for the AR requestor.

---

## **Phase 1 Deliverables**
- **Multi-agent pipeline** (Comparison, Ranking, Communication).  
- **Streamlit-based basic UI**.  
- **MongoDB integration** for storing parsed data.  
- **JD & resume upload functionality**.  
- **Ranked results with LLM-based reasoning**.
- Fully automated email dispatch via **Communication Agent**.

---

## **Phase 2 Roadmap**
### **Frontend Upgrade**  
- Replace **Streamlit** with **React + TailwindCSS** for modern AR Requestor & Recruiter dashboards.  

### **UI Enhancements**  
- Separate pages for:  
  - **JD Upload (AR Requestor)**  
  - **Resume Pool Management (Recruiter)**  
  - **Real-time status tracking with progress bars**  

### **Advanced Analytics**  
- Leaderboards, hot skills, error rates, and pipeline monitoring.  


---

## **Requirements**
- **Python 3.8+**  
- **MongoDB** (local or cloud)  
- API keys for **OpenAI**, **Google AI**, **Groq**, **LlamaCloud**  
- **Streamlit** for UI testing (Phase 1)


# 📈 AI-Powered Sales Document Analyzer

An intelligent end-to-end AI application that extracts, analyzes, and visualizes insights from sales documents (PDFs) using LLMs, NLP, and dynamic data visualization.

Built with **Streamlit + Groq LLM API + NLP pipelines**, this tool transforms unstructured sales documents into actionable insights, structured KPIs, and interactive charts.

---

## 🔥 Key Features

### 📄 Smart PDF Processing
- Extracts text using multiple engines to ensure maximum accuracy:
  - `PyPDF2`
  - `PyMuPDF`
  - `pdfplumber`
- Automatically selects the best extraction output based on document structure.

### 🧠 AI-Powered Analysis (LLM)
Powered by the Groq API:
- 📊 **Comprehensive Sales Analysis**
- 📋 **Executive Summary**
- ⚠️ **Risk Assessment**
- 🎯 **KPI Extraction** (Outputs structured Markdown tables)

### 📊 KPI Extraction & Visualization
- Converts AI output directly into structured data.
- Automatically generates interactive dashboards:
  - **Line charts** for time-series data.
  - **Bar charts** for categorical KPIs.
  - **Metric dashboards** for quick overviews.
- Seamlessly handles revenue trends, product performance, and regional sales metrics.

### 💬 Interactive Q&A
- Ask custom questions directly against the document context.
- Predefined smart queries for quick insights.
- Context-aware answers utilizing LLM generation.

### ⚙️ NLP-Based Insights (Local Processing)
- **Sentiment Analysis** powered by HuggingFace Transformers.
- **Readability Score** utilizing the Flesch Index.
- **Term Extraction** using advanced Regex patterns.

### 📈 Data Insights Dashboard
- Displays word count, readability, and estimated reading time.
- Dynamic KPI visualization engine.
- Exportable AI reports.

### 💾 Export Options
Download your results in multiple formats:
- AI Analysis Reports
- KPI Data (CSV/JSON)
- Executive Summaries
- Risk Assessments

---

## 🏗️ Architecture Overview

flowchart TD
    A[📄 PDF Input] --> B[Text Extraction]
    B --> |PyPDF2, PyMuPDF, pdfplumber| C[🧠 LLM Processing]
    C --> |Groq API| D[🎯 Structured KPI Parsing]
    D --> E[📊 Visualization Engine]
    E --> |Plotly| F[💻 Streamlit Dashboard]

## 🛠️ Tech Stack

| Category | Tools & Libraries |
| :--- | :--- |
| **Frontend** | Streamlit |
| **Backend** | Python |
| **LLM** | Groq API (LLaMA3) |
| **NLP** | HuggingFace Transformers |
| **PDF Processing** | PyPDF2, PyMuPDF, pdfplumber |
| **Visualization** | Plotly |
| **Data Handling** | Pandas, NumPy |

---

## 🚀 Environment Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/sales-doc-analyzer.git](https://github.com/your-username/sales-doc-analyzer.git)
cd sales-doc-analyzer

2. Install Dependencies
Bash
pip install -r requirements.txt
3. Set API Keys
You will need a Groq API key to run the LLM inference.

Bash
export ALL_GROQ_API_KEYS="gsk_xxxxx,gsk_yyyyy"
4. Run the Application
Bash
streamlit run app.py

Usage
Upload a sales PDF via the sidebar.

Choose an analysis type:

Comprehensive Analysis

KPI Extraction

Summary / Risk Assessment

View the results:

Read AI-generated insights.

Interact with generated charts and metrics.

Ask custom questions in the Q&A section to dive deeper.

Export your results using the download buttons.


Unique Highlights
🔄 Multi-engine PDF extraction fallback ensures no text is left behind.

🔑 Multi-API key rotation guarantees reliability and bypasses rate limits.

📊 Auto KPI → Chart pipeline turns raw text into visual data instantly.

🧠 Hybrid System combining cutting-edge LLMs with traditional NLP.

🎯 Structured AI outputs optimized specifically for visual rendering.

# Multi-A3 (Ask–Analyze–Acute) — Intelligent Multi-Source Research Assistant (Advanced RAG)

## Overview

Multi-A3 is an intelligent multi-source research assistant built using Retrieval-Augmented Generation (RAG).  
It ingests multiple document types (PDF, CSV, Markdown), builds a unified knowledge base, and intelligently routes user queries to the appropriate tool for answering, analysis, or summarization.

The system ensures grounded responses using citations and confidence scoring.

---

## Architecture

PDF / CSV / Markdown  
→ Data Ingestion (Eaters)  
→ MYMULTIWIKI (FAISS + BM25 Hybrid Retrieval)  
→ Hero Dispatcher (LLM Intent Classification)  
→ Tool (Ask / Analyze / Acute)  
→ LLM Response  

---

## Key Features

• Multi-source ingestion (PDF, CSV, Markdown)  
• Hybrid Retrieval (Dense + Keyword using FAISS + BM25)  
• LLM-based Intent Classification (Hero Dispatcher)  
• Multi-tool architecture:
  - Ask → factual Q&A  
  - Analyze → cross-source reasoning  
  - Acute → summarization  
• Source-based citations  
• Confidence scoring  
• Interactive Gradio UI  

---

## System Modules

### PDFEater()
Loads technical documents and chunks text for embedding.

### CSVEater()
Transforms structured rows into contextual documents.

### MARKDOWNEater()
Processes unstructured markdown content.

### MYMULTIWIKI()
Creates embeddings and builds hybrid retrieval system (FAISS + BM25).

### Hero()
Central dispatcher using LLM-based intent classification.

### AskMe()
General factual Q&A across sources.

### Analyzer()
Cross-source reasoning and validation (especially CSV + documentation).

### TellInShort()
Summarization across multiple sources.

---

## Use Cases

### 1. CSV vs Documentation Validation  
Validate analytical reports against actual datasets.

### 2. GitHub Project Research Assistant  
Answer questions using README + dataset + documentation together.

---

## How to Run

### 1. Install Dependencies

```

pip install -r requirements.txt

```

---

### 2. Add OpenRouter API Key

**Option 1 (Colab Recommended)**  
Add secret:

```

OPENAI_API_KEY

```

**Option 2 (Local)**

```

export OPENAI_API_KEY="your_key"

```

---

### 3. Run Notebook

• Run all cells  
• Launch Gradio UI  

---

### 4. Example Queries(Sample files provided for Testing)

```

compare the sales report with csv
summarize all documents
is the dataset consistent with documentation

```

---

## Future Scope

• Clarification agent for ambiguous queries  
• UI improvements  
• Deployment as web app  

---

## Demo

Demo video: Link Coming Soon.

---

## Author

Shikhar Sharma  
NT Batch — Industry Practice Assignment

